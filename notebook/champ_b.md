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

### Observations (en ligne)

````{topic} Observations
On observe différents cas d'influence d'objets sur d'autres dont l'action ne correspond pas à des forces déjà présentées en mécanique:

* Une bobine parcourue par un courant peut dévier un jet d'électrons
* De même un aimant peut dévier un jet d'électrons
* Un aimant peut entraîner le déplacement d'un autre aimant ou d'un circuit parcouru par un courant

```{margin}
Il est évident que les actions réciproques à celle citées existent aussi.
```

Malgré la diversité des actions envisagées, leur étude peut-être modélisée de la même manière: on va introduire un intermédiaire entre la cause (aimant ou circuit électrique) et la conséquence (mouvement d'un aimant/déviation de particules chargées). Cet intermédiaire est le __champ magnétique__. Son unité sera le __Tesla (T)__.

```{figure} ./images/em_action_magnetique.jpg
:name: fig_champ_magnetique
:align: center
Introduction de l'intermédiaire "champ magnétique"
```
````


### Interprétation en terme de champ magnétique
````{important} __Champ magnétique__

Soit une particule chargé de charge $q$ en un point M possédant une vitesse $\overrightarrow{v}$. L'action, appelée force de Lorentz, d'un circuit parcouru par un courant ou d'un aimant peut-être modélisée par une force dont l'expression mathématique est:

$$
\overrightarrow{F} = q \overrightarrow{v} \wedge \overrightarrow{B}(M)
$$

où $\overrightarrow{B}(M)$ est un champ vectoriel dont les caractéristiques ne dépendent que du circuit ou de l'aimant. On l'appelle champ magnétique et son unité est le Tesla (T). M est le point où se trouve la particule de charge $q$.

````

````{topic} Notion de champ magnétique

Comme on le verra par la suite, l'action d'un champ magnétique se généralisera à des dispositifs globalement neutres comme d'autres circuits électriques ou d'autres aimants. On parlera alors de force de Laplace.

La notion de champ peut paraître très abstraite. Elle est pourtant cruciale. Pour comprendre sa première utilité, on peut faire le parallèle avec le champ de gravitation. Si son intervention n'est pas nécessaire pour calculer la force exercée par une masse sur une autre masse, sa définition permet de découplé l'étude de la cause (première masse) de la seconde. On peut donc ainsi travailler sur l'action d'un champ de gravitation donné (qu'on pourra même déterminer expérimentalement) sur une particule massique, un corps solide... sans se soucier de ce qui le crée. Pour le champ magnétique, c'est le même principe. Vu la diversité des façons de créer un champ magnétique, son intervention est encore plus utile. De plus, des études plus poussées en électromagnétisme montrerait que cet outils a pris aujourd'hui une place prépondérante dans des domaines comme la théorie des champs.
````

## Cartes de champ magnétiques

### Lignes de champ. Caractérisation expérimentale

````{important} __Ligne de champ magnétique__

Une ligne de champ magnétique est une courbe avec laquelle le champ magnétique est colinéaire en tout point de la-dite courbe.

````

```{figure} ./images/em_fil_infini.jpg
:name: fig_fil_infini
:align: center
Exemple : Carte de champ pour un fil infini
```
```{figure} ./images/Electromagnetisme_1_Deuxfils.jpg
:name: fig_deux_fils_champ_b
:align: center
Exemple : Carte de champ de deux fils. L'intensité est identique dans les deux fils mais n'est pas dans le même sens: elle sort de la feuille pour le fil de gauche et entre dans la feuille pour le fil de droite
```
```{figure} ./images/em_carte_champ_dipole_magnetostatique.jpg
:name: fig_dipole_magneto_aimant
:align: center
Exemple : Carte de champ pour un petit aimant droit
```
```{figure} ./images/Electromagnetisme_1_Spire_Solene.jpg
:name: fig_spire_solen_champ_b
:align: center
Champ magnétique pour une spire circulaire et une bobine longue.
```

````{admonition} Exemple : Bobine infinie (à connaitre)
:class: tip

On peut montrer que le champ magnétique est nulle à l'extérieur du solenoïde et uniforme à l'intérieur:

$$
\overrightarrow{B} = \mu_0 n I \overrightarrow{e_z}
$$

où n est le nombre de spire par unité de longuer, I l'intensité qui parcourt les spires et $\overrightarrow{e_z}$ le vecteur axial __orienté en cohérence__ avec I.
````

```{topic} Matérialisation expérimentale

Les aimants, sur des liaisons pivots quasi-parfaites ou de la limaille de fer aura tendance à l'aligner le long des lignes de champ: on peut ainsi caractériser les lignes de champ magnétiques.
```

### Caractéristiques générales

* Principe de symétrie (cf. suite)
* Orientation du champ proche du circuit: règle du tire-bouchon basé sur l'intensité.
* Le champ en un point donné sera proportionnelle à l'intensité I qui circule dans le circuit.
* En un point où deux lignes se croisent, le champ est nécessairement nul.
* Une ligne de champ qui boucle sur elle-même enlace nécessairement des courants. Le sens total de parcours des courants enlacés (calculés comme une somme algébrique) peut-être déterminé par la règle du tire-bouchon.

````{margin}
Ce dernier point est un aspect qualitatif d'un théorème utile pour calculer un champ magnétique créé par une distribution de courant: le théorème d'Ampère (cf. deuxième année).
````

### Conservation du flux du champ magnétique

````{topic} Rappel : Orientation d'une surface

* En géométrie vectorielle, une surface plane est orientée par un vecteur appelé vecteur surface dont la norme est égale à l'aire de la surface considérée et l'orientation est perpendiculaire à la surface.

    * Cette définition se généralise facilement à une surface non plane par une approche différentielle. On "découpe" la surface en des surfaces infinitésimales $\overrightarrow{dS}$ qui sont approchables par des surfaces planes. Le vecteur surface totale est la somme de tous les vecteurs surfaces considérés (ici une intégrale sur une surface).
* _Sens d'orientation d'une surface non fermée_: Soit une surface $\Sigma$ délimitée par un contour $\Gamma$ orienté. La surface est alors orientée par convention en cohérence avec le contour $\Gamma$ en appliquant la règle du tire-bouchon (ou du bonhomme d'Ampère).
   * Cette convention d'orientation fonctionne dans les deux sens. On peut très bien orienter le contour de la surface à partir de l'orientation de la surface elle-même. 
* _Sens d'orientation d'une surface fermée_: Soit une surface $\Sigma$ fermée, on oriente la surface, par convention, __vers l'extérieur__.
````

````{important} __Flux du champ magnétique__

Soit un champ vectoriel $\overrightarrow{B}(M)$ définit en tout point M de l'espace et une surface $\Sigma$ quelconque orientée décomposée en un ensemble de surface plane infinitésimale $\overrightarrow{dS}$. On définit le flux du (pseudo-)vecteur $\overrightarrow{B}$ à travers $\Sigma$ comme l'intégrale:

$$
\Phi = \int_{M \in \Sigma} \overrightarrow{B}(M) \cdot \overrightarrow{dS}(M)
$$

````

````{important} __Conservation du flux du champ magnétique__
Le flux du champ magnétique est conservé, c'est-à-dire qu'il est toujours nul à travers une surface fermée.
````

````{important} Cas d'un tube de champ

```{margin}
C'est cette application qui explique le terme de "conservation du flux".
```

Un tube de champ est une surface fermée, orientée de l'intérieur vers l'extérieur, constituée d'une surface latérale ($S_L$) uniquement formée de lignes de champ et de deux surfaces quelconques ($S_1$) et ($S_2$) la fermant à ses extrémités.

```{figure} ./images/em_tube_champ.jpg
:name: fig_tube_de_champ_magn_tique
:align: center
Tube de champ magnétique
```

Le flux du champ magnétique à travers un tube de champ se ramène au seul flux à traversd la surface $(C_1)$ et la surface $(C_2)$ (car $\overrightarrow{dS} est perpendiculaire aux lignes de champ sur la surface latérale). La conservation du flux du champ magnétiques s'écrit donc ($\overrightarrow{dS_1}$ et $\overrightarrow{dS_2}$ sont orientés dans le même sens):

$$
\iint_{M \in C_1} \overrightarrow{B}_1 (M) \cdot \overrightarrow{dS_1} = \iint_{M \in C_2} \overrightarrow{B}_2 (M) \cdot \overrightarrow{dS_2}
$$
````

````{important} __Conséquence de la conservation du flux__
```{margin}
Les réciproques de ces affirmations sont aussi vraies (influence de l'intensité du champ sur la section du tube de champ associé).
```

* Lorsque les lignes de champ magnétique se resserrent, l'intensité du champ magnétique augmente.
* Lorsque les lignes de champ magnétique s'écartent, l'intensité du champ magnétique diminue.
* Si les lignes de champ forme un tube de section constant, alors le champ est uniforme.

````

### Créer un champ magnétique uniforme (en ligne)

````{topic} Champ magnétique uniforme
Si l'on ne peut créer un champ magnétique uniforme dans tout l'espace, on peut par contre créer un champ magnétique dont les variations (intensité ET orientation) sont relativement faibles sur une zone donnée. On utilise généralement deux dispositifs:

* les bobines de Helmoltz: ce sont deux spires parallèles et coaxiales de rayon R distantes de R. On peut montrer que le champ magnétique au milieu des bobine varie peu.
* une bobine longue: on peut montrer que le champ magnétique est globalement uniforme à l'intérieur de la bobine tant qu'on reste loin des bords.
````

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

#### Exemples de distribution (en ligne)
(exemple_dist)=
````{topic} Exemples de distribution

__Distribution linéique__  
* Un fil infini parcouru par une intensité I
* Une spire circulaire de rayon $R$ parcouru par une intensité $I$.
* Une bobine de longueur infini constitué de spire circulaire de rayon $R$ et d'épaisseur négligeable jointives parcouru un courant $I$. On donne en général le nombre de spire par unité de longueur $n$

__Distribution volumique__  
* Un cylindrique infini de rayon $R$ parcouru par une distribution volumique $\overrightarrow{j_v}(M) = j_0 \overrightarrow{e_z}$. C'est la modélisation du fil infini en tenant compte de l'épaisseur du fil (en supposant la distribution homogène).

__Distribution surfacique__
* Nappe de courant : Une bande infinie de large $L$, d'épaisseur négligeable. On note $Ox$ l'axe normal à la nappe et $Oy$ l'axe correspondant à l'axe (infini) de la bande. Si la conduction a lieu suivant $Oy$, on la décrira par une distribution surfacique $\overrightarrow{j_s}(M) = j_0 \overrightarrow{e_y}$ (cas d'une distribution homogène des courant sur la nappe).
````


### Notions de symétries et d'invariance

#### Invariance
````{margin}
En pratique, les invariances que nous rencontreront  seront associée à une indépendance vis-à-vis d'une coordonnée.__
````
```{important} __Invariance__

Soit une transformation de l'espace $\mathcal{T}$. On dit qu'elle laisse invariante un champ scalaire $C(M)$ si et seulement si pour tout point M' image des points M de l'espace, $C(M) =C(M')$.
```

_On distingue principalement les invariances par translation et par rotation_.

#### Symétrie et anti-symétrie planaire d'un vecteur
````{important} __Symétrie planaires__
Soit un plan $\Pi$. On dit que le champ vectoriel $\overrightarrow{j}(M))$ présente une symétrie par rapport à $\Pi$ si et seulement si pour tout point M' image de M par rapport à $\Pi$, $\overrightarrow{j}(M')$ est symétrique de $\overrightarrow{j}(M)$ par rapport à $\Pi$
````

````{important} __Antisymétrie planaires__

Soit un plan $\Pi$. On dit que le champ vectoriel $\overrightarrow{j}(M))$ présente une anti-symétrie par rapport à $\Pi$ si et seulement si pour tout point M' image de M par rapport à $\Pi$, $\overrightarrow{j}(M')$ est l'antisymétrique de $\overrightarrow{j}(M)$ par rapport à $\Pi$, c'est-à-dire que $\overrightarrow{j}(M')$ est _l'opposé_ du symétrique de $\overrightarrow{j}(M)$.
````

````{margin}
Ces propriétés ne s'appliquent quà des points SUR les plans de symétrie/d'antisymétrie.
````
```{important} __Conséquence sur l'orientation du champ magnétique__

* __En tout point M d'un plan de symétrie d'un champ de vecteur'__, le champ magnétique est __contenu__ dans le plan.
* __En tout point M d'un plan d'antisymétrie d'un champ de vecteur__, le champ magnétique est __perpendiculaire__ au plan.
```


#### Symétrie et anti-symétrie planaire d'un pseudo-vecteur
````{margin}
Un pseudo-vecteur est en général issu d'un produit vectoriel entre deux vecteurs.
````
Les pseudo-vecteur sont des éléments mathématiques possédant les mêmes caractéristiques que les vecteurs (direction, sens, norme ou possibilité de projection dans une base orthonormée) MAIS qui n'auront pas les mêmes propriétés de symétrie. C'est le cas du moment cinétique et surtout __du champ magnétique qui est un pseudo-vecteur.__

````{important} __Symétries  et antisymétries planaires__
Pour un pseudo-vecteur, les plans de symétries et d'anti-symétrie sont inversés.
````
````{margin}
Ces propriétés ne s'appliquent quà des points SUR les plans de symétrie/d'antisymétrie.
````
```{important} __Conséquence sur l'orientation du champ magnétique__

* __En tout point M d'un plan de symétrie du champ magnétique__, le champ magnétique est __perpendiculaire__ au plan.
* __En tout point M d'un plan d'antisymétrie du champ magnétique__, le champ magnétique est __contenu__ dans le plan.
```



### Principe de Curie
```{margin}
Un plan de symétrie n'a pas les mêmes conséquences sur $\overrightarrow{j}(M)$ et sur $\overrightarrow{B}$.
```
````{important} __Principe de Curie__
Lorsque certaines causes produisent certains effets, les éléments de symétrie des causes doivent se retrouver dans les effets produits.
````

## Ordres de grandeurs de champs créés

### Champ magnétique par un aimant droit

* Aimants néodyme: 0,3 à 1 T
* IRM (électro-aimant): 6T
* Champ magnétiue terrestre : $0.5 \times 10^{-5} \rm{T} = 0.5 \rm{gauss}$

### Champ créé par un circuit électrique (en ligne)

````{topic} Théorème d'Ampère (pas à connaître en première année)
La circulation du champ magnétique sur un contour orienté (C) fermé est le produit de $\mu_0$ par la somme algébrique des intensités des courants enlacés par ce contour, les intensités dont l'orientation n'est pas en cohérence avec celle du contour (règle du tire- bouchon) étant changées de signe:

$$
\oint_{(C)} \overrightarrow{B}\cdot \overrightarrow{dl} = \mu_0 \sum\limits_{i} \alpha_i I_i
$$
où $\alpha_i = \pm 1$ suivant que l'intensité $I_i$ est orientée en cohérence avec le contour.
````

## Principe du dipôle magnétique

````{topic} Principe
De prime abord, on associe la création d'un champ magnétique à un déplacement de particules chargées, c'est-à-dire à des courants. On dispose ainsi de lois (loi de Biot et Savart ou théorème d'Ampère) qui permettent d'établir la cartographie de champ magnétique, connaissant les courants. Le problème est que la seule approche par les courants limite beaucoup l'étude des "objets magnétiques", entendons par là, des objets créant un champ magnétique. En effet, les aimants courants ne sont pas des circuits électriques dans lesquels on fait parcourir un courant qu'on peut quantifier. De plus, si l'on pourrait modéliser un tel comportement par des mouvements microscopiques (mouvement orbital des électrons par exemple, cf. TD), les ordres de grandeurs montrent que cette modélisation est insuffisante pour caractériser la majorité des phénomènes magnétiques dans la matières. On doit admettre deux points:

* La matière peut créer des champs magnétiques (ex: les aimants) dont l'origine n'est pas forcément lié à un déplacement __physique__ de charges, même microscopique.
* Que le champ magnétique créé par des matériaux magnétiques soit lié à un mouvement (microscopique ou macroscopique) ou à une "autre cause" (...), les distances caractéristiques mises en jeu permettent de supposer que les champs "qui nous intéressent" sont souvent créés à grandes distances de la cause.
````

### Approximation dipolaire. Carte de champ magnétique
````{important} __Approximation dipolaire__

Soit un champ magnétique créé par un dispositif particulier (aimant, circuit, phénomène microscopique...) situé autour d'un point O. On se place dans le cadre de l'approximation dipolaire si l'on considère que le point M où l'on calcule/étudie le champ magnétique est "loin" du dispositif, c'est-à-dire que la distance OM est grande devant la taille caractéristique L du dispositif.

````

````{topic} Exemples

* Soit une spire de rayon 1cm parcourue par un courant I. On pourra se placer dans le cadre de l'approximation dipolaire si l'on considère des point M situé à une distance OM >>1cm (on pourra prendre O au centre de la spire).
* Soit un atome constitué d'électrons tournant autour du noyau. Ce sont des particules chargées en mouvement qui créent donc un champ magnétique. On peut définir un "rayon" de l'atome comme une zone au sein de laquelle est confiné (dans une vision classique) l'électron. A une distance d grande devant ce rayon, on pourra considérer qu'on est dans le cadre de l'approximation dipolaire.
* Le cas d'un aimant droit est particulier, car ce sont en réalité des phénomènes microscopiques qui sont à l'origine du magnétisme de l'aimant. Même si l'aimant est grand, l'échelle mise en jeu dans les phénomènes magnétiques est très petite, c'est pourquoi on arrive à se placer dans le cadre de l'approximation dipolaire à des distances qui paraissent petites devant la taille de l'aimant.
````

````{topic} Champ magnétique dans le cadre de l'approximation dipolaire

Dans le cadre de l'approximation dipolaire, les dispositifs magnétiques, possèdent malgré leur grande variété de réalisation des cartes de champs de forme relativement similaire. On pourra distinguer plusieurs "classes de dispositifs" :

* les monopôles magnétiques... qui n'existent en réalité pas (plus précisément, on n'en connaît pas même si la théorie quantique prévoit qu'ils peuvent exister).
* les dipôles magnétiques: ce sont les plus courants
* les quadripôles magnétiques, les octopôles magnétiques... (on peut augmenter le nombre de pôles mais toujours par paire).
````

#### Cas du dipôle magnétique.
Malgré la grande diversité des dipôles magnétiques, le champ magnétique créé __dans le cadre de l'approximation dipolaire__ est toujours le même. 


```{figure} ./images/em_carte_champ_dipole_magnetostatique.jpg
:name: fig_dipole_magneto
:align: center
Dipôle magnétostatique
```
```{important} Champ magnétique créé par un dipôle magnétique
A un dipôle magnétique, on peut associer un __moment dipolaire magnétique__ $\overrightarrow{M}$ tel que le champ magnétique créé en un point P par le dipôle situé au point O dans le cadre de l'approximation dipôlaire s'écrit:

$$
\overrightarrow{B}(M) = \frac{\mu_0}{4 \pi} \frac{3 (\overrightarrow{M} \cdot \overrightarrow{r}) \overrightarrow{r} - r^2 \overrightarrow{M}}{r^5}
$$
avec $\overrightarrow{r} = \overrightarrow{OP}$
```

La carte de champ fait apparaître deux lobes partant du point O où se trouve le dipôle et une orientation communes des lignes de champs. Le moment dipolaire $\overrightarrow{M}$ qu'on place généralement à l'endroit où se trouve le dipôle donne l'orientation des lignes de champ. Les lignes de champ partent du pôle nord magnétique et arrivent au pôle sud magnétique.

Les dipôles magnétiques regroupent un ensemble de dispositifs très variés (matériau aimanté droit, circuit parcouru par un courant...) à différentes échelles (microscopiques ou macroscopiques) dont le champ magnétique créé à grande distance (approximation dipolaire) possèdent la même géométrie et dont l'intensité et l'orientation peut être définie simplement à l'aide d'une grandeur: le moment dipolaire (vectoriel).


````{note} __Cas d'une spire circulaire__

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

````{topic} Vecteur surface

Pour un contour fermé $\Gamma$, on définit le vecteur surface $\overrightarrow{S}$ associé par:

$$
\overrightarrow{S} = \iint_{S(\Gamma)} \overrightarrow{dS}
$$

soit la somme des vecteurs surfaces de chaque petit morceau de la surface $S(\Gamma)$ définie par le contour. Ces éléments sont orientés soit arbitrairement, soit --- très souvent --- en cohérence avec l'orientation du contour (règle du tire-bouchon).

Si dans le cas général, le calcul de $\overrightarrow{S}$ peut être relativement complexe, __on ne retiendra que__ le cas simple d'une surface plane. Alors:

$$
\overrightarrow{S} = S \overrightarrow{n}
$$

où S est la surface délimité par le contour et $\overrightarrow{n}$ le vecteur normal à la surface dans le sens en cohérence avec l'orientation du contour s'il y en a.
````

````{important} __Spire plane de forme quelconque (Admise)__

Soit une spire plane parcourue par une intensité $I$. On note $\overrightarrow{S}$ le vecteur surface orienté en cohérence avec l'intensité $I$. Le moment dipolaire magnétique de la spire dans le cadre de l'approximation dipolaire est:

$$
\overrightarrow{M} = I \overrightarrow{S}
$$

````

#### Cas d'un "multi-pôles" (HP - en ligne)

````{topic} Multipoles
```{figure} ./images/em_quadrupolechamp.jpg
:name: fig_multipole
:align: center
Exemple de carte de champ de multipôles
```
````
