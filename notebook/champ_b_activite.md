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
# Origine et ordre de grandeur du moment magnétique
Le magnétisme possède deux origines:

* Le mouvement "physique" des particules chargées.
* Le spin $\overrightarrow{S}$ des particules chargées: c'est une grandeur purement quantique qui possède les mêmes comportements mathématiques qu'un moment cinétique (on parle d'ailleurs de moment cinétique intrinsèque) mais qui ne correspond pas physiquement à un mouvement de rotation observable de la particules (les échelles sont trop petites pour pouvoir encore parler de trajectoire).


## Echelle microscopique. Moment cinétique et moment magnétique
A l'échelle microscopique, les électrons sont en mouvement autour du noyau. Le mouvement créé donc un champ magnétique propre. Le mouvement des électrons est un mouvement orbital autour du noyau, on peut donc lui associer un moment cinétique orbital par rapport au noyau.

````{important} __Moment cinétique orbital et moment magnétique__
Un mouvement orbital d'une particule chargée engendre un moment magnétique $\overrightarrow{m_L}$ proportionnel à son moment cinétique orbital $\overrightarrow{L}$. Le coefficient de proportionnalité est appelé rapport gyromagnétique.
````

````{tip} __Exercice : Rapport gyromagnétique de l'électron dans un atome__
Déterminer le rapport gyromagnétique de l'électron dans un atome en orbite circulaire de rayon $R$ à la vitesse $v$.
````

````{tip} __Exercice : Modèle de Bohr de l'atome.__
On considère un atome dans le modèle de Bohr: les électrons réalisent des orbites circulaires dont le moment cinétique total est quantifié: $\left \| \overrightarrow{L}\right \| = n \hbar$. Montrer que le moment magnétique de l'atome est quantifié est peut se mettre sous la forme $\left \| \overrightarrow{M}\right \| = n \mu_B$. $\mu_B$ est appelé magneton de Bohr.
````

````{margin} Facteurs de Landé
Pour l'électron $g=2$, pour le proton, $g=5.586$ et pour le neutron $g=-3.826$
````
````{note} __Spin__

A l'échelle microscopique, le moment magnétique total est causé par le moment cinétique orbital ET le moment cinétique intrinsèque aux particules (appelé spin) $\overrightarrow{S}$. On parle de moment cinétique total $\overrightarrow{J}$:

$$
\overrightarrow{J} = \overrightarrow{L} + \overrightarrow{S}
$$

On peut alors associer au spin, un moment magnétique de spin proportionnel $\overrightarrow{m_S} = g \gamma \overrightarrow{S}$ où $\gamma$ est le rapport gyromagnétique et $g$ un facteur de correction appelé facteur de Landé. Le moment magnétique total de la particule vec $\overrightarrow{m} = \overrightarrow{m_S} + \overrightarrow{m_L}$

````


````{topic} Remarque

Le moment magnétique de spin se superposant au moment magnétique orbital, la mesure de $\overrightarrow{m}$ ne permet pas de dissocier les deux. Plusieurs expériences sur l'aimantation des matériaux (expériences de Einstein et Haas ou expérience de Barnett) ont permis de mesurer $\overrightarrow{m}$. On observa alors que celui-ci possédait une valeur double du moment magnétique orbital qui était celui attendu par la mécanique classique (dans le cas de l'électron). Si ce ne sont pas ces expériences qui ont poussé à l'introduction du spin, elle ont montré que le seul moment orbital ne suffisait pas à expliquer le magnétisme dans la matière.

