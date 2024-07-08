# **Cours HTML CSS**
Les notions suivantes m'ont permies de résoudre les différents exercices en HTML et CSS
## **1.CSS ET L'HERITAGE** 
En CSS, si vous appliquez un style à une balise, toutes les balises qui se trouvent à l'intérieur prendront le même style.

--------
## **2.APPLIQUER UNE IMAGE DE FOND**
La propriété permettant d'indiquer une image de fond est background-image. Comme valeur, on doit renseigner url("nom_de_image.png").

```css
body
{
background-image: url("nom_de_image.png");
}```

Il existe des options disponible pour le fond telles que:
### 2.1. background-attachment
* ***fixed***: l'image de fond reste fixe.
 
```css
 body
 {
 background-image: url("nom_de_image.png");
  background-attachment: fixed; 
 }
 `
* ***scroll***: l'image de fond défile avec le texte (par défaut).
 
` body
 {
 background-image: url("nom_de_image.png");
  background-attachment: scroll; 
 }
 `
### 2.2. background-repeat : répétition du fond
* ***no-repeat***: le fond ne sera pas répété. L'image sera donc unique sur la page.
* ***repeat-x***: le fond sera répété uniquement sur la première ligne, horizontalement.
* ***repeat-y***: le fond sera répété uniquement sur la première colonne, verticalement.
* ***repeat***: le fond sera répété en mosaïque (par défaut).
 
***Exemple d'utilisation***
  
` body
{
background-image: url("nom_de_image.png");
background-repeat: no-repeat;
}`

### 2.3. background-position : position du fond
* ***top***: en haut 
* ***bottom***: en bas 
* ***left***: à gauche
* ***center***: centré
* ***right***: à droite.
 
***Exemple d'utilisation***
  
Il est possible de combiner ces mots. Par exemple, pour aligner une image en haut à droite, vous taperez :

` background-position: top right;`
## 3.LA TRANSPARENCE:OPACITY
Elle se fait avec la  propriété opacity.
1. ***Avec une valeur de 1***, l'élément sera totalement opaque : c'est le comportement par défaut.
2. ***Avec une valeur de 0***, l'élément sera totalement transparent.

 ***Exemple d'utilisation***

`p{opacity: 0.6; }`

------   
## 4.  Les bordures et les ombres
Les différents types de bordures:
* solid
* dotted
* dashed
* double
* groove
* ridge
* inset
* outset
 
 Ainsi, pour avoir une bordure bleue, en tirets, épaisse de 3 pixels autour de mes titres, je vais écrire :

 `h1
{
 border: 3px blue dashed;
}
`
### 4.1 bordures arroundies
 La propriété border-radius va nous permettre d'arrondir facilement les angles de n'importe quel élément. Il suffit d'indiquer
 la taille (« l'importance ») de l'arrondi en pixels.
 
`p
{
border-radius: 10px;
}
`
    
## 5.CREATION D'APPARENCES DYNAMIQUES
* ***Au survol***  : avec la propriété hover. hover signifie « survoler ». a:hover peut donc se traduire par : « Quand la souris est sur le lien ».
 
`a:hover
{
}
`

* ***Active***: Quand le visiteur clique sur le lien.
 On peut par exemple changer la couleur de fond du lien lorsque l'on clique dessus :

`a:active
{
 background-color: #FFCC66;
}
`
* ***visited***: Quand le visiteur a déjà vu la page.concernée. Vous pouvez changer cette apparence avec :visited (qui signifie « visité »). En pratique, sur les liens consultés, on ne peut
 pas changer beaucoup de choses à part la couleur.
`a:visited
  {
  color: #AAA;
  }`

----
## 6.TRANSFORMATION DES ELEMENTS AVEC DISPLAY
* ***display : block;*** les liens vont se positionner les uns en-dessous des autres (comme des blocs normaux) et il devient possible de  modifier leurs dimensions !
 
```css
a
 {
 display: block;
 }```
* ***display : inline;*** Eléments d'une ligne. Se placent les uns à côté des autres.
 
```css
nav, section
 {
 display: inline;
 }
 ```
* ***display : inline-block;*** Eléments positionnés les uns à côté des autres  mais qui peuvent être redimensionnés.

`nav
 {
 display: inline-block;
 width: 150px;
 border: 1px solid black;
 vertical-align: top;
 }
 `
* ***display : none;*** Eléments non affichés.
 
  `nav
{
 display: inline-block;
}
----
## 7.LES POSITIONNEMENTS absolu, fixe, relatif 
### 7.1 Le positionnement absolu
il nous permet de placer un élément n'importe où sur la page (en haut à gauche, en bas à droite, tout au centre, etc.).
***Exemple d'utilisation***
`element
{
 position: absolute;
}`
### 7.2  Le positionnement fixe
Identique au positionnement absolu mais, cette fois, l'élément reste toujours visible, même si on
descend plus bas dans la page.

***Exemple d'utilisation***

`element
{
 position: fixed;
}`
### 7.3  Le positionnement relatif 
Permet de décaler l'élément par rapport à sa position normale.
***Exemple d'utilisation***

` element
{
position: relatif;
}
`

## 8.SUPPERPOSITION DES ELEMENTS AVEC z-index
Les éléments positionnés en absolu sont placés par-dessus le reste des éléments de la page ! Par ailleurs, si vous placez deux
éléments en absolu vers le même endroit, ils risquent de se chevaucher. Dans ce cas, utilisez la propriété z-index pour indiquer quel élément doit apparaître au-dessus des autres.
***Exemple d'utilisation***

`element
 {
 position: absolute;
 right: 0px;
 bottom: 0px;
 z-index: 1;
  }
  element2
  {
  position: absolute;
  right: 30px;
  bottom: 30px;
  z-index: 2;
  }`
    
----
## 9.LES TABLES
* ***Colspan***: pour fusionner les cellules d'une table
 
***Exemple:***
`<td colspan="2">`
Cette cellule est la fusion de deux cellules . 
* ***rowspan***: pour fusionner les lignes d'une table .
 
***Exemple:***
`<td rowspan"2">`

Cette cellule est la fusion de deux lignes . 

 ## 10.LES FORMULAIRES
* les champs texte
 
`<input type="text" />`
* les champs de type checkbox
 
` <input type="checkbox" />`
* les champs de type radio
 
`<input type='radio'/>`
* la balise select pour une liste d'options
```html
<select name="pays">
<option value="france">France</option>
<option value="espagne">Espagne</option>
<option value="italie">Italie</option>
<option value="royaume-uni">Royaume-Uni</option>
<option value="canada">Canada</option>
<option value="etats-unis">États-Unis</option>
<option value="chine">Chine</option>
<option value="japon">Japon</option>
</select>
```
* le bouton submit
 
  `<input type="submit" value="Envoyer" />`
* le bouton reset
 
  `<input type="reset" value="Annuler" />`
-----
 ## 11-LES MEDIA
 Ce sont des règles que l'on peut appliquer dans certaines conditions. Concrètement, vous allez pouvoir dire « Si la résolution de l'écran du visiteur est inférieure à
 tant, alors applique les propriétés CSS suivantes ». Cela vous permet de changer l'apparence du site dans certaines conditions :
 vous pourrez augmenter la taille du texte, changer la couleur de fond, positionner différemment votre menu dans certaines
 résolutions, etc.

  Je préfère personnellement pour des raisons pratiques à écrire ces règles dans le même fichier CSS que d'habitude.
 Dans ce cas, on écrit la règle dans le fichier .css comme ceci :
 
 `@media screen and (max-width: 1280px)
 {
 /* Rédigez vos propriétés CSS ici */
 }
 `
 
 
