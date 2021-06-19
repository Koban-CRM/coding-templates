# Structure API Compte

Voici la structure JSON d'un compte via l'API Koban.
Elle est à utiliser pour les mises à jour via l'API et est également retournée par les méthodes de sélection.

**Version Compatible** : Juin 2021 et supérieures

```json
{
    "Label": "SNCF RESEAU", 					// Nom du compte
    "Obsolete": false,							// Obsolète O/N
    "FirstName": null,							// Prénom du compte (dans le cas d'un Particulier)
    "Gender": null,
    "StructCode": null,
    "Status": {
    	"Label": "Prospect",
        "Code": "PRO",
        "Guid": "60cd9f910dc36124f4d11baa",
        "DUpdated": 0.0,
        "Updated": "0001-01-01T00:00:00",
        "DCreated": 0.0,
        "Created": "0001-01-01T00:00:00"
	},
    "Type": {
    	"Label": "Professionnel",
        "Code": "PRO",
        "Guid": "60cd9f910dc36124f4d11bd1",
        "DUpdated": 0.0,
        "Updated": "0001-01-01T00:00:00",
        "DCreated": 0.0,
        "Created": "0001-01-01T00:00:00"
	},
    "Extcode": "C1000739",
    "OtherCode": null,
    "Comments": null,
    "AccountingCode": null,
    "Address": {
    	"Guid": null,
        "Extcode": null,
        "Reference": null,
        "Compl": null,
        "Street": "8 chemin de hausses",
        "ZipCode": "64100",
        "City": "BAYONNE",
        "Name": null,
        "FirstName": null,
        "Phone": null,
        "Country": "FR"
	},
    "InvoiceAddress": null,
    "DelivAddress": [],
    "Website": null,
    "Phone": null,
    "Cell": null,
    "Fax": null,
    "EMail": null,
    "OfficialNumber": null,
    "Vat": null,
    "Unsuscribe": false,
    "InvalidMail": false,
    "InvalidSMS": false,
    "ModeRglt": null,
    "EcheanceCode": null,
    "Title": null,
    "eShop": null,
    "TaxRate": 0.0,
    "AssignedTo": null,
    "UpdatedBy": "60cd9f910dc36124f4d11b9b",
    "Tags": null,
    "MoreFields": null,
    "Origin": null,
    "NextAction": null,
    "UTMCampaign": null,
    "UTMMedium": null,
    "UTMSource": null,
    "Optin": false,
    "Geo": null,
    "AccountToInvoice": null,
    "IBAN": null,
    "Guid": "60cda25c0dc36124f4d11cfa",
    "DUpdated": 1624096380.3639998,
    "Updated": "2021-06-19T09:53:00.364",
    "DCreated": 1624096380.3639998,
    "Created": "2021-06-19T09:53:00.364""
}
```

