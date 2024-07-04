# API

### Access and endpoints

Here you can find endpoints :

| Environment                                     | Endpoint                           | Comments                 |
| ----------------------------------------------- | ---------------------------------- | ------------------------ |
| PRODUCTION                                      | https://app-koban.com/api/v1       |                          |
| SANDBOX                                         | http://rct.itsonlyleads.com/api/v1 | Ask Koban to open access |
| FUTURE VERSION<br />*Warning ! Alpha version !* | http://test.app-koban.com/api/v1   | Ask Koban to open access |

### Authentication

For authentication, you must provide two keys on your **header request**.
This keys can be found on Koban under **Parameters > API**.

- **X-ncApi** : API Key
- **X-ncUser** : User login key

Example : 20 first leads

```http
GET https://app-koban.com/api/v1/ncLead/GetPending?st=0&s= HTTP/1.1
Host: app-koban.com
Connection: keep-alive
X-ncApi: YOUR API KEY
X-ncUser: YOUR USER KEY
Accept: application/json
```

### Methods Documentation

Here you can find API methods list.

The first link provides all methods in the actual Koban cloud version. The second link provides all methods in the next Koban cloud version.

- [Browse all methods](https://documenter.getpostman.com/view/1804856/SzKSSKAk?version=latest)

### Dealing with Tags and specific fields with API

You can create, update or retrieve accounts, contacts, leads, deals or actions with the API. For each object, tags and specific field can be retrieved.

#### Tags

Tags are retrieved or updated with Tags array.

Each part of this array consists of minimum two properties :

- **TagCategoryCode** : Tag category code (*you can customize it under Koban parameters > General > Tag Category, select your category and change External Code*) 
- **Label** : The label of the tag
- **ExternalCode** : If you prefer find your tag by its code, use this property

Warning ! the tag must be declared in Koban before inserting it with the API !

#### Specific objects 

Specific objects are retrieved or updated with **MoreFields** array.

Each part of this array consists of two properties :

- **FieldId** : The specific field ID in Koban (*you can find it in Koban parameters > Object (Third, Contact, Lead...) > Customization*)
- **Value** : The specific field value. The format is :
  - true or false for a boolean value
  - DD/MM/YYYY for a date
  - Label or External code for a list value

### Webhooks

#### Documentation

Koban can launch a webhook on several events.

You can register your webhook by two ways :

- From the API with the [ncHook](https://app-koban.com/Static/apidoc.html#operation/ncHook_Subscribe) methods
- From Koban directly under **Parameters > API > Webhooks**.

#### Payloads

You can find here payloads description for all webhooks.

##### Account

```
[
          {
            "GridLabel": "TESTTTTTT", // Account Label
            "Location": null, // Geographic location
            "LastActionClosedEnd": "/Date(-62135596800000)/", // Last action closed date
            "LastActionComment": null, // Last action comment
            "FirstName": null, // First name
            "Optin": false, // Optin
            "Address": null, // Address object
            "Website": null, // Web site
            "Gender": null, // Gender
            "Origin": {
              "ExternalCode": "WEB",
              "Label": "WEB",
              "sId": "551020cb0dc36102a082f1ba"
            }, // Account Origin
            "oType": {
              "ExternalCode": "PRO",
              "Label": "Professionnel",
              "sId": "5502afe50dc3610e8c5fd664"
            }, // Account type
            "oStatus": {
              "ExternalCode": "CLI",
              "Label": "Client",
              "sId": "5502afe50dc3610e8c5fd661"
            }, // Account status
            "oAssignedToIdUser": {
              "Label": "Guillaume Kobanne",
              "Login": "guillaume@itsonlyleads.com",
              "Name": "Kobanne",
              "FullName": "Guillaume Kobanne",
              "sId": "5502a6d30dc361046cba4b1e",
              "Mobile": null,
              "AvatarThumbnail": "5502a6d30dc361046cba4b1d_smallman2_th.jpg",
              "AvatarThumbnailUrl": "https://nocrmmedia.s3-eu-west-1.amazonaws.com/5502a6d30dc361046cba4b1d_smallman2_th.jpg?AWSAccessKeyId=AKIAJ7E7TZUWJVQTCWNQ&Expires=1893452400&Signature=P06qUbbeZssKp9g%2BAelhdqly6NE%3D"
            }, // User Assigned to account
            "LastQuoteSent": "/Date(-62135596800000)/", // Last quote sent date
            "Unsuscribe": false, // Unsuscribed from Emailing
            "VatNumber": null, // VAT Number
            "OfficialNumber": "ffrdde", // Official (SIRET) Number
            "PaymentMode": {
              "ExternalCode": "CHQ",
              "Label": "Par chèque",
              "sId": "5791d0710dc36117a8d6a56c"
            }, // Payment mode
            "Comments": null, // Comments
            "OtherAssignedToIdUsersLb": "", 
            "AccountingCode": "411TE7", // Internal accounting code
            "Phone": null, // Phone
            "Fax": null, // Fax
            "Photo": null,
            "PhotoUrl": "https://nocrmmedia.s3-eu-west-1.amazonaws.com/?AWSAccessKeyId=AKIAJ7E7TZUWJVQTCWNQ&Expires=1893452400&Signature=zzuFAqEbTXM%2BwvIBjWa9Y2VGcR8%3D",
            "Mobile": null, // Mobile
            "EMail": null, // EMail
            "EMailSec": null, // Secondary EMail
            "FrequencyRDVDate": "/Date(1494666003829)/", // Next periodical meeting advised
            "Tags": null, // Tags collection
            "oSource": null, // Marketing Source
            "oCanal": null, // Marketing Canal
            "oCampaign": null, // Marketing Campaign
            "LastInteraction": "/Date(1452170049655)/", // Last interaction Date (RGPD)
            "UnsuscribeSMS": false, // Unsuscribed from SMS Channel
            "UnsuscribePhoning": false, // Unsuscribed from phoning
            "UnsuscribeFullProspection": false, // Unsuscribed from all forms of prospection
            "Forget": false, // RGPD Forget
            "TaxAccountId": "57f4ca0e0dc3611764666ca7", // Tax Account Guid
            "IBAN": null, // IBAN
            "IsPrivate": false, // Is Private
            "CanDelete": false, // Can be deleted
            "AssignedToId": "5502a6d30dc361046cba4b1e", // User assigned Guid 
            "OtherAssignedToId": null,
            "StructureId": null, // Structure Guid
            "CreationDate": "/Date(1452170049655)/", // Creation Date
            "LastUpdateDate": "/Date(1579771515726)/", // Last Update date
            "ExternalCode": null, // External Code
            "OtherCode": null, // Other code
            "Obsolete": false, // Deleted
            "MoreFields": [
              {
                "FieldId": "5583bc220dc3610a94746d3b", // Field Id
                "Value": "Valeur" // Field value
              },
              ....
            ],
            "sId": "568e69510dc3610c100e7baf", // Guid Koban
            "Label": "TESTTTTTT" // Account label
          }
        ]
```

##### Contact

```
 [
                {
                    "InvalidMail": false, // Invalid Email
                    "Points": 0, // Score
                    "Tags": null, // Tags list
                    "CanDecide": false, // Can Decide
                    "CanBuy": false, // Is a buyer
                    "ToSync": false, // To sync in external systems
                    "ExtrLogin": null, // Extranet Login
                    "IsInvoicingContact": false, // Is default invoicing contact
                    "Optin": false, // Optin
                    "EMail": "maxime@evotion.fr", // EMail
                    "EMailSec": null, // Secondary Email
                    "Phone": null, // Phone
                    "Mobile": "06 66 54 84 84", // Cell
                    "OtherAssignedToIdUsersLb": "",
                    "Photo": null,
                    "PhotoUrl": "https://nocrmmedia.s3-eu-west-1.amazonaws.com/?AWSAccessKeyId=AKIAJ7E7TZUWJVQTCWNQ&Expires=1893452400&Signature=zzuFAqEbTXM%2BwvIBjWa9Y2VGcR8%3D",
                    "oActualThird": null, // Actual Account associated (see Account properties)
                    "Function": null, // Function
                    "oAssignedToIdUser": null,
                    "Gender": null, // Gender
                    "Origin": null, // Contact Origin
                    "oSource": null, // Marketing Source
                    "oCampaign": null, // Marketing Campaign
                    "LastActionClosedEnd": "/Date(-62135596800000)/", // Last action closed date
                    "Name": null, // name
                    "FirstName": null, // FirstName
                    "Comments": null, // Comments
                    "LastInteraction": "/Date(-62135596800000)/", // Last interaction date
                    "Unsuscribe": false, // Unsuscribed from emails
                    "UnsuscribeSMS": false, // Unsuscribed from SMS channels
                    "UnsuscribePhoning": false, // Unsuscribed from phoning prospection
                    "UnsuscribeFullProspection": false, // Unsuscribed from all prospection channels
                    "Forget": false, // Forgetted (RGPD)
                    "IsPrivate": false, // Is private
                    "CanDelete": false, // Is deletable
                    "AssignedToId": null, // User associated guid
                    "OtherAssignedToId": null,
                    "StructureId": null, // Structure Guid
                    "CreationDate": "/Date(-62135596800000)/", // Creation Date
                    "LastUpdateDate": "/Date(1579769877905)/", // Last update date
                    "ExternalCode": null, // External Code
                    "OtherCode": null, // Other Code
                    "Obsolete": false, // Deleted
                    "MoreFields": [], // Specific Fields 
                    "sId": "57553c100dc361125c84e65b", // Guid Koban
                    "GridLabel": "maxime@evotion.fr", // Label
                    "Label": "maxime@evotion.fr"
                }
            ]
```

##### Deal

Look at this page for description : [Webhook Deal](/api/webhook/deal.md)