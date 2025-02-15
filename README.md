# **COURS HTML CSS**
Les notions suivantes m'ont permies de résoudre les différents exercices en HTML et CSS
## **1. CSS ET L'HERITAGE** 
En CSS, si vous appliquez un style à une balise, toutes les balises qui se trouvent à l'intérieur prendront le même style.

--------
## **2. APPLIQUER UNE IMAGE DE FOND**
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
## 3. LA TRANSPARENCE:OPACITY
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
## 4.  LES BORDURES ARRONDIES
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

 La propriété border-radius va nous permettre d'arrondir facilement les angles de n'importe quel élément. Il suffit d'indiquer
 la taille (« l'importance ») de l'arrondi en pixels.
 
```css
p
{
border-radius: 10px;
}
```
    
## 5. CREATION D'APPARENCES DYNAMIQUES
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
## 6. TRANSFORMATION DES ELEMENTS AVEC DISPLAY
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
## 7. LES GRID
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
fusionner les 2 premières cases des 2 lignes.IL faut écrire:

***Voici le code pour l'obtenir***

***code HTML***

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>grid-auto-flow</title>
    <link rel="stylesheet" href="grid-row-start.css"/>
</head>
<body>
   <div class="grid-container">
        <div class="grid-case-coller">1</div>
        <div class="grid-case">2</div>
        <div class="grid-case">3</div>
        <div class="grid-case">4</div>
        <div class="grid-case">5</div>
   </div> 
</body>
</html>
```

***code CSS***

```css
.grid-container{
    display: grid;
    grid-template-columns: repeat(3,100px);
    grid-template-rows: repeat(3,100px);
    gap:10px;
    grid-row-start:span 2;
}
.grid-case{
    align-items: center;
    background-color: cornflowerblue;
    color: white;
}
.grid-case-coller{
    align-items: center;
    background-color: cornflowerblue;
    color: white;
}
.grid-case-coller{
    grid-row: span 2;
    grid-column: 1;
}
```

### 7.2 Order de placement des grid

La propriété CSS grid-auto-flow contrôle l'ordre dans lequel les éléments sont placés dans une grille, ainsi que la direction dans laquelle la grille s'agrandit lorsqu'il n'y a plus de place pour un nouvel élément dans la grille définie.

Il existe 3:

* ***row:*** Les éléments sont placés par lignes successives (par défaut).
* ***column:*** Les éléments sont placés par colonnes successives.
* ***dense:***  Les éléments sont placés en essayant de combler les trous créés par des éléments plus grands.
* ***row dense:*** Les éléments sont placés par lignes en essayant de combler les trous.
* ***column dense:***  Les éléments sont placés par colonnes en essayant de combler les trous.

 
***Exemple d'utilisation:***

Exemple sur les colonnes. Avec grid-auto-flow: column;

***Code HTML***

```HTML
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

```CSS
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 100px);
    grid-template-rows: repeat(3, 100px);
    gap: 10px;
    grid-auto-flow: column;
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
-----
## 8.LES FLEX-BOX
### 8.1 LES FLEX-DIRECTIONS
La propriété CSS flex-direction définit l'orientation principale des éléments flexibles dans un conteneur flex. Elle permet de déterminer si les éléments doivent être disposés horizontalement ou verticalement, et dans quel ordre.

* ***row (par défaut) :*** Les éléments flexibles sont disposés horizontalement de gauche à droite.
* ***row-reverse :*** Les éléments flexibles sont disposés horizontalement de droite à gauche.
* ***column :*** Les éléments flexibles sont disposés verticalement de haut en bas.
* ***column-reverse :*** Les éléments flexibles sont disposés verticalement de bas en haut.

***Exemple avec column-reverse***

***code HTML***

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemple de column-reverse</title>
    <link rel="stylesheet" href="styles.css"/>
</head>
<body>
    <div class="container">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
    </div>
</body>
</html>
```

***code CSS***

```CSS
.container {
    display: flex;
    flex-direction: column-reverse; /* Les éléments sont disposés de bas en haut */
    gap: 10px;
    padding: 10px;
    border: 1px solid #ccc;
    width: 200px;
    background-color: lightgray;
}

.item {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: cornflowerblue;
    color: white;
    width: 100%;
    height: 50px;
    border-radius: 5px;
    font-size: 16px;
}
```
### 8.2 JUSTIFY-CONTENT
* ***flex-start :*** Les éléments sont alignés au début de l'axe principal (par défaut).
* ***flex-end :*** Les éléments sont alignés à la fin de l'axe principal.
* ***center :*** Les éléments sont centrés le long de l'axe principal.
* ***space-between :*** L'espace entre les éléments est égal, le premier élément est aligné au début et le dernier à la fin de l'axe principal.
* ***space-around :*** L'espace entre les éléments est égal, avec la moitié de cet espace appliqué aux bords de chaque élément.
* ***space-evenly :*** L'espace entre les éléments est égal, y compris aux bords du conteneur.
  
### 8.3 FLEX-SHRINK
La propriété CSS flex-shrink définit la capacité d'un élément flexible à rétrécir si nécessaire. Elle est utilisée dans un conteneur flexible (flex container) pour spécifier comment l'espace est distribué entre les éléments lorsque l'espace disponible est insuffisant.

***Exemple d'utilisation***

***code HTML***

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="flex-shrink.css"/>
    <title>flex-strink</title>
</head>
<body>
    <div class="flex-container">
        <div class="flex-item flex-shrink1">1</div>
        <div class="flex-item flex-shrink2">2</div>
        <div class="flex-item flex-shrink3">3</div>
    </div>
</body>
</html>
```

***code CSS***

```CSS
.flex-container{
    display: flex;
    width: 300px;
    background-color: bisque;
}
.flex-item{
    background-color: chocolate;
    width:50%;
    height: 50%;
    display: flex;
    margin: 5%;
    color: white;
    justify-content: center;
}
.flex-shrink1{
    flex-shrink:1;

}
.flex-shrink2{
    flex-shrink: 3;

}
.flex-shrink3{
    flex-shrink: 3;
}
```
-------
## 9. LES POSITIONNEMENTS absolu, fixe, relatif 
### 9.1 Le positionnement absolu
Le positionnement absolu permet de positionner un élément par rapport à son conteneur positionné le plus proche. Un élément avec une position absolue est retiré du flux normal du document et peut être placé à des coordonnées spécifiques à l'intérieur de son conteneur.

***Exemple d'utilisation***
```css
element
{
 position: absolute;
}
```
### 9.2  Le positionnement fixe
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

## 10. SUPPERPOSITION DES ELEMENTS AVEC z-index
Si vous placez deux éléments en absolu vers le même endroit, ils risquent de se chevaucher. Dans ce cas, utilisez la propriété z-index pour indiquer quel élément doit apparaître au-dessus des autres.
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
## 11. LES TABLES
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

 ## 12. LES FORMULAIRES
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
 ## 13. LES MEDIA
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

 ## 14. LES PSEUDO-CLASSES
 Les pseudo-classes en CSS sont des mots-clés ajoutés aux sélecteurs qui spécifient un état spécial de l'élément sélectionné. Elles permettent de cibler des éléments 
 en fonction de leur état dans le document. Les plus connues sont: hover, active, focus .

* ***:hover***  Ciblé lorsqu'un utilisateur pointe un élément avec un périphérique de pointage, mais ne l'a pas encore activé.
* ***:active***  Ciblé lorsqu'un utilisateur active un élément (par exemple, en cliquant dessus).
* ***:focus***  Ciblé lorsqu'un élément a le focus (par exemple, lorsqu'un utilisateur clique sur un champ de formulaire).
* ***:nth-child(n)***  Ciblé le n-ième enfant d'un parent.
* ***:nth-of-type(n)***  Ciblé le n-ième enfant d'un certain type d'élément parmi ses frères et sœurs.
* ***:first-child***  Ciblé le premier enfant d'un parent.
* ***:last-child***  Ciblé le dernier enfant d'un parent.
* ***:only-child***  Ciblé lorsqu'un élément est le seul enfant de son parent.
* ***:not(selector)***  Ciblé tous les éléments qui ne correspondent pas au sélecteur.
* ***:disabled***  Ciblé les éléments qui sont désactivés (comme les champs de formulaire désactivés).

## 15.LES PSEUDO-ELEMENTS
* ***::before***   Insère du contenu avant le contenu d'un élément.
* ***::after***   Insère du contenu après le contenu d'un élément.
* ***::first-line***  Cible la première ligne d'un bloc de texte.
* ***::first-letter***  Cible la première lettre d'un bloc de texte.
* ***::selection***  Cible la partie du document sélectionnée par l'utilisateur.
* ***::placeholder***  Cible le texte d'espace réservé (placeholder) d'un élément de formulaire.

