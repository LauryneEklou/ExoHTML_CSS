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
}
```

Il existe des options disponible pour le fond telles que:
### 2.1. background-attachment
* ***fixed***: l'image de fond reste fixe.
 
```css
 body
 {
 background-image: url("nom_de_image.png");
  background-attachment: fixed; 
 }
 ```
* ***scroll***: l'image de fond défile avec le texte (par défaut).
 
```css
body
 {
 background-image: url("nom_de_image.png");
  background-attachment: scroll; 
 }
 ```
### 2.2. background-repeat : répétition du fond
* ***no-repeat***: le fond ne sera pas répété. L'image sera donc unique sur la page.
* ***repeat-x***: le fond sera répété uniquement sur la première ligne, horizontalement.
* ***repeat-y***: le fond sera répété uniquement sur la première colonne, verticalement.
* ***repeat***: le fond sera répété en mosaïque (par défaut).
 
***Exemple d'utilisation***
  
```css
body
{
background-image: url("nom_de_image.png");
background-repeat: no-repeat;
}
```

### 2.3. background-position : position du fond
* ***top***: en haut 
* ***bottom***: en bas 
* ***left***: à gauche
* ***center***: centré
* ***right***: à droite.
 
***Exemple d'utilisation***
  
Il est possible de combiner ces mots. Par exemple, pour aligner une image en haut à droite, vous taperez :

```css
background-position: top right;
```
## 3.LA TRANSPARENCE:OPACITY
Elle se fait avec la  propriété opacity.
1. ***Avec une valeur de 1***, l'élément sera totalement opaque : c'est le comportement par défaut.
2. ***Avec une valeur de 0***, l'élément sera totalement transparent.

 ***Exemple d'utilisation***

```css
p{
opacity: 0.6;
}
```

------   
## 4.  LES BORDURES ARRONDIES ET OMBRES
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

```css
h1
{
 border: 3px blue dashed;
}
```
### 4.1 BORDURES ARRONDIES
 La propriété border-radius va nous permettre d'arrondir facilement les angles de n'importe quel élément. Il suffit d'indiquer
 la taille (« l'importance ») de l'arrondi en pixels.
 
```css
p
{
border-radius: 10px;
}
```
    
## 5.CREATION D'APPARENCES DYNAMIQUES
* ***Au survol***  : avec la propriété hover. hover signifie « survoler ». a:hover peut donc se traduire par : « Quand la souris est sur le lien ».
 
```css
a:hover
{
}
```

* ***Active***: Quand le visiteur clique sur le lien.
 On peut par exemple changer la couleur de fond du lien lorsque l'on clique dessus :

```css
a:active
{
 background-color: #FFCC66;
}
```
* ***visited***: Quand le visiteur a déjà vu la page.concernée. Vous pouvez changer cette apparence avec :visited (qui signifie « visité »). En pratique, sur les liens consultés, on ne peut
 pas changer beaucoup de choses à part la couleur.
```css
a:visited
  {
  color: #AAA;
  }
```

----
## 6.TRANSFORMATION DES ELEMENTS AVEC DISPLAY
* ***display : block;*** les liens vont se positionner les uns en-dessous des autres (comme des blocs normaux) et il devient possible de  modifier leurs dimensions !
 
```css
a
 {
 display: block;
 }
```
* ***display : inline;*** Eléments d'une ligne. Se placent les uns à côté des autres.
 
```css
nav, section
 {
 display: inline;
 }
 ```
* ***display : inline-block;*** Eléments positionnés les uns à côté des autres  mais qui peuvent être redimensionnés.

```css
nav
{
display: inline-block;
width: 150px;
border: 1px solid black;
vertical-align: top;
}
```
* ***display : none;*** Eléments non affichés.
 
```css
nav
{
 display: inline-block;
}
```
----
## 7.LES GRID
CSS Grid Layout, souvent appelé simplement "Grid", est une technique de mise en page en CSS qui permet de créer des grilles bidimensionnelles. Il est conçu pour la mise en page des éléments dans des lignes et des colonnes, ce qui permet de créer des designs complexes de manière simple et flexible.
***Exemple d'utilisation***
Nous pouvons transformer 9 éléments qui sont au départ alignés verticalement en un grillage composé de 3 lignes et 3 colonnes:

***code HTML***

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemple de Grille CSS</title>
  <link rel="stylesheet" href="grid.css">
</head>
<body>
  <div class="grid-container">
    <div class="grid-item">1</div>
    <div class="grid-item">2</div>
    <div class="grid-item">3</div>
    <div class="grid-item">4</div>
    <div class="grid-item">5</div>
    <div class="grid-item">6</div>
    <div class="grid-item">7</div>
    <div class="grid-item">8</div>
    <div class="grid-item">9</div>
  </div>
</body>
</html>
```

