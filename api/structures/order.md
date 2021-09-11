# Structure API Commande

Voici la structure JSON d'une commande via l'API Koban.
Elle est à utiliser pour les mises à jour via l'API et est également retournée par les méthodes de sélection.

**Version Compatible** : Aout 2021 et supérieures

```
{
    	"Dateorder": "2021-02-15", 	// Date Commande
    	"Extcode": "",				// Code Externe Commande
    	"Number": "CM210003",		// Numéro Commande
    	"Status": "PENDING",		// Statut. Peut etre : DRAFT (Brouillon), PENDING (En cours), CLOSED (Terminé), TOVALID, TODELIVER, DELIVERED. Si Status est égal à PENDING ou CLOSED, alors le devis ou l'opportunité liés seront gagnés
    	"Third": { "Extcode": "C1000446" }, // Compte associé (renseigner la clé)
    	"Deal": { "Extcode": "D10004" }, // Opportunité associée (renseigner la clé)
    	"Quote": { "Number": "D10004" }, // Devis associé (renseigner obligatoirement Number. Si le devis est fourni, l'opportunité associée sera celle du devis)
    	"Lines": // Lignes de commande
    	[
    		{
    			"Label": "Line name", // Libellé
    			"Extcode": "line code", // Code externe ligne
    			"Comments": "", // Commentaires
    			"Ht": 10, // Montant HT
    			"PrHt": 8, // Montant Prix de revient HT
    			"Quantity": 1, // Quantité
    			"Product": { "Reference": "A" }, // Référence Produit
    			"Red": 0, // Réduction
    			"Ttc": 12, // Montant TTC
    			"Vat": 20, // Taux de TVA
    			"UnitPrice": 10 // Montant unitaire HT
    		}
    	]
}
```

