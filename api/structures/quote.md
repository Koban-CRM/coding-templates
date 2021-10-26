# API Model Structure - Quote

You can find here JSON structure for a delivery in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From October 2021

```
[
   {
    	"Datesent": "2021-02-15",
        "Label": "Quote title",
    	"Extcode": "",
    	"Number": "CM210003",
    	"Status": "PENDING",
    	"Deal": { "Extcode": "C1000446" },
    	"Sections":
    	[
            {
                "Label": "Section Label",
                "Lines":
                [
                    {
                        "Label": "Line name",
                        "Extcode": "line code",
                        "Comments":"",
                        "Ht": 10,
                        "PrHt": 8,
                        "Quantity": 1,
                        "Product": { "Reference": "A" },
                        "Red": 0,
                        "Ttc": 12,
                        "Vat": 20,
                        "UnitPrice": 10
                    }
                ]
            }
    	]
    }
]
```

| Property          | Comment                                       | In POST methods | In GET methods                              |
| ----------------- | --------------------------------------------- | --------------- | ------------------------------------------- |
| DateSent          | Quote date                                    | yes             | yes                                         |
| Extcode           | External Code                                 | yes             | yes                                         |
| Number            | Number                                        | yes             | yes                                         |
| Guid              | Koban Guid                                    | no              | yes                                         |
| Status            | Delivery Status. Can be DRAFT, SENT           | yes             | yes                                         |
| IsWon             | Define if quote is won (equivalent to result) | no              | yes                                         |
| Result            | Result Code (WON, LOST or SLEEP)              | no              | yes                                         |
| ResultDate        | Result Date                                   | no              | yes                                         |
| AssignedTo        | Assigned to User                              | no              | yes (Guid only)                             |
| Label             | Quote label                                   | yes             | yes                                         |
| Header            | Quote header                                  | no              | yes                                         |
| Deal              | Deal linked                                   | yes             | yes (External Code and Guid)                |
| Third             | Third linked                                  | no              | yes (Label, Guid, Extcode)                  |
| AccountToInvoice  | Account to invoice                            | no              | yes (Label, Guid, Extcode)                  |
| Contact           | Contact linked                                | no              | yes (Guid, External code, name, first name) |
| CustomerReference | Customer reference                            | no              | yes                                         |
| DeliveryAddress   | Delivery address                              | no              | yes                                         |
| WorkBegin         | Work begin date                               | no              | yes                                         |
| Sections          | Quote sections                                | yes             | yes                                         |

### Quote Section

| Property | Comment          | In POST methods | In GET methods |
| -------- | ---------------- | --------------- | -------------- |
| Label    | Section label    | yes             | yes            |
| Comments | Section Comments | yes             | yes            |
| Lines    | Quote lines      | yes             | yes            |

### Quote Line

| Property        | Comment                    | In POST methods                                          | In GET methods                           |
| --------------- | -------------------------- | -------------------------------------------------------- | ---------------------------------------- |
| Label           | Category Reference         | yes. If not filled, then will be filled by Product Label | yes                                      |
| Guid            | Line Guid                  | no                                                       | yes                                      |
| Extcode         | Line external code         | yes                                                      | yes                                      |
| Comments        | Comments                   | yes                                                      | yes                                      |
| Ht              | Amount without taxes       | yes                                                      | yes                                      |
| Prht            | Buying price without taxes | yes                                                      | yes                                      |
| Product         | Product linked             | yes (Fill Reference)                                     | yes (Guid, Reference, Regroup and Label) |
| Quantity        | Quantity                   | yes                                                      | yes                                      |
| Red             | Discount without taxes     | yes                                                      | yes                                      |
| Ttc             | Amount with taxes          | yes                                                      | yes                                      |
| Vat             | Taxes rate                 | yes                                                      | no                                       |
| TaxAccountId    | Koban tax account Guid     | no                                                       | yes                                      |
| UnitPrice       | Unit price (without taxes) | yes                                                      | yes                                      |
| Notes           | Line notes                 | yes                                                      | yes                                      |
| Margin          | Margin HT                  | yes                                                      | yes                                      |
| DeclinaisonCode | Declinaison code           | yes                                                      | yes                                      |