# API Model Structure - Invoice

You can find here JSON structure for an invoice in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
[{
    	"DeliveryDate": "15/05/2020",
    	"Extcode": "Delivery Code",
    	"Number": "DEL1550",
    	"Third": { "Extcode": "XXXXXX" },
        "Status": "PENDING",
        "DeliveryAddress":{
            "Compl": "BAT A",
            "Street": "8 Rue Mermoz",
            "ZipCode": "05100",
            "City": "BRIANCON",
            "Country": "FR"
        },
        "GestDocument": "5523cf8b0dc3630a04e9a906",
    	"Order": { "Number": "C20-0479"},
        "DepositGuid": "5be410134e86af14447ce000",
    	"Lines":
    	[
    		{
    			"Label": "Line name",
    			"Extcode": "line eshop code",
    			"Comments":"",
    			"Ht": 10,
    			"PrHt": 8,
    			"Quantity": 1,
    			"Product": { "Reference": "DEV" },
    			"Red": 0,
    			"Ttc": 12,
    			"Vat": 20,
    			"UnitPrice": 10
    		}
    	]
    }
]
```

| Property          | Comment                                                      | In POST methods                      | In GET methods                        |
| ----------------- | ------------------------------------------------------------ | ------------------------------------ | ------------------------------------- |
| InvoiceDate       | Invoice Date                                                 | yes                                  | yes                                   |
| Extcode           | External Code                                                | yes                                  | yes                                   |
| Number            | Number                                                       | yes                                  | yes                                   |
| IsAsset           | Is asset                                                     | yes                                  | no                                    |
| Guid              | Koban Guid                                                   | no                                   | yes                                   |
| DueDate           | Due date                                                     | yes                                  | no                                    |
| Status            | Invoice Status. Can be DRAFT, PENDING, INPROBLEM, INPAYMENT, CLOSED | yes                                  | yes                                   |
| Header            | Header                                                       | yes                                  | no                                    |
| InCompta          | Is comptabilized                                             | yes                                  | no                                    |
| GestDocument      | Koban document model guid                                    | yes                                  | no                                    |
| AssignedTo        | User assigned                                                | yes (Fill FullName or External Code) | no                                    |
| MarketingCampaign | UTM Campaign                                                 | yes                                  | no                                    |
| Source            | UTM Source                                                   | yes                                  | no                                    |
| Canal             | UTM Medium                                                   | yes                                  | no                                    |
| PaymentMode       | Payment Mode                                                 | yes (Fill Code)                      | yes (List value Guid, Code and label) |
| GestDocument      | Koban Document model used. Koban Guid                        | yes                                  | yes                                   |
| Order             | Order linked                                                 | yes (Fill Number or External Code)   | yes                                   |
| Third             | Account linked                                               | yes                                  | yes                                   |
| OtherThird        | Account invoiced                                             | yes                                  | no                                    |
| Contact           | Contact linked                                               | no                                   | yes                                   |
| Amount            | Amount without taxes                                         | no                                   | yes                                   |
| AmountTtc         | Amount with taxes                                            | no                                   | yes                                   |
| CurrencyCode      | Currency code                                                | no                                   | yes                                   |
| Origin            | Invoice origin                                               | yes (Fill code)                      | yes (List value Guid, Code and label) |
| Lines             | Delivery line                                                | yes                                  | yes                                   |

### Invoice Line

| Property  | Comment                    | In POST methods      | In GET methods                  |
| --------- | -------------------------- | -------------------- | ------------------------------- |
| Label     | Category Reference         | yes                  | yes                             |
| Extcode   | Line external code         | yes                  | yes                             |
| Comments  | Comments                   | yes                  | yes                             |
| Ht        | Amount without taxes       | yes                  | yes                             |
| Prht      | Buying price without taxes | yes                  | yes                             |
| Product   | Product linked             | yes (Fill Reference) | yes (Guid, Reference and Label) |
| Quantity  | Quantity                   | yes                  | yes                             |
| Red       | Discount without taxes     | yes                  | yes                             |
| Ttc       | Amount with taxes          | yes                  | yes                             |
| Vat       | Taxes rate                 | yes                  | yes                             |
| UnitPrice | Unit price (without taxes) | yes                  | yes                             |