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
# Actions d'un champ magnétique. Forces de Laplace 

## Position du problème (en ligne)
````{topic} Observations

* Action d'un aimant sur un autre aimant: Il n'y a pas de mouvement --- en tout cas visibles à l'échelle macroscopique et pourtant, comme on l'a précisé, l'interaction est d'origine magnétique.
* Action d'un aimant sur un circuit: Un circuit est localement neutre et c'est l'ensemble du circuit qui est déplacé par le champ magnétique, pas seulement les charges en mouvement.


L'action d'un champ magnétique se généralise à tout objet magnétique par l'étude de l'action d'un champ à des ensemble des particules (pour nous des solides) composant le solide. On pourra distinguer de prime abord deux types d'actions:

* l'action d'un champ magnétique sur un circuit fermé.
* l'action d'un champ magnétique sur un dipôle magnétique.

Fort heureusement, cette action, ayant pour origine la même interaction fondamentale, aura les mêmes caractéristiques dans les deux cas. On parlera de __force de Laplace__.
```{note} Remarque

On définit normalement la force de Laplace comme l'action d'un champ magnétique sur un circuit parcouru par une intensité. On peut alors généraliser les caractéristiques de son action sur un dipôle magnétique au moyen d'une moyen du dipôle en terme de circuit électrique --- on a vu qu'une spire, dans l'approximation dipolaire était considérée comme un dipôle magnétostatique.

```
````

## Force de Laplace

### Modélisation générale. Action sur un circuit

````{important} __Définition : Force de Laplace sur un élément infinitésimal__

Soit un circuit $\Gamma$ parcouru par une intensité I plongé dans un champ magnétique $\overrightarrow{B}$. Le champ magnétique exerce une action sur le circuit global appelé force de Laplace. Chaque petit élément $\overrightarrow{dl}$ en un point M du circuit subit une force:

$$
\overrightarrow{dF}(M) = I \overrightarrow{dl} \wedge \overrightarrow{B}(M)
$$

````

```{margin} Remarque

On rappelle qu'on doit définir la force ET le moment résultant. Comme on a défini les forces appliquées sur chaque "point" du circuit, on peut calculer ces deux éléments.
```
````{important} __Fondamental : Action résultante sur un circuit__

La résultante de toute les actions sur chaque point du circuit sera:

$$
\overrightarrow{F}(\Gamma)= \oint_{M \in \Gamma} I \overrightarrow{dl}(M) \wedge \overrightarrow{B}(M)
$$
Le moment résultant en un point A sera:

$$
\overrightarrow{M}_{A}(\overrightarrow{F}(\Gamma))= \oint_{M \in \Gamma} \overrightarrow{AM} \wedge (I \overrightarrow{dl}(M) \wedge \overrightarrow{B}(M))
$$

````

````{topic} __Exercice : Les forces de Laplace travaillent__  

1. Pourquoi est-ce surprenant que les forces de Laplace travaillent?
1. Dans un morceau de conducteur parallélépipèdique parcouru par une intensité I (sur sa longueur), déterminer l'influence qualitative d'un champ magnétique B sur la trajectoire des charges.
1. Information: si deux parois sont chargées par des charges opposées, il se crée un champ électrique entre les deux parois dirigés de la paroi négatives vers la paroi positive. Montrer qu'alors, le réseau "fixe" du circuit subit une force qui le déplace dans la direction attendue par les forces de Laplace.
1. Expliquer pourquoi dans ces conditions, les forces de Laplace peuvent "indirectement" travailler.

```{note} Remarque

La déformation du nuage électronique de conduction implique un travail interne dû à l'interaction entre le réseau atomique cristallin et les électrons de conduction. Il existe des modèles permettant de traiter cette interaction comme le modèle de Drüde. On pourrait même montrer qu'en régime stationnaire (I=cste), cette force dérive d'un potentiel! L'énergie potentielle associée en régime stationnaire est proportionnelle à l'opposé du flux du champ magnétique à travers le circuit. Il vient qu'un circuit en régime stationnaire aura tendance à se déplacer et s'orienter de manière à maximiser le flux du champ magnétique à travers lui.

```
````

### Champ magnétique uniforme. Action résultante sur un circuit indéformable


