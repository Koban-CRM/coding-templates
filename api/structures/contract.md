# API Model Structure - Contract

You can find here JSON structure for a contract in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From October 2021

```
{
    "Label": "Account Label",
    "Third": { "Extcode": "XXXXXXX" },
    "From": "13/03/2020",
    "To": "12/03/2021",
    "PeriodicityCode": "Y",
    "InvoicePeriodicityCode": "M",
    "Lines":[
        {
            "Product": { "Reference": "PR" },
            "Label": "Abonnement",
            "Quantity": 4
        }
    ]
}
```

| Property               | Comment                                                      | In POST methods | In GET methods |
| ---------------------- | ------------------------------------------------------------ | --------------- | -------------- |
| Label                  | Label                                                        | yes             | yes            |
| Third                  | Account linked                                               | yes             | yes            |
| Guid                   | Koban Guid                                                   | no              | yes            |
| From                   | Contract start time                                          | yes             | yes            |
| To                     | Contract end time                                            | yes             | yes            |
| Lines                  | Contract lines                                               | yes             | yes            |
| PeriodicityCode        | Periodicity Code. Can be :<br />- M : Monthly<br />- T : Quarterly<br />- Y : Yearly<br />- 2Y : 2 years<br />- 3Y : 3 years<br />- 4Y : 4 years<br />- 5Y : 5 years | yes             | yes            |
| InvoicePeriodicityCode | Invoicing Periodicity Code. Can be :<br />- M : Monthly<br />- T : Quarterly<br />- Y : Yearly<br />- 2Y : 2 years<br />- 3Y : 3 years<br />- 4Y : 4 years<br />- 5Y : 5 years | yes             | yes            |

### Contract Line

| Property | Comment           | In POST methods                   | In GET methods |
| -------- | ----------------- | --------------------------------- | -------------- |
| Label    | Line label        | yes                               | yes            |
| sId      | Line Koban Guid   | no                                | yes            |
| Product  | Product Reference | yes. Must fill Reference Property | yes            |
| Quantity | Quantity          | yes                               | yes            |