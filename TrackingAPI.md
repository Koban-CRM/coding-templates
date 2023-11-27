# API de tracking

### endpoints

Les endpoints principaux sont les suivants :

| Environnement                                          | Endpoint                          | Commentaires                                      |
| ------------------------------------------------------ | --------------------------------- | ------------------------------------------------- |
| PRODUCTION                                             | https://addin-koban.com           |                                                   |
| SANDBOX                                                | https://trk-preprod.app-koban.com | Demande d'accès préalable auprès du support Koban |
| SANDBOX **V5**                                         | http://devttrack.itsonlyleads.com | Demande d'accès préalable auprès du support Koban |
| FUTURE VERSION **V5**<br />*Warning ! Alpha version !* | http://testtrack.itsonlyleads.com | Demande d'accès préalable auprès du support Koban |

### Authentication

Les paramètres d'authentification suivants sont nécessaires

| Server  | The Koban Tracking Server. By default :   https://addin-koban.com |
| ------- | ------------------------------------------------------------ |
| Zid     | La clé de sécurité. Disponibles sous Paramètres > API        |
| Clé API | Disponible sous Paramètres > API                             |

### Transmettre les valeurs de champ à Koban

Les informations d'engagement sont transmises à Koban via des valeurs de champ. Chaque champ dispose d'un code interne à Koban qui doit être transmis via l'API de Tracking.

#### Champs standard

Ces champs standards peuvent être transmis à Koban :

| **Champ**             | **Code**             | **Format**                                                   |
| --------------------- | -------------------- | ------------------------------------------------------------ |
| SIRET                 | third_officialnumber | Texte                                                        |
| Code externe          | third_extcode        | Texte                                                        |
| Nom Entreprise        | third_label          | Texte                                                        |
| Adresse > Complément  | third_adrscompl      | Texte                                                        |
| Adresse > Rue         | third_adrsstreet     | Texte                                                        |
| Adresse > Code Postal | third_adrszipcode    | Texte                                                        |
| Adresse > Ville       | third_adrscity       | Texte                                                        |
| Adresse > Pays        | third_adrscountry    | Format ISO 2 lettres                                         |
| Nom                   | contact_name         | Texte                                                        |
| Prénom                | contact_firstname    | Texte                                                        |
| Civilité              | contact_gender       | Code de la valeur de liste Appelation dans Koban             |
| EMail                 | contact_email        | Texte                                                        |
| Numéro de téléphone   | contact_phone        | Texte                                                        |
| Fonction              | contact_function     | Texte ou si le champ fonction est paramétré comme liste, libellé du  valeur de liste |
| Mobile                | contact_mobile       | Texte                                                        |
| Commentaires          | contact_comment      | Texte                                                        |
| Optin                 | Optin                | on ou off                                                    |

#### Tags

##### Code

Le code de chaque tag est transmis selon le code suivant :

**Tag + Identifiant de la catégorie de tag**

Ex. :

*Tag56e118c00dc3610dc461fbf4*

##### Format

La valeur transmise peut être soit le libellé exact, soit le code externe du tag.

#### Champs personnalisé

##### Code

Le code de chaque champ personnalisé est transmis selon le code suivant :

**Spé + Identifiant du champ personnalisé**

Ex. :

*Spe56e98f390dc3610c5cb4032a*

##### Valeur

| Type de champ | Format                                                       |
| ------------- | ------------------------------------------------------------ |
| Texte         | Texte                                                        |
| Numérique     | Nombre (séparateur point)                                    |
| Date          | Date au format DD/MM/YYYY                                    |
| Oui/Non       | Les valeurs suivantes sont acceptées :<br />- pour true : on, true<br />- pour false : off, false |



#### Transmission coté serveur

Pour chaque point d'engagement, vous devez disposer de l'identifiant du formulaire et de l'identifiant du point d'engagement. L'information est transmise ensuite via un http POST :

```
POST http(s)://SERVERKOBAN/Form/sbm?id=[IDFORMULAIRE]&cid=[cid]&zid=[CLESECURITE]&_cnl=&_scl=&_lp=[IDLANDINGPAGE]&utm_campaign=[utm_campaign]&utm_source=[utm_source]&utm_medium=[utm_medium]&utm_content=[utm_content]&utm_term=[utm_term] HTTP/1.1

  Host: SERVERKOBAN

  Connection: keep-alive

  Content-Length: 105

  Accept: */*

  Content-Type: application/x-www-form-urlencoded; charset=UTF-8

contact_name=ACMETEST&Tag5502afe50dc3610e8c5fd66f=5502afe50dc3610e8c5fd66c&Spe57cfe7b40dc3610ed8db0bf5=38
```

[See example here](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest#cd216ab2-f29d-417e-bf0c-32ef63b19fd7).

##### Retour

La méthode retourne un JSON avec cette structure :

* s (Succès true or false)

* a
  * ld : Guid Piste créée ou mise à jour
  * ctc : Guid Contact créé ou mis à jour
  * th: Guid Compte créé ou mis à jour