* __Principe de traitement:__ l'utilisation des forces de Laplace permet de traiter le circuit comme un solide.
* __Position du problème:__ On considère un circuit fermé $\Gamma$ dans un champ magnétique uniforme $\overrightarrow{B_0}$. On traitera successivement les trois cas suivants: 
    * __Cas A:__ Le circuit est quelconque (à une maille) et parcouru par une intensité I quelconque et pouvant varier.
    * __Cas B:__ Le circuit est quelconque (à une maille) et parcouru par une intensité I constante (on parlera de régime stationnaire).
    * __Cas C:__ Le circuit est une spire rectangulaire parcouru par une intensité I constante.
Dans tous les cas, on se place dans l'ARQS, c'est-à-dire que l'intensité est la même en tout point du circuit. 

#### Résultante des forces
````{important} __Fondamental : Force de Lapalce résultante. Champ uniforme__

Généralisation (Cas A): Dans tous les cas, la résultante des actions d'un champ magnétique uniforme est nulle. Elle ne provoque donc pas de translation globale (déplacement du centre d'inertie).

````

````{important} __Démonstration__

>\begin{align*}
\overrightarrow{F}(\Gamma)&= \oint_{M \in \Gamma} I \overrightarrow{dl}(M) \wedge \overrightarrow{B}(M)\\
&= I\underbrace{(\oint_{M \in \Gamma} \overrightarrow{dl}(M))}_{0} \wedge \overrightarrow{B_0}\\
&=0
\end{align*}
````

#### Moment résultant des forces de Laplace en un point O fixe
````{important} __Fondamental : Moment de Laplace résultante. Champ uniforme__

Généralisation (Cas A --- Admis): Pour un circuit quelconque de moment magnétique $\overrightarrow{M}$, l'action d'un champ magnétique uniforme $\overrightarrow{B_0}$ est un couple dont le moment est $\overrightarrow{M} \wedge \overrightarrow{B_0}$

````

````{topic} Démonstration
```{figure} ./images/em_spire_moment.jpg
:name: fig_spire_moment
:align: center
```
>
>Nous ne prouvons cette expression que dans le cas C, c'est-à-dire pour une géométrie particulière. C'estle seul cas où la preuve est à connaître.
>
>Prenons un système de coordonnées cartésiennes d'axe Ox et Oy parallèles aux côtés du carré et d'axe Oz perpendiculaire au plan de la spire. On oriente Oz de sorte que $\overrightarrow{M} = Ia^2 \overrightarrow{e_z}$. On pose $\overrightarrow{B_0} = B_{0x} \overrightarrow{e_x} + B_{0y} \overrightarrow{e_y} + B_{Oz} \overrightarrow{e_z}$.
>
>La résultante des forces est nulle, donc on peut choisir le point où l'on calcule le moment des forces de Laplace. On choisit le point O au centre du carré. On distingue le calcul du moment sur chaque côté du carré:
>* __Segment AB:__ $\overrightarrow{dl} = dx \overrightarrow{e_x}$; $\overrightarrow{OM} = x \overrightarrow{e_x} - \frac{a}{2} \overrightarrow{e_y}$ donc:
>\begin{align*}
\overrightarrow{M_{AB}} &= \int_{-a/2}^{a/2} (x \overrightarrow{e_x} - \frac{a}{2} \overrightarrow{e_y}) \wedge (I dx \overrightarrow{e_x}) \wedge (B_{0x} \overrightarrow{e_x} + B_{0y} \overrightarrow{e_y} + B_{Oz} \overrightarrow{e_z})\\
&= \int_{-a/2}^{a/2} (x \overrightarrow{e_x} - \frac{a}{2} \overrightarrow{e_y}) \wedge (I dx B_{0y} \overrightarrow{e_z} - I dx B_{Oz} \overrightarrow{e_y})\\
&= \int_{-a/2}^{a/2} \left(-I x(B_{0y}\overrightarrow{e_y} + B_{0z}\overrightarrow{e_z}) - I \frac{a}{2} B_{0y} \overrightarrow{e_x}\right) dx\\
&= -I \frac{a^2}{2} B_{0y} \overrightarrow{e_x}
\end{align*}
>
>* __Segment BC:__ $\overrightarrow{dl} = dy \overrightarrow{e_y}$; $\overrightarrow{OM} = \frac{a}{2} \overrightarrow{e_x} +y \overrightarrow{e_y}$ donc:
>\begin{align*}
\overrightarrow{M_{AB}} &= \int_{-a/2}^{a/2} (\frac{a}{2} \overrightarrow{e_x} +y \overrightarrow{e_y}) \wedge (I dy \overrightarrow{e_y}) \wedge (B_{0x} \overrightarrow{e_x} + B_{0y} \overrightarrow{e_y} + B_{Oz} \overrightarrow{e_z})\\
&= I \frac{a^2}{2} B_{0x} \overrightarrow{e_y}
\end{align*}
>
>* __Segment CD:__ $\overrightarrow{dl} = -dx \overrightarrow{e_x}$; $\overrightarrow{OM} = x \overrightarrow{e_x} + \frac{a}{2} \overrightarrow{e_y}$ donc:
>\begin{align*}
\overrightarrow{M_{AB}} &= \int_{-a/2}^{a/2} (x \overrightarrow{e_x} + \frac{a}{2} \overrightarrow{e_y}) \wedge (-I dx \overrightarrow{e_x}) \wedge (B_{0x} \overrightarrow{e_x} + B_{0y} \overrightarrow{e_y} + B_{Oz} \overrightarrow{e_z})\\
&= -I \frac{a^2}{2} B_{0y} \overrightarrow{e_x}
\end{align*}
>
>* __Segment DA:__ $\overrightarrow{dl} = -dy \overrightarrow{e_y}$; $\overrightarrow{OM} = -\frac{a}{2} \overrightarrow{e_x} +y \overrightarrow{e_y}$ donc:
>\begin{align*}
\overrightarrow{M_{AB}} &= \int_{-a/2}^{a/2} (-\frac{a}{2} \overrightarrow{e_x} +y \overrightarrow{e_y}) \wedge (-I dy \overrightarrow{e_y}) \wedge (B_{0x} \overrightarrow{e_x} + B_{0y} \overrightarrow{e_y} + B_{Oz} \overrightarrow{e_z})\\
&= I \frac{a^2}{2} B_{0x} \overrightarrow{e_y}
\end{align*}
>
>En sommant, il vient:
>\begin{align*}
\overrightarrow{\Gamma} &= -I a^2 B_{0y} \overrightarrow{e_x} + I a^2 B_{0x} \overrightarrow{e_y}\\
 &= I a^2 \overrightarrow{e_z} \wedge \overrightarrow{B_0}\\
 &= \overrightarrow{M} \wedge \overrightarrow{B_0}
