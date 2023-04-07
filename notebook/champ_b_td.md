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

````{tip} __Exercice : Lecture d'une carte de champ__

Trois fils infinis longs et parallèles entre eux sont parcourus par des courants $I_1,I_2$ et $I_3$. Les lignes de champ sont représentées sur la carte ci-dessous. On rappelle que le champ magnétique créé par un fil infini s'écrit:

$$
\overrightarrow{B(M)} = \frac{\mu_0 I}{2 \pi M_0 M} \overrightarrow{e_{\theta,M/fil}}
$$

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