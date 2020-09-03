# Rendre compatible un HTML email brut

Vous disposez d'un template HTML email brut. Vous trouverez ci-dessous les différentes étapes pour le rendre compatible avec Koban.

Vous avez la possibilité d'importer un template HTML brut dans Koban sous forme d'un fichier zip. A la racine du fichier zip doit se trouver votre template au format **.html**.

### Images

Les images doivent être présentes dans un répertoire **img** au niveau du fichier zip. Les URL des images dans le code HTML doivent pointer vers ce répertoire en relatif.

### Liens

#### Afficher en ligne

Le shortcode à figurer est **[[!ShowInLine]]**.

*<u>Exemple :</u>*

```
<a href='[[!ShowInLine]]'>Afficher dans un navigateur</a>
```

#### Désinscription

Le shortcode à figurer est **[[!Unsubscribe]]**.

*<u>Exemple :</u>*

```
<a href='[[!Unsubscribe]]'>Se désinscrire</a>
```

#### Préférences

Le shortcode à figurer est **[[!Preferences]]**.

*<u>Exemple :</u>*

```
<a href='[[!Preferences]]'>Préférences de réception</a>
```

