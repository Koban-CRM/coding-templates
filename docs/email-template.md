# Modèles d'EMail



## Blocs

### Texte

#### Définition

Un bloc Texte est de type &lt;div&gt; et doit se positionner sous le &lt;td&gt; de la zone et comporter un attribut **data-kbnblock="text"**.

```html
<div data-kbnblock="text" style="font-size:12px">
    <h2>Lorem Ipsum</h2>
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    </p>
</div>
```

#### Style

Les styles pouvant être définis au niveau du bloc texte (directement au niveau du &lt;div&gt;) sont les suivants :

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

Un bloc Image est de type &lt;img&gt; et doit se positionner sous le &lt;td&gt; de la zone et comporter un attribut **data-kbnblock="image"**.

```html
<img data-kbnblock="image" src="/Content/img/cdn/logo.png" style="display:block" border="0" />
```

#### Style

Les styles suivants sont repérés par Koban et doivent être placés directement au niveau de la balise **img** :

- **margin** : Positionner margin:auto pour avoir une image centrée
- **padding** : Pour disposer d'un espacement, définissez un style padding en px qui sera repéré par Koban.

### Bouton

#### Définition

Un bloc bouton est de type **table** et doit se positionner sous le &lt;**td**&gt; de la zone et comporter un attribut **data-kbnblock="button"**.

```html
<table data-kbnblock="button" width="100%" cellspacing='0' cellpadding='0'>
    <tr>
        <td align="center">
            <table cellspacing='0' cellpadding='0'>
                <tr>
                    <td class='button' bgcolor='#000099'>
                        <a class='link' href='#' title='Mettre à jour' target='_blank' style='padding:8px 12px;font-family:Helvetica, Arial, sans-serif;font-size:16px;color:#FFFFFF;text-decoration:none;display:inline-block'>
                            Mettre à jour
                        </a>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
</table>
```

#### Options

Au niveau de la balise &lt;a&gt;, les attributs suivants sont repérés :

- **title** : Le titre du lien
- **href** : Le lien du bouton

#### Style

Au niveau de la balise &lt;**a**&gt;:

- **font-family** : La police du bouton (valeurs possibles : Arial, Courier New, Georgia, Helvetica, Tahoma, Times New Roman, Trebuchet MS, Verdana)
- **font-size** : La taille du texte du bouton (valeurs possibles : 8px, 9px, 10px, 11px, 12px, 14px, 16px, 18px, 20px, 22px, 24px, 30px, 36px, 40px)
- **color** : La couleur du texte du bouton
- **border-radius** : L'arrondi du bouton (en px)

Au niveau de la balise &lt;**td**&gt;:

- attribut **align** : L'alignement dans la zone (valeurs possibles : left, center, right)
- attribut **bgcolor** : La couleur de fond du bouton

### Divider

#### Définition

Un bloc Divider est de type &lt;div&gt; et doit se positionner sous le &lt;td&gt; de la zone et comporter un attribut **data-kbnblock="divider"**.

```html
<div data-kbnblock="divider" style="height:20px"></div> 
```

#### Style

Le style suivant est repéré au niveau de la balise &lt;div&gt;:

- **height** : La hauteur en px du séparateur

### Groupe d'image

### Image et texte

### Réseaux sociaux