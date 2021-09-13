# API Model Structure - Delivery

You can find here JSON structure for a delivery in the Koban API.

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

| Property        | Comment                                | In POST methods | In GET methods               |
| --------------- | -------------------------------------- | --------------- | ---------------------------- |
| DeliveryDate    | Delivery Date                          | yes             | yes                          |
| Extcode         | External Code                          | yes             | yes                          |
| Number          | Number                                 | yes             | yes                          |
| Guid            | Koban Guid                             | no              | yes                          |
| Status          | Delivery Status. Can be DRAFT, PENDING | yes             | yes                          |
| DeliveryAddress | Delivery Address                       | yes             | yes                          |
| GestDocument    | Koban Document model used. Koban Guid  | yes             | yes                          |
| Order           | Order linked                           | yes             | yes (External Code and Guid) |
| Third           | Account linked                         | yes             | yes (External code and Guid) |
| DepositGuid     | Deposit Koban Guid                     | no              | yes                          |
| Lines           | Delivery line                          | yes             | yes                          |

### Delivery Line

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