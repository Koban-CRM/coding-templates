# API Koban Immobilier

Vous trouverez sur cette page des exemples de cas d'utilisation de l'API Koban Immobilier

## Préambule

Afin de vous connecter à l'API Koban, il est nécessaire de vous authentifier. Vous trouverez sur cette [page](../API.md) l'ensemble des informations nécessaires.

L'ensemble des exemples est disponible sur cette page :

[https://documenter.getpostman.com/view/1804856/SzKQyLUw](https://documenter.getpostman.com/view/1804856/SzKQyLUw)

## Stock

Le stock des programmes et des lots est récupérable par un système distant via l'API. De même, une alimentation du stock dans Koban est possible à partir d'un système distant via l'API.

### Liste des programmes

La méthode à appeler est [ncDealProcess/GetAll](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#8733c229-9409-496c-908c-4fbd2bb17ee2).

### Liste des lots

La méthode à appeler est [ncDeal/GetUpdated](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#9f747eeb-fa95-4e1e-b03e-66f4527de5fe).

Cette méthode prend comme paramètre updated, de format date UNIX qui permet de ne récupérer que les lots créés ou modifiés dans Koban depuis une certaine date.

Le retour est un tableau paginé de lots dont les propriétés immobilier sont les suivantes :

- Label : Le nom du lot
- Status : Le statut du lot :
  - LIBRE - Lot libre
  - OPTION - Au moins une option est en cours sur ce lot
  - PRERESV - Lot préréservé
  - RESV - Lot réservé
  - BLOQUE - Lot bloqué
  - (*) : D'autres statuts peuvent également être disponible en fonction de votre paramétrage
- Process : Le programme
- Result : Définit si le lot a été acté ou non. Si oui, Result est égal à WON
- Extcode : Le code externe
- Amountprev : Le montant du lot
- Tags : Tableau de segmentation du lot. Le tableau comprend X valeurs (TagCategory, Label)  dont TagCategory correspond à :
  - NBPIECES : Le nombre de pièces
  - TPLOG : Type de logement
  - ETAGE : Etage 
- MoreFields : Tableau des informations supplémentaires. Le tableau comprend X valeurs (FieldId, Value) dont FieldId correspond au champ personnalisé créé dans Koban. Pour récupérer les valeurs, il faut consulter la page de paramétrage Programmes et Lots > Personnalisation
- Type : Le type du lot. NULL si le lot est principal, **Secondary** si le lot est secondaire.
- Link : Si le lot est secondaire, donne l'identifiant Koban du lot principal attaché.
- Guid : L'identifiant Koban du lot

### Alimenter les lots

#### Méthode à appeler

La méthode à appeler est [ncDeal/PostMany?uniqueproperty=Extcode&thirduniqueproperty=Extcode](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#0b003fe9-260c-4b5e-ba3e-2e4b91859c69)

Cette méthode prend comme corps de requête un tableau de lot dont les propriétés sont les mêmes que celles retournées par la méthode de liste ci-dessus.

#### Lots secondaires

La méthode de transmission des lots secondaires d'un lot principal est la suivante :

- Dans ncDeal/PostMany, alimentez d'abord le lot principal
- Puis rappelez ncDeal/PostMany pour alimenter les lots secondaires en remplissant les propriétés :
  - Type : **Secondary**
  - Link : Le <u>code externe</u> du lot principal
- Vous pouvez transmettre le lot principal et le lot secondaire dans la même requête à la condition que le lot principal figure en premier dans le tableau

## Dénonciations

Les dénonciations peuvent être alimentées dans Koban par un outil externe.

Plusieurs étapes sont nécessaire pour la pose d'une dénonciation :

- Vérifier que la dénonciation est possible pour le programme concerné
- Eventuellement créer le prospect avec toutes ses coordonnées
- Poser la dénonciation

### Vérifier que la dénonciation est possible

Il vous faut appeler la méthode de vérification grâce aux coordonnées du prospect concerné (Email, Nom et prénom, numéro de téléphone) et du programme (grâce à son code).

La méthode à appeler est [ncDenonc/CheckDenonc](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#9618d302-595a-4c99-91e4-766c82b3eff7)

Le résultat permet de savoir si une dénonciation est possible :

- Si Activated = false, alors le module dénonciation n'est pas activé. Une dénonciation est impossible.
- Si IsDenonced = true, alors une dénonciation existe déjà pour ce prospect. Une dénonciation est impossible.
- Si Exists = true, alors le prospect est déjà référencé dans Koban mais la dénonciation est possible. Dans ce cas, il convient de passer l'étape de création du prospect et de poser directement la dénonciation.

### Créer le prospect

Si vous devez au préalable créer le prospect dans Koban, vous devez appeler la méthode [ncThird/PostOne](https:/app-koban.com/Static/apidoc.html#operation/ncThird_PostOne).

Les informations à transmettre sont les suivantes :

- Coordonnées du prospect (Nom, Prénom, EMail, téléphone, mobile...)
- Le programme qui intéresse le prospect
- Eventuellement le profil des lots qui l'intéresse (Typologie, Nb de pièces)
- Des informations supplémentaires (Budget, source marketing)
- L'origine du prospect (CGP par exemple dans le cas d'une dénonciation via un CGP)

### Poser la dénonciation

Dernièrement, vous devez poser la dénonciation en appelant la méthode [ncDenonc/Create](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#e4bd4243-facd-48f3-80e9-b422089910f5). Les informations à fournir sont identiques à la méthode de vérification appelée en étape 1.

## Options

L'API Koban permet de vérifier qu'une pose d'option est possible et ensuite de pouvoir poser une option.

Via un WebHook, vous pouvez également être notifié en cas d'une pose d'option sur Koban. Si vous associez un système distant à Koban sur les options, vous devez également vérifier que votre système gère l'expiration d'option de la même manière que Koban, afin que les systèmes soient synchrones.

### Vérification préalable à la pose d'option

Pour vérifier qu'une pose d'option est possible sur un lot, vous devez appeler la méthode [ncOption/GetLotStatus](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#069a1f5d-0ba0-427f-b609-5192ca0f1a9f).

Cette méthode doit **<u>être appelée avant chaque pose d'option</u>**.

Le seul paramètre nécessaire est le code du lot.

Les résultats possibles sont les suivants :

- Result = 0. Aucune option n'est posée. La pose d'option est possible
- Result = 1 et MaxRank = 1. Une option en cours de rang 1 est posée. La pose d'option est possible en rang 2. EndDate donne la date et l'heure d'expiration de l'option en rang 1.
- Result = 1 et MaxRank = 2. Deux options sont en cours. La pose d'option n'est pas possible.
- Result = -1. Le lot est inconnu dans Koban. La pose d'option n'est pas possible.

### Pose d'option

Une fois la vérification effectuée, la pose d'option est possible via la méthode [ncOption/Add](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#16a2a9e1-baf8-4815-be2c-9a0e3d4e53ce).

Les paramètres à fournir sont les suivants :

- Third.Guid : L'identifiant Koban du compte préalablement créé (via une dénonciation par exemple)
- Deal.Extcode : Le code du lot
- DateOption : La date de pose de l'option en timestamp UNIX
- Rank : Le rang de l'option demandé (1 ou 2), en fonction du résultat de la vérification préalable
- Part.Guid : Eventuellement, l'identifiant Koban du partenaire posant l'option

Le résultat sera le suivant :

- success : Si true, la pose d'option a réussi. Si false, la pose d'option n'est pas possible et la raison est retournée par errorcode et message
- errorcode : 
  - Si errorcode = 01, alors le prospect a déjà 3 options en cours
  - Si errorcode = 02, le lot n'est pas au statut libre ou option (déjà réservé par exemple)
  - Si errorcode = 03, l'utilisateur effectuant la pose d'option via l'API a atteint sa limite d'option en simultané
  - Si errorcode = 04, une préréservation est déjà en cours pour ce lot
  - Si errorcode = 05, il y a déjà 2 options en cours pour ce lot

### Expiration d'option dans le système distant

Si un système distant est connecté, les options doivent expirer suivant les règles suivantes :

- Expiration possible toutes les 30 minutes à heure et demi-heure fixe
- L'expiration doit tenir compte de la durée de vie des options paramétrée dans Koban et de l'éventuellement date de prolongation.

### Prolongation d'option

La méthode permettant de prolonger une option est [ncOption/Prolong](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#6c26a601-3c10-47a0-85cf-b0df501a8513).

Les seuls paramètres à transmettre sont Deal.Extcode, Rank et DateProlongation (au format UNIX).

Le résultat sera le suivant :

- success : Si true, la prolongation a été effectuée. Si false, la prolongation a été faite n'a pas été faite et la raison est retournée par errorcode
- errorcode. Si errorcode = 01, alors l'option correspondant au lot et au rang n'a pas été trouvée. Si errorcode = 02, la prolongation a déjà été effectuée.

### Annulation d'option

En cas d'annulation d'option, la méthode à appeler est [ncOption/Undo](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#f3e9cdca-74d0-406f-9f09-be167d166689).

Les seuls paramètres à transmettre sont Deal.Extcode et Rank.

Le résultat sera le suivant :

- success : Si true, l'annulation a été effectuée. Si false, l'annulation n'a pas été faite et la raison est retournée par errorcode
- errorcode. Si errorcode = 01, alors l'option correspondant au lot et au rang n'a pas été trouvée.

### Notification par Koban d'un système distant via un webhook

Les URL à appeler par Koban sont paramétrables par l'administrateur au niveau de l'interface de paramétrage du module Koban Immobilier.

En cas d'authentification nécessaire sur ces URL (header, querystring...), il est nécessaire de contacter le support Koban pour la mise en place du processus d'authentification.

Les différentes notifications possibles sont les suivantes :

#### Vérification préalable à la pose d'option

Cette notification s'effectue au moment du clic sur le bouton "Poser une option" dans Koban. Elle permet de vérifier qu'un système distant autorise la pose d'option avant même que cette option soit posée.

L'URL est appelée en GET avec un paramètre querystring **extcode** ayant pour valeur le code du lot.

La réponse attendue est au format JSON avec les propriétés suivantes :

- status : si true, la pose d'option est possible. si false, la pose d'option n'est pas possible
- rank : Eventuellement le rang de la prochaine option

#### Après la pose d'option

L'URL est appelée en POST, les paramètres transmis en form-encoded.

| Paramètre            | Description                               |
| -------------------- | ----------------------------------------- |
| Deal_Extcode         | Code externe du lot                       |
| Deal_Guid            | Code Koban du lot                         |
| Third_Extcode        | Code externe du compte posant l’option    |
| Third_Guid           | Guid Koban du compte posant l’option      |
| Rank                 | Rang de l’option (1 ou 2)                 |
| ExpDate              | Date d’expiration de l’option (Timestamp) |
| Third_Name           | Nom du réservataire                       |
| Third_FirstName      | Prénom du réservataire                    |
| Third_EMail          | EMail du réservataire                     |
| AssignedTo_Name      | Nom du commercial                         |
| AssignedTo_FirstName | Prénom du commercial                      |
| AssignedTo_EMail     | EMail du commercial                       |

Le retour attendu est au format JSON avec les propriétés suivantes **:**

- success : true ou false

- error : Erreur éventuelle composée des propriétés :
  - message : libellé de l’erreur
  - code : Code de l’erreur

#### Après une annulation d'option

L'URL est appelée en POST, les paramètres transmis en form-encoded.

| Paramètre     | Description                            |
| ------------- | -------------------------------------- |
| Deal_Extcode  | Code externe du lot                    |
| Deal_Guid     | Code Koban du lot                      |
| Third_Extcode | Code externe du compte posant l’option |
| Third_Guid    | Guid Koban du compte posant l’option   |
| Rank          | Rang de l’option (1 ou 2)              |

Le retour attendu est au format JSON avec les propriétés suivantes **:**

- success : true ou false

- error : Erreur éventuelle composée des propriétés :
  - message : libellé de l’erreur
  - code : Code de l’erreur

#### Après une prolongation d'option

L'URL est appelée en POST, les paramètres transmis en form-encoded.

| Paramètre     | Description                                  |
| ------------- | -------------------------------------------- |
| Deal_Extcode  | Code externe du lot                          |
| Deal_Guid     | Code Koban du lot                            |
| Third_Extcode | Code externe du compte posant l’option       |
| Third_Guid    | Guid Koban du compte posant l’option         |
| Rank          | Rang de l’option (1 ou 2)                    |
| ExpDate       | Date d’expiration de l’option (Timestamp)    |
| PrgDate       | Date de prolongation de l’option (Timestamp) |

Le retour attendu est au format JSON avec les propriétés suivantes **:**

- success : true ou false

- error : Erreur éventuelle composée des propriétés :
  - message : libellé de l’erreur
  - code : Code de l’erreur

## Dossier de réservation

L'API Koban permet de poser un dossier de réservation incomplet (pose initiale) ainsi que de désister un dossier de réservation existant.

### Pose de préréservation initiale

La méthode Koban à appeler est [ncPreresv/Add](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#33bceee9-4493-49a3-9bdf-4d8851c45a74).

Les paramètres à transmettre sont :

- Deal.Extcode : Le code du lot
- Third.Guid : L'identifiant Koban du prospect (réservataire 1)
- PrixVente : Le prix de vente
- Garantie : Le montant de la garantie
- Part.Guid : L'identifiant Koban du partenaire effectuant la demande de réservation

Les résultats possibles sont :

- success : Si true, la pose du dossier de réservation a été effectuée. Si false, la pose du dossier de réservation n'a pas été faite et la raison est retournée par errorcode
- errorcode. Si errorcode = 01, alors le lot n'existe pas, Si errorcode = 02, le prospect n'existe pas.

### Désistement

La méthode Koban à appeler est [ncPreresv/Desist](https://documenter.getpostman.com/view/1804856/SzKQyLUw?version=latest#a62d2c84-51f4-47e8-8834-1862d398a547).

Les paramètres à transmettre sont :

- Deal.Extcode : Le code du lot
- Third.Guid : L'identifiant Koban du prospect (réservataire 1)

Les résultats possibles sont :

- success : Si true, le désistement a été effectué. Si false, le désistement n'a pas été fait et la raison est retournée par errorcode
- errorcode. Si errorcode = 01, alors le lot n'existe pas, Si errorcode = 02, le prospect n'existe pas.

### Notification par Koban d'un système distant via Webhook

Les URL à appeler par Koban sont paramétrables par l'administrateur au niveau de l'interface de paramétrage du module Koban Immobilier.

En cas d'authentification nécessaire sur ces URL (header, querystring...), il est nécessaire de contacter le support Koban pour la mise en place du processus d'authentification.

Les différentes notifications possibles sont les suivantes :

#### Validation d'un dossier de réservation

L'URL est appelée en POST, les paramètres transmis en form-encoded.

| Paramètre                | Description                          |
| ------------------------ | ------------------------------------ |
| Lot_Code                 | Code externe du lot                  |
| Vendeur_Groupe           | Groupe Vendeur                       |
| Res1Genre                | Genre Réservataire 1                 |
| _id                      | Guid Préréservation                  |
| DealId                   | Guid Lot                             |
| ThirdId                  | Guid Acquéreur                       |
| PrixVente                | Prix de vente                        |
| Garantie                 | Montant de Garantie                  |
| AssignedToId             | Guid Commercial                      |
| OptionId                 | Guid Option initiale                 |
| PreresaDate              | Date de préréservation               |
| Annexe1_cent             | Montant Annexe 1 (en centimes)       |
| Annexe2_cent             | Montant Annexe 1 (en centimes)       |
| Annexe3_cent             | Montant Annexe 1 (en centimes)       |
| Annexe4_cent             | Montant Annexe 1 (en centimes)       |
| Annexe5_cent             | Montant Annexe 1 (en centimes)       |
| DealProcessId            | Guid Programme                       |
| Res1Nom                  | Nom Réservataire 1                   |
| Res1Prenom               | Prénom Réservataire 1                |
| Res1DateNaissance        | Date de naissance  Réservataire  1   |
| CanalOrigine_sId         | 591411344e86af13648bc05d             |
| CanalOrigine_Label       | Canal d'origine                      |
| Res1NomSCI               | Nom SCI                              |
| Res1Adr_Street           | Adresse - Rue Réservataire 1         |
| Res1Adr_Complement       | Adresse - Complément Réservataire 1  |
| Res1Adr_ZipCode          | Adresse - Code Postal Réservataire 1 |
| Res1Adr_City             | Adresse - Ville Réservataire 1       |
| Res1Phone                | Numéro de téléphone Réservataire 1   |
| Res1Mail                 | EMail Réservataire 1                 |
| Res2                     | Réservataire 2 (O/N)                 |
| Res2Nom                  | Nom Réservataire 2                   |
| Res2Prenom               | Prénom Réservataire 2                |
| Res2Phone                | Numéro de téléphone Réservataire 2   |
| Res2Mail                 | EMail Réservataire 2                 |
| AutreParking             | Autre Parking                        |
| Options                  | Options                              |
| FraisNotaireMontant_cent | Montant frais de notaire (centimes)  |
| Apport_cent              | Montant Apport (centimes)            |
| PretImmo1_cent           | Montant Prêt Immo 1 (centimes)       |
| TVA                      | TVA                                  |
| PretImmo2_cent           | Montant Prêt Immo 2 (Centimes)       |
| CanalVente_Label         | Canal de vente                       |
| Res1Profession_Label     | Profession Réservaire 1              |
| Res2DateNaissance        | Date de naissance Réservataire 2     |
| Res2Profession_Label     | Profession Réservaire 2              |
| Res2Adr_Street           | Rue Réservataire 2                   |
| Res2Adr_ZipCode          | Code postal Réservataire 2           |
| Res2Adr_City             | Ville Réservataire 2                 |
| FraisNotaireOffert       | Frais de notaire offert (O/N)        |
| NatureAchat_Label        | Nature achat                         |
| PlusieursPrets           | Plusieurs prêts (O/N)                |
| PTZ                      | PTZ (O/N)                            |
| PTZMontant_cent          | Montant PTZ (centimes)               |
| AssignedTo_Name          | Nom Commercial                       |
| AssignedTo_FirstName     | Prénom Commercial                    |
| AssignedTo_EMail         | EMail Commercial                     |

Le retour attendu est au format JSON avec les propriétés suivantes **:**

- success : true ou false

- error : Erreur éventuelle composée des propriétés :
  - message : libellé de l’erreur
  - code : Code de l’erreur

#### Désistement d'un dossier de réservation

L'URL est appelée en POST, les paramètres transmis en form-encoded.

| Paramètre    | Description         |
| ------------ | ------------------- |
| Deal_Extcode | Code externe du lot |
| Deal_Guid    | Code Koban du lot   |

Le retour attendu est au format JSON avec les propriétés suivantes **:**

- success : true ou false

- error : Erreur éventuelle composée des propriétés :
  - message : libellé de l’erreur
  - code : Code de l’erreur