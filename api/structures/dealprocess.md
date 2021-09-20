# API Model Structure - Deal Process

You can find here JSON structure for a deal process in the Koban API.

It is to be used for updates via the API and is also returned by the selection methods.

**Versions** : From August 2021

```
[
   {
      "Label":"Deal Title",
      "Extcode":44,
      "Steps": [
          {
              "Label": "Step Label",
              "Extcode": "Step Code"
          },
          {
              "Label": "Step Label 2",
              "Extcode": "Step Code 2"
          }
      ],
      "MoreFields":[
          { 
              "FieldId": "XXXXXXXX",
              "Value": "Value"
          }
      ],
      "Rights":[
      	  {
      		  "ExternalCode": "Step Code",
      		  "Group": "User Group Code",
      		  "Allowed": true,
      		  "RightType": "ALL"
      	  }
      ]
   }
]
```

| Property      | Comment                                                      | In POST methods | In GET methods |
| ------------- | ------------------------------------------------------------ | --------------- | -------------- |
| Label         | Label                                                        | yes             | yes            |
| Extcode       | External Code                                                | yes             | yes            |
| Regroup       | Regroupment code                                             | yes             | yes            |
| Guid          | Koban Guid                                                   | no              | yes            |
| IsActive      | Define is process is active                                  | yes             | yes            |
| IsActiveDeals | Define if deals are active in this process                   | yes             | yes            |
| Vat           | Vat Rate                                                     | yes             | no             |
| Steps         | Steps. List of (Label - Code values)                         | yes             | yes            |
| Rights        | Rights for user groups and specific steps (by default empty).<br />Values are composed of : External Code (Step Code), Group (User group code), allowed (if step is allowed to group), RightType (Right type, can be ALL, USER, STR) | yes             | no             |
| MoreFields    | Specific fields                                              | yes             | no             |
