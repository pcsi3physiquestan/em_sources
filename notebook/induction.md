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
# Induction et application
## Introduction

### Observation expérimentale (en ligne)
````{topic} Observations expérimentales
Expérimentalement, on observe que:

* Un aimant se déplaçant dans une bobine crée une tension aux bornes de la bobine
* Une bobine alimentée se déplaçant dans une autre bobine créée une tension aux bornes de la bobine
* Une bobine alimentée par un courant variable crée dans une bobine l'entourant une tension

Les différentes expériences réalisées montrent la création d'une force électromotrice induite à l'intérieur des différents circuits. Il apparaît que ce phénomène d'induction apparaît lorsque les caractéristiques du champ magnétique vu du circuit sont variables. Une étude quantitative montrerait que le phénomène d'induction est dû à la variation du flux du champ magnétique à travers le circuit.

Par des mesures plus précises, on observe que:

* La tension créé dans la bobine au passage de l'aimant crée un courant qui crée un champ magnétique variable exerçant une force sur l'aimant. Cette force tend à ralentir l'aimant (ou la bobine).
* Dans le cas d'une bobine parcourue par une intensité variable. On observe que la tension induite dans la seconde bobine est variable aussi créant un courant variable dans la bobine. Le champ magnétique ainsi créé est aussi variable et va induire aussi une tension dans la première bobine. Cette tension tend à s'opposer aux variations de l'intensité dans la première bobine.

````

### Loi de Lenz
Dans tous les exemples données (en ligne), l'effet créé par la variation du flux du champ magnétique va lui-même engendrer un effet sur le flux du champ magnétique: cet effet est opposé à la cause initiale: on parle de __loi de modération__.

````{important} __Fondamental : Loi de Lenz__

Un phénomène d'induction suit un loi de modération, c'est-à-dire que l'effet produit tend à s'opposer à la cause qui lui a donner naissance.

````

### Loi de Faraday
````{important} __Fondamental : Loi de Faraday__

Un circuit conducteur $\Gamma$ plongé dans un champ magnétique $\overrightarrow{B}$ est le siège d'une force électromotrice appelée force électromotrice induite: $e = - \frac{d \phi}{dt}$ où $\phi$ est le flux du champ magnétique à travers le circuit (dont la surface est orientée) et la f.e.m. induite est orientée dans le circuit en cohérence avec la surface orientée (règle du tire-bouchon).

````

````{topic} Remarque

Il apparaît clairement dans cette loi la nécessité d'un flux variable. Cela peut se produire de deux façons (qui peuvent être simultanées):

