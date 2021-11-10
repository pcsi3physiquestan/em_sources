---
jupytext:
  encoding: '# -*- coding: utf-8 -*-'
  formats: ipynb,md:myst
  split_at_heading: true
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Champ magnétique. Introduction

## Observation expérimentale

### Observations
On observe différents cas d'influence d'objets sur d'autres dont l'action ne correspond pas à des forces déjà présentées en mécanique:

* Une bobine parcourue par un courant peut dévier un jet d'électrons
* De même un aimant peut dévier un jet d'électrons
* Un aimant peut entraîner le déplacement d'un autre aimant ou d'un circuit parcouru par un courant

````{dropdown} Remarque

Il est évident que les actions réciproques à celle citées existent aussi.

Malgré la diversité des actions envisagées, leur étude peut-être modélisée de la même manière: on va introduire un intermédiaire entre la cause (aimant ou circuit électrique) et la conséquence (mouvement d'un aimant/déviation de particules chargées). Cet intermédiaire est le __champ magnétique__. Son unité sera le __Tesla (T)__.

````

```{figure} ./images/em_action_magnetique.jpg
:name: fig_champ_magnetique
:align: center
Introduction de l'intermédiaire "champ magnétique"
```

### Interprétation en terme de champ magnétique
````{dropdown} Remarque

Comme nous l'avons vu, lorsqu'on traite des particules chargées en mouvement près d'un circuit électrique, leur mouvement peut-être décrit par un champ scalaire dont les caractéristiques dépendent du circuit électrique (forme, intensité, position/orientation...).

````

````{important} __Définition : Champ magnétique__

Soit une particule chargé de charge $q$ en un point M possédant une vitesse $\overrightarrow{v}$. L'action, appelée force de Lorentz, d'un circuit parcouru par un courant ou d'un aimant peut-être modélisée par une force dont l'expression mathématique est:

\begin{equation}
\overrightarrow{F} = q \overrightarrow{v} \wedge \overrightarrow{B}(M)
\end{equation}

où $\overrightarrow{B}(M)$ est un champ vectoriel dont les caractéristiques ne dépendent que du circuit ou de l'aimant. On l'appelle champ magnétique et son unité est le Tesla (T). M est le point où se trouve la particule de charge $q$.

````

````{dropdown} Remarque

Comme on le verra par la suite, l'action d'un champ magnétique se généralisera à des dispositifs globalement neutres comme d'autres circuits électriques ou d'autres aimants. On parlera alors de force de Laplace.

La notion de champ peut paraître très abstraite. Elle est pourtant cruciale. Pour comprendre sa première utilité, on peut faire le parallèle avec le champ de gravitation. Si son intervention n'est pas nécessaire pour calculer la force exercée par une masse sur une autre masse, sa définition permet de découplé l'étude de la cause (première masse) de la seconde. On peut donc ainsi travailler sur l'action d'un champ de gravitation donné (qu'on pourra même déterminer expérimentalement) sur une particule massique, un corps solide... sans se soucier de ce qui le crée. Pour le champ magnétique, c'est le même principe. Vu la diversité des façons de créer un champ magnétique, son intervention est encore plus utile. De plus, des études plus poussées en électromagnétisme montrerait que cet outils a pris aujourd'hui une place prépondérante dans des domaines comme la théorie des champs.

````

## Cartes de champ magnétiques

### Lignes de champ. Caractérisation expérimentale

````{important} __Définition : Ligne de champ magnétique__

Une ligne de champ magnétique est une courbe avec laquelle le champ magnétique est colinéaire en tout point de la-dite courbe.

````

````{panels}
```{figure} ./images/em_fil_infini.jpg
:name: fig_fil_infini
:align: center
Exemple : Carte de champ pour un fil infini
```
---
```{figure} ./images/Electromagnetisme_1_Deuxfils.jpg
:name: fig_deux_fils_champ_b
:align: center
Exemple : Carte de champ de deux fils. L'intensité est identique dans les deux fils mais n'est pas dans le même sens: elle sort de la feuille pour le fil de gauche et entre dans la feuille pour le fil de droite
```
````

````{panels}
```{figure} ./images/em_carte_champ_dipole_magnetostatique.jpg
:name: fig_dipole_magneto_aimant
:align: center
Exemple : Carte de champ pour un petit aimant droit
```
---

```{figure} ./images/Electromagnetisme_1_Spire_Solene.jpg
:name: fig_spire_solen_champ_b
:align: center
Champ magnétique pour une spire circulaire et une bobine longue.
```
````

````{admonition} Exemple : Bobine infinie
:class: tip, dropdown

On peut montrer que le champ magnétique est nulle à l'extérieur du solenoïde et uniforme à l'intérieur:

\begin{equation}
\overrightarrow{B} = \mu_0 n I \overrightarrow{e_z}
\end{equation}

où n est le nombre de spire par unité de longuer, I l'intensité qui parcourt les spires et $\overrightarrow{e_z}$ le vecteur axial __orienté en cohérence__ avec I.

````

__Matérialisation expérimentale:__

Les aimants, sur des liaisons pivots quasi-parfaites ou de la limaille de fer aura tendance à l'aligner le long des lignes de champ: on peut ainsi caractériser les lignes de champ magnétiques.

__Principe de symétrie (non exhaustif):__

* Les invariances des causes (courants) se retrouvent dans les invariances du champ magnétique
* Sur un plan d'anti-symétrie des causes, le champ magnétique est contenu dans le plan.
* Sur un plan de symétrie des causes, le champ magnétique est perpendiculaire au plan.


### Caractéristiques générales

* Principe de symétrie (cf. suite)
* Orientation du champ proche du circuit: règle du tire-bouchon basé sur l'intensité.
* Le champ en un point donné sera proportionnelle à l'intensité I qui circule dans le circuit.
* En un point où deux lignes se croisent, le champ est nécessairement nul.
* Une ligne de champ qui boucle sur elle-même enlace nécessairement des courants. Le sens total de parcours des courants enlacés (calculés comme une somme algébrique) peut-être déterminé par la règle du tire-bouchon.

````{dropdown} Remarque

Ce dernier point est un aspect qualitatif d'un théorème utile pour calculer un champ magnétique créé par une distribution de courant: le théorème d'Ampère (et sa formulation locale l'équation de Maxwell-Ampère). Cette formulation n'est pas donnée complètement en première année et sera vue l'année prochaine.

````

### Conservation du flux du champ magnétique

````{dropdown} Remarque

Orientation d'une surface: En géométrie vectorielle, une surface plane est orientée par un vecteur appelé vecteur surface dont la norme est égale à l'aire de la surface considérée et l'orientation est perpendiculaire à la surface.

Cette définition se généralise facilement à une surface non plane par une approche différentielle. On "découpe" la surface en des surfaces infinitésimales $\overrightarrow{dS}$ qui sont approchables par des surfaces planes. Le vecteur surface totale est la somme de tous les vecteurs surfaces considérés (ici une intégrale sur une surface).

Sens d'orientation d'une surface non fermée: Soit une surface $\Sigma$ délimitée par un contour $\Gamma$ orienté. La surface est alors orientée par convention en cohérence avec le contour $\Gamma$ en appliquant la règle du tire- bouchon (ou du bonhomme d'Ampère).

Cette convention d'orientation fonctionne dans les deux sens. On peut très bien orienter le contour de la surface à partir de l'orientation de la surface elle-même. 

Sens d'orientation d'une surface fermée: Soit une surface $\Sigma$ fermée, on oriente la surface, par convention, vers l'extérieur.

````


````{important} __Définition : Flux du champ magnétique__

Soit un champ vectoriel $\overrightarrow{B}(M)$ définit en tout point M de l'espace et une surface $\Sigma$ quelconque orientée décomposée en un ensemble de surface plane infinitésimale $\overrightarrow{dS}$. On définit le flux du vecteur $\overrightarrow{B}$ à travers $\Sigma$ comme l'intégrale:

\begin{equation}
\Phi = \int_{M \in \Sigma} \overrightarrow{B}(M) \cdot \overrightarrow{dS}(M)
\end{equation}

````

````{important} __Fondamental : Conservation du flux du champ magnétique__

Le flux du champ magnétique est conservé, c'est-à-dire qu'il est toujours nul à travers une surface fermée.

````

````{important} __Définition : Tube de champ__

Un tube de champ est une surface fermée, orientée de l'intérieur vers l'extérieur, constituée d'une surface latérale ($S_L$) uniquement formée de lignes de champ et de deux surfaces quelconques ($S_1$) et ($S_2$) la fermant à ses extrémités.

```{figure} ./images/em_tube_champ.jpg
:name: fig_tube_de_champ_magn_tique
:align: center
Tube de champ magnétique
```

````

````{tip} __Exercice : Calcul du flux du champ magnétique sur un tube de champ__

1. Exprimer le flux du champ magnétique à travers un tube de champ en fonction des flux entrant en $S_1$ et sortant en $S_2$
1. En déduire une interprétation de la notion de conservation du flux.


````

````{important} __Fondamental : Conséquence de la conservation du flux__


* Lorsque les lignes de champ magnétique se resserrent, l'intensité du champ magnétique augmente.
* Lorsque les lignes de champ magnétique s'écartent, l'intensité du champ magnétique diminue.
* Si les lignes de champ forme un tube de section constant, alors le champ est uniforme.

```{dropdown} Remarque

Les réciproques de ces affirmations sont aussi vraies (influence de l'intensité du champ sur la section du tube de champ associé).

```

````

### Créer un champ magnétique uniforme
Si l'on ne peut créer un champ magnétique uniforme dans tout l'espace, on peut par contre créer un champ magnétique dont les variations (intensité ET orientation) sont relativement faibles sur une zone donnée. On utilise généralement deux dispositifs:

* les bobines de Helmoltz: ce sont deux spires parallèles et coaxiales de rayon R distantes de R. On peut montrer que le champ magnétique au milieu des bobine varie peu.
* une bobine longue: on peut montrer que le champ magnétique est globalement uniforme à l'intérieur de la bobine tant qu'on reste loin des bords.

## Symétrie des champs magnétiques

### Les distributions de courant
On a vu que les courants sont responsables du champ magnétiques. Il faut donc pouvoir décrire une __distribution de courant__ dans l'espace pour ensuite pouvoir déterminer le champ magnétique en tout point.

On a 3 types de description des courants :
* une description linéique : cela correspond à la vision des courant électrique déjà utilisé en électrocinétique. On considère que la conduction électrique a lieu sur des lignes et on décrit les courant par l'intensité électrique et le sens de l'intensité. __Cela revient à négliger la section des fils électriques.__
* une description volumique : A l'image du fil électrique, les charges se déplacent en réalité dans des volumes et non des lignes. On peut alors découper ces volumes en des volumes $d \tau_M$ infinitésimaux autour de chaque point M. Dans ces volumes, on peut considérer que les charges mobiles ont une concentration uniforme $\rho(M)$ (principe du calcul différentiel) et vitesse $\overrightarrow{v}(M)$ identique. On décrit alors la distribution de courant par __la densité volmumique de charge__ : $\overrightarrow{j_v}(M) = \rho(M) \overrightarrow{v}(M)$.
* une description surfacique : Il arrive qu'une des deux dimensions du fil soit négligeable devant l'autre (cas des nappes de courant), les charges se déplacent presque dans des surfaces et non des lignes. On peut alors découper ces surfaces en des surfaces $d \Sigma_M$ infinitésimales autour de chaque point M de la surfaces où il y a du courant. Dans ces surfaces, on peut considérer que les charges mobiles ont une concentration _surfacique_ uniforme $\sigma(M)$ (principe du calcul différentiel) et vitesse $\overrightarrow{v}(M)$ identique. On décrit alors la distribution de courant par __la densité surfacique de charge__ : $\overrightarrow{j_s}(M) = \sigma(M) \overrightarrow{v}(M)$.

````{attention}
$\overrightarrow{j_s}$ et $\overrightarrow{j_v}$ n'ont PAS la même unité.
````

(exemple_dist)=
````{admonition} Exemples de distribution
:class: tip, dropdown

__Distribution linéique__  
* Un fil infini parcouru par une intensité I
* Une spire circulaire de rayon $R$ parcouru par une intensité $I$.
* Une bobine de longueur infini constitué de spire circulaire de rayon $R$ et d'épaisseur négligeable jointives parcouru un courant $I$. On donne en général le nombre de spire par unité de longueur $n$

__Distribution volumique__  
* Un cylindrique infini de rayon $R$ parcouru par une distribution volumique $\overrightarrow{j_v}(M) = j_0 \overrightarrow{e_z}$. C'est la modélisation du fil infini en tenant compte de l'épaisseur du fil (en supposant la distribution homogène).

__Distribution surfacique__
* Nappe de courant : Une bande infinie de large $L$, d'épaisseur négligeable. On note $Ox$ l'axe normal à la nappe et $Oy$ l'axe correspondant à l'axe (infini) de la bande. Si la conduction a lieu suivant $Oy$, on la décrira par une distribution surfacique $\overrightarrow{j_s}(M) = j_0 \overrightarrow{e_y}$ (cas d'une distribution homogène des courant sur la nappe).

````

#### Lien entre distribution et intensité.
Il faut faire attention car le nom des distributions de courantpeut être trompeur.

````{tip} Exercice
On considère les deux exemples précédente : 
1. fil infini de rayon $R$ parcouru par une distribution axiale uniforme. Calculer l'intensité qui traverse une section transverse du cylindre (orientée suivant $+\overrightarrow{e_z}$).
2. nappe de courant de largeur $L$ parcourue par une densité uniforme. Calculer l'intensité qui traverse la nappe suivant l'axe Oy.

````

> Résolution  
> __Cas volumique__ : On commence par décomposer la __surface__ transverse du cylindre (un cercle de rayon $R$) en des surfaces élémentaires $dS(M)$ orientée suivant $+\overrightarrow{e_z}$ autour de chaque point M dela surface. La quantité de charge qui traverse cette surface $dS(M)$ entre $t$ et $t+dt$ et l'ensemble des charges contenu à l'instant $t$ dans le cylindre élementaire appuyé sur dS et de hauteur $vdt$ ($v$ étant la vitesse ces charges, elle est bien constante sur une durée dt tendant vers 0).
>
>La surface et donc le volume $v(M) dtdS(M)$ étant infinitésimaux, on peut considérer que la densité volumique de charges mobiles y est uniforme et la quantité de charges est donc $\rho(M)v(M) dt dS(M)$, ce qu'on peut réécrire vectoriellement :
> \begin{equation}
\overrightarrow{j_v}(M) \cdot \overrightarrow{dS}(M)
\end{equation}
> Il vient que l'intensité totale s'écrit :
> \begin{equation}
\iint_{\Sigma} \overrightarrow{j_v}(M) \cdot \overrightarrow{dS}(M)
\end{equation}
>
> Dans le cas uniforme, il vient $I = j_0 \pi R^2$
>
> __Cas surfacique__ : Cette fois, les charges ne traverse pas une surface mais une __ligne transverse__ à la conduction (avec suivant Oz) (faire le parallèle avec une barrière de péage). On commence par décomposer la __ligne transverse__ du cylindre en des lignes élémentaires $dz$ orientée suivant $+\overrightarrow{e_y}$ autour de chaque point M de la ligne. La quantité de charge qui traverse cette ligne $dz$ entre $t$ et $t+dt$ et l'ensemble des charges contenu à l'instant $t$ dans le rectangle élementaire appuyé sur dz et de hauteur $vdt$ ($v$ étant la vitesse ces charges, elle est bien constante sur une durée dt tendant vers 0).
>
>La ligne et donc lsurface $v(M) dtdz$ étant infinitésimaux, on peut considérer que la densité surfacique de charges mobiles y est uniforme et la quantité de charges est donc $\sigma(M)v(M) dt dz$, ce qu'on peut réécrire vectoriellement :
> Il vient que l'intensité totale s'écrit :
> \begin{equation}
\int j_s(M) dz
\end{equation}
> où $j_s(M)$ est la valeur de la composante de $\overrightarrow{j_s}$ suivant $\overrightarrow{e_y}$.
>
>Dans le cas uniforme, il vient : $I = L j_0$

### Notions de symétries et d'invariance

#### Invariance
```{important} __Invariance__

Soit une transformation de l'espace $\mathcal{T}$. On dit qu'elle laisse invariante un champ scalaire $C(M)$ si et seulement si pour tout point M' image des points M de l'espace, $C(M) =C(M')$.
```

En pratique, les invariances que nous rencontreront correspondant à un champ scalaire (ou la composante scalaire d'un champ vectoriel)  dont l'expression mathématique ne dépend pas d'une coordonnée de l'espace. __A condition d'avoir choisi un type de repère adapté à l'invariance.__

On distingue alors les invariances par translation et par rotation.

````{admonition} Exemple
:class: tip, dropdown

* Considérons un fil infini parcouru par un courant I. 
    * La distribution de courant est alors invariante par translation suivant l'axe du fil.
    * Elle est aussi invariante par rotation autour de l'axe du fil.
    * On va donc choisir un repère cylindre d'axe, l'axe du fil. L'invariance par translation correspond à une indépendance vis-à-vis de la coordonnée $z$ et l'invariance par rotation correspond à une indépendance vis-à-vis de la coordonnées $\theta$.

````

#### Symétrie et anti-symétrie planaire d'un vecteur
````{important} __Symétrie planaires__

Soit un plan $\Pi$. On dit que le champ vectoriel $\overrightarrow{j}(M))$ présente une symétrie par rapport à $\Pi$ si et seulement si pour tout point M' image de M par rapport à $\Pi$, $\overrightarrow{j}(M')$ est symétrique de $\overrightarrow{j}(M)$ par rapport à $\Pi$

````

````{important} __Antisymétrie planaires__

Soit un plan $\Pi$. On dit que le champ vectoriel $\overrightarrow{j}(M))$ présente une anti-symétrie par rapport à $\Pi$ si et seulement si pour tout point M' image de M par rapport à $\Pi$, $\overrightarrow{j}(M')$ est __l'opposé__ du symétrique de $\overrightarrow{j}(M)$ par rapport à $\Pi$

````

````{admonition} Exemple
:class: tip, dropdown

* Considérons un fil infini parcouru par un courant I. 
    * Tout plan perpendiculaire au fil est plan d'antisymétrie des courants (la densité de courant linéique (l'intensité) est transformée en -I par symétrie).
    * Tout plan contenant le fil est plan de symétrie des courants.
