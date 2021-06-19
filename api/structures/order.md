# Structure API Commande

Voici la structure JSON d'une commande via l'API Koban.
Elle est à utiliser pour les mises à jour via l'API et est également retournée par les méthodes de sélection.

**Version Compatible** : Juin 2021 et supérieures

```json
{
    {
    	"Dateorder": "2021-02-15",
    	"eShop": "",
    	"eShopStatus": "",
    	"Extcode": "",
    	"Number": "CM210003",
    	"Status": "PENDING",
    	"Third": { "Extcode": "C1000446" },
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
}
```

