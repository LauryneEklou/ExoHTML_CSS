Les notions suivantes m'ont permies de résoudre les différents exercices en HTML et CSS
1.CSS ET L'HERITAGE: 
 En CSS, si vous appliquez un style à une balise, toutes les balises qui se trouvent à l'intérieur prendront le même style.

2.APPLIQUER UNE IMAGE DE FOND:
 La propriété permettant d'indiquer une image de fond est background-image. Comme valeur, on doit renseigner url("nom_de_l_image.png").
	Il existe des options disponible pour le fond telles que:
2.1. background-attachment : fixer le fond
  	-fixed : l'image de fond reste fixe ;
 	-scroll : l'image de fond défile avec le texte (par défaut).

2.2. background-repeat : répétition du fond
	 -no-repeat : le fond ne sera pas répété. L'image sera donc unique 	sur la page.
	 -repeat-x : le fond sera répété uniquement sur la première ligne, 	horizontalement.
	 -repeat-y : le fond sera répété uniquement sur la première colonne, verticalement.
 	 -repeat : le fond sera répété en mosaïque (par défaut).

2.3. background-position : position du fond
	 - top : en haut 
         -bottom : en bas 
         -left : à gauche
         -center : centré
         - right : à droite.
3.LA TRANSPARENCE:OPACITY
Elle se fait avec la  propriété opacity.
-Avec une valeur de 1, l'élément sera totalement opaque : c'est le    	comportement par défaut. 
-Avec une valeur de 0, l'élément sera totalement transparent.

 4.  Les bordures et les ombres
  Les différents types de bordures:
	-solid
	-dotted
	-dashed
	-double
	-groove
	-ridge
	-inset
	-outset

4.1 bordures arroundies
 La propriété border-radius.

5.CREATION D'APPARENCES DYNAMIQUES
-Au survol:avec la propriété hover.
-Active:Quand le visiteur clique sur le lien.
-visited: Quand le visiteur a déjà vu la page concernée.

6.TRANSFORMATION DES ELEMENTS AVEC DISPLAY
- display: block; les liens vont se positionner les uns en-dessous des autres (comme des blocs normaux) et il devient possible de  modifier leurs dimensions !
-display:inline; Eléments d'une ligne. Se placent les uns à côté des autres.
-display: inline-block; Eléments positionnés les uns à côté des autres  mais qui peuvent être redimensionnés.
-display:none; Eléments non affichés.

7.LES POSITIONNEMENTS absolu, fixe, relatif 
7.1 Le positionnement absolu : il nous permet de placer un élément n'importe où sur la page (en haut à gauche, en bas à droite, tout au centre, etc.).
7.2  Le positionnement fixe : identique au positionnement absolu mais, cette fois, l'élément reste toujours visible, même si on
descend plus bas dans la page.
7.3  Le positionnement relatif : permet de décaler l'élément par rapport à sa position normale.

8.SUPPERPOSITION DES ELEMENTS AVEC z-index
Les éléments positionnés en absolu sont placés par-dessus le reste des éléments de la page ! Par ailleurs, si vous placez deux
éléments en absolu vers le même endroit, ils risquent de se chevaucher. Dans ce cas, utilisez la propriété z-index pour indiquer
quel élément doit apparaître au-dessus des autres.
