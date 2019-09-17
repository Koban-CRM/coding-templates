# Modèles d'EMail



## Blocs

### Texte

#### Définition

Un bloc Texte est de type <div> et doit se positionner sous le <td> de la zone et comporter un attribut **data-kbnzone="text"**.

```html
<div data-kbnblock="text" style="font-size:12px">
    <h2>Lorem Ipsum</h2>
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
</div>
```

#### Style

Les styles pouvant être définis au niveau du bloc texte (directement au niveau du <div>) sont les suivants :

- **font-size** : Taille du texte (valeurs possibles : 8px, 9px, 10px, 11px, 12px, 14px, 16px, 18px, 20px, 22px, 24px, 30px, 36px, 40px)
- **text-align** : Alignement (valeurs possibles : justify, center, left, right)
- **color** : Couleur de la police
- **line-height** : Hauteur de ligne, exprimée en px ou en %

#### Texte deux colonnes

Il est possible de positionner un texte sous 2 colonnes via le code suivant :

```html
<div data-kbnblock="text">
    <table>
        <tr>
            <td width="280" style="font-size:12px">
                <h2>Lorem Ipsum</h2>
                <p>
                	Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
				</p>
            </td>
            <td width="280" style="font-size:12px">
            	<h2>Lorem Ipsum</h2>
                <p>
                	Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
				</p>
            </td>
        </tr>
    </table>
   
</div>
```

### Image

#### Définition

Un bloc Image est de type &lt;img&gt; et doit se positionner sous le &lt;td&gt; de la zone et comporter un attribut **data-kbnzone="image"**.

```html
<img data-kbnblock="image" src="/Content/img/cdn/logo.png" style="display:block" border="0" />
```

#### Style

Les styles suivants sont repérés par Koban et doivent être placés directement au niveau de la balise **img** :

- **margin** : Positionner margin:auto pour avoir une image centrée
- **padding** : Pour disposer d'un espacement, définissez un style padding en px qui sera repéré par Koban.

### Bouton

### Divider



### Groupe d'image

### Image et texte

### Réseaux sociaux