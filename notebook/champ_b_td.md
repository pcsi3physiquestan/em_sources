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
# Entrainement

````{tip} __Exercice : Symétrie__

Reprendre les distributions de courant données dans [le cours sur les symétries](exemple_dist) et déterminer:
* les symétries des courants
* les symétries des champs magnétiques
* un maximum d'information sur l'orientation du champ magnétique, la dépendance de ses composantes en les coordonnées et la parité des composante.

On choisira le type de repère de manière réfléchi quand il n'est pas donné.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Symétrie d'un champ magnétique._


````{tip} __Exercice : Lecture d'une carte de champ__

Trois fils infinis longs et parallèles entre eux sont parcourus par des courants $I_1$ (bas gauche), $I_2$ (bas droite) et $I_3$ (haut centre). Les lignes de champ sont représentées sur la carte ci-dessous.

```{figure} ./images/Electromagnetisme_TD1_EX1_1.jpeg
:name: fig_td1_ex1_carte_champ
:align: center
Carte de champ dans un plan perpendiculaire à l'axe des fils.
```

1. Expliquer pourquoi il était attendu que les lignes de champs soient contenues dans le plan perpendiculaire au fil.
1. Déterminer le signe de $I_1,I_2$ et $I_3$.
1. Que peut-on dire de $I_1$ et $I_2$?
1. Quelle est la valeur du champ $\overrightarrow{B}$ en A ? 
1. Préciser si le champ magnétique sera plus fort autour de P ou de M.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Carte de champ magnétique._
* _$\Longrightarrow$ Symétrie d'un champ magnétique._

````{tip} __Exercice : Générer un champ tournant. Double bobinage__

1. On considère deux bobines longues qui pourront être assimilées à des bobines infinies quant au  champ magnétique qu'elles créent. Ces deux bobines sont disjointes et leurs axes forment un angle de $90 ^{\circ}$ (on ne s'intéressera pas ici à la manière de réaliser en pratique une telle configuration). Les deux bobines sont parcourus par des courants sinusoïdaux de même amplitude $I_0$, de même pulsation $\omega$ mais déphasé de $\pi/2$. Montrer que le champ magnétique résultant est un champ tournant dont on déterminera les caractéristiques.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Champ magnétique d'une bobine longue._

````{tip} _(*)Moments magnétiques intrinséque et moment d'inertie.__

On considère un électron qu'on représente sous la forme d'un corpuscule sphérique de charge totale e et de rayon R en rotation autour de son diamètre; son moment cinétique est $\sigma = s \hbar = s \frac{h}{2 \pi}$ où $h = 6.63 \times 10^{-34} \rm{J.s}$ est la constante de Planck.

Le moment d'inertie d'un boule de masse  uniformément répartie sur son axe est $J = \frac{2}{5} m_E R^2$.

1. Déterminer son moment magnétique en supposant la charge uniformément répartie en surface. 
2. Calculer l'énergie cinétique et la vitesse à la périphérie. Commenter. On donne $s = 1/2; R = 2.8 \times 10^{-15} \rm{m}; m_e = 9.1\times 10^{-31} \rm{kg}$.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Dipôle magnétique._
* _$\Longrightarrow$ Moment magnétique._



````{tip} __Exercice : (Recherche) Matériau ferromagnétique__

1. A partir du magnéton de Bohr, proposer un modèle et une estimation permettant de déterminer le champ maximal d'un aimant droit composé de Fer à proche distance. Comparer aux valeurs trouvées.
````