# Modèles d'EMail

Le but de cette section est de vous guider dans la construction d'un template HTML email Koban compatible avec l'éditeur 2019.

## Principe de base

Un modèle d'email Koban est un fichier HTML directement lisible par un navigateur. Il comporte cependant quelques spécificités permettant d'initialiser l'interface de l'éditeur Koban.

Ce modèle est composé de **zones**. Ces zones sont repérés par Koban dans le modèle HTML et transformées en zones sur lesquelles l'utilisateur peut glisser/Déplacer des blocs (image, texte, bouton, groupe d'image...).
On peut également prépositionner des **blocs** dans les zones préalablement créées.

Le modèle d'email sera transmis dans Koban sous la forme d'un fichier zip contenant :

- Un fichier .html à la racine
- Un répertoire img contenant les images associées

## Déclaration initiale du modèle de mail

Le modèle d'email doit comporter au moins 2 balises méta en entête :

- **x-kbn-title** qui permet de donner un nom au modèle

- **x-kbn-description** qui permet de donner une description au modèle

- **x-kbn-category** dans le cas d'un thème, permet de ranger le modèle dans une catégorie

```html
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<meta name="x-kbn-title" content="Restaurant" />
<meta name="x-kbn-category" content="Promotions" />
<meta name="x-kbn-description" content="Annoncez les menus de votre restaurant" />
```

## Zones

Une zone du modèle d'email s'identifie dans le code HTML par un attribut **data-kbnzone** dont la valeur sera le **nom de la zone**. Elle sera présente sous la forme d'un &lt;td&gt;.

```html
<table cellpadding="0" cellspacing="0" id="main" bgcolor="#EEEEEE" border="0" width="600" style="width:600px;padding: 0; margin: 0;background-color:#EEEEEE;">
    <tr>
        <td class="container" id="ct_preheader" data-kbnzone="PreHeader" width="600" style="width:600px">
        </td>
    </tr>
</table>
```

## Blocs

Des blocs peuvent être prépositionnés à l'intérieur d'une zone. Ils sont repérés par Koban dans un modèle email de la manière suivante, en fonction du type de bloc désiré.

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
            <td valign="top" width="280" style="font-size:12px">
                <h2>Lorem Ipsum</h2>
                <p>
                	Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
				</p>
            </td>
            <td valign="top" width="20"></td>
            <td valign="top" width="280" style="font-size:12px">
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
<img data-kbnblock="image" src="img/logo.png" style="display:block" border="0" />
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

#### Définition

Un bloc Groupe d'image est de type &lt;table&gt; et doit se positionner sous le &lt;td&gt; de la zone et comporter un attribut **data-kbnblock="imagegroup"**.

```html
<table data-kbnblock="imagegroup" width="100%">
	<tr>
		<td><img src="img/logo.png" width="300px" /></td>
		<td><img src="img/logo.png" width="300px" /></td>
	</tr>
</table>
```

#### Style

- **width**: Au niveau de l'image, permet de définir la largeur par défaut de l'image.

### Image et texte

#### Définition

Un bloc Image est de type &lt;div&gt; et doit se positionner sous le &lt;td&gt; de la zone et comporter un attribut **data-kbnblock="textimg"**.

```html
<div data-kbnblock="textimg">
	<table>
		<tr>
			<td valign="top" width="290">
				<h2>Lorem Ipsum</h2>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
			</td>
			<td width="20"></td>
			<td width="290">
				<img src="http://cdn.kbn.onl/default/logo.png" />
			</td>
		</tr>
	</table>
</div>
```

#### Style

Au niveau de la balise td du texte :

- **color** : Couleur du texte

### Réseaux sociaux

#### Définition

Un bloc Réseaux sociaux est de type &lt;table&gt; et doit se positionner sous le &lt;td&gt; de la zone et comporter un attribut **data-kbnblock="social"**.

```html
<table data-kbnblock="social" width="100%" data-iconsize="big" data-iconshape="circle" data-iconstyle="color" data-alignment="horizontal">
	<tr>
		<td align="center">
			<table cellpadding="0" cellspacing="0">
				<tr>
					<td data-media="facebook"><img src="https://cdn.kbn.onl/default/social/big/color/circle/facebook.png" /></td>
					<td data-media="twitter"><img src="https://cdn.kbn.onl/default/social/big/color/circle/twitter.png" /></td>
					<td data-media="snapchat"><img src="https://cdn.kbn.onl/default/social/big/color/circle/snapchat.png" /></td>
				</tr>
			</table>
		</td>
	</tr>
</table>
```

#### Options

- **Taille d'icone** : Positionner au niveau de &lt;table&gt; l'attribut **data-iconsize** avec les valeurs possibles : big, small
- **Forme d'icone** : Positionner au niveau de &lt;table&gt; l'attribut **data-iconshape** avec les valeurs possibles : rounded, circle, square, outlined
- **Style d'icone** : Positionner au niveau de &lt;table&gt; l'attribut **data-iconstyle** avec les valeurs possibles : white, color, black, grey
- **Alignement** : Positionner au niveau de &lt;table&gt; l'attribut **data-alignement** avec les valeurs possibles : horizontal, vertical

#### Réseaux sociaux disponibles

Les réseaux sociaux possibles sont à positionner au niveau du noeud td dans l'attribut **data-media**. Les valeurs possibles sont : facebook, twitter, linkedin, youtube, pinterest, tumblr, instagram, snapchat, rss, email, website.

Nota : Les URL des images des réseaux sociaux ne sont pas interprétés par Koban mais peuvent permettre de disposer d'un rendu correct en HTML pur.

La construction de l'URL se fait de la manière suivante :

https://cdn.kbn.onl/default/social/[SIZE]/[STYLE]/[SHAPE]/[SOCIAL].png

## Exemples

Dans le repository git, vous trouverez sous le répertoire email-templates un ensemble de modèles de base pour vous aider à démarrer.