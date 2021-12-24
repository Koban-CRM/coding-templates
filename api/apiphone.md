# Koban Phone - Cas d'utilisation

Vous trouverez sur cette page des exemples d'intégration à une plateforme téléphonique, lorsque celle-ci n'est pas disponible en standard via une extension.
Le principe est un appel d'une URL depuis la plateforme téléphonique en cas d'appel.

## Préalable

Vous devez demander au support Koban l'activation de cette fonctionnalité sur votre compte.

## Click To Call

Tous les numéros de téléphones affichés dans Koban sont des liens de type **tel:**.

Votre plateforme doit être en mesure de les interpréter pour lancer l'appel.

## Remontée de Fiche et Création d'action

### Appel entrant

Sur un appel entrant, vous devez appeler cette URL :

**[KOBANSERVER]/Contact/OpenPhone?showaction=[ACTION]&notes=[NOTE]&phone=[PHONE].**

Les paramètres sont les suivants:

**KOBANSERVER** : URL de votre serveur Koban

**ACTION** : true pour afficher le popin de création d'action, false sinon 

**NOTE** : Commentaire affiché dans le popin

**PHONE** : Numéro de téléphone appelant au format **+(PAYS)(NUMERO)**. Ex. : +33145247000

### Suite d'un appel sortant

Sur un appel sortant, on peut également appeler cette URL ci-dessus pour afficher la fenetre de création d'action.