# API Model Structure - Product

You can find here JSON structure for a product in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
{
    "Reference": "Reference",
    "OtherCode": "",
    "Comments": "Product comments",
    "eShopURL": "https://my.shop/ProductPage",
    "Label": "Category Label",
    "Ht": 10,
    "Margin": 2,
    "PrHt": 8,
    "Vat": 20,
    "Ttc": 12,
    "IsSelling": true,
    "IsManufactured": true,
    "VatUpdatable": true,
    "Model": "Model",
    "Brand": "Brand",
    "Packing": "Pack",
    "StockMin": 15,
    "PCB": 10,
    "Catproduct": { "Reference": "Parent Reference"},
    "Regroup": "Regroupment code",
    "Classification": "Classification code",
    "Unit": "Unit code",
    "Obsolete": false,
    "MoreFields": [
        {
            "FieldId": "Koban Field Guid",
            "Value": ""
        }
    ],
    "Declinaisons":[
    	{
    		"Label": "Size",
    		"Values":
    			[
    				{ "Label": "XL", "BarCode": "XXXXXXX" },
    				{ "Label": "M", "BarCode": "XXXXXXX" }
    			]
    	}
	]
}
```

| Property       | Comment                              | In POST methods | In GET methods                   |
| -------------- | ------------------------------------ | --------------- | -------------------------------- |
| Reference      | Product Reference                    | yes             | yes                              |
| OtherCode      | Product Other code                   | yes             | no                               |
| Label          | Product Label                        | yes             | yes                              |
| Guid           | Koban Guid                           | no              | yes                              |
| Comments       | Comments                             | yes             | yes                              |
| eShopURL       | eShop Product Page URL               | yes             | yes                              |
| Ht             | Amount without taxes                 | yes             | yes                              |
| Margin         | Margin without taxes                 | yes             | yes                              |
| PrHt           | Buying price without taxes           | yes             | yes                              |
| Vat            | Taxes %                              | yes             | yes                              |
| Ttc            | Amount with taxes                    | yes             | yes                              |
| IsSelling      | Define if product can be sold        | yes             | yes                              |
| IsManufactured | Define if product is deliverable     | yes             | yes                              |
| VatUpdatable   | Define if tax is updatable           | yes             | yes                              |
| Model          | Model                                | yes             | yes                              |
| Brand          | Brand                                | yes             | yes                              |
| Packing        | Packing                              | yes (Code)      | yes (Koban Guid)                 |
| StockMin       | Minimum stock                        | yes             | yes                              |
| PCB            | PCB                                  | no              | yes                              |
| Catproduct     | Product category                     | yes (Reference) | yes (Label, Guid and reference)  |
| Regroup        | Regroupment                          | yes (Code)      | yes (Label)                      |
| Classification | Classification                       | yes (Code)      | yes (Label)                      |
| Unit           | Unit                                 | yes (Code)      | yes (Code)                       |
| Obsolete       | Define if product is obsolete or not | yes             | yes                              |
| MoreFields     | Specific fields array                | yes             | yes (Koban Field guid and Value) |
| Declinaisons   | Product Declinaisons                 | yes             | yes                              |
| DCreated       | Creation Date (timestamp)            | yes             | yes                              |
| DUpdated       | Last update date (timestamp)         | no              | yes                              |
| IsProviding    | Define if product can be bought      | yes             | yes                              |
| BarCode        | Bar code                             | yes             | yes                              |
| ImageUrl       | Product image absolute URL           | yes             | yes                              |

# API Price structure

You can find here JSON structure for a product price in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
{
    "Product": { "Reference": "Product Reference"},
    "AccountType": { "Guid": "xxxxxxx"},
    "Third": { "Extcode": "XXXXX"},
    "Ht": 10,
    "Margin": 2,
    "PrHt": 8,
    "VatRate": 20,
    "Ttc": 12
}
```

| Property    | Comment                    | In POST methods             | In GET methods   |
| ----------- | -------------------------- | --------------------------- | ---------------- |
| Product     | Product                    | yes                         | yes              |
| AccountType | Account Type               | yes (Guid)                  | no               |
| Third       | Account                    | yes (External code or Guid) | yes (Koban Guid) |
| Ht          | Amount without taxes       | yes                         | yes              |
| Margin      | Margin without taxes       | yes                         | yes              |
| PrHt        | Buying price without taxes | yes                         | yes              |
| VatRate     | Taxes %                    | yes                         | yes              |
| Ttc         | Amount with taxes          | yes                         | yes              |

# API Product Provider structure

You can find here JSON structure for a product provider link in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From November 2021

```
{
    "Product": { "Reference": "Product Reference"},
    "Third": { "Extcode": "XXXXX"},
    "Ht": 10,
    "VatRate": 20,
    "Ttc": 12,
    "ProviderCode": "ABC",
    "MinQuantityToOrder": 5
}
```

| Property           | Comment                   | In POST methods             | In GET methods   |
| ------------------ | ------------------------- | --------------------------- | ---------------- |
| Product            | Product                   | yes (Reference)             | yes              |
| Third              | Provider Account          | yes (External code or Guid) | yes (Koban Guid) |
| ProviderCode       | Provider Code             | yes                         | yes              |
| MinQuantityToOrder | Minimum quantity to order | yes                         | yes              |
| Ht                 | Amount without taxes      | yes                         | yes              |
| VatRate            | Taxes %                   | yes                         | yes              |
| Ttc                | Amount with taxes         | yes                         | yes              |
| RemRate            | Reduction rate %          | yes                         | yes              |