````

````{tip} Exercice : Conséquence sur les coordonnées
On considérons un champ magnétique $\overrightarrow{B}(M)$ qui possède comme plan de symétrie le plan $xOy$ d'un repère cartésien $(0, \overrightarrow{e_x}, \overrightarrow{e_y}, \overrightarrow{e_z})$.

On note les composantes de $\overrightarrow{B}(M(x, y, z))$ :
* $B_x(x, y, z)$
* $B_y(x, y, z)$
* $B_z(x, y, z)$

1. Préciser la parité des fonctions $B_x, B_y, B_z$ en $z$.
1. Reprendre la même question en supposant que $xOy$ est un plan d'anti-symétrie.

Il est important de comprendre à travers cet exercice que le lien entre parité et symétrie n'est PAS intuitif.
````

````{tip} Exercice : Sur le plan

1. Justifier (à retenir) que le vecteur champ magnétique en tout point $M_0$ du plan $\Pi$ est contenu dans le plan $\Pi$.

On considérons un vecteur champ magnétique $\overrightarrow{B}(M)$ qui possède comme plan de d'antisymétrie le plan $\Pi_A$.

1. Justifier (à retenir) que le vecteur champ magnétique en tout point $M_0$ du plan $\Pi_A$ est perpendiculaire plan $\Pi_A$