* Le champ magnétique est lui-même variable (on parle d'induction de Neumann)
* Le circuit est mobile ou se déforme dans le champ magnétique (on parle d'induction de Lorentz)

Dans la suite, on ne traitera que des cas où la variation du flux est causé par l'une ou l'autre des configurations, pas les deux en même temps.

Les conventions d'orientation sont primordiales. D'autant que l'on va associer une représentation géométrique des circuits à leur schématisation électrique. Si l'on ne fait pas attention, tous les calculs sera faux et même physiquement aberrants (car la loi de modération de Lenz ne sera plus vérifié).

Une f.e.m. tend à créer (si c'est la seule source) un courant qui circule dans le sens de la f.e.m. (puissance fournie positive), il vient que le champ magnétique induit par ces courants s'opposera à celui initial, on retrouve alors la loi de Lenz. Même si la fermeture du circuit va permettre la circulation d'un courant, il faut bien remarquer que la variation du flux magnétique crée une force électromotrice (tension en quelque sorte). Le courant n'est qu'une cause secondaire.

La situation sur le schéma (à une maille) de la f.e.m. induite n'a pas d'importance. En réalité, il s'agit d'une f.e.m. résultant de l'action du champ magnétique sur l'ensemble du circuit. On pourrait associer à la loi de Faraday une équation locale (équation de Maxwell-Faraday) qui le montrerait en associant le champ magnétique au champ électrique (qui rappelons le est en lien directe avec le potentiel électrique dans un circuit).

````


## Champs variables et circuits fixes

### Principe d'auto-induction
__Position du problème:__ Commençons par remarquer qu'un circuit électrique parcouru par un courant électrique engendre un champ magnétique et donc a priori un flux magnétique non nul à travers le circuit lui-même (on parle de __flux propre__). Si l'intensité qui circule dans le circuit est variable, alors le champ magnétique l'est aussi, donc son flux sera variable. Il devrait donc se produire un phénomène d'induction à travers le circuit, c'est-à-dire qu'une f.e.m. induite devrait s'opposer à la variation du courant (cause initiale). Cela se produit: c'est le __phénomène d'auto-induction__.

````{tip} __Méthode : Cas d'une bobine de grande longueur__  

Soit une bobine de longueur D contenant N spires jointives circulaires de section S parcourues par un courant $i(t)$.

1. Déterminer le flux propre de la bobine, c'est-à-dire le flux du champ magnétique créé par la bobine à travers la bobine elle-même. On assimilera le champ magnétique créé à celui créé par une bobine infinie.
1. Déterminer l'expression de la f.e.m. auto-induite et commenter son expression. Préciser la modélisation électrique du composant et ses caractéristiques.
1. Estimer l'ordre de grandeur de l'inductance ainsi définie pour différentes valeurs de bobines. Commenter.
````

````{topic} Correction

>__On notera l'importance d'un schéma et des conventions d'orientation.__

>
```{figure} ./images/em_auto_inductance.jpg
:name: fig_auto_inductance
:align: center
Plan d'une spire
```
>* Le champ magnétique créé par une bobine infinie s'écrit $\overrightarrow{B} = \mu_0 n I \overrightarrow{e_z}$ avec $\overrightarrow{e_z}$ en cohérence avec le sens de I et $n = \frac{N}{D}$. On choisit d'orienter les surfaces des spires suivant $+ \overrightarrow{e_z}$ (__c'est un choix__). Le flux à travers une spire est donc:
>$$
\Phi_1 = S \overrightarrow{e_z} \cdot \mu_0 n I \overrightarrow{e_z} = \mu_0 I \frac{NS}{D}
$$
>Le flux à travers la bobine complète est donc:
>$$
\Phi = \mu_0 I \frac{N^2 S}{D}
$$
>* En orientant la force électromotrice auto-induite en cohérence avec l'axe Oz (\cref{fig_auto_inductance}), il vient:
>$$
e = - \frac{d \Phi}{dt} = - \mu_0 \frac{N^2S}{D} \frac{dI}{dt}
$$
>On reconnaître l'équation d'évolution d'une inductance avec $L = \frac{\mu_0 N^2 S}{D}$
>* Pour les bobines à air, on a $D \sim 10 \rm{cm}$ et $S \sim 1 \rm{dm^{2}}$ soit $L \sim \times 10^{-7} N^2$. Il faut donc 10 spires pour avoir $L = 1 \rm{mH}$ et près de 3000 spires (sur 10 centimètres) pour avoir $L = 1 \rm{H}$. On pourra remarquer que les ordre de grandeur choisis ici ne valide PAS l'hypothèse d'une bobine longue. Dans ces conditions, le champ magnétiques chute très rapidement et l'inductance diminue aussi. Il est donc très compliqué de créer une bobine à air de forte inductance.
````


````{margin}
En pratique, on oriente cette effet en convention récepteur dans un circuit électrique, ce qui donne les équation d'évolution habituel d'une bobine. On pourra, comme en électrocinétique, conduire des bilans de puissance directement sur le circuit équivalent.

````
````{important} __Définition : Auto-inductance__

Le flux propre d'un composant est toujours proportionnel à l'intensité qui le traverse et la f.e.m. induite est de même proportionnel à la dérivée temporelle de l'intensité. Le facteur de proportionnalité, identique, est appelé inductance (ou plus précisément auto-inductance):

$$
\Phi = L I
$$
La loi de Faraday donne la fem auto-induide: $e = - L \frac{d I}{dt}$ La valeur de l'inductance dépend de la géométrie du circuit.
````


### Induction mutuelle 
__Position du problème:__ Considérons deux bobines longues de même axe. On suppose que l'une est imbriquée dans l'autre, de sorte que l'approximation du champ créé par une bobine infinie reste valable. On note $I_i, D_i, S_i$ et $N_i$ les intensités, longueur, section et nombre de spire de la bobine i.

__Champ propre et champ extérieur:__ Les phénomènes d'induction pour chaque bobine résultent de la superposition du champ magnétique propre à la bobine considéré et du champ magnétique créé par l'autre bobine. Ce dernier phénomène est appelé phénomène d'induction mutuelle. Dans le cas de deux bobines, ces deux champs peuvent être a priori de même ordre de grandeur, on ne peut donc négliger un champ devant l'autre.

````{tip} __Méthode : Flux mutuel entre deux bobines longues coaxiales__  

On suppose le champ magnétique créé par chaque bobine assimilable __dans la bobine__ à celui d'une bobine longue à l'intérieur de la bobine (et est nul à l'extérieur). On pose $D_1 > D_2$ et $S_2 > S_1$. On suppose que les intensités "tournent" dans le même sens en progressant suivant les Oz positifs.

1. Déterminer le flux du champ créé par la bobine 1 dans la bobine 2.
1. Déterminer le flux du champ créé par la bobine 2 dans la bobine 1.
1. En déduire une modélisation électrique de l'ensemble.
1. Que se passe-t-il si on inverse l'enroulement du bobinage 2?


````

````{topic} Correction
>__On rappelle l'importance des conventions d'orientation.__
>
```{figure} ./images/em_induc_mutelle_3d.jpg
:name: fig_induc_mutuelle_3d
:align: center
```
>* On oriente le vecteur surface $\overrightarrow{S}$ dans le sens des z positifs. Le champ magnétique créé par la bobine 1 est $\overrightarrow{B_1} = \mu_0 \frac{N_1}{D_1} I_1 \overrightarrow{e_z}$ à l'intérieur de la bobine 1. Comme cette bobine est plus longue, le champ magnétique est non nul dans chaque spire de la bobine 2. Par contre, le flux magnétique n'est non nul que dans la surface $S_1$ car $S_2 > S_1$. Il vient:
>$$
\Phi_{1 \rightarrow 2} = \mu_0 \frac{N_1 N_2}{D_1} I_1 S_1
$$
>* Le champ magnétique créé par la bobine 2 est $\overrightarrow{B_2} = \mu_0 \frac{N_2}{D_2} I_2 \overrightarrow{e_z}$ à l'intérieur de la bobine 2. Comme cette bobine est plus courte, le champ magnétique n'est non nul pour les spires de la bobine 1 que sur une longueur $D_2$ correspondant à un nombre de spires: $D_2 \frac{N_1}{D_1}$. Par contre, le flux magnétique est non nul sur toute la surcae des spires. Il vient:
>$$
\Phi_{2 \rightarrow 1} = \mu_0 \frac{N_2}{D_2} \frac{D_2 N_1}{D_1} I_2 S_1 = \mu_0 \frac{N_1 N_2}{D_1} I_2 S_1
$$
>* Notons $L_1$ et $L_2$ les auto-inductances de chaque bobine. La loi de Faraday donne:
>\begin{align*}
e_1 = - \mu_0 \frac{N_1 N_2}{D_1} S_1 \frac{d I_2}{dt}\\
e_2 = - \mu_0 \frac{N_1 N_2}{D_1} S_1 \frac{d I_1}{dt}
\end{align*}
>On obtient alors la modélisation \cref{fig_mutuelle_modele}.
>* L'intensité $I_2$ tourne alors dans le sens contrainre à $\overrightarrow{e_z}$. Il vient que $e_1$ change de signe. On peut garder la même expression en changeant de sens la tension (\cref{fig_mutuelle_modele_inv}).
````

```{figure} ./images/em_mutuelle_modele.jpg
:name: fig_mutuelle_modele
:align: center
Cas des intensités tournant dans le même sens
```
```{figure} ./images/em_mutuelle_modele_inv.jpg
:name: fig_mutuelle_modele_inv
:align: center
Cas des intensités tournant dans des sens opposés
```

````{important} __Définition : Inductance mutuelle__

Généralisation (Admise): Soit deux circuits $\Gamma_1$ et $\Gamma_2$ parcourue par des courants d'intensité respectives $I_1$ et $I_2$. Le flux du champ magnétique total à travers le circuit 1 (réciproquement 2) se décompose en deux parties: le flux propre et le flux mutuel. Ce dernier est proportionnel à l'intensité $I_2$ (réciproquement $I_1$). Le coefficient de proportionnalité est appelé coefficient d'inductance mutuelle $M_{2 \rightarrow 1}$ (respectivement $M_{1 \rightarrow 2}$):

\begin{equation}
\begin{bmatrix}
\phi_1\\
\phi_2
\end{bmatrix}
=
\begin{bmatrix}
L_1 & M_{2 \rightarrow 1}\\
M_{1 \rightarrow 2} & L_2
\end{bmatrix}
\begin{bmatrix}
I_1\\
I_2
\end{bmatrix}
\end{equation}

```{topic} Remarque

Les coefficients dépendent la géométrie de chaque circuit et de leur disposition relative. Ils peuvent être négatifs à priori (on peut s'en convaincre en observant ce qui se passe si l'on inverse le sens de branche d'une des bobines dans l'exercice~\ref{exe:exe_flux_mutuel_entre_deux_bobines_longues_coaxiales}: le coefficient d'inductance mutuel est).

```
````

````{important} __Fondamental : Propriété des coefficient d'inductance mutuelle (Admis)__

Ils sont égaux: $M_{2 \rightarrow 1} = M_{1 \rightarrow 2}$. On les notera $M$ par la suite.

````

````{important} __Définition : Circuits en influence totale__

Deux circuits sont dits en influence totale si le flux total du champ magnétique à travers le premier circuit correspond au flux total traversant le second circuit (les deux circuits s'appuie sur le même tube de champ). 

````

````{important} __Fondamental : Inductance mutuelle de circuit en influence totale__

Lorsque deux circuits sont en influence totale, $M = \sqrt{L_1 L_2}$. L'inductance mutuelle entre les deux circuits est alors maximale.
````

````{topic} Remarque

Avoir une inductance mutuelle maximale est extrêmement intéressant car dans ces conditions, le premier circuit exerce une influence maximale par induction sur le second (et réciproquement). En général, on utilise l'inductance mutuelle pour transmettre une information ou de l'énergie. Dans les deux cas, l'influence totale permet de minimiser les pertes. Lorsqu'il n'y a pas influence totale, le transfert d'énergie n'est pas maximale, cela correspond à une fuite des lignes de champ magnétique.

````

### Bilan énergétique

````{important} __Fondamental : Energie emmagasinée__

L'énergie totale emmagasinée par deux bobinages en influence mutuelle de coefficient M est:

$$
E_{mag} = \frac{1}{2}L_1 I_1^2 + \frac{1}{2}L_2 I_2 ^2 + M I_1 I_2
$$

````

````{topic} Démonstration
>__Démonstration :__ Considérons le système complet constitué des deux bobines. La puissance reçue par la bobine 1 s'écrit: $P_1 = i_1 (L_1 \frac{di_1}{dt} + M \frac{di_2}{dt})$. De même la puissance reçue par la bobine 2 s'écrit: $P_2 = i_2 (L_2 \frac{di_2}{dt} + M \frac{di_1}{dt})$. La puissance totale reçue s'écrit donc:
>\begin{align*}
P &= L_1 i_1 \frac{di_1}{dt} + L_2 i_2 \frac{di_2}{dt} + M (i_1 \frac{di_2}{dt} + i_2 \frac{di_1}{dt})\\
& = \frac{d}{dt}(\frac{1}{2}L_2 i_2^2 + \frac{1}{2}L_1 i_1^2 + M i_1 i_2)
\end{align*}
>On peut écrire la puissance reçue sous la forme d'une dérivée temporelle d'une grandeur: l'énergie emmagasinée.
````

````{topic} __Interprétation:__
 L'énergie est donné à un instant t pour une configuration d'intensité $(I_1,I_2)$. Si dans le circuit 1, l'intensité venait à diminuer pour atteindre 0, sa variation engendrerait:

* un phénomène d'auto-induction dans le circuit 1: la f.e.m. auto-induite fournirait de la puissance au circuit 1 selon les lois habituelle de l'électrocinétique.
* un phénomène d'induction mutuelle dans le circuit 2: la f.e.m. induite fournirait au circuit 2 une puissance selon les lois habituelle de l'électrocinétique.


On trouve donc (et c'est une généralisation de l'interprétation de l'énergie stockée dans une bobine) que l'énergie totale ci-dessus correspond à l'énergie que peut fournir le système au reste du circuit s'il annulait entièrement les deux intensités. On a donc bien un réservoir d'énergie.
L'induction mutuelle peut permettre:

* soit de transférer une information portée par la "forme" de l'intensité induite dans le second circuit.
* soit de transférer de l'énergie d'un circuit à l'autre

```{admonition} Exemples
  
* Les puces RFID fonctionnent sur le principe d'induction: le circuit fixe parcouru par un courant asservi va induire un courant dans le second circuit qui en retour va perturber le premier. La mesure de cette perturbation permet la communication entre la borne de contrôle et la puce.
* Outre les transformateurs étudié ci-dessous, on peut citer certains stimulateurs cardiaques dont les batteries sont rechargées en moyen d'une autre bobine en influence mutuelle. On évite ainsi le recours à une opération chirurgicale.
```
````


````{topic} Complément : Coefficient d'induction mutuelle

Les résultats précédents montre que le coefficients d'induction mutuelle ne peut être supérieur aux inductances mise en jeu. Pour l'augmenter il faut:

* se placer dans des conditions proches de l'influence totale. On utilise, si on peut des "circuits magnétiques", c'est-à-dire des matériaux possédant des propriétés magnétiques fortes. On ne détaillera pas pourquoi certains matériaux ont ces propriétés (matériaux ferreux surtout) mais il faut savoir que:

* ce sont des matériaux qui ont la tendance à canaliser le champ magnétique en leur sein (d'où le nom de "circuit magnétiques", comme un circuit électrique canalise le champ électrique le long du fil)
* on introduit leur __perméabilité magnétique__ $\mu$. Plus cette perméabilité est grande, plus le matériau tend à canaliser les lignes de champ magnétiques. Dans les calculs, cela revient (pour nous) à remplacer la perméabilité magnétique du vide $\mu_0$ par $\mu$. (pour le fer doux, on a $\mu \approx 4000 \mu_0$).
* mais ces matériaux sont aussi conducteurs. Il peut donc se produire un phénomène d'induction qui génère des courants internes au matériau (__courants de Foucault__). Ils entrainent des pertes énergétiques dans le circuit magnétique.

* augmenter significativement les valeurs des inductances. Pour ce faire, on utilise des noyaux de matériaux magnétiques ("fer doux"). Comme précédemment, l'augmentation de la perméabilité magnétique canaliser les lignes de champ et peut augmenter significativement l'inductance (cas d'une bobine longue).
````

### Application au transformateur
#### Présentation générale

````{important} __Définition : Transformateur électrique__

Un transformateur électrique est une machine électrique permettant de modifier les valeurs de tension et d'intensité du courant délivrées par une source d'énergie électrique alternative, en un système de tension et de courant de valeurs différentes, mais de même fréquence et de même forme. Nous étudions ici des transformateurs statiques c'est-à-dire dans lesquelles le transfert d'énergie entre les deux circuits s'effectue par induction par le biais d'un circuit magnétiques qui canalise le flux du champ magnétique d'un circuit vers l'autre.
```{figure} ./images/em_schema_transfo_reel.png
:name: fig_transfo_schema_reel
:align: center
Schéma électrique d'un transformateur
```

````

__Eléments de vocabulaire:__

* L'entrée du transformateur, d'où vient l'énergie électrique, est appelé circuit primaire.
* La sortie du transformateur, où est transférée l'énergie est appelée circuit secondaire.
* La partie du flux magnétique traversant une section du circuit magnétique est appelée flux commun car il va traverser chaque spire des deux circuits primaire et secondaire, le reste du flux constitue les fuites de champs magnétiques.


__Caractéristiques:__ Ces caractéristiques ne sont pas exhaustives mais informent sur l'utilisation faite et les performances du transformateur:

* Le rapport de transformation en tension $m =\frac{U_2}{U_1}$. Ce rapport dépend a priori du circuit secondaire dans les cas réel. C'est pourquoi, les constructeurs donnent en général soit le rapport de transformation "à vide" (le circuit secondaire étant laissé ouvert), soit le rapport de transformation "nominal" (c'est-à-dire pour une charge électrique choisie par le constructeur (normalement la charge prévue à la réalisation)).
* Le rapport de transformation en courant: $\eta = \frac{I_2}{I_1}$. Ce rapport est moins souvent donné car il dépend trop fortement de la charge en sortie. On lui préfère des données comme les puissances apparentes en entrée (puissance que fournirait un générateur dont l'impédance de sortie est purement résistive) ou en sortie (la puissance que recevrait un récepteur purement résistif).
* La perméabilité magnétique (relative) du circuit magnétique. On rappelle que plus cette valeur est haute, plus les lignes de champ seront canalisées dans le circuit.
* Le rendement énergétique: $\rho = \frac{P_2}{P_1}$. C'est un élément important évidemment.


#### Cas du transformateur parfait

````{important} __Définition : Transformateur parfait__

Un transformateur est dit "parfait" si:

* les pertes par effet Joule dans les bobinages ("pertes cuivre") et dans le circuit magnétiques (par courants de Foucault - "perte fer") sont négligeables.
* les circuits sont en influence totale (les fuites de champ magnétiques sont négligeables), c'est-à-dire que la perméabilité magnétique du circuit magnétique est quasi-infinie.
* les phénomènes d'auto-induction dans les bobinages sont négligeables.

```{figure} ./images/em_schema_transfo_ideal.png
:name: fig_schema_transfo_ideal
:align: center
Schéma électrique du transformateur idéal
```

````

````{important} __Fondamental : Lois des tensions__

Le rapport de transformation d'un transformateur parfait est égal au rapport du nombre de spires de l'enroulement secondaire par celui de l'enroulement primaire et est indépendant de la charge placée sur le secondaire: $m = \frac{U_2}{U_1} = \frac{N_2}{N_1}$

````

````{margin}
On travaille ici en valeur absolue. Le signe de $U_1$ et $U_2$ dépend du sens de l'enroulement. En général, on précise ce sens sur le schéma du transformateur.
````
````{important} Démonstration


>Soit $\Phi_C$ le flux traversant une section du circuit magnétique enlacé par le primaire et le secondaire. Ce flux est le même pour toute section du circuit magnétique (on parle de flux commun) puisqu'on suppose qu'il n'y a pas de fuite de champ magnétique. Il traverse notamment chaque spire du primaire et chaque spire du secondaire. La loi de Faraday pour le primaire s'écrit donc:
>$$
\vert U_1 \vert = - \frac{d N_1 \Phi_C}{dt}
$$
>et pour le secondaire:
>$$
\vert U_2 \vert = - \frac{d N_2 \Phi_C}{dt}
$$
>Il vient le rapport demandé.
````


````{tip} __Exercice : Bilan de puissance__
Dans un transformateur parfait, la puissance reçue par le circuit primaire est égale à la puissance fournie par le circuit secondaire. En déduire que :

$$
	\frac{I_2}{I_1} = - \frac{1}{m}
$$
On précisera le sens des intensités amenant à cette relation.
````

````{important} Démonstration

__Sous l'hypothèse__ de perte d'un rendement énergétique égale à 1, la démonstration est directe.
````

````{topic} Complément : Rapport de transformation des courants (HP en première année)
:class: dropdown, hint
Puisque le champ magnétique circule le long du circuit magnétique. On peut calculer sa circulation le long d'une ligne de champ bouclée. Le théorème d'Ampère s'écrit:
$$
\frac{\oint \overrightarrow{B} \cdot \overrightarrow{dl}}{\mu_0 \mu_r} = \pm N_1 I_1 \pm N_2 I_2
$$
Le signe plus/moins dépend de l'orientation du bobinage. Dans le cas d'un transformateur parfait, la perméabilité relative étant infini, le terme de guache est donc nul. Il vient:
$$
\frac{I_2}{I_1} = \pm \frac{N_1}{N_2} = \pm \frac{1}{m}
$$
Dans les représentation schématiques, le sens de l'enroulement est représenté par un point: il définit le sens à choisir pour l'instant de manière à avoir un rapport positif.
````


#### Différents transformateurs (en ligne)

````{topic} Typologie
Il existe plusieurs manières de classer les transformateurs. Si l'on ne s'intéresse qu'à la loi des tensions, on distinguera trois cas:

* __m>1__ : Le transformateur sert à augmenter la tension. Les centrales électriques s'en servent pour créer une haute tension portée par les lignes HT. Le transport haute tension est en effet très pratique car, comme on l'a vu, cela est couplée avec une diminution de l'intensité, donc des pertes par effet Joule.
* __m<1__ : Le transformateur abaisse la tension. On se sert de ces transformateurs à l'autre bout du réseau électrique, pour ramener les hautes tensions du réseau au valeurs "standards" (220V efficace en France). Ces transformateurs sont aussi utilisé pour abaisser la tension du secteur, par exemple dans les adaptateurs censés fournir des tensions continues beaucoup plus basses. Cela était d'autant plus nécessaire que les circuits de redressement (diodes et condensateurs - moins vrai aujourd'hui) ne pouvaient fonctionner à des tensions aussi élevées que celle du secteur.
* __m=1__ : on conserver la même valeur de tension. C'est transformateur ont une utilité particulière: il joue le rôle de transformateur d'isolement. En effet il n'y a pas de contact électrique (on dit "galvanique") entre le primaire et le secondaire. Ainsi, si le primaire est reliée à la Terre, le secondaire ne le sera pas: c'est le principe d'isolement.
````


````{topic} Remarque

Il existe aussi des transformateurs délivrant non pas une mais plusieurs tensions. Des fils de sortie sont reliés non seulement aux extrémités du bobinages mais aussi à des spires intérieures (cf. \cref{fig_transfo_symetrique}). Le nombre de spire varie alors suivant les branchements considérés et la tension de sortie aussi. On se sert notamment de tels transformateurs pour créer des alimentations symétriques. Un fil, sortie au milieu du transformateur aura un potentiel médian vis-à-vis des deux autres aux extrémités. C'est ce point de potentiel, une fois le redressement effectué qui est appelé "0V" sur les alimentations symétriques.

```{figure} ./images/Electromagnetisme_3_Transfo.jpg
:name: fig_transfo_symetrique
:align: center

```

````

````{topic} Modélisation du transformateur réel
Dans la pratique, le rendement ne peut être égale à 1 à cause des pertes interne. Rappelons que les pertes peuvent être dues:

* aux pertes par effet Joule dans les bobinages (perte cuivre) et dans l'entrefer (perte fer)
* aux effet d'auto-induction dans les bobinages (ce sont plus des effets de retard que des pertes proprement dites)
* aux fuites de champ qui impliquent que même si le secondaire est à vide, le primaire peut débiter de l'énergie.

Une étude plus complète conduirait à modéliser ces pertes par des dipôles "décorant" un modèle de transformateur parfait. Une telle modélisation (qui reste un modèle avec ses défauts) n'est pas à connaître par coeur en première année.
````

## Champs constants et circuits mobiles

### Rails de Laplace
````{dropdown} Remarque

On considère le dispositif des rails de Laplace présenté au chapitre précédent. Nous avions vu que l'étude faite précédemment était incomplète. La raison est que lorsque le barreau se met en mouvement sous l'effet de la force de Laplace, le flux du champ magnétique à travers le circuit va varier: un phénomène d'induction se met alors en place.

````

````{tip} __Méthode : Etude des rails de Laplace__  

On néglige tout phénomène d'auto-induction.

1. Prévoir qualitativement l'évolution du rail mobile.
1. Décrire les successions de cause qui conduisent à cette évolution.
1. En déduire les équations du mouvement de la barre.
1. Déterminer la vitesse limite de la barre. Commenter.
1. Faire un bilan de puissance électrique dans le circuit et un bilan de puissance mécanique. Comparer notamment la puissance apportée au mobile par les forces de Laplace et la puissance cédée par le circuit par effet d'induction.

````

````{topic} Commentaires sur les hypothèse de modélisation

* Le champ magnétique créé par l'aimant est uniforme et suivant l'axe normal au plan du circuit électrique ainsi réalisé. On a choisit de l'orientation comme suivant le schéma.
    * Caractère normal: peu importe car seule la composante normale joue dans le flux
    * Caractère uniforme: rend l'étude plus complexe (voire nécessite un traitement numérique) MAIS le principe qualitative et le principe de conversion d'énergie électromécanique est toujours vraie.
* La résistance totale du circuit formé est notée R est ne dépend pas de la position de la barre.
    * Discutable car la résistance des rails va varier avec leur longueur. Quid des jointures. Cela dit, si on place une résistance, on peut considérer que la résistance des fils lui sera négligeable.
* On néglige le champ magnétique propre au circuit devant celui créé par l'aimant.
    * Calculons un ordre de grandeur: $i_{\max}=E/R$ et le champ magnétique propre est tel que $B_{\max} < \frac{\mu_0 I}{\textrm{distance au circuit}} $ (et ça c’est quand on est proche des fils, le champ magnétique pouvant décroître en $1/r^2$ voire $1/r^3$). Si B est produit par un aimant $B\approx 0,1 \rm{T}$. Il faudrait donc une intensité de l'ordre de $10^3 \rm{A}$  ou $10^4 \rm{A}$ pour que le champ magnétique propre ne soit pas négligeable. L'hypothèse est donc largement vraisemblable. _Attention: ce n'est plus vrai si le champ est créé par un autre circuit: il faut tenir compte de l'inductance propre._
* La barre glisse sans frottements sur les rails
    * Très criticable en pratique. D'autant que l'accumulation des charges au contact tend à plaquer la tige mobile sur les rails.
````


### Spire en rotation
````{tip} __Méthode : Spire rectangulaire en rotation__  

Considérons une spire rectangulaire de côté a et b en rotation autour d'un axe Oz. L'ensemble est soumis à un champ magnétique uniforme et constant dirigé dans la direction Ox.

1. Expliquer pourquoi, si l'on veut maintenir la spire en rotation uniforme, elle doit être entraîner par un moteur.
1. La spire possède une résistance $r$. Déterminer la puissance moyenne que doit fournir le moteur.
1. On ouvre très légèrement la spire (de sorte que le flux de B reste inchangé) et on branche sur la spire une résistance $R>>r$ au moyen de fil gainée protégée du champ magnétique. Déterminer la puissance moyenne fournie à la résistance $R$.
1. A un instant $t=0$, on éteint le moteur (plus de couple). Quel va être le régime permanent final?
1. Préciser des applications possibles des cas de figure traités aux deux questions précédentes.
````

### Cas de conducteur. Courants de Foucault

````{tip} __Exercice : Courants de Foucaults__  


1. Cas de Lorentz: On considère un matériau conducteur tournant au voisinage d'un aimant dont le champ n'est pas uniforme.
    1. Expliquer pourquoi il apparaît des courants induits dans le conducteur --- on les appelle des courants de Foucault.
    1. Pourquoi ce phénomène va tendre à ralentir le mouvement du conducteur. Citer une application.
1. Cas de Neumann: On considère un matériau conducteur sous l'influence d'un champ magnétique variable.
    1.* Expliquer pourquoi il apparaît des courants induits dans le conducteur --- on les appelle des courants de Foucault.
    1.* Commenter l'évolution thermodynamique du conducteur. Citer une application.

````


### Moteurs, alternateurs, génératrices
On a vu sur l'exemple du rail de Laplace que le phénomène d'induction se traduisait du point du vue énergétique comme un transfère de puissance: soit d'une puissance électrique (fem induite) vers une puissance mécanique (force de Laplace). Soit à l'inverse d'une puissance mécanique vers une puissance électrique. La transformation d'un type de puissance vers un autre est appelé transduction. 

Nous allons étudié l'utilisation de la transduction sur deux cas: les moteurs et les alternateurs. Leur principe général de construction est basé sur:

* un stator, partie fixe.
* un rotor, partie mobile en rotation autour d'un axe fixe: c'est sur le rotor qu'on place le système d'entraînement (alternateur) ou la charge (moteur).

Le principe de construction dépend du type de machine construite: machine synchrone, machine asynchrone, machine à courant continu.

#### Machine synchrone
Le principe de la machine synchrone a été déjà été expliqué, au moins dans son fonctionnement moteur. Précisons certains points:

````{tip} __Exercice : Machine asynchrone__  
1. Fonctionnement moteur
    1. Comment s'effectue le transfert de puissance entre le stator et le rotor?
    1. Proposer un modèle électrique du circuit du stator.
    1. Ecrire l'équation mécanique générale qui décrit le mouvement du rotor --- on n'évaluera pas les différents termes. Si l'aimant est conducteur, quel autre phénomène peut entrer en jeu? Est-il favorable ou défavorable au comportement moteur?
    1. On ne considère pas l'aimant conducteur. Justifier qu'un couple résistance constant (frottements solides ou charges) ne modifie pas la vitesse de rotation en régime stationnaire. Quel est par contre la conséquence? Que se passe-t-il si la charge est trop forte?
1. Fonctionnement générateur:
    1. Justifier que si le stator n'est pas alimenté mais branché sur une charge, un couple moteur sur le rotor peut générer un courant électrique dans le stator: c'est le principe des alternateurs.
    1. L'auto-induction dans le stator pose-t-elle un problème en terme de rendement de puissance?

````

#### Machine asynchrone
```{figure} ./images/Electromagnetisme_3_Asynchrone.png
:name: fig_machine_asynchrone
:align: center
Machine asynchrone
```

Le moteur asynchrone est un peu similaire à la machine synchrone à un détail (pas si détail!) près: le rotor n'est plus un aimant permanent ou un circuit dont un générateur extérieur impose le courant (ce qui revient à réaliser un dipôle permanent) mais un circuit fermé/un conducteur (une ["cage d'écureuil"](fig_machine_asynchrone)). La présence d'un champ magnétique tournant va créé un flux magnétique variable et donc un phénomène d'induction. Des courants vont circuler dans le rotor qui va alors subir une force de Laplace et se mettre en mouvement.

````{tip} __Exercice : Machine asynchrone__  

Pourquoi un régime stationnaire à la vitesse de synchronisme ne peut exister si le rotor est en charge?

````

C'est l'une des différences fondamentales avec la machine synchrone. Il vient notamment que la vitesse de rotation va dépendre de la charge (au contraire de la machine synchrone). Par contre, une machine asynchrone est beaucoup plus facile à démarrer.

#### Machine à courant continu
La machine à courant continu fonctionne, comme son nom l'indique... avec un courant continu. Elle peut:

* soit transformer l'énergie mécanique du rotor en courant dans les bobinages du rotor: il fonctionne comme génératrice.
* soit transformer un apport d'énergie électrique en un mouvement de rotation du rotor: il fonctionne comme moteur.


Un  avantage de la machine à courant continu est que l'on peut passer d'un fonctionnement à l'autre sur la même machine, sans modifier sa technologie.

Jusque là, rien de nouveau... Le problème est qu'il s'agit ici de transformer un apport d'énergie continue en un autre autre en utilisant le phénomène d'induction dont la particularité est de n'apparaître qu'avec un flux magnétique variable! L'autre problème est que le courant entrant/sortant se fait par le rotor... qui tourne.

````{tip} __Exercice : Machine à courant continu simple: spire en rotation.__  

On considère comme rotor le cas d'une spire rectangulaire de longueur b et de largeur a conductrice. La spire est légèrement ouverte sur l'axe de symétrie Oz de la largeur (cf. \cref{fig_mcc}) de manière à pouvoir y brancher une source de courant. Elle est de plus fixée rigidement sur un arbre en liaison pivot d'axe Oz avec le stator. Ce dernier est constitué d'un aimant permanent. On considère ici un dipôle (les pôles sont représentées sur les schéma) qui assure un champ magnétique globalement axé dans la même direction dans toutes la zones où tourne la spire (du pôle Nord vers le pôle Sud).

```{figure} ./images/Electromagnetisme_3_Continu.jpg
:name: fig_mcc
:align: center
Machine à courant continu
```

__Modèle du champ magnétique:__ On considère, pour simplifier que le champ magnétique est radiale (système de coordonnées cylindrique d'axe Oz) tel que: $B_r(r, \theta) = -B_r (r, \theta + \pi)$ (on parle d'antisymétrique du champ). On note l'axe Ox, l'axe d'antisymétrie et l'origine des angles $\theta$. On supposera que de chaque côté de l'axe, le champ a une intensité constante.

On note $\Gamma_{ext}$ le couple extérieur (entraînement moteur, frottements, charge sur l'arbre...), $E_{ext}$ la tension d'alimentation de la machine (qui sera nulle si la machine fonctionne en génératrice) R la résistance de la spire, $R_{ext}$ la résistance de charge sur le circuit (en fonctionnement génératrice ou la résistance interne de l'alimentation en fonctionnement moteur). On note aussi $J$ le moment du rotor sur l'axe Oz.

1. Fonctionnement moteur 
    1. Montrer, sans calcul, qu'un tel champ magnétique assure, en présence d'un courant $i$, un couple de force qui va faire tourner la spire (effet moteur). Comment appelle-t-on cette force?
    1. Exprimer le moment de cette force motrice sous la forme: $\overrightarrow{\Gamma_L} = K i \overrightarrow{e_z}$
    1. Lorsque la spire a fait un demi-tour, comment évolue le couple moteur? Justifier alors l'utilisation d'un commutateur (la pièce cylindrique coupée représentée avec les armatures A et B) pour permettre un couple moteur sur l'ensemble du tour.
    1. On note R la résistance de la spire. Quel phénomène se produit dans le circuit lorsque la spire tourne? Ce phénomène est-il favorable au couple moteur? Quel est l'effet sur le circuit électrique du rotor?
    1. Modéliser le schéma électrique de la spire en exprimer les caractéristiques des dipôles ajoutés.
    1. Exprimer les équations mécaniques et électriques de la machine à courant continu.
    1. Déterminer la vitesse de rotation du moteur en régime permanent. Commenter.
    1. Commenter les dépendances du temps caractéristiques que met le moteur à atteindre son régime permanent.
1. Fonctionnement générateur: On prend $E_{ext} = 0$
    1. Expliquer pourquoi la rotation du rotor va imposer un courant dans le circuit.
    1. Les équations déterminée précédemment change-t-elle? Conclure.
````

_Critiques du modèle (non exhaustives)_

* La principale critique qu'on peut faire la modélisation du champ magnétique. En pratique, un simple dipôle par probablement créé un champ magnétique peu homogène et un couple variable et peut-être pas naturellement orientée suivant l'axe de rotation. Cela peut induire des forces de réaction à la liaison pivot. Dans les moteur à courant continu actuel, on utilise des multipôles magnétiques de manière à augmenter l'effet de symétrie/antisymétrie cylindrique. Le principe de Curie ("la symétrie des causes de retrouve dans la symétrie des effets") assure alors un champ magnétique relativement radiale.
* La circulation d'une intensité i peut créer un phénomène d'auto-induction. Il suffit alors d'ajouter au modèle électrique une inductance qu'on pourrait mesurer expérimentalement. En pratique, l'effet d'auto- induction est comme souvent faible vis-à-vis de l'effet dû à l'aimant permanent.


````{important}
__Machine à courant continu --- Cas général:__

Dans le cas général, le rotor est constitué d'un bobinage dont la géométrie est plus complexe qu'une simple spire. Néanmoins, à l'image de l'auto-inductance et de l'inductance mutuelle. Certains propriétés vont toujours être vérifiée:

* La force de Laplace est toujours proportionnelle à l'intensité, seule le facteur de proportionnalité K varie. Dans les modèles ici, ce facteur est supposé constant.
* La force électromotrice induite dans le circuit est toujours proportionnelle à la vitesse angulaire $\omega$ du rotor. Dans les modèles ici, ce facteur est supposé constant et identique au précédent.

On obtient alors les "équations d'une machine à courant continu": $e = K \omega$ et $\Gamma_L = Ki$ avec la force électromotrice orientée en convention récepteur.
````

## S'entrainer

### Applications
````{tip} __Exercice : Deux bobines réelles en inductance mutuelle.__  

On considère deux bobines d'auto-inductance L, de résistance R et de coefficient d'inductance mutuelle M. La première est court-circuitées et la seconde reliée à un générateur délivrant une tension $E(t) = E_0 \cos \omega t$. Déterminer les équations couplées pour les amplitudes complexes des intensités dans chaque circuit.

````

### Entrainement
````{tip} __Exercice : Pince ampèremétrique__

On considère un tore de section carré de c\^oté $a$ et de rayon moyen $R$ sur lequel on a enroulé $n$ spires jointives, les deux extrémités du fil étant court-circuités. On note Oz l'axe du tore et dans un repère cylindrique, chaque spire est contenue dans un plan. Le circuit est parcouru par un courant d'intensité $I$. 


1. Justifier que le champ magnétique a pour forme $\overrightarrow{B}(M) = B_{\theta}(r,z) \overrightarrow{e_{\theta}}$

Le champ magnétique créé par un tel dispositif est:

*. nul à l'extérieur du tore
*. $\overrightarrow{B}(r,z) = \frac{\mu_0 nI}{2 \pi r} \overrightarrow{e_{\theta}}$ à l'intérieur du tore.

1. Déterminer le flux du champ magnétique à travers le tore. En déduire l'inductance propre du tore.

On place sur l'axe Oz un fil infini parcouru par un courant $i$. La résistance totale du bobinage est noté $r$ et et au lieu d'un court-circuit, le fil du tore est fermé sur un voltmètre d'impédance interne $R_V$.

1. Déterminer le flux mutuel du champ magnétique du fil infini à travers le tore.
1. Si $i$ varie, exprimer la force électromotrice d'induction dans le tore en fonction de $i$ et $I$ et des autres paramètres du tore. En déduire l'équation différentielle qui relie $i(t)$ et $I(t)$.
1. Déterminer $I(t)$ en régime sinusoïdal forcé et en déduire la valeur mesurée par le voltmètre. Préciser l'intérêt d'un tel dispositif et ses limites.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Symétrie des champs._
* _$\Longrightarrow$ Flux du champ magnétique._
* _$\Longrightarrow$ Loi de Faraday._
* _$\Longrightarrow$ Régime sinusoïdal forcé._


````{tip} __Exercice : Transimpédance__


1. On considère un transformateur parfait de rapport en tension m. Le primaire est relié à un générateur de Thévenin de f.e.m. $e_1(t)$ et de résistance de sortie $R_g$. La sortie est reliée à une impédance $\underline{Z}$. Montrer que circuit est équivalent à celui d'une impédance $\underline{Z_{eq}}$ branchée directement sur le générateur et dont on déterminera l'expression. On parle de transimpédance.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Transformateur parfait._

````{tip} __Exercice : *Pertes énergétiques dans un conducteur__

On considère un conducteur cylindrique de hauteur h et de rayon R d'axe Oz plongé dans un champ magnétique variable: $\overrightarrow{B} = B(t)\overrightarrow{e_z} = B_0 \cos (2 \pi f t) \overrightarrow{e_z}$. Le phénomène d'induction créé des champs électriques qui engendrent des courants circulant suivant des cercles concentriques d'axe Oz. On peut montrer que:

* Pour une ligne de courant de rayon $r$, d'épaisseur $dr$ et de largeur $dz$. Le courant qui circule peut s'écrire $I(r) = j(r) dr dz$ où $j(r)$ est appelée densité volumique de courant. On peut lui associer un vecteur donnant à la fois l'intensité et la direction/sens du courant: $\overrightarrow{j}(r) = j(r) \overrightarrow{e_{\theta}}$
* La résistance $R(r)$ d'une ligne de courant de rayon $r$, d'épaisseur dr et de largeur dz s'écrit: $R(r) = \frac{2 \pi r}{\gamma dr dz}$.



1. Justifier qualitativement l'apparition de courants induits dans le conducteur.
1. Commenter le sens du champ magnétique créé par les courants induit. A quel condition sur $j(r)$ et $\frac{dB}{dt}$ la loi de Lenz sera-t-elle vérifiée?
1. Déterminer la force électromotrice induite sur une ligne de courant de rayon $r$, d'épaisseur $dr$ et de largeur $dz$. En déduire la densité volumique de courant $j(r)$ sur cette spire.
1. Déterminer l'énergie perdue par effet Joule dans l'ensemble du conducteur. Commenter la dépendance en la fréquence. Cette dépendance est générale pour les courants de Foucault.
1. Présenter deux cas: l'un où les pertes par effets Joule dues aux courants de Foucault sont utiles et l'autre où elles sont problématiques.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Symétrie des champs._
* _$\Longrightarrow$ Flux du champ magnétique._
* _$\Longrightarrow$ Loi de Faraday._
* _$\Longrightarrow$ Effet Joule._
* _$\Longrightarrow$ Conducteur._

````{tip} __Exercice : Double rail de Laplace__

On considère deux rails fixes et parallèles (distances a les séparant) conducteurs de résistance négligeable et de dimensions infinies. On place sur ces rails deux tiges perpendiculairement aux rails de sortent que chacune réalisent un contact avec les deux rails. Chaque tige possède alors une résistance r identique. L'ensemble est plongé dans un champ magnétique constant et uniforme d'axe Oz perpendiculaire au circuit rectangulaire formé par les tiges et les rails. A l'instant initiale, les deux tiges sont séparées d'une distance L et on communique une vitesse $v_0$ (vers la gauche) à la tige de gauche, la tige de droite étant immobile.

1. Déterminer qualitativement le mouvement des deux tiges en fonction du temps. 
1. Retrouver ces conclusions par une étude quantitative.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Flux du champ magnétique._
* _$\Longrightarrow$ Action de Laplace._

````{tip} __Exercice : Couplage de machines à courant continu__

Deux machines à courant continu à aimants permanents identiques sont électriquement connectées avec un interrupteur K en série entre les deux. On néglige tout frottement et on suppose que les machines fonctionnent à vide (pas de couple résistant). On note J le moment d'inertie des deux machines et R la résistance électrique propre de moteur. A $t=0$, on ferme l'interrupteur K alors que la machine 1 tourne à une vitesse angulaire et que la machine 2 est immobile.

1. Déterminer l'évolution des vitesses angulaires de chaque machine en négligeant tout phénomène d'auto-induction. Représenter leur évolution et commenter les valeurs finales obtenues. Effectuer un bilan énergétique
1. Reprendre l'étude précédente en tenant compte des phénomènes d'auto-induction modélisés par une inductance L identique pour chaque moteur (cas pseudo-périodique).
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Machine à courant continu._
