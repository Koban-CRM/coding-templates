# Tracking API

### Access and endpoints

Here you can find endpoints :

| Environment                                            | Endpoint                          | Comments                 |
| ------------------------------------------------------ | --------------------------------- | ------------------------ |
| PRODUCTION                                             | https://addin-koban.com           |                          |
| SANDBOX                                                | https://trk-preprod.app-koban.com | Ask Koban to open access |
| SANDBOX **V5**                                         | http://devttrack.itsonlyleads.com | Ask Koban to open access |
| FUTURE VERSION **V5**<br />*Warning ! Alpha version !* | http://testtrack.itsonlyleads.com | Ask Koban to open access |

### Authentication

The following identification parameters are necessary for use of the tracking API

| Server  | The Koban Tracking Server. By default :   https://addin-koban.com |
| ------- | ------------------------------------------------------------ |
| Zid     | Your account security key. Available under Parameters > API  |
| Clé API | Available under Parameters > API                             |

### Field types in Koban

Engagement information is passed through field values. Each field has an internal Koban code that must be transmitted via the tracking API.

#### Standard fields

All of the following fields can be transmitted to Koban :

| **Champ**             | **Code**             | **Format**                                                   |
| --------------------- | -------------------- | ------------------------------------------------------------ |
| Official code (SIRET) | third_officialnumber | Texte                                                        |
| External Code         | third_extcode        | Texte                                                        |
| Company name          | third_label          | Texte                                                        |
| Address > Complement  | third_adrscompl      | Texte                                                        |
| Address > Street      | third_adrsstreet     | Texte                                                        |
| Address > Zip Code    | third_adrszipcode    | Texte                                                        |
| Address > City        | third_adrscity       | Texte                                                        |
| Address > Country     | third_adrscountry    | Format ISO 2 lettres                                         |
| Name                  | contact_name         | Texte                                                        |
| First Name            | contact_firstname    | Texte                                                        |
| Gender                | contact_gender       | Code de la valeur de liste Appelation dans Koban             |
| EMail                 | contact_email        | Texte                                                        |
| Phone number          | contact_phone        | Texte                                                        |
| Function              | contact_function     | Texte ou si le champ fonction est paramétré comme liste, libellé du  valeur de liste |
| Cell                  | contact_mobile       | Texte                                                        |
| Comments              | contact_comment      | Texte                                                        |
| Optin                 | Optin                | on ou off                                                    |

#### Transmission on the server side

For each point of engagement, you must have the form identifier and the associated landing page.
The information must then be transmitted via an http POST as follows:

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

#### Return

The method returns a JSON with this structure :

* s (Success true or false)

* a
  * ld : Lead Guid created or updated
  * ctc : Contact Guid updated
  * th: Third Guid updated

