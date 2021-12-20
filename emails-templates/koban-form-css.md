# Formulaires Koban sur un site internet : Personnalisation CSS

Les formulaires Koban, une fois intégrés via une copie du code HTML peuvent être personnalisés pour "coller" au design du site internet sur lequel ils sont présents.

L'utilisateur pourra directement fournir son CSS personnalisé pour chaque formulaire. Koban se charge ensuite de charger ce CSS directement depuis le site internet sur lequel le formulaire est publié.

## Structure des classes de formulaire

### Structure de base HTML

Chaque formulaire dispose de différentes zones :

- Les champs en eux-même
- La case à cocher Optin
- Le bouton de soumission
- Le texte "RGPD" précisant comment les données sont traitées

Chaque champ est inclu dans un groupe.

Au sein de ce groupe, deux noeuds sont présents :

- Le libellé du champ
- Le champ en lui-même

```html
<div class='ncFieldct cti5693b0580dc3631238633ee2 tp'>
    <label>EMail</label>
    <div class='ncField'>
        <input data-fid='5693b0580dc3631238633ee2' type='email' pattern='[^ @]*@[^ @]*' name='contact_email' required></input>
	</div>
</div>
```

### Classes Koban

#### Descriptif

Un formulaire Koban dispose toujours de l'identifiant **ncform**.

Chaque groupe dispose toujours de la classe CSS **ncFieldct**. Une classe générée automatiquement correspondant à l'identifiant du champ dans le formulaire précédé de **cti** est également présente.

Il est conseillé d'éviter de personnaliser le CSS via ces classes **cti** afin de permettre une réutilisabilité de votre code CSS sur d'autres formulaires Koban.

Le libellé est présenté sous l'entité **label**.

Le champ en lui-même est embarqué dans un **div** dont la classe est **ncField**.

#### Sélecteurs CSS correspondant

| Zone du formulaire | Sélecteur CSS    |
| ------------------ | ---------------- |
| Groupe Champ       | .ncFieldct       |
| Libellé du champ   | .ncFieldct label |
| Champ input        | .ncFieldct input |

### Types de champ

Les types de champ HTML sont :

- **input** : Pour les zones email, téléphone, texte, numérique
- **select** : Pour les listes déroulantes (champs personnalisés, origine, tags)
- **textarea** : Zone de commentaire
- **input type='checkbox'** : Pour les cases à cocher. Ces champs ont au niveau de leur groupe une classe spéciale **.tpboolean** permettant de personnaliser le libellé plus facilement.

### Zone Optin

Le bouton Optin est un champ classique de type checkbox et encapsulé dans un groupe **ncFieldct**. Au niveau de l'input, un attribut **data-fid="optin"** est présent.

### Le Bouton de soumission

Le bouton de soumission est une entité lien (**a**) et est encapsulée dans un div dont la classe est **ncSendZone**. 
Du style inline par défaut est souvent présent sur le code HTML fourni par Koban, si vous souhaitez le surcharger, n'oubliez pas de préciser !important pour chaque commande CSS.

### Texte RGPD

Le texte est encapsulé dans un div dont la classe est **ncFinality**.

## Fourniture du style via Koban

Une fois votre style CSS développé, vous pouvez le coller directement au niveau de Koban pour qu'il soit chargé en même temps que le formulaire.

Pour cela, ouvrez votre formulaire dans Koban et cliquez sur **Style**.

Collez ensuite votre code CSS et cliquer sur **Enregistrer**.