````

````{important} __Orientation du champ__

Cette observation est __fondamental__ car cela signifie qu'en connaissance les symétries du champ magnétique, on peut l'orienter en de nombreux points. On obtiendra ainsi une expression simplifier du champ magnétique.
````

### Principe de Curie
````{important} __Fondamental : Principe de Curie__

Lorsque certaines causes produisent certains effets, les éléments de symétrie des causes doivent se retrouver dans les effets produits.
````

Dans le cas du champ magnétique, la cause est la distribution de courants et la conséquence est le champ magnétique. Les symétries (et invariances) de la distribution de courant se retrouvera donc pour le champ magnétique.

````{important} __Conséquence sur le champ magnétique__

Mais le champ magnétique est particulier (on dit que c'est un __pseudo-vecteur__ car à l'image du moment cinétique, il s'obtient mathématiquement par un produit vectoriel). Concrètement, cela signifie que __pour le champ magnétique__ :
* les invariances de la distribution de courants sont aussi des invariances du champ magnétique
* les plans de symétrie de la distribution de courants sont des plans d'anti-symétrie du vecteur champ magnétique.
* les plans d'anti-symétrie de la distribution de courants sont des plans de symétrie du vecteur champ magnétique.
````

````{admonition} Exemple : Détermination de la structure du champ B
:class: tip
On va utiliser le principe de Curie pour préciser la structure du champ magnétique pour un fil infini.
````

>* Pour un point M de l'espace, le plan perpendiculaire au fil __et passant par M__ est un plan d'anti-symétrie des courants (défini par les vecteurs ($\overrightarrow{e_r}), \overrightarrow{e_{\theta}}$, c'est donc un plan de symétrie du vecteur $\overrightarrow{B}$. __Il vient qu'au point M qui est sur ce plan, le champ magnétique est contenu dans ce plan : $B_z(M) = 0$.__
>* Pour un point M de l'espace, le plan contenant le fil __et passant par M__ est un plan de symétrie des courants (défini par les vecteurs ($\overrightarrow{e_r}), \overrightarrow{e_z}$, c'est donc un plan d'anti-symétrie du vecteur $\overrightarrow{B}$. __Il vient qu'au point M qui est sur ce plan, le champ magnétique est perpendiculaire dans ce plan donc suivant $\overrightarrow{e_\theta}$ : $B_r(M) = B_z(M) = 0$__
>* __Invariance__ : La distribution du courant est invariante par translation suivant l'axe donc si les courant ne dépendent pas de $z$, les composantes de $\overrightarrow{B}$ non plus.
>* __Invariance__ : La distribution du courant est invariante par rotation autour de l'axe donc si les courant ne dépendent pas de $\theta$, les composantes de $\overrightarrow{B}$ non plus.
>
>
>__Synthèse__ : Il vient qu'on peut écrire une expression simplifiée du champ magnétique en tout point M de l'espace :
>
>\begin{equation}
	\overrightarrow{B}(M) = B_{\theta}(r) e_{\theta}
\end{equation}

Cette expression simplifiée permet de réaliser des calculs simples pour expliciter $B_{\theta}$ grâce au théorème d'Ampère (cf deuxième année).

## Ordres de grandeurs de champs créés

### Champ magnétique par un aimant droit

* Aimants néodyme: 0,3 à 1 T
* IRM (électro-aimant): 6T

````{dropdown} Remarque

Il faut aussi connaître l'ordre du champ magnétique terrestre créé par les mouvements du noyau liquide: $0.5 \times 10^{-5} \rm{T} = 0.5 \rm{gauss}$.

````

### Champ créé par un circuit électrique
````{admonition} Théorème d'Ampère (pas à connaître en première année)
:class: dropdown

La circulation du champ magnétique sur un contour orienté (C) fermé est le produit de $\mu_0$ par la somme algébrique des intensités des courants enlacés par ce contour, les intensités dont l'orientation n'est pas en cohérence avec celle du contour (règle du tire- bouchon) étant changées de signe:
\begin{equation}
\oint_{(C)} \overrightarrow{B}\cdot \overrightarrow{dl} = \mu_0 \sum\limits_{i} \alpha_i I_i
\end{equation}
où $\alpha_i = \pm 1$ suivant que l'intensité $I_i$ est orientée en cohérence avec le contour.
````

````{dropdown} Remarque

On pourrait avoir bien entendu plusieurs types de charges. La circulation est un opérateur mathématique qui a déjà été utilisé dans les calculs de travaux des forces en mécanique. Le principe de calcul est identique, sauf qu'à nouveau, il n'y a pas de mouvement le long du contour choisi.

````

````{tip} __Exercice : Cas simple. Ordre de grandeur__

Estimer à partir du théorème d'Ampère le nombre de spire d'un bobinage nécessaire pour obtenir un champ 100 fois supérieure au champ terrestre à une distance proche du bobinage. Commenter.

````

## Principe du dipôle magnétique
De prime abord, on associe la création d'un champ magnétique à un déplacement de particules chargées, c'est-à-dire à des courants. On dispose ainsi de lois (loi de Biot et Savart ou théorème d'Ampère) qui permettent d'établir la cartographie de champ magnétique, connaissant les courants. Le problème est que la seule approche par les courants limite beaucoup l'étude des "objets magnétiques", entendons par là, des objets créant un champ magnétique. En effet, les aimants courants ne sont pas des circuits électriques dans lesquels on fait parcourir un courant qu'on peut quantifier. De plus, si l'on pourrait modéliser un tel comportement par des mouvements microscopiques (mouvement orbital des électrons par exemple, cf. TD), les ordres de grandeurs montrent que cette modélisation est insuffisante pour caractériser la majorité des phénomènes magnétiques dans la matières. On doit admettre deux points:

* La matière peut créer des champs magnétiques (ex: les aimants) dont l'origine n'est pas forcément lié à un déplacement __physique__ de charges, même microscopique.
* Que le champ magnétique créé par des matériaux magnétiques soit lié à un mouvement (microscopique ou macroscopique) ou à une "autre cause" (...), les distances caractéristiques mises en jeu permettent de supposer que les champs "qui nous intéressent" sont souvent créés à grandes distances de la cause.



### Approximation dipolaire. Carte de champ magnétique
````{important} __Définition : Approximation dipolaire__

Soit un champ magnétique créé par un dispositif particulier (aimant, circuit, phénomène microscopique...) situé autour d'un point O. On se place dans le cadre de l'approximation dipolaire si l'on considère que le point M où l'on calcule/étudie le champ magnétique est "loin" du dispositif, c'est-à-dire que la distance OM est grande devant la taille caractéristique L du dispositif.

````

````{admonition} Exemples
:class: tip, dropdown


* Soit une spire de rayon 1cm parcourue par un courant I. On pourra se placer dans le cadre de l'approximation dipolaire si l'on considère des point M situé à une distance OM >>1cm (on pourra prendre O au centre de la spire).
* Soit un atome constitué d'électrons tournant autour du noyau. Ce sont des particules chargées en mouvement qui créent donc un champ magnétique. On peut définir un "rayon" de l'atome comme une zone au sein de laquelle est confiné (dans une vision classique) l'électron. A une distance d grande devant ce rayon, on pourra considérer qu'on est dans le cadre de l'approximation dipolaire.
* Le cas d'un aimant droit est particulier, car ce sont en réalité des phénomènes microscopiques qui sont à l'origine du magnétisme de l'aimant. Même si l'aimant est grand, l'échelle mise en jeu dans les phénomènes magnétiques est très petite, c'est pourquoi on arrive à se placer dans le cadre de l'approximation dipolaire à des distances qui paraissent petites devant la taille de l'aimant.


````

````{important} __Fondamental : Champ magnétique dans le cadre de l'approximation dipolaire__

Dans le cadre de l'approximation dipolaire, les dispositifs magnétiques, possèdent malgré leur grande variété de réalisation des cartes de champs de forme relativement similaire. On pourra distinguer plusieurs "classes de dispositifs" :

* les monopôles magnétiques... qui n'existent en réalité pas (plus précisément, on n'en connaît pas même si la théorie quantique prévoit qu'ils peuvent exister).
* les dipôles magnétiques: ce sont les plus courants
* les quadripôles magnétiques, les octopôles magnétiques... (on peut augmenter le nombre de pôles mais toujours par paire).


````
````{dropdown} Remarque

De cette présentation relativement abstraite, retenons pour l'instant deux points:

* les dipôles sont les cas de figure les plus couramment rencontrés (pour nous en tout cas).
* on fait apparaître la notion de "pôles" d'un dispositif magnétique


````

#### Cas du dipôle magnétique.
Malgré la grande diversité des dipôles magnétiques, le champ magnétique créé __dans le cadre de l'approximation dipolaire__ est toujours le même. 


````{panels}
```{figure} ./images/em_carte_champ_dipole_magnetostatique.jpg
:name: fig_dipole_magneto
:align: center
Dipôle magnétostatique
```
---

```{important} Fondamental : Champ magnétique créé par un dipôle magnétique
A un dipôle magnétique, on peut associer un __moment dipolaire magnétique__ $\overrightarrow{M}$ tel que le champ magnétique créé en un point P par le dipôle situé au point O dans le cadre de l'approximation dipôlaire s'écrit:
\begin{equation}
\overrightarrow{B}(M) = \frac{\mu_0}{4 \pi} \frac{3 (\overrightarrow{M} \cdot \overrightarrow{r}) \overrightarrow{r} - r^2 \overrightarrow{M}}{r^5}
\end{equation}
avec $\overrightarrow{r} = \overrightarrow{OP}$
```

La carte de champ fait apparaître deux lobes partant du point O où se trouve le dipôle et une orientation communes des lignes de champs. Le moment dipolaire $\overrightarrow{M}$ qu'on place généralement à l'endroit où se trouve le dipôle donne l'orientation des lignes de champ. Les lignes de champ partent du pôle nord magnétique et arrivent au pôle sud magnétique.
````

Les dipôles magnétiques regroupent un ensemble de dispositifs très variés (matériau aimanté droit, circuit parcouru par un courant...) à différentes échelles (microscopiques ou macroscopiques) dont le champ magnétique créé à grande distance (approximation dipolaire) possèdent la même géométrie et dont l'intensité et l'orientation peut être définie simplement à l'aide d'une grandeur: le moment dipolaire (vectoriel).


````{admonition} Exemple : Cas d'une spire circulaire
:class: tip, dropdown

On considère une spire circulaire de rayon $R$ parcourue par un courant $I$. A une distance $r >> R$ du centre de la spire, on peut considérer qu'on se place dans le cadre de l'approximation dipolaire. Le moment magnétique de la spire est:
$$
\overrightarrow{M} = \pi R^2 I \overrightarrow{n}
$$

où $\overrightarrow{n}$ est le vecteur normal à la spire orienté en cohérence avec le sens de l'intensité $I$ orientée dans le circuit. On peut réécrire cette expression sous la forme:

$$
\overrightarrow{M} = I \overrightarrow{S}
$$

où $\overrightarrow{S}$ est le vecteur surface associé à la spire (\ref{enc:enc_vecteur_surface_et_moment_dipolaire_d_un_circuit}).

````

````{dropdown} Complément : Vecteur surface

Pour un contour fermé $\Gamma$, on définit le vecteur surface $\overrightarrow{S}$ associé par:

\begin{equation}
\overrightarrow{S} = \iint_{S(\Gamma)} \overrightarrow{dS}
\end{equation}

soit la somme des vecteurs surfaces de chaque petit morceau de la surface $S(\Gamma)$ définie par le contour. Ces éléments sont orientés soit arbitrairement, soit --- très souvent --- en cohérence avec l'orientation du contour (règle du tire-bouchon).

Si dans le cas général, le calcul de $\overrightarrow{S}$ peut être relativement complexe, __on ne retiendra que__ le cas simple d'une surface plane. Alors:

\begin{equation}
\overrightarrow{S} = S \overrightarrow{n}
\end{equation}

où S est la surface délimité par le contour et $\overrightarrow{n}$ le vecteur normal à la surface dans le sens en cohérence avec l'orientation du contour s'il y en a.
````

````{important} __Fondamental : Spire plane de forme quelconque (Admise)__

Soit une spire plane parcourue par une intensité $I$. On note $\overrightarrow{S}$ le vecteur surface orienté en cohérence avec l'intensité $I$. Le moment dipolaire magnétique de la spire dans le cadre de l'approximation dipolaire est:

\begin{equation}
\overrightarrow{M} = I \overrightarrow{S}
\end{equation}

````

#### Cas d'un "multi-pôles" (HP)
```{figure} ./images/em_quadrupolechamp.jpg
:name: fig_multipole
:align: center
Exemple de carte de champ de multipôles
```

### Origine et ordre de grandeur du moment magnétique
Le magnétisme possède deux origines:

* Le mouvement "physique" des particules chargées.
* Le spin $\overrightarrow{S}$ des particules chargées: c'est une grandeur purement quantique qui possède les mêmes comportements mathématiques qu'un moment cinétique (on parle d'ailleurs de moment cinétique intrinsèque) mais qui ne correspond pas physiquement à un mouvement de rotation observable de la particules (les échelles sont trop petites pour pouvoir encore parler de trajectoire).


#### Echelle microscopique. Moment cinétique et moment magnétique
A l'échelle microscopique, les électrons sont en mouvement autour du noyau. Le mouvement créé donc un champ magnétique propre. Le mouvement des électrons est un mouvement orbital autour du noyau, on peut donc lui associer un moment cinétique orbital par rapport au noyau.

````{important} __Fondamental : Moment cinétique orbital et moment magnétique__

Un mouvement orbital d'une particule chargée engendre un moment magnétique $\overrightarrow{m_L}$ proportionnel à son moment cinétique orbital $\overrightarrow{L}$. Le coefficient de proportionnalité est appelé rapport gyromagnétique.

````

````{tip} __Exercice : Rapport gyromagnétique de l'électron dans un atome__

Déterminer le rapport gyromagnétique de l'électron dans un atome en orbite circulaire de rayon $R$ à la vitesse $v$.

````

````{tip} __Exercice : Modèle de Bohr de l'atome.__

On considère un atome dans le modèle de Bohr: les électrons réalisent des orbites circulaires dont le moment cinétique total est quantifié: $\left \| \overrightarrow{L}\right \| = n \hbar$. Montrer que le moment magnétique de l'atome est quantifié est peut se mettre sous la forme $\left \| \overrightarrow{M}\right \| = n \mu_B$. $\mu_B$ est appelé magneton de Bohr.

````

````{important} Fondamental : Spin

A l'échelle microscopique, le moment magnétique total est causé par le moment cinétique orbital ET le moment cinétique intrinsèque aux particules (appelé spin) $\overrightarrow{S}$. On parle de moment cinétique total $\overrightarrow{J}$:

\begin{equation}
\overrightarrow{J} = \overrightarrow{L} + \overrightarrow{S}
\end{equation}

On peut alors associer au spin, un moment magnétique de spin proportionnel $\overrightarrow{m_S} = g \gamma \overrightarrow{S}$ où $\gamma$ est le rapport gyromagnétique et $g$ un facteur de correction appelé facteur de Landé. Le moment magnétique total de la particule vec $\overrightarrow{m} = \overrightarrow{m_S} + \overrightarrow{m_L}$

````

````{admonition} Exemple : Facteurs de Landé
:class: tip, dropdown

Pour l'électron $g=2$, pour le proton, $g=5.586$ et pour le neutron $g=-3.826$

````

````{dropdown} Remarque

Le moment magnétique de spin se superposant au moment magnétique orbital, la mesure de $\overrightarrow{m}$ ne permet pas de dissocier les deux. Plusieurs expériences sur l'aimantation des matériaux (expériences de Einstein et Haas ou expérience de Barnett) ont permis de mesurer $\overrightarrow{m}$. On observa alors que celui-ci possédait une valeur double du moment magnétique orbital qui était celui attendu par la mécanique classique (dans le cas de l'électron). Si ce ne sont pas ces expériences qui ont poussé à l'introduction du spin, elle ont montré que le seul moment orbital ne suffisait pas à expliquer le magnétisme dans la matière.

````

Le moment cinétique orbital des électrons n'a pas de raison d'être identique dans deux atomes différentes: en pratique, ce sont surtout ses valeurs extrêmes qui vont varier d'un atome à un atome, (se reporter aux nombres quantiques en chimie). Au contraire, le spin, est intrinsèque à la particules. Autrement dit, il sera toujours le même, quelque soit l'environnement de la particules (d'où la dénomination de moment cinétique intrinsèque). De plus, il est quantifié, c'est-à-dire qu'il ne peut prendre que des valeurs discrètes.

````{admonition} Exemple : Spin de l'électron
:class: tip, dropdown

Le spin de l'électron ne peut valoir que $- \hbar/2$ ou  $\hbar/2$

````





#### Echelle macroscopique. Aimantation
Les effets magnétiques à l'échelle macroscopique sont dues:

* A des circuits électriques parcourus pas des courants. Il est nécessaire de faire circuler des forts courants sur des longs bobinages pour créer de forts champs magnétiques. Cela rend de tels dispositifs délicats à créer (effet Joule, pression magnétique...).
* A l'accumulation de dipôles magnétiques. En effet, le champ magnétique total est la résultante de l'action de chaque moment magnétique (attention, c'est une somme vectoriel !). Dans le cadre de l'approximation dipolaire, on peut considérer que l'ensemble de moments magnétiques se situent approximativement au même endroit, loin de l'endroit où l'on calcul le champ magnétique. Il suffit donc de calculer le moment magnétique total en les sommant.



````{important} Définition : Moment magnétique total. Cas discret

A l'échelle microscopique ou en considérant un ensemble discret de dipôle magnétique $\overrightarrow{m_i}$ regroupées. Le moment magnétique total s'écrit :

$$
\overrightarrow{m_{Total}} = \sum\limits_{i} \overrightarrow{m_i}
$$

````

````{important} Définition : Aimantation

A l'échelle mésoscopique, on peut considérer que la matière --- y compris --- les dipôles magnétiques forment un ensemble continu. Pour un volume infinitésimal, la notion d'uniformité reste valable. On va donc définir une grandeur intensive associée au moment magnétique: l'aimantation $\overrightarrow{M}$. Elle est définie comme la quantité de moment magnétique par unité de volume. Pour un volume $d \tau$:

\begin{equation}
\overrightarrow{dm_{Total}} = \overrightarrow{M} d \tau
\end{equation}
````

````{dropdown} Remarque

Approche statistique: On peut définir le moment magnétique moyen $\left\langle \overrightarrow {m} \right\rangle$ dans un volume $d \tau$ et le nombre $n$ d'atomes ou molécules par unité de volume possédant un moment magnétique. On aura:

$$
\overrightarrow{dm_{Total}} = \overrightarrow{M} d \tau = n \left\langle \overrightarrow {m} \right\rangle d \tau
$$

````

#### Différents types de matériaux
Le fait que la somme précédente soit vectorielle implique une possibilité d'avoir une aimantation nulle à l'échelle macroscopique, autrement dit un matériau non aimanté. A l'inverse si l'aimantation est non nulle, le matériau sera aimanté. Il créé alors un champ magnétique.

Partons de l'échelle microscopique. A cette échelle, les atomes et molécules possèdent un grand nombre d'électrons en orbite et leur moment magnétique se somment. Dans la plupart des atomes, les moments magnétiques résultant de tous les moments magnétiques orbitaux et intrinsèques s'annulent, il n'y a donc pas d'aimantation au repos à l'échelle microscopique comme macroscopique. A l'inverse, certains matériaux possèdent un moment magnétique résultant non nul qui peut donc créer une aimantation à l'échelle macroscopique (mais pas forcément).

Deux effets s'opposent :

* Si l'on impose un champ magnétique sur un dipôle magnétique, il tend à s'orienter dans le sens du champ magnétique. Il vient qu'un ensemble de dipôles vont avoir tendance à s'aligner les uns avec les autres augmentant ainsi l'aimantation totale (cela minimise l'énergie potentielle totale).
* L'agitation thermique tend à désordonner la matière donnant ainsi aux moments magnétiques une orientation aléatoire et donc à annuler l'aimantation.

La compétition entre les deux effets s'expriment par le facteur de Boltzmann. On a donc trois cas:

* Il n'y a de toute façons pas d'aimantation à l'échelle microscopique, donc pas plus à l'échelle macroscopique. On parle de matériaux __diamagnétiques__.
* L'agitation thermique est trop forte et empêche l'organisation de la manière. L'aimantation au repos est alors très faible (négligeable) et le matériau n'est pas aimanté au repos. On parle de matériaux __paramagnétiques__.
* Les interactions dipolaires sont suffisamment fortes pour prendre le pas sur l'agitation thermique. Une aimantation permanente à grande échelle peut alors exister. On parle de matériaux __ferromagnétiques__. C'est grâce à ces matériaux qu'on créer des aimants permanents.

````{dropdown} Remarque

Cette compétition montre que si l'on augmente suffisamment la température, un matériau ferromagnétique va se désaimanter et devenir paramagnétique. C'est ce qu'on observe [en pratique (lien externe)](http://www.canal-u.tv/video/tele2sciences/temperature_de_curie_du_fer.8992). L'effet est assimilable à une transition de phase. La température de transition de phase est appelée température de Curie. $T_{Curie}(Fer)=770 ^{\circ}C$.

````

````{tip} Exercice : Fer à température ambiante (Recherche)

A température ambiante, le fer est un matériau ferromagnétique. Il ne crée pourtant pas forcément un champ magnétique permanent. Pourquoi?

````

#### Effet d'un champ (excitation) magnétique extérieur(e)
Si l'on place un matériau dans un champ magnétique extérieur (on parle d'excitation magnétique), son aimantation va réagir (à cause des forces magnétiques). L'évolution de l'aimantation va dépendre du type de matériaux:

* Dans tous les matériaux, l'application d'une excitation magnétique va créer un phénomène d'induction. Ce phénomène suit une loi de modération, c'est-à-dire que l'aimantation créé va s'opposer à l'excitation pour créer diminuer le champ total. On parle de __diamagnétisme__. Ce phénomène (création d'un aimantation opposée) est de très faible amplitude.
* Dans les matériaux paramagnétiques et ferromagnétiques, l'application d'une excitation magnétique tend à aligner les moments dipolaires existants dans le sens de l'excitation magnétique, augmentant le champ magnétique total. Ce phénomène est alors bien plus important que le phénomène de modération qui devient négligeable. On peut donc aimanter ces matériaux. La différence notoires entre matériaux paramagnétiques et ferromagnétiques et que les premiers ne gardent pas une aimantation lorsque éteint l'excitation magnétique alors que les seconds conservent une aimantation permanente (effet mémoire, on parle d'hystérésis).


#### Champ magnétique terrestre
L'origine du champ magnétique terrestre est délicate à expliquer. On sait qu'il est dû au noyaux ferreux de la Terre mais les températures énormes sont bien au-delà de la température de Curie. C'est la partie extérieure du noyau, sous forme de fer liquide qui permet, grâce aux mouvements de convection de générer le champ magnétique terrestre. On parle de dynamo auto-excitée car le champ magnétique créé tend à créer des courants qui vont eux-mêmes induire un champ magnétique dans le même sens que le champ excitateur. Ce champ est primordial pour la vie sur Terre car il dévie les particules dangereuses issues du soleil. L'intensité moyenne du champ terrestre est $5 \times 10^{-5} \rm{T} = 0.5 \rm{gauss}$.

Un modèle dipolaire pour le champ magnétique terrestre en surface est un modèle descriptif relativement correct (à 80%). Si l'on veut être plus précis, on peut procéder à un "développement multipolaire" en décrivant ce champ comme un dipôle auquel se superpose un quadripôle, auquel se superpose ... A noter que la structure du champ n'est pas constante (les "pôles" se sont ainsi inversées une centaine de fois en 80 millions d'années). Au passage, le pôle Sud magnétique est à l'heure actuelle proche du pôle Nord géographique et inversement.


## Travaux dirigés

````{tip} __Exercice : Symétrie__

Reprendre les distributions de courant données dans [le cours sur les symétries](exemple_dist) et déterminer:
* les symétries des courants
* les symétries des champs magnétiques
* un maximum d'information sur l'orientation du champ magnétique, la dépendance de ses composantes en les coordonnées et la parité des composante.

On choisira le type de repère de manière réfléchi quand il n'est pas donné.
````

````{tip} __Exercice : Lecture d'une carte de champ__

Trois fils infinis longs et parallèles entre eux sont parcourus par des courants $I_1,I_2$ et $I_3$. Les lignes de champ sont représentées sur la carte ci-dessous. On rappelle que le champ magnétique créé par un fil infini s'écrit:

\begin{equation}
\overrightarrow{B(M)} = \frac{\mu_0 I}{2 \pi M_0 M} \overrightarrow{e_{\theta,M/fil}}
\end{equation}

où $M_0$ est le projeté de M sur le fil et $\overrightarrow{e_{\theta,M/fil}}$ est le vecteur orthoradiale associé au point M dans un système de coordonnées cylindriques d'axe le fil orienté.

```{figure} ./images/Electromagnetisme_TD1_EX1_1.jpeg
:name: fig_td1_ex1_carte_champ
:align: center
Carte de champ dans un plan perpendiculaire à l'axe des fils.
```


1. Déterminer le signe de $I_1,I_2$ et $I_3$.
1. Que peut-on dire de $I_1$ et $I_2$?
1. Quelle est la valeur du champ $\overrightarrow{B}$ en A ? En déduire une estimation du rapport $I_3/I_2$.
1. On sait que le champ en M vaut 0,01 T. Estimer la valeur du champ en P.
````

````{tip} _Exercice : Moments magnétiques intrinséque et moment d'inertie.__

On considère un électron qu'on représente sous la forme d'un corpuscule sphérique de charge totale e et de rayon R en rotation autour de son diamètre; son moment cinétique est $\sigma = s \hbar = s \frac{h}{2 \pi}$ où $h = 6.63 \times 10^{-34} \rm{J.s}$ est la constante de Planck.

Le moment d'inertie d'un boule de masse  uniformément répartie sur son axe est $J = \frac{2}{5} m_E R^2$.

1. Déterminer son moment magnétique en supposant la charge uniformément répartie en surface. 
1. Calculer l'énergie cinétique et la vitesse à la périphérie. Commenter. On donne $s = 1/2; R = 2.8 \times 10^{-15} \rm{m}; m_e = 9.1\times 10^{-31} \rm{kg}$.
````

````{tip} __Exercice : Générer un champ tournant. Double bobinage__

1. On considère deux bobines longues qui pourront être assimilées à des bobines infinies quant au  champ magnétique qu'elles créent. Ces deux bobines sont disjointes et leurs axes forment un angle de $90 ^{\circ}$ (on ne s'intéressera pas ici à la manière de réaliser en pratique une telle configuration). Les deux bobines sont parcourus par des courants sinusoïdaux de même amplitude $I_0$, de même pulsation $\omega$ mais déphasé de $\pi/2$. Montrer que le champ magnétique résultant est un champ tournant dont on déterminera les caractéristiques.
````

````{tip} __Exercice : (Recherche) Matériau ferromagnétique__

1. A partir du magnéton de Bohr, proposer un modèle et une estimation permettant de déterminer le champ maximal d'un aimant droit composé de Fer à proche distance. Comparer aux valeurs trouvées.
````