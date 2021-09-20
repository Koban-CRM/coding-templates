# API Model Structure - Deal

You can find here JSON structure for a deal in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
[
   {
      "Label":"Deal Title",
      "Extcode":44,
      "Process":{
         "Code":6
      },
      "Status":{
         "Code":"QUOTESENT"
      },
      "Third": {
          "Extcode": "1555"
      },
      "Amountprev":131000.0,
      "Tags":[
         {
            "TagCategoryCode":"TAGCATEGORY",
            "Label":"Tag Label"
         }
      ],
      "Result":null
   }
]
```

| Property     | Comment                                             | In POST methods                  | In GET methods               |
| ------------ | --------------------------------------------------- | -------------------------------- | ---------------------------- |
| Label        | Label                                               | yes                              | yes                          |
| Extcode      | External Code                                       | yes                              | yes                          |
| Guid         | Koban Guid                                          | no                               | yes                          |
| Process      | Deal Process                                        | yes (Fill Code or Guid)          | yes                          |
| Status       | Deal step                                           | yes (Fill Code or Guid)          | yes                          |
| Third        | Account linked                                      | yes                              | yes                          |
| Amountprev   | Deal Amount                                         | yes                              | yes                          |
| Tags         | Tags                                                | yes                              | yes                          |
| Result       | Deal Result. Can be WON, LOST or SLEEP              | yes                              | yes                          |
| MoreFields   | Specific fields                                     | yes                              | yes                          |
| Description  | Description                                         | yes                              | yes                          |
| Comments     | Comments                                            | no                               | yes                          |
| AssignedTo   | User assigned to                                    | yes (Fill Extcode or Guid)       | yes                          |
| Origin       | Origin                                              | yes (Fill Code)                  | no                           |
| Vat          | Vat Rate                                            | yes                              | no                           |
| ProcessLabel | Deal Process label                                  | no                               | yes                          |
| Contact      | Contact linked                                      | yes (Fill Extcode, name or Guid) | yes (Returns Guid and Label) |
| Products     | Products linked                                     | no                               | yes                          |
| DPrev        | Prevision result date                               | yes                              | yes                          |
| DResult      | Result date                                         | yes                              | yes                          |
| Type         | Deal type (null or SECONDARY). Used for immo plugin | yes                              | no                           |
| Link         | Deal linked guid if type is secondary               | yes                              | no                           |
