# API Model Structure - Account

You can find here JSON structure for an account (company or person) in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
{
    "Label": "Account Label",
    "FirstName": "FirstName (for a person)",
    "Gender": null,
    "StructCode": null,
    "Status": {
        "Code": "CLI"
    },
    "Type": {
        "Code": "PRO"
    },
    "Extcode": "External Code",
    "OtherCode": null,
    "Comments": "Comments",
    "AccountingCode": "411FEF",
    "Address": {
    	"Reference": "Code",
    	"Name": "Address Contact name",
    	"FirstName": "Address Contact First name",
    	"Phone": "Address Contact phone",
    	"Compl": "Address complement",
    	"Street": "Address street",
    	"ZipCode": "00000",
    	"City": "Address City",
    	"Country": "FR"
    },
    "DelivAddress": {
    	"Reference": "Code",
    	"Name": "Address Contact name",
    	"FirstName": "Address Contact First name",
    	"Phone": "Address Contact phone",
    	"Compl": "Delivery Address complement",
    	"Street": "Delivery Address street",
    	"ZipCode": "00000",
    	"City": "Delivery Address City",
    	"Country": "FR"
    },
    "Website": null,
    "Phone": null,
    "Cell": null,
    "Fax": null,
    "EMail": null,
    "ModeRglt": "PAYMENTMODE LIST VALUE CODE",
    "OfficialNumber": null,
    "Vat": null,
    "Unsuscribe": false,
    "InvalidMail": false,
    "InvalidSMS": false,
    "Title": null,
    "eShop": null,
    "TaxRate": 0,
    "AssignedTo": {
        "Extcode": "User Code"
    },
    "Tags": [
    	{
    		"TagCategoryCode": "ACTIVITY",
    		"Label": "Agriculture"
		}
	],
    "MoreFields": [
        {
            "FieldId": "5583bc220dc3610a94746d3b",
            "Value": "Field Value"
        },
        {
            "FieldId": "5583bc2c0dc3610a94746d3c",
            "Value": ""
        },
        {
            "FieldId": "55bb1fc80dc3610a9c3128d8_lb",
            "Value": ""
        },
        {
            "FieldId": "55bb1fc80dc3610a9c3128d8",
            "Value": ""
        },
        {
            "FieldId": "55e706ce0dc36404a8cd2278",
            "Value": "true"
        }
    ],
    "Origin": {
        "Code": "WEB"
    },
    "UTMSource": "UTM Marketing Source",
    "UTMMedium": "UTM Marketing Medium",
    "UTMCampaign": "UTM Marketing Campaign",
    "Optin": true,
    "DCreated": 1555608374,
    "DUpdated": 1555608374
}
```

| Property         | Comment                                                      | In POST methods                | In GET methods |
| ---------------- | ------------------------------------------------------------ | ------------------------------ | -------------- |
| Label            | Company Label or Name for a person                           | yes                            | yes            |
| Extcode          | External Code                                                | yes                            | yes            |
| Guid             | Koban Guid                                                   | yes                            | yes            |
| OtherCode        | Other Code                                                   | yes                            | no             |
| Obsolete         | Obsolete or not                                              | yes                            | no             |
| FirstName        | First name (for a person)                                    | yes                            | yes            |
| Gender           | Civility Code                                                | yes                            | yes            |
| Status           | Status                                                       | yes (Fill Code)                | yes            |
| Type             | Type                                                         | yes (Fill Code)                | yes            |
| Comments         | Comments                                                     | yes                            | yes            |
| AccountingCode   | Accounting Code                                              | yes                            | yes            |
| Address          | Address Object (Street, Complement, ZipCode, City, Country). County must by ISO 2 letters. | yes                            | yes            |
| InvoiceAddress   | Invoice Address Object (Street, Complement, ZipCode, City, Country). County must by ISO 2 letters. | yes                            | yes            |
| DelivAddress     | Array of Delivery addresses Object (External Code, Koban Guid, Street, Complement, ZipCode, City, Country). County must by ISO 2 letters. | yes (Fill Extcode or Guid)     | yes            |
| Website          | Web site                                                     | yes                            | yes            |
| Phone            | Phone                                                        | yes                            | yes            |
| Cell             | Cell                                                         | yes                            | yes            |
| Fax              | Fax                                                          | yes                            | yes            |
| EMail            | EMail                                                        | yes                            | yes            |
| OfficialNumber   | SIREN                                                        | yes                            | yes            |
| Vat              | VAT Number                                                   | yes                            | yes            |
| Unsuscribe       | true if account has unsuscribed                              | yes                            | yes            |
| InvalidMail      | true if account email detected invalid                       | yes                            | no             |
| InvalidSMS       | true if account cell detected invalid                        | yes                            | no             |
| ModeRglt         | Payment mode Code                                            | yes (Fill list Value)          | no             |
| EcheanceCode     | Term mode                                                    | yes (fill Term label)          | no             |
| eShop            | eShop origin                                                 | yes                            | yes            |
| TaxRate          | Tax rate                                                     | yes                            | yes            |
| AssignedTo       | User assigned.<br />If FullName is provided, it must by "First Name + Name" filled in Koban | yes (Fill Extcode or FullName) | yes            |
| Tags             | Tag array                                                    | yes                            | yes            |
| MoreFields       | Specific fields array                                        | yes                            | yes            |
| Origin           | Origin list value                                            | yes (Fill Code)                | yes            |
| NextAction       | Next action                                                  | no                             | no             |
| UTMCampaign      | UTM Campaign                                                 | yes                            | yes            |
| UTMMedium        | UTM Medium                                                   | yes                            | yes            |
| UTMSource        | UTM Source                                                   | yes                            | yes            |
| Optin            | true if account is optin                                     | yes                            | yes            |
| Geo              | Geographical coords. X and Y subproperties                   | yes                            | no             |
| AccountToInvoice | Account to invoice                                           | yes (Fill Extcode or Guid)     | yes            |
| IBAN             | IBAN coords. BANQUE, GUICHET, SWIFT, IBAN subproperties      | no                             | no             |
