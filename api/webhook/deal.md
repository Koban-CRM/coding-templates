# WebHook Opportunité

Voici la structure JSON renvoyée par le WebHook Koban Opportunité à l'URL entrée en paramètre

**Version Compatible** : Juin 2021 et supérieures

```
[
  {
    "MoreFields": [], // Champs personnalisés Opportunité
    "Tags": null, // Tags Opportunité
    "Amount": { // Montant Opportunité
      "Currency": { // Devise
        "Symbol": "€",
        "Label": "Euro",
        "Code": "EUR"
      },
      "cent": 155000, // Montant en centimes
    },
    "Description": null, // Description
    "Probability": 5, // Probabilité
    "oDealProcessStep": { // Etape
      "Label": "A qualifier",
      "sId": "60cd9f910dc36124f4d11bbc"
    },
    "oAssignedToIdUser": { // Affectation
      "FullName": "Philippe DURAND",
      "ExternalCode": null,
      "sId": "60cd9f910dc36124f4d11b9b",
    },
    "ResultDate": "/Date(-62135596800000)/",
    "ResultCode": null, // Résultat (null : En cours, WON : Gagné, LOST : Perdu, SLEEP : En sommeil)
    "oContact": null,
    "oThird": { // Compte associé
      "GridLabel": "Colas Rail - Egypt",
      "sId": "60cda2590dc36124f4d11cbe",
      "Label": "Colas Rail - Egypt"
    },
    "oDealProcess": { // Processus associé
      "Label": "Mon processus",
      "ExternalCode": null,
      "OtherCode": null,
      "sId": "60cd9f910dc36124f4d11bc0"
    },
    "ExternalCode": null, // Code externe Opportunité
    "OtherCode": null, // Autre code Opportunité
    "sId": "60cda5b00dc36124f4d11d50", // Identifiant unique
    "Label": "TEST OPP" // Nom Opportunité
  }
]
```