Le moment cinétique orbital des électrons n'a pas de raison d'être identique dans deux atomes différentes: en pratique, ce sont surtout ses valeurs extrêmes qui vont varier d'un atome à un atome, (se reporter aux nombres quantiques en chimie). Au contraire, le spin, est intrinsèque à la particules. Autrement dit, il sera toujours le même, quelque soit l'environnement de la particules (d'où la dénomination de moment cinétique intrinsèque). De plus, il est quantifié, c'est-à-dire qu'il ne peut prendre que des valeurs discrètes.

Le spin de l'électron ne peut valoir que $- \hbar/2$ ou  $\hbar/2$
````

## Echelle macroscopique. Aimantation (en ligne)

````{topic} Origine macroscopique
Les effets magnétiques à l'échelle macroscopique sont dues:

* A des circuits électriques parcourus pas des courants. Il est nécessaire de faire circuler des forts courants sur des longs bobinages pour créer de forts champs magnétiques. Cela rend de tels dispositifs délicats à créer (effet Joule, pression magnétique...).
* A l'accumulation de dipôles magnétiques. En effet, le champ magnétique total est la résultante de l'action de chaque moment magnétique (attention, c'est une somme vectoriel !). Dans le cadre de l'approximation dipolaire, on peut considérer que l'ensemble de moments magnétiques se situent approximativement au même endroit, loin de l'endroit où l'on calcul le champ magnétique. Il suffit donc de calculer le moment magnétique total en les sommant.

```{note} __Moment magnétique total. Cas discret__

A l'échelle microscopique ou en considérant un ensemble discret de dipôle magnétique $\overrightarrow{m_i}$ regroupées. Le moment magnétique total s'écrit :

$$
\overrightarrow{m_{Total}} = \sum\limits_{i} \overrightarrow{m_i}
$$

```

```{note} __Aimantation__

A l'échelle mésoscopique, on peut considérer que la matière --- y compris --- les dipôles magnétiques forment un ensemble continu. Pour un volume infinitésimal, la notion d'uniformité reste valable. On va donc définir une grandeur intensive associée au moment magnétique: l'aimantation $\overrightarrow{M}$. Elle est définie comme la quantité de moment magnétique par unité de volume. Pour un volume $d \tau$:

$$
\overrightarrow{dm_{Total}} = \overrightarrow{M} d \tau
$$
```
_On a en général recours à une approche statistique._
````


````{topic} Différents types de matériaux
Le fait que la somme précédente soit vectorielle implique une possibilité d'avoir une aimantation nulle à l'échelle macroscopique, autrement dit un matériau non aimanté. A l'inverse si l'aimantation est non nulle, le matériau sera aimanté. Il créé alors un champ magnétique.

Partons de l'échelle microscopique. A cette échelle, les atomes et molécules possèdent un grand nombre d'électrons en orbite et leur moment magnétique se somment. Dans la plupart des atomes, les moments magnétiques résultant de tous les moments magnétiques orbitaux et intrinsèques s'annulent, il n'y a donc pas d'aimantation au repos à l'échelle microscopique comme macroscopique. A l'inverse, certains matériaux possèdent un moment magnétique résultant non nul qui peut donc créer une aimantation à l'échelle macroscopique (mais pas forcément).

Deux effets s'opposent :

* Si l'on impose un champ magnétique sur un dipôle magnétique, il tend à s'orienter dans le sens du champ magnétique. Il vient qu'un ensemble de dipôles vont avoir tendance à s'aligner les uns avec les autres augmentant ainsi l'aimantation totale (cela minimise l'énergie potentielle totale).
* L'agitation thermique tend à désordonner la matière donnant ainsi aux moments magnétiques une orientation aléatoire et donc à annuler l'aimantation.

La compétition entre les deux effets s'expriment par le facteur de Boltzmann. On a donc trois cas:

* Il n'y a de toute façons pas d'aimantation à l'échelle microscopique, donc pas plus à l'échelle macroscopique. On parle de matériaux __diamagnétiques__.
* L'agitation thermique est trop forte et empêche l'organisation de la manière. L'aimantation au repos est alors très faible (négligeable) et le matériau n'est pas aimanté au repos. On parle de matériaux __paramagnétiques__.
* Les interactions dipolaires sont suffisamment fortes pour prendre le pas sur l'agitation thermique. Une aimantation permanente à grande échelle peut alors exister. On parle de matériaux __ferromagnétiques__. C'est grâce à ces matériaux qu'on créer des aimants permanents.

```{note} Remarque

Cette compétition montre que si l'on augmente suffisamment la température, un matériau ferromagnétique va se désaimanter et devenir paramagnétique. C'est ce qu'on observe [en pratique (lien externe)](http://www.canal-u.tv/video/tele2sciences/temperature_de_curie_du_fer.8992). L'effet est assimilable à une transition de phase. La température de transition de phase est appelée température de Curie. $T_{Curie}(Fer)=770 ^{\circ}C$.

```

Si l'on place un matériau dans un champ magnétique extérieur (on parle d'excitation magnétique), son aimantation va réagir (à cause des forces magnétiques). L'évolution de l'aimantation va dépendre du type de matériaux:

* Dans tous les matériaux, l'application d'une excitation magnétique va créer un phénomène d'induction. Ce phénomène suit une loi de modération, c'est-à-dire que l'aimantation créé va s'opposer à l'excitation pour créer diminuer le champ total. On parle de __diamagnétisme__. Ce phénomène (création d'un aimantation opposée) est de très faible amplitude.
* Dans les matériaux paramagnétiques et ferromagnétiques, l'application d'une excitation magnétique tend à aligner les moments dipolaires existants dans le sens de l'excitation magnétique, augmentant le champ magnétique total. Ce phénomène est alors bien plus important que le phénomène de modération qui devient négligeable. On peut donc aimanter ces matériaux. La différence notoires entre matériaux paramagnétiques et ferromagnétiques et que les premiers ne gardent pas une aimantation lorsque éteint l'excitation magnétique alors que les seconds conservent une aimantation permanente (effet mémoire, on parle d'hystérésis).
````

## Champ magnétique terrestre (en ligne)

````{topic} Sur Terre
L'origine du champ magnétique terrestre est délicate à expliquer. On sait qu'il est dû au noyaux ferreux de la Terre mais les températures énormes sont bien au-delà de la température de Curie. C'est la partie extérieure du noyau, sous forme de fer liquide qui permet, grâce aux mouvements de convection de générer le champ magnétique terrestre. On parle de dynamo auto-excitée car le champ magnétique créé tend à créer des courants qui vont eux-mêmes induire un champ magnétique dans le même sens que le champ excitateur. Ce champ est primordial pour la vie sur Terre car il dévie les particules dangereuses issues du soleil. L'intensité moyenne du champ terrestre est $5 \times 10^{-5} \rm{T} = 0.5 \rm{gauss}$.

Un modèle dipolaire pour le champ magnétique terrestre en surface est un modèle descriptif relativement correct (à 80%). Si l'on veut être plus précis, on peut procéder à un "développement multipolaire" en décrivant ce champ comme un dipôle auquel se superpose un quadripôle, auquel se superpose ... A noter que la structure du champ n'est pas constante (les "pôles" se sont ainsi inversées une centaine de fois en 80 millions d'années). Au passage, le pôle Sud magnétique est à l'heure actuelle proche du pôle Nord géographique et inversement.
````