# API Koban - Exemple d'utilisation

## Contact - Synchroniser les contacts dans un outil externe

Cet exemple d'utilisation illustre la synchronisation des contacts Koban dans un outil externe et de manière bi-directionnelle.

On conviendra ici que la synchronisation initiale a déjà été effectuée et que seuls les modifications effectuées transitent d'un outil à l'autre.
Par ailleurs, il est convenu que l'identifiant unique d'un contact de l'outil externe est stocké dans Koban dans le champ **ExternalCode**.

Pour des raisons de simplification, la gestion de la pagination dans un sens comme dans l'autre n'est pas abordée.

**<u>Prérequis :</u>**

- Disposer des clés API de votre compte Koban
- Avoir effectué une synchronisation initiale

### Principes

Le principe de synchronisation retenu est le suivant :

* Récupération des contacts modifiés de Koban et mise à jour de l'outil externe
* Mise à jour des contacts Koban 

Une **date de dernière synchronisation** est stockée dans l'outil externe.

### Avant la synchronisation

Il convient de :

* Stocker la date et l'heure de début de processus (utile pour la dernière étape) dans une variable
* Récupérer tous les contacts modifiés dans l'outil externe dans un tableau

### Récupérer les contacts modifiés de Koban

**<u>Méthode à utiliser :</u>**

Appelez la méthode API [ncContact/GetUpdated](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#1949eb63-c517-4941-a87e-1522bf8863a6) en GET.
Elle permet de récupérer tous les contacts créés ou modifiés depuis une date donnée (exprimée en timestamp).

Lancez cette méthode avec les paramètres suivants :

* **updated** : La date de dernière synchronisation stockée et transmise en timestamp (par exemple 1704841204 pour le 01/01/2024)
* **s** : L'index de démarrage de la pagination. On va le renseigner à 0
* l : La taille d'une page. On va la renseigner à 20

L'URL d'appel va donc donner :

**[SERVERKOBAN]/api/v1/ncContact/GetUpdated?updated=1704841204&s=0&l=20** 

L'appel va retourner la liste des contacts au format JSON dans la propriété List.

Chaque contact dispose de propriétés qu'on peut donc remonter dans l'outil externe :

* **Extcode** : Le code unique du contact dans l'outil externe. Si cette valeur est nulle, alors il faudra créée le contact dans l'outil externe, sinon le mettre à jour
* **Guid** : Le code unique Koban du contact
* **Name** : Nom de famille
* **FirstName** : Prénom
* **Function** : Fonction
* **EMail** : EMail
* **Phone** : Numéro de téléphone
* **Cell** : Numéro de Mobile
* **Third** : Compte (Société par exemple) sur laquelle est attachée le contact. Il s'agit d'un objet JSON comprenant les propriétés Label (Nom de la société), Guid (code unique Koban), Extcode (code unique de l'outil externe si vous décidez de synchroniser également les comptes)

### Mettre à jour les contacts Koban depuis l'outil externe

Appelez la méthode API [ncContact/PostMany](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#f5324fdf-1630-45d7-b937-15b3870b2654) en POST.
Cette méthode permet de créer ou de mettre à jour une liste de contact dans Koban.

Lancez cette méthode avec les paramètres suivants :

- **uniqueproperty** : Extcode
- **thirduniqueproperty** : Extcode

Ces propriétés permettent à Koban de connaitre les clés à utiliser pour l'appel.
Ici on lui dit qu'on va utiliser la propriété Extcode pour savoir si le contact existe déjà dans Koban, et qu'on va rattacher ce contact à un compte dont la clé est fournie 

Fournissez ensuite dans le body une liste de contact (au format JSON) avec les mêmes propriétés énumérées dans le premier point. Cette liste de contact à injecter dans Koban a été positionnée dans une variable (cf "Avant la synchronisation").

Par exemple :

```json
[{
    "Extcode": "C0001",
    "FirstName": "Bertrand",
    "Name": "OLLIER",
    "EMail": "b.ollier@acme.fr",
    "Phone": "06 61 61 61 61",
    "Function": "Responsable Projet",
    "Third": {
        "Extcode": "S0001"
    }
}]
```

### Gestion des conflits

Lorsqu'on met à jour les contacts dans l'outil externe depuis la liste des contacts récupérée de Koban, il se peut que le contact ait également été modifié dans l'outil externe depuis la dernière synchronisation (en comparant par exemple la date de dernière synchronisation avec la date de dernière modification du contact stockée dans votre outil externe).

Dans ce cas, vous pouvez :

- Choisir que l'outil externe est maitre. Donc ne pas mettre à jour le contact dans l'outil externe et laisser la mise à jour se faire dans Koban.
- Choisir que Koban est l'outil maitre. Dans ce cas, vous effectuez la mise à jour de l'outil externe et n'envoyez pas ce contact dans Koban
- Lever une erreur pour laisser l'utilisateur décider (en envoyant par exemple un email d'alerte).

### Fin de la synchronisation

La date de fin de synchronisation est mise à jour dans l'outil externe avec la date stockée au démarrage du processus.