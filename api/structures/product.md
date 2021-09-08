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
| IsManufactured | Define if product is manufactured    | yes             | yes                              |
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