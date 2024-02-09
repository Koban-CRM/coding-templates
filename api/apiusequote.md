# API Koban - Exemple d'utilisation

## Devis - Récupérer les devis gagnés dans un outil externe

Cet exemple d'utilisation illustre la récupération des devis gagnés dans Koban à intervalle régulier pour les traiter dans un outil externe.
Il est convenu que l'identifiant unique d'un compte de l'outil externe est stocké dans Koban dans le champ **Code externe**.

Pour des raisons de simplification, la gestion de la pagination n'est pas abordée.

**<u>Prérequis :</u>**

- Disposer des clés API de votre compte Koban
- Avoir dans votre outil Koban les comptes de votre système externe (dont le code interne est stocké dans le champ Koban **Code externe**)

### Principes

Le principe de synchronisation retenu est le suivant :

* Récupération des devis modifiés de Koban depuis la veille
* Tri des devis gagnés dans la liste récupérée et stockage dans l'outil externe

### Récupérer les devis modifiés de Koban

**<u>Méthode à utiliser :</u>**

Appelez la méthode API [ncQuote/GetUpdated](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#3521217e-e478-42c2-8788-540b41d6fbd3) en GET.
Elle permet de récupérer tous les devis créés ou modifiés depuis une date donnée (exprimée en timestamp).

Lancez cette méthode avec les paramètres suivants :

* **updated** : La date de dernière synchronisation stockée et transmise en timestamp (par exemple 1704841204 pour le 01/01/2024)
* **s** : L'index de démarrage de la pagination. On va le renseigner à 0
* l : La taille d'une page. On va la renseigner à 20

L'URL d'appel va donc donner :

**[SERVERKOBAN]/api/v1/ncQuote/GetUpdated?updated=1704841204&s=0&l=20** 

L'appel va retourner la liste des devis au format JSON dans la propriété List. Il s'agit d'un tableau d'objets Devis (dont la définition est donnée ci-dessous).

Dans cette liste, tous les devis gagnés ont la propriété **Result** égale à **WON**. Il convient donc de filtrer cette liste pour ne récupérer que les devis gagnés

### Focus sur l'objet devis retourné

L'objet devis est très volumineux et permet d'avoir en un appel les informations souvent nécessaires :

- L'opportunité associée
- Le compte concerné
- Le contact associé
- L'ensemble des lignes composant le devis avec les produits associés

#### L'objet devis principal

L'objet devis est constitué, entre autres, des propriétés suivantes :

- **Status** : DRAFT ou SENT. Défini si le devis a été envoyé par email depuis Koban
- **Result** : Le résultat du devis. WON si il a été gagné, LOST si il a été perdu ou bien vide si il est en cours
- **Number** : Le numéro du devis
- **ResultDate** : La date à laquelle le devis a été gagné (ou perdu)
- **Guid** : Le code interne Koban du devis
- **Deal** : L'opportunité associé (objet décrit ci-dessous)
- **Third** : Le compte associé (objet décrit ci-dessous)
- **Contact** : Le contact associé (objet décrit ci-dessous)
- **Sections** : Les sections et les lignes du devis. Il s'agit d'un tableau de sections. Pour chaque section, plusieurs lignes sont disponibles dans le tableau Lines. L'objet Ligne est décrit ci-dessous

#### L'opportunité associée

Il s'agit d'un objet dont les propriétés principales sont les suivantes :

- **Label** : Le libellé de l'opportunité
- **Guid** : Le code interne Koban de l'opportunité

Si vous souhaitez récupérer plus d'informations, il convient de lancer la méthode API [ncDeal/GetOne](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#5e7e1c92-350a-4fb8-9969-1dac29586c80) en GET avec comme paramètres :

- **id** : Le code interne Koban de l'opportunité

#### Le compte concerné

Il s'agit d'un objet dont les propriétés principales sont les suivantes :

- **Label** : Le libellé du compte
- **Guid** : Le code interne Koban du compte
- **Extcode** : Le code externe du compte

Si vous souhaitez récupérer plus d'informations, il convient de lancer la méthode API [ncThird/GetOne](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#fc544c1c-bd86-4fe2-9347-a81f0a306fba) en GET avec comme paramètres :

- **id** : Le code interne Koban du compte

#### Le contact concerné

Il s'agit d'un objet dont les propriétés principales sont les suivantes :

- **Name**: Le nom du contact
- **FirstName** : Le prénom du contact
- **EMail** : L'email du contact
- **Guid** : Le code interne Koban du contact

Si vous souhaitez récupérer plus d'informations, il convient de lancer la méthode API [ncContact/GetOne](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#6f54d9a5-84d0-488e-8c22-1b21723dff52) en GET avec comme paramètres :

- **id** : Le code interne Koban du contacts

#### Les lignes du devis

Chaque ligne du devis (présente dans l'arborescence JSON sous Section.Lines) comporte les propriétés suivantes :

* **Label** : Le libellé de la ligne
* **Guid** : L'identifiant interne Koban de la ligne
* **Quantity** : La quantité
* **Ht** : Le montant HT
* **Ttc** : Le montant TTC
* **Prht** : Le prix de revient HT
* **Margin** : La marge HT
* **UnitPrice** : Le prix unitaire
* **Red** : La remise HT
* **Comments** : La désignation complète
* **Product** : Le produit lié. Il s'agit d'un objet dont les propriétés principales sont les suivantes :
  * **Reference** : La référence (ou code) Produit
  * **Label** : Le libellé du produit dans le catalogue
  * **Guid** : Le code interne Koban du produit
  * **Unit** : L'unité