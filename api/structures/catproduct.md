# API Model Structure - Product category

You can find here JSON structure for a product category in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
{
    "Reference": "Code 5",
    "eShopURL": "https://my.shop/CategoryPage",
    "Label": "Category Label",
    "ParentCategory": { "Reference": "Parent Reference"},
    "Obsolete": false 
}
```

| Property       | Comment                               | In POST methods                     | In GET methods |
| -------------- | ------------------------------------- | ----------------------------------- | -------------- |
| Reference      | Category Reference                    | yes                                 | yes            |
| eShopURL       | eShop category page URL               | yes                                 | no             |
| Label          | Category Label                        | yes                                 | yes            |
| Guid           | Koban Guid                            | no                                  | yes            |
| Obsolete       | Define if category is obsolete or not | yes                                 | yes            |
| ParentCategory | Parent Category                       | yes. You must fill Parent reference | yes            |