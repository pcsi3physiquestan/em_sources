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
# Champs magnétiques. Méthodes et exercices.
## Méthodes
### Lien entre distribution et intensité.
Il faut faire attention car le nom des distributions de courantpeut être trompeur.

````{tip} Exercice
On considère les deux exemples suivants : 
1. fil infini de rayon $R$ parcouru par une distribution axiale uniforme. Calculer l'intensité qui traverse une section transverse du cylindre (orientée suivant $+\overrightarrow{e_z}$).
2. nappe de courant de largeur $L$ parcourue par une densité uniforme. Calculer l'intensité qui traverse la nappe suivant l'axe Oy.

````

````{topic} Correction
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
````

### Symétrie et coordonnées
_Note : quand on exprime un champ vectoriel $\overrightarrow{j(M)}$ dans une base:_

$$
\overrightarrow{j(M)} = j_r(M) \overrightarrow{e}_r + j_\theta(M) \overrightarrow{e}_\theta + j_z(M) \overrightarrow{e}_z
$$
_alors les 3 composantes $j_r, j_\theta, j_z$ sont des champs scalaires._

````{tip} Conséquence sur les coordonnées
On considérons un vecteur $\overrightarrow{j}(M)$ qui possède comme plan de symétrie le plan $xOy$ d'un repère cartésien $(0, \overrightarrow{e_x}, \overrightarrow{e_y}, \overrightarrow{e_z})$.

On note les composantes de $\overrightarrow{j}(M(x, y, z))$ :
* $j_x(x, y, z)$
* $j_y(x, y, z)$
* $j_z(x, y, z)$

1. Préciser la parité des fonctions $j_x, j_y, j_z$ en $z$.
1. Reprendre la même question en supposant que $xOy$ est un plan d'anti-symétrie.
1. Reprendre les deux mêmes questions en pour si $xOy$ et un plan de symétrie/d'antisymétrie d'un __pseudo-vecteur__ $\overrightarrow{B}(M)$

Il est important de comprendre à travers cet exercice que le lien entre parité et symétrie n'est PAS intuitif et qu'il est différent pour vecteur et un pseudo-vecteur.
````

````{tip} Pseudo-vecteur et plan de symétrie/anti-symétrie

On considére un pseudo-vecteur champ magnétique $\overrightarrow{B}(M)$ qui possède comme plan de de symétrie le plan $\Pi_S$.
1. Justifier (à retenir) que le pseudo-vecteur champ magnétique en tout point $M_0$ du plan $\Pi_S$ est contenu dans le plan $\Pi_S$.

On considére un pseudo-vecteur champ magnétique $\overrightarrow{B}(M)$ qui possède comme plan de d'antisymétrie le plan $\Pi_A$.

1. Justifier (à retenir) que le pseudo-vecteur champ magnétique en tout point $M_0$ du plan $\Pi_A$ est perpendiculaire plan $\Pi_A$

````

### Déterminer l'orientation du champ magnétique
````{admonition} Détermination de la structure du champ B
:class: tip
Déterminer la structure du champ magnétique pour un fil infini en utilisant le principe de Curie.
````

````{topic} Correction
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
````

### Ordre de grandeur du champ magnétique

````{tip} __Cas simple__

Estimer à partir du théorème d'Ampère le nombre de spire d'un bobinage nécessaire pour obtenir un champ 100 fois supérieure au champ terrestre à une distance proche du bobinage. Commenter.

````