***code CSS***

```css
 .grid-container {
    display: grid;
    grid-template-columns: repeat(3, 100px);
    grid-template-rows: repeat(3, 100px);
    gap: 10px;
  }
  
  .grid-item {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #4CAF50;
    color: white;
    font-size: 20px;
    border: 2px solid #fff;
    border-radius: 10px;
  }
```
### 7.1 Fusion des éléments dans un grid
Si par exemeple vous avez un grid composé 6 éléments disposés en 2 lignes et en 3 colonnes et que vous voulez
fusionner les 2 premières cases des 2 lignes, comme illustrer sur la figure ci-dessous.

![Texte alternatif](cours_CSS/azure.jpg)

## 8.LES POSITIONNEMENTS absolu, fixe, relatif 
### 8.1 Le positionnement absolu
il nous permet de placer un élément n'importe où sur la page (en haut à gauche, en bas à droite, tout au centre, etc.).
***Exemple d'utilisation***
```css
element
{
 position: absolute;
}
```
### 8.2  Le positionnement fixe
Identique au positionnement absolu mais, cette fois, l'élément reste toujours visible, même si on
descend plus bas dans la page.

***Exemple d'utilisation***

```css
element
{
 position: fixed;
}
```
### 8.3  Le positionnement relatif 
Permet de décaler l'élément par rapport à sa position normale.
***Exemple d'utilisation***

```css
element
{
position: relatif;
}
```

## 9. SUPPERPOSITION DES ELEMENTS AVEC z-index
Les éléments positionnés en . Par ailleurs, si vous placez deux
éléments en absolu vers le même endroit, ils risquent de se chevaucher. Dans ce cas, utilisez la propriété z-index pour indiquer quel élément doit apparaître au-dessus des autres.
***Exemple d'utilisation***

```css
element
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
 }
```
    
----
## 10.LES TABLES
* ***Colspan***: pour fusionner les cellules d'une table
 
***Exemple:***
```html
<td colspan="2">
 ```
Cette cellule est la fusion de deux cellules .
 
* ***rowspan***: pour fusionner les lignes d'une table .
 
***Exemple:***
```html
<td rowspan"2">
```
Cette cellule est la fusion de deux lignes . 

 ## 11.LES FORMULAIRES
* les champs texte
 
```html
<input type="text" />
```
* les champs de type checkbox
 
```html
<input type="checkbox" />
```
* les champs de type radio
 
```html
<input type='radio'/>
```
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
 
  ```html
  <input type="submit" value="Envoyer" />
  ```
* le bouton reset
 
  ```html
  <input type="reset" value="Annuler" />
  ```
-----
 ## 12-LES MEDIA
 Ce sont des règles que l'on peut appliquer dans certaines conditions. Concrètement, vous allez pouvoir dire « Si la résolution de l'écran du visiteur est inférieure à
 tant, alors applique les propriétés CSS suivantes ». Cela vous permet de changer l'apparence du site dans certaines conditions :
 vous pourrez augmenter la taille du texte, changer la couleur de fond, positionner différemment votre menu dans certaines
 résolutions, etc.

  Je préfère personnellement pour des raisons pratiques à écrire ces règles dans le même fichier CSS que d'habitude.
 Dans ce cas, on écrit la règle dans le fichier .css comme ceci :
 
 ```css
@media screen and (max-width: 1280px)
 {
 /* Rédigez vos propriétés CSS ici */
 }
 ```
 
 
