# Structure API Compte

Voici la structure JSON d'un compte via l'API Koban.
Elle est à utiliser pour les mises à jour via l'API et est également retournée par les méthodes de sélection.

**Version Compatible** : Juin 2021 et supérieures

```
{
    "Label": "SNCF RESEAU", 		 			// Nom du compte			
    "Obsolete": false,							// Obsolète O/N
    "FirstName": null,							// Prénom du compte (dans le cas d'un Particulier)
    "Gender": null,								// Civilité
    "StructCode": null,							// Code Structure (non utilisé)
    "Status": {
    	"Code": "PRO",							// Code externe du statut
	},
    "Type": {
    	"Code": "PRO",							// Code Type
	},
    "Extcode": "C1000739",						// Code Externe
    "OtherCode": null,							// Autre code
    "Comments": null,							// Commentaires
    "AccountingCode": null,						// Compte comptable
    "Address": {								// Adresse principale
        "Extcode": null,
        "Compl": null,
        "Street": "8 chemin de hausses",
        "ZipCode": "64100",
        "City": "BAYONNE",
        "Name": null,
        "FirstName": null,
        "Phone": null,
        "Country": "FR"
	},
    "InvoiceAddress": {							// Adresse de facturation
        "Extcode": null,
        "Compl": null,
        "Street": "8 chemin de hausses",
        "ZipCode": "64100",
        "City": "BAYONNE",
        "Name": null,
        "FirstName": null,
        "Phone": null,
        "Country": "FR"
	},
    "DelivAddress": [							// Adresses de livraison
        {
            "Extcode": null,
            "Compl": null,
            "Street": "8 chemin de hausses",
            "ZipCode": "64100",
            "City": "BAYONNE",
            "Name": null,
            "FirstName": null,
            "Phone": null,
            "Country": "FR"
        }
    ],
    "Website": null,							// Site web
    "Phone": null,								// Téléphone
    "Cell": null,								// Mobile
    "Fax": null,								// Fax
    "EMail": null,								// EMail
    "OfficialNumber": null,						// SIRET
    "Vat": null,								// Code TVA
    "Unsuscribe": false,						// Désinscrit (O/N)
    "InvalidMail": false,						// Email invalide (O/N)
    "InvalidSMS": false,						// SMS invalide (O/N)
    "ModeRglt": "CB",							// Code Mode de règlement
    "TaxRate": 0.0,								// Taux de TVA
    "AssignedTo": "Louise DUMONT",				// Affectation
    "Tags": [									// Liste des Tags
    	{
            "TagCategoryCode": "CODE",
            "Label": "Nom Tag",
            "ExternalCode": "CodeTag"
        }
    ],
    "MoreFields": [								// Liste des champs complémentaires
    	{
            "FieldId": "60cda25c0dc36124f4d11cfb",
            "Value": "Customized field value"
        }
    ],
    "Origin": {									// Code Origine
    	"Code": "WEB"
    },
    "Optin": false,								// Optin
    "AccountToInvoice": {						// Identifiant Autre compte à facturer
    	"Extcode" : "C1000740"
    },					
    "Guid": "60cda25c0dc36124f4d11cfa",			// Identifiant Koban
    "DUpdated": 1624096380.3639998,
    "Updated": "2021-06-19T09:53:00.364",
    "DCreated": 1624096380.3639998,
    "Created": "2021-06-19T09:53:00.364"
}
```

