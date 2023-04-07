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
# Mouvement de particules chargées
````{topic} Remarque

On a déjà vu en mécanique que des particules chargées pouvaient être soumises à une force particulière: l'interaction électrostatique. Cette interaction résulte simplement d'interactions entre charges qu'elles soient mobiles ou immobiles. En réalité, on observe que pour des particules chargées en mouvement, l'interaction devient plus complexe: on parle d'interaction électromagnétique. Du point de vue classique, cette interaction est regroupée dans ce qu'on appelle la force de Lorentz. Celle-ci permet de décrire de nombreux phénomènes électromagnétiques, notamment quand on s'intéresse à un grand nombre de particules chargées à une échelle pas trop petite. Il apparaît alors que la force de Lorentz dépend de la position relative des charges ainsi que de leur mouvement relatif. Nous allons faire apparaître naturellement deux champs vectoriels: l'un dit électrique en relation avec l'interaction électrique de Coulomb déjà connue et l'autre, en relation avec les interactions de charges en mouvement sera appelé champ magnétique. Le but du cours d'électromagnétisme de première année est de savoir comment calculer ces champs à  partir des données de leur cause: les distributions de positions et de vitesses (= courant électrique) des charges. On peut noter qu'à l'échelle atomique, l'utilisation des champs électromagnétiques demande le passage à la mécanique quantique et la théorie des champs qui n'est évidemment pas au programme de première année.

````

## Influences des particules chargées immobiles et mobiles: force de Lorentz

### Force de Coulomb: Champ électrostatique
#### Interaction entre deux charges statiques

````{important} __Définition : Force électrostatique de Coulomb__

Soit deux particules chargées de charges $q_1$ et $q_2$ située aux points $M_1$ et $M_2$. La charge en $M_1$ exerce sur la charge en $M_2$ une force appelée force électrostatique de Coulomb dont l'expression est:

$$
\overrightarrow{F_{M_1 \rightarrow M_2}} = \frac{q_1 q_2}{4 \pi \epsilon_0} \frac{\overrightarrow{M_1 M_2}}{M_1 M_2^3}
$$

où $\epsilon_0$ est une constante appelée permittivité du vide: $\epsilon_0 = 8.85 \times 10^{-12} \rm{m^{-3}.kg^{-1}.A^{2}.s^{4}}$

````

````{important} __Définition : Champ électrique pour une particule chargée__

Soit une particule chargée située au point P de chargé $q$, on peut définir le champ électrostatique créé par P en un point M quelconque par:

$$
\overrightarrow{E_{q}}(M) = \frac{q}{4 \pi \epsilon_0} \frac{\overrightarrow{PM}}{PM^3}
$$
````

````{topic} Champ et force
Pour une particule chargé de charge q' mise en M, la force exercée par P sur la particule est alors $\overrightarrow{F} = q' \overrightarrow{E_q}(M)$. En faisant le parallèle entre le champ électrostatique et le champ de gravitation, on voit tout de suite l'intérêt de définir cette grandeur.
````

````{topic} __Principe de superposition__
Considérons maintenant une distribution de charge $\{q_i\}$ en des points $\{P_i\}$ distincts. Si une particule chargé $q'$ se trouve en un point M de l'espace. La résultante des forces électriques de tous les points  sur M est la somme de chaque interactions de Coulomb. Il vient:


Le champ électrique créé par une distribution de charge $\{q_i\}$ en un point M donné est la somme des champ créés par chaque charge seule.

````

### Circulation de charge: champ magnétique.

````{important} __Définition : Champ magnétique (Rappel)__

Soit une particule chargé de charge $q$ en un point M possédant une vitesse $\overrightarrow{v}$. L'action d'un champ magnétique $\overrightarrow{B}$ sur la charge $q$ s'écrit:

$$
\overrightarrow{F} = q \overrightarrow{v} \wedge \overrightarrow{B}(M)
$$

````

### Force de Lorentz. Ordre de grandeur
````{important} __Définition : Force de Lorentz__

Si on considère une particule chargé mobile dans un champ électrique et magnétique, il vient alors que ces deux champs exercent une action conjugué électromagnétique appelée force de Lorentz et qui a pour expression:

$$
\overrightarrow{F} = q (\overrightarrow{E} + \overrightarrow{v} \wedge \overrightarrow{B})
$$