\end{align*}
````

#### Puissance des forces de Laplace

````{important} __Fondamental : Puissance des forces de Laplace. Circuit à $I$ constant__

Généralisation (Cas B --- Admis): Pour un circuit quelconque de moment magnétique $\overrightarrow{M}$ constant (c'est-à-dire que le circuit n'est pas déformable ET que l'intensité est constante) dans un champ uniforme $\overrightarrow{B_0}$, les forces de Laplace dérivent d'un potentiel et l'énergie potentielle associée est: $E_{PL} = - \overrightarrow{M} \cdot \overrightarrow{B_0}$.

__Cette propriété n'est PAS vraie dans le cas A où l'intensité varie.__

````

### Si le champ n'est pas uniforme (HP - en ligne)
````{topic} Cas non uniforme
La résultante des forces n'est plus nulle. Dans le cas général, le moment des forces est différent et la force ne dérive pas d'un potentiel. Néanmoins, si le champ varie lentement devant la taille du circuit (cas semblable à l'approximation dipolaire), le moment et la puissance des forces reste globalement valables (circuit indéformable) et on peut même trouver une expression (HP) à la résultante des forces.

* (Admis) Dans un champ magnétique non uniforme mais variant lentement, un circuit filiforme indéformable tend à se déplacer dans les zones de plus fort champ magnétique et à s'orienter suivant le champ magnétique.
````

### Action sur un dipôle magnétique 
Les affirmations précédentes lorsque le champ n'est pas uniforme font apparaître les cas "où le champ varie sur des distances grandes devant la taille du circuit". Cela correspond à considérer la taille du circuit comme très petite, soit se placer dans le cadre de l'approximation dipolaire. Ainsi, la majorité des résultats trouvés précédemment vont se généraliser à un dipôle magnétique quelconque dans le cadre de l'approximation dipolaire.

````{important} __Fondamental : Action des forces de Laplace sur un dipôle magnétique -Champ uniforme__


* La résultante des forces de Laplace est nulle.
* Le moment des forces de Laplace s'écrit:

$$
\overrightarrow{\Gamma} = \overrightarrow{M} \wedge \overrightarrow{B}
$$

Si le dipôle est rigide (c'est-à-dire $\overrightarrow{M} = cste$), alors la force dérive d'un potentiel et $E_{PL} = - \overrightarrow{M} \cdot \overrightarrow{B}$ 

````

### Utilisation des forces de Laplace (en ligne)

````{topic} Moteur synchrone
Une machine synchrone est un dispositif permettant de transformer:

* soit un apport d'énergie électrique alternatif en une énergie cinétique --- un mouvement de rotation: on parle de moteur.
* soit un mouvement (rotation) en un signal électrique alternatif: on parle d'alternateur.

Une machine synchrone est composée de deux parties:

* un stator, élément... statique!, composé de plusieurs bobinages reliées à une source électrique (cas moteur) ou un réseau récepteur (alternateur). Ces bobinages sont décalées d'un même angle les uns par rapport aux autres. En général, une machine asynchrone fonctionne avec des courants triphasés et le stator est composé de 3 bobinages écartés d'angle de $120 ^{\circ}$ (on pourrait le réaliser avec 2 bobinages seulement).
* un rotor, élément... en rotation!, composé d'aimants permanents ou de bobinage alimenté par un courant continu. Le principe est qu'il peut-être représenté par un dipôle magnétique (ou dans les cas réels par un multipôle magnétique, mais le principe est le même) en rotation autour d'un axe.


En fonctionnement moteur, les bobinages du stator sont alimentés en régime triphasé, c'est-à-dire qu'il sont soumis à la même tension sinusoïdal de pulsation $\omega$ mais déphasées successivement de $2 \pi /3$. Les intensités circulant dans les bobinages (normalement identiques) permettent ainsi de superposer trois champs magnétiques dont la résultante est assimilable à un champ magnétique tournant à une vitesse angulaire correspondant à la pulsation du signal triphasé.

Interprétation: On a vu qu'un dipôle magnétique tendait à s'aligner sur le champ magnétique. Comme celui-ci est tournant, le rotor va tourner à la même vitesse (vitesse de synchronisme) que le champ magnétique.
````

### Méthode : Action d'un champ magnétique uniforme sur un circuit déformable

```{figure} ./images/em_rail_laplace.jpg
:name: fig_rail_laplace
:align: center
Rails de Laplace
```
Position du problème: Nous allons étudier l'effet des forces de Laplace sur un circuit pouvant se déformer. Le circuit en question est appelé "rails de Laplace".

Soit deux rails conducteurs parallèles distants d'une distance a. On repère les points des rails sur un axe Ox. Au point $x=0$, on a relié à chaque rail un générateur qui délivre une tension E constante. Au point $x=x_0$, on place une tige conductrice de masse m qui joint les deux rails. Sa vitesse initiale est suivant Ox et vaut $v(t=0)=v_0$. L'ensemble est plongé dans un champ magnétique   créé par un aimant.

Hypothèse de modélisation:

* Le champ magnétique créé par l'aimant est uniforme et suivant l'axe normal au plan du circuit électrique ainsi réalisé. On a choisit de l'orientation comme suivant le schéma.
* La résistance totale du circuit formé est notée R et ne dépend pas de la position de la barre.
* On néglige le champ magnétique propre au circuit devant celui créé par l'aimant.
* La barre glisse sans frottements sur les rails



````{tip} __Exercice : Etude du mouvement de la barre__  

1. Justifier qualitativement que la barre se déplace.
1. Expliquer pourquoi, suivant le signe de E, le circuit va s'agrandir ou se rétrécir.
1. Exprimer, pour une vitesse $v(t)$, la puissance reçue par la barre par l'intermédiaire des forces de Laplace.
1. Si le mouvement dure suffisamment longtemps, on constate expérimentalement que la barre tend vers une vitesse constante, même en diminuant au maximum les frottements. Cette observation est-elle cohérente la seule connaissance de la force de Laplace?
````

## Travaux dirigés
````{tip} __Exercice : Définition de l'Ampère__

L'unité Ampère est définie comme l'intensité circulant dans deux fils infinis situé à une distance de 1m telle que la force exercée par un fil un unité de longueur (1m) de l'autre fil soit égale à $2.10^{-7} \rm{N}$.

1. Retrouver la valeur de cette force au moyen des formules données du champ magnétique créé par un fil infini.
1. Commenter le caractère attractif/répulsif de la force d'interaction suivant les sens de parcours des intensités.
````

````{tip} __Exercice : Equilibre d'un losange conducteur__

```{figure} ./images/Electromagnetisme_TD2_EX2_1.jpeg
:name: fig_td2_ex2_losange
:align: center

```
On considère un circuit formé de 4 tiges rigides de masses m et de longueur a. Le circuit, fermé est parcouru par un courant i constant. Le point supérieur est fixé sur un plafond fixe dans un référentiel galiléen. Le point inférieur est contraint à ne pouvoir bouger que sur un axe verticale fixe. Ce mouvement s'effectue sans frottements. L'ensemble du losange ne peut que se translater sur lui-même. L'ensemble est placé dans un champ de pesanteur uniforme vers le bas et dans un champ magnétique dirigé suivant la normale au plan du losange.

1. Etudier les positions d'équilibre du système et leur stabilité par une étude énergétique. On admettra que la force de Lapalce dérive d'une énergie potentielle dont l'expression est $Ep = - I \Phi$ où $\Phi$ est le flux du champ magnéique à travers le losange.
````

````{tip} __Exercice : Pression magnétique sur un supraconducteur__

Un supraconducteur est un conducteur dans lequel le champ magnétique est imposé nul. En présence d'un champ magnétique extérieur $\overrightarrow{B_0}$, des courants de surfaces $\overrightarrow{j_S}$ (une densité surfacique de courant) apparaissent sur le conducteur de manière à annuler le champ magnétique intérieur. Ces courants sont données par la relation "de passage" :

$$
\overrightarrow{B_{ext}} - \overrightarrow{B_{int}} = \mu_0 \overrightarrow{j_S} \wedge \overrightarrow{n_{int \rightarrow ext}}
$$

où: $\overrightarrow{B_{ext}}$ est le champ à l'extérieur du supraconducteur, $\overrightarrow{B_{int}}$ est le champ à l'intérieur du supraconducteur et $n_{int \rightarrow ext}$ est le vecteur normale au point de la surface où l'on évalue les courants orienté de l'intérieur vers l'extérieur. On considère un supraconducteur occupant toute la partie $x>0$ (infini suivant y et z). L'espace $x<0$ est plongé dans un champ magnétique uniforme: $\overrightarrow{B_0} = B_0 \overrightarrow{e_z}$.

1. Justifier sans calculs que les courants surfaciques créés ne vont pas dépendre de y et z.
1. Montrer que $\overrightarrow{j_S} = \frac{B_0}{\mu_0} \overrightarrow{e_y}$.
1. On considère une portion de surface du supraconducteur infinitésimale dS d'extension dy et dz. Exprimer l'intensité qui circule dans ce petit élément de surface. 
1. En déduire la force surfacique de Laplace exercée par le champ magnétique sur la surface du supraconductrice. Commetner le terme utilisé de pression magnétique.
````

````{tip} __Exercice : Interaction entre un aimant et une spire__

Un dipôle magnétique de moment $\overrightarrow{M_1} = M_1 \overrightarrow{u_z}$ est situé en un point $O_1$. Une spire circulaire $S_2$, de rayon $R_2$, parcourue par un courant $i_2$ constante, a son centre $O_2$ situé sur l'axe $O_1 z$. La distance $O_1 O_2$ est égale à $d$,l'axe de la spire est suivant $\overrightarrow{e_z}$. On considère $R_2 << d$.

1. Déterminer la force de Laplace exercée par le dipôle sur la spire en utilisant la formule du champ magnétique créé par un dipôle magnétique donnée dans le cours.
1. En utilisant le moment magnétique de la spire $S_2$, retrouver l'expression précédente.
````

````{tip} __Exercice : Pression magnétique sur un conducteur__

On considère une bobine longue assimilable à un solénoïde infini de rayon R. On l'assimile à un cylindre très fin parcouru par une densité surfacique de courant $\overrightarrow{j_S} = j_S \overrightarrow{e_{\theta}}$.

1. Déterminer l'intensité qui circule à travers une longueur de 1m de solénoïde.
1. En comparant le résultat trouvé à celui qu'on trouverait pour un solénoïde composé de n spires jointives par unité de longueurs, déterminer le champ magnétique créé par la bobine.
1. Déterminer la force surfacique (appelée pression magnétique) exercée par le champ magnétique sur la bobine.

L'expression trouvée ici est générale à la pression exercée par un champ magnétique qui est nul sur l'une des deux surfaces d'un conducteur (surfaciques évidemment).
[resume]
1. Au Laboratoire National des Champs Magnétiques Intenses (Toulouse), on réalise des bobines non destructives (c'est-à-dire qu'elles ne sont pas détruites après la génération du champ magnétique) pouvant aller jusqu'à 80T. Déterminer la pression magnétique subit par le bobinage. Commenter.
````