````

````{topic} Remarque

A l'échelle macroscopique, cette force tend à décroître rapidement. Cette force devient importante quand:

* on est à très petite échelle, là où les forces de gravitation sont très faibles.
* on a des portions importantes de matières chargées (exemple: billes chargées d'électricité statique)
* quand la matière est organisée d'une certaine manière, le champ magnétique créé peut devenir relativement important: c'est le cas de la magnétite et des matériaux dits ferromagnétiques (les aimants).
* au moyens de circuits électriques parcourus par de forts courants: c'est le cas de grandes spires.


Pour calculer cette force, il faut connaître les champs électriques et magnétiques. Pour l'instant, nous supposerons connus les champs magnétiques et électriques en tout point de l'espace et nous étudierons le mouvement d'une particule chargée dans de tels champs sans forcément en connaître la cause.

Nous supposerons de plus que ces champs sont uniformes. Nous verrons par la suite que pour créer un champ uniforme sur des distances notoires, on peut:

* créer un champ magnétique uniforme dans un solénoïde infini c'est-à-dire dans une zone d'un solénoïde éloignée des bords.
* créer un champ électrique uniforme grâce à des plans infinis, c'est-à-dire en se plaçant suffisamment proche du plan et éloigné des bords. On verra par la suite que le condensateur plan permet de réaliser un tel dispositif.

Cette liste n'est pas exhaustive, on citera aussi les bobines de Helmholtz pour créer un champ magnétique uniforme dans une zone donnée. Sauf contre-indication, on négligera l'action du poids dans tout le chapitre.

````

## Force de Lorentz

### Expression. Principe fondamental de la dynamique
La force dépend de la vitesse et semble donc dépendre du référentiel. Il n'en est rien à condition de se placer dans un cadre de mécanique relativiste. Nous supposerons pour simplifier que tous les mouvements étudiés s'effectuent dans un référentiel galiléen.

__Principe fondamental de la dynamique:__ Appliqué à la particule M de masse m et de charge q, il s'énonce évidemment: 

$$
m \frac{d \overrightarrow{v}}{dt} = q (\overrightarrow{E} + \overrightarrow{v} \wedge \overrightarrow{B})
$$

### Analyse énergétique
__On ne s'intéresse ici qu'à des champs statiques.__

La force magnétique ne travaille pas au contraire de la force électrostatique. C'est-à-dire que le champ magnétique n'agit que sur la direction de la vitesse et non son module. Seul le champ électrostatique peut modifier le module de la vitesse d'une particule.

````{important} __Fondamental : Force électrostatique. Energie potentielle électrostatique (Admise)__

Le champ électrique en régime statique est conservatif: $\overrightarrow{E} = - \overrightarrow{grad} V$ où $V$ est le potentiel électrostatique. La force électrique est donc aussi conservative: l'énergie potentielle électrique sera donc: $E_p = qV$.

````

## Mouvement d'une particule chargée dans un champ électrostatique uniforme

### Applications
````{tip} __Méthode : Accélération de particules__  

On considère deux plaques infinies $P_1$ et $P_2$ distantes d'une distance $d$ et chargées uniformément et portées chacune aux potentiels respectifs $V_1$ et $V_2$. Des particules de charge $q$ sont libérées sans vitesse initiale de la plaque 1. On oriente un axe Ox perpendiculaire aux plaques avec la plaque $P_1$ est en $x=0$. On admet que le champ électrique est uniforme entre les deux plaques et suivant $\overrightarrow{e_x}$: $\overrightarrow{E} = E_0 \overrightarrow{e_x}$.

1. Déterminer son expression en fonction de $V_1,V_2$ et $d$.
1. Montrer que pour que les charges $q$ se dirigent vers la plaque 2, il faut ordonner $V_1$ et $V_2$.
1. Déterminer alors la vitesse des charges quand elles arrivent sur la plaque 2. En déduire que l'expression "on accélère les charges au moyens d'une tension accélératrice U" a un sens (expliquer notamment pourquoi l'hypothèse d'un champ uniforme est inutile).


````

__Généralisation:__
On voit que la simple donnée de la tension accélératrice permet de connaître la variation d'énergie cinétique et donc la vitesse des charges en sortie d'un tel dispositif. Si l'utilisation de plaques est très fréquente, on peut très bien imaginer d'autres systèmes d'accélération.

````{important} __Définition : Electron-volt__

L'électron-volt est une unité énergétique définie comme l'énergie cinétique d'un électron accéléré depuis le repos par une tension de 1V: $1 \rm{eV} = 1.6 \times 10^{-19} J$.
\tcblower{}
Cette unité est très utile à l'échelle microscopique.

````

````{tip} __Méthode : Déviation d'un faisceau électronique__  

On considère maintenant une particule possédant une vitesse $v_0$ perpendiculaire à un champ $\overrightarrow{E}$ uniforme. On suppose que le champ n'est établi que sur distance $d$ et que les particules sont des électrons. A la sortie de la zone de déviation, il n'y a plus de champ électrique et on place un écran à une distance D de la zone sur lequel est repéré l'impact du faisceau électronique.

1. Déterminer la déflexion, c'est-à-dire la position verticale du faisceau sur l'écran.
1. Estimer les tensions de déflexion mise en jeu dans un oscilloscope. Commenter


````

## Mouvement d'une particule chargée dans un champ magnétique uniforme et constant.
Dans toute cette partie, on considère une particule de masse $m$ et de charge $q$ plongée dans un champ magnétique placé suivant l'axe Oz. On suppose qu'il n'y a aucune autre force en jeu.
On peut placer la particule au milieu d'un solénoïde de grande dimension.

### Etude de la trajectoire. Pulsation cyclotron
````{important} Définition : Pulsation cyclotron

On appelle pulsation cyclotron: $\omega_c = \left\vert \frac{qB}{m} \right\vert$. On définit le vecteur associé: $\overrightarrow{\Omega} = - \frac{q \overrightarrow{B}}{m}$.

````
````{important} Fondamental : Caractéristiques générales du mouvement (Admis)

On note $\phi$ l'angle entre la vitesse initiale et le champ magnétique. Le mouvement d'une particule chargée dans un champ magnétique uniforme est uniforme et composée de 2 mouvements:

* un mouvement rectiligne uniforme suivant l'axe du champ magnétique à la vitesse.
* un mouvement circulaire uniforme dans le plan perpendiculaire à $\overrightarrow{B}$. Les caractéristiques de ce mouvement circulaire seront données par la suite.

Le mouvement est donc un mouvement hélicoïdal.

Si la vitesse initiale de la charge est perpendiculaire à $\overrightarrow{B}$ ($\phi = \pi/2$), alors la trajectoire est un cercle contenu dans le plan perpendiculaire au champ magnétique.
````

````{important} Fondamental : Cas du mouvement circulaire plan

Soit une particule de charge $q$ dans un champ magnétique uniforme $\overrightarrow{B}$. Si la vitesse initiale $v_0$ est perpendiculaire à $\overrightarrow{B}$, le mouvement est circulaire. Les caractéristiques du mouvement sont:

* le mouvement est uniforme à la vitesse $v_0$
* la vitesse angulaire est la pulsation cyclotron $\omega_c = \vert \frac{qB}{m} \vert$
* le rayon est $R = \vert \frac{mv_0}{qB} \vert$
* le cercle est parcouru dans le sens en cohérence avec le vecteur $-q\overrightarrow{B}$ (règle du tire-bouchon)
````

````{important} __Démonstration__

>Cette preuve est à connaître. On part du postulat que le mouvement est contenu dans le plan perpendiculaire à $\overrightarrow{B}$.
>
>__Caractère circulaire.__
>
>Remarquons que la force magnétique est toujours perpendiculaire à la vitesse. On va se placer dans le repère de Fresnet puisque la trajectoire est plane. Il vient que :
>* l'accélération tangentielle est nulle donc $\frac{\rm{d}v}{\rm{dt}} = 0$ : le mouvement est uniforme.
>* l'accélération tangentielle s'écrit a pour norme  $qBv$ si on note $v$ la norme de la vitesse (puisque le champ magnétique est perpendiculaire à la vitesse). Il vient qu'elle est constante ($v$ est constante).
>
>De plus, on sait que $a_N = \frac{v^2}{R}$. comme $a_N$ et $v$ sont constant, il vient que le rayon de courbure est constant. __La seule trajectoire plane de rayon de courbure constante est un cercle__ donc la trajectoire est circulaire.
>
>__Relation vitesse et rayon__
>On se place donc dans un système de coordonnées cylindriques d'axe Oz confondu avec $\overrightarrow{B}$: $\overrightarrow{B} = B \overrightarrow{e_z}$.
>
>Avant même de passer à une preuve quantitative, remarquons que:
>
>* Sur un mouvement circulaire uniforme, l'accélération est centripète de sorte que la force magnétique doit être centripète (suivant $-\overrightarrow{e_r}$). Or le trièdre $(\overrightarrow{F}, q \overrightarrow{v}, \overrightarrow{B})$ doit être directe par définitio de la force magnétique. Il vient effectivement que:
>
>* si $q >0$, $\overrightarrow{v}$ est suivant $- \overrightarrow{e_{\theta}}$ soit en cohérence avec $-q\overrightarrow{B}$
>* si $q <0$, $\overrightarrow{v}$ est suivant $ \overrightarrow{e_{\theta}}$ soit en cohérence avec $-q\overrightarrow{B}$
>
>
>
>Le PFD projeté dans la base cylindrique s'écrit:
>\begin{align*}
-m R \dot \theta^2 \overrightarrow{e_r} + m R \ddot \theta \overrightarrow{e_{\theta}} &= q R \dot \theta \overrightarrow{e_{\theta}} \wedge B \overrightarrow{e_z}\\
-m R \dot \theta^2 \overrightarrow{e_r} + m R \ddot \theta \overrightarrow{e_{\theta}} &= q R B \dot \theta \overrightarrow{e_r}
\end{align*}
>
>En projection sur $\overrightarrow{e_{\theta}}$, on retrouve que le mouvement est uniforme ($\ddot \theta = 0$) et en projection sur $\overrightarrow{e_r}$, il vient:
>
>$$
\dot \theta = - \frac{q B}{m}
$$
>soit la pulsation cyclotron en valeur absolue. On a bien $\dot \theta <0$ si $q > 0$ et $\dot \theta >0$ si $q < 0$ soit l'orientation de la trajectoire en cohérence avec $-q \overrightarrow{B}$.
>
>De $v_0 = R \dot \theta$, il vient immédiatement l'expression du rayon.
````


````{margin}
Si le champ magnétique ne peut accélérer les particules (on a vu qu'il ne travaillait pas), il est fort utile pour dévier les faisceaux de particules. C'est par exemple un champ magnétique qui est utilisé dans les anciennes télévisions.
````
````{tip} __Méthode : Déflexion par un champ magnétique__  

On suppose que le champ magnétique n'existe qu'entre y=0 et y=D. Pour un champ $B=0.1\rm{T}$ et un électron dont la vitesse initiale de $2\times10^{7} \rm{m.s^{-1}}$

1. Déterminer la distance D à mettre pour dévier la particule d'un angle $\theta=1,71 ^{\circ}$
2. Quel champ électrique permettrait la même déviation sur la même distance D. Commenter.

````


### Exemple d'utilisation: cyclotron et spectrométrie de masse (en ligne)

````{topic} Le cyclotron
La déviation ainsi obtenue est utilisée  dans le cyclotron. Il s'agit d'un accélérateur de particules chargées qui conjugue les effets des deux champs. Les particules évoluent dans deux demi-cylindre, appelés dees, de rayon R dans lesquels règnent un champ magnétique uniforme perpendiculaire à la face circulaire. Entre les deux dees se trouve  une petite épaisseur dans laquelle règne un champ électrique uniforme mais qui varier au cours du temps (de manière périodique). Après un premier temps de chauffe, les électrons, sortant d'un dee sont accélérés par le champ électrique en direction de l'autre dee. Les particules vont effectuer des demi-cercles dans chaque dee, revenant ainsi dans dans l'espace d'accélération. Entre-temps, le champ électrique a varié et s'est inversé de sorte que les particules vont être à nouveau accélérer. La distance entre les deux dees étant faible devant R, on peut supposer que le champ E est constant durant le passage des particules.

On peut remarquer que le temps entre eux passages dans la zone d'accélération est constant, il vaut la demi-période de rotation calculée précédemment, le champ doit donc avoir une période T, soit une pulsation $\omega_c$. D'où le nom de pulsation cyclotron.

Ainsi, pour une différence de potentiel de 10kV, l'énergie cinétique Ec (en supposant l'énergie nulle au départ) après n passages est: $Ec = nqU$. Il aurait donc fallu une différence de potentiel de $10 * nkV$ pour obtenir la même accélération. Si le champ électrique est le même dans les deux cas, cela signifie un espace n fois plus grand.
````

````{topic} Spectromètre de masse
On peut aussi remarquer que le rayon R dépend de $v_0$ mais aussi de la masse de la particule. C'est cette propriété qui est utilisée dans le spectromètre de masse: en introduisant des particules accélérées toutes à la même vitesse dans un champ magnétique uniforme, on peut séparer des particules chargées de masse différentes.

En général, le spectromètre de masse est couplé avec un dispositif réalisant une chromatographie (liquide ou gazeuse). En couplant le temps de migration dans la colonne de chromatographie avec le point d'arrivée de l'élément dans le collecteur à la sortie du spectromètre, on obtient de nombreuses informations. En les comparant avec les tables, on peut en général déterminer la nature des composés étudiés.
````

### Cas d'un champ magnétique non uniforme. (HP - en ligne)

````{topic} B non uniforme
On s'intéresse ici à des champs magnétiques dont les variations sont faibles.

Commençons par remarquer que dans le cas d'un champ magnétique uniforme le mouvement hélicoïdal se fait sur la surface d'un tube de champ (les lignes de champ étant des droites).

Pour un champ magnétique variant faiblement, on arrive à montrer que les particules vont à nouveaux tourner autour de la direction globale du champ en s'enroulant sur un tube de champ. Si le tube se rétrécit le rayon de l'hélice va se rétrécir et inversement.

Observation: Lorsqu'elles arrivent sur Terre, les particules chargées issues des vents solaires subissent ainsi la déviation par le champ magnétique terrestre. Vers les pôles, elles vont suivre les lignes de champ qui bouclent aux pôles magnétiques. Ces le seul endroits où elles peuvent atteindre la haute atmosphère et leur interaction avec celle-ci créé un phénomène particulier: les aurores boréales.
````

## Entrainement
````{tip} __Exercice : Spectrographe de masse__

```{figure} ./images/Mecanique_TD7_EX1_1.jpeg
:name: fig_spec_masse_td
:align: center
Spectromètre de masse
```

Le principe d’un spectrographe de masse est représenté \cref{fig_spec_masse_td}. Dans un chambre une chambre d’ionisation (1) on produit des ions  de masse m et de charge $q=2e$. Ces ions pénètrent par le trou $T_1$ d’une plaque $P_1$ dans une enceinte (A); leur vitesse en $T_1$ est négligeable. Dans l’enceinte (A), ces ions sont accélérés par une tension $U=V_{P1} - V_{P2}$, puis sortent de (A) par un trou $T_2$ percé dans la plaque $P_2$. Ils pénètrent alors dans une enceinte (D) où règne un champ magnétique B uniforme et constant perpendiculaire au plan de la figure. La vitesse des ions en $T_2$ est notée $v_0$. On néglige le poids.

_Données : $e=1.6 \times 10^{-19} \rm{C}$; $U=4000\rm{V}$; $B=0.1\rm{T}$; unité de masse atomique: $m_0 = 1.67 \times 10^{-27} \rm{kg}$._


1. Exprimer la vitesse $v_0$ en fonction de q, m et U.
1. Préciser le sens de B pour que les ions puissent être recueillis dans la fente O du collecteur (C). Calculer littéralement le rayon R de la trajectoire des ions dans l’enceinte (D).
1. L’élément zinc contient deux isotopes de nombres de masse $A_1=68$ et $A_2 = 70$. On souhaite recueillir en O l’isotope $A_1$. Calculer numériquement la distance $l=T_2 O$ et évaluer la largeur maximale de la fente du collecteur.
````

````{tip} __Exercice : Focalisation par un champ électrique__

```{figure} ./images/Mecanique_TD7_EX2_1.jpeg
:name: fig_focalisation_chp_elec
:align: center

```

Des électrons, préalablement accélérés par une tension V=10kV, pénètrent dans la fente supposée très fine dans une région où règne un champ électrique uniforme $\overrightarrow{E} = E \overrightarrow{e_y}$. On désire recueillir ces électrons à travers une fente B pratiquée dans le plan opaque (xAy), à la distance AB=L=20cm de A. On peut régler l’angle $\alpha$ que fait le vecteur vitesse $\overrightarrow{v_0}$ des électrons en A avec l’axe (Ax), ainsi que la norme et le sens du champ électrostatique E. Le vecteur $v_0$ est supposé parallèle au plan (Oxy).

1. Quelles sont les valeurs optimales à donner à $\alpha$ et E pour réaliser la focalisation de ces électrons, sachant que le faisceau incident présente une faible dispersion angulaire $\Delta \alpha << \alpha$?

````

````{tip} __Exercice : Focalisation par un secteur magnétique__

```{figure} ./images/Mecanique_TD7_EX3_1.jpeg
:name: fig_focalisation_chp_magnetique
:align: center

```

On considère un secteur magnétique d’angle $90 ^{\circ}$ définissant la zone d’action d’un champ magnétique B. permanent et uniforme dans lequel pénètrent des ions positifs monochargés de masse m et accélérés sous une tension de valeur absolue V. On note e la charge élémentaire.

1. Calculer le module de la vitesse $v_0$ des ions à l’entrée du secteur magnétique, en supposant qu’ils sont émis sans vitesse avant l’accélération sous la tension V et préciser le sens de variation du potentiel au cours de l’accélération.
1. Le secteur magnétique est conçu pour une trajectoire circulaire moyenne de rayon R fixée par construction. On notera O le centre de la trajectoire et Oxy le plan du cercle, le secteur magnétique occupant le premier quadrant. Indiquer, en fonction de R, e, m et V, l’expression du champ magnétique correspondant à cette trajectoire.
1. Les ions issus d’une fente A située à une distance d de la face d’entrée du secteur magnétique et forment un faisceau peu dispersé en angle autour de la direction Ax perpendiculaire à la face à la face d’entrée du dispositif. Montrer que, pour un rapport e/m donné qui impose le choix de B, les ions provenant de A dont la vitesse est perpendiculaire à B sont focalisés en un point A’ que l’on déterminera. Peut-on parler de stigmatisme?
````

````{tip} __Exercice : Conduction dans un métal en présence d’un champ magnétique__

L’espace est repéré par les axes cartésiens Ox, Oy, Oz et les vecteurs $(\overrightarrow{u_x}, \overrightarrow{u_y}, \overrightarrow{u_z})$. On s’intéresse ici à la conduction dans un métal assurée par des électrons de charge q=-e, de masse m, de densité n. Le métal est placé dans un champ électrique $\overrightarrow{E} = E_x \overrightarrow{u_x}+E_y \overrightarrow{u_y}+E_z \overrightarrow{u_z}$ et un champ magnétique $\overrightarrow{B} = B \overrightarrow{u_z}$. Ces champs sont uniformes et permanents. L’interaction entre les électrons et les ions fixes du réseau est modélisé par une force de frottement: $\overrightarrow{f} = - \frac{m}{\tau} \overrightarrow{v}$, v étant la vitesse des électrons.

1. Déterminer l’unité de $\tau$.
1. Etablir l’équation différentielle du mouvement d’un électron. Que devient cette équation en régime permanent.
1. On note $j=nqv$ le vecteur densité de courant. Montrer qu’en régime permanent, les composantes de ce vecteur vérifie le système d’équations:
\begin{align*}
j_x - q \tau \frac{B}{m} j_y = \gamma E_x\\
q \tau \frac{B}{m} j_x + j_y  = \gamma E_y\\
j_z = \gamma E_z
\end{align*}
où $\gamma$ est une constante que l’on déterminera.
1. En déduire que l’on peut écrire $j_x$ et $j_y$ sous la forme suivante: $j_x = \gamma (\alpha E_x + \beta E_y)$ et $j_y = \gamma (-\beta E_x + \alpha E_y)$ où $\alpha$ et $\beta$ sont deux constantes à déterminer en fonction des données.
1. Si la conduction ne peut avoir lieu que suivant Ox, montrer que la présence du champ B impose la présence d’un champ électrique (appelé champ de Hall) et déterminer sa direction. Calculer la constante de Hall: $\frac{E_y}{j_x B}$.
````