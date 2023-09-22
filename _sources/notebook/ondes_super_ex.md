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
# Application et entrainement

## Applications
````{admonition} Battements lumineux
:class: attention
En comparant des ordres de grandeurs adaptés, montrer qu'on ne peut observer un phénomène de "battements lumineux".
````
````{admonition} Bilan sur les interférences
:class: attention
Reproduire dans un tableau le bilan des grandeurs caractéristiques qu'on peut calculer pour étudier une figure d'interférences et donner les valeurs possibles qu'elles peuvent prendre pour des cas d'interférences constructives et des cas d'interférences destructives.
````

_Point utile pour cet exercice_
* _$\Longrightarrow$ Conditions d'interférences destructives et constructives._

## Entrainement
````{admonition} Trous d'Young. Représentation de Fresnel
:class: attention
On considère une source de lumière monochromatique de longueur d'onde $\lambda$, ponctuelle située au point S et émettant dans le vide. A une distance $D_1$ de S, on place une plaque opaque percé de 2 trous $S_1$ et $S_2$ distants de a. On suppose que ces deux trous sont de taille $\epsilon$ très faibles. On note O le milieu des deux trous et Ox l'axe normale au plan. Dans un premier temps, la source S est située sur l'axe Ox. On note Oy l'axe passant par les deux trous et Oz l'axe perpendiculaire dans le plan de la plaque.

1. Quelle phénomène justifie qu'à la sortie des trous, on puisse considérer l'existence d'un faisceau élargi. Rappeler alors la relation (approximative) entre l'ouverture angulaire du faisceau et la taille du trou.
1. Faire un schéma du dispositif en représentant les faisceaux sortant des deux trous. Justifier qu'on puisse observer des interférences entre deux ondes lumineuses dans un zone qu'on précisera.
1. Dans l'hypothèse d'un trou infiniment petit, que devient cette hypothèse? Quel problème pratique pose l'utilisation d'un trou top petit? On supposera ce problème non limitant dans l'étude faite ici et on supposera $\epsilon=0$ dans toute la suite du problème de sorte que l'on puisse les assimiler à deux sources nouvelles sources ponctuelles secondaires.
1. On place un écran parallèle à la plaque à une distance $D_2$ de la plaque et on suppose $D_2\gg a$. Sur l'écran, on repère la position d'un point à ses coordonnées $(y,z)$ par rapport au centre A, intersection de l'écran et de l'axe Ox.  On s'intéresse à l'éclairement en un point M de coordonnées $(y_M,0)$. On suppose $D_2\gg y_M$ et on donne $\sqrt{1+e}\approx 1+ \frac{e}{2}$ si $e\ll 1$.

1. On considère l'onde passant par le trou $S_1$.
    1. Exprimer la distance $SS_1 M$ parcouru par l'onde. 
    1. En déduire l'amplitude du champ électrique (au sens $E(x,t)$ - abus de langage - associé à cette onde au point M (on prendre S comme origine des phases et on traitera le champ électrique comme une grandeur scalaire). 
    1. Montrer que l'on peut introduire une grandeur $e$ exprimée en fonction de $D_2$, a et $y_M$ très petite devant 1 et permettant d'utiliser l'approximation donnée dans l'énoncé. Simplifier alors l'expression de l'amplitude (au sens $E(x,t)$).
1. Répondre aux questions précédentes pour l'onde passant par le trou $S_2$.
1. Déterminer par le calcul l'amplitude complexe de l'onde résultante en un point de coordonnées $(y_M;0)$ puis son amplitude réelle. Déterminer alors les positions des franges brillantes et des franges sombres ainsi que l'interfrange.
1. On déplace la source S d'une distance d dans la direction Oy. On suppose les résultats précédents toujours vrais, déterminer le nombre de franges brillantes que l'on voit défiler au point $A(0;0)$ sur l'écran pendant l'opération.
````

_Point utile pour cet exercice_
* _$\Longrightarrow$ Retard d'une onde_
* _$\Longrightarrow$ Conditions d'interférences destructives et constructives._
* _$\Longrightarrow$ Interfrange._
* _$\Longrightarrow$ Développements limités._

````{admonition} Doublet du sodium.
:class: attention

On considère l'expérience des trous d'Young présentées dans l'exercice précédent. On se place dans le même cadre d'approximation de sorte que pour une lumière monochromatique de longueur d'onde $\lambda$, on obtiendra les mêmes résultats. Pour un point M de l'écran, le champ électrique s'écrit:

$$
E(M,t) = 2 E_{1m} \cos(\frac{\pi a y_M}{\lambda D_2}) \cos(\omega t - \Phi_M)
$$
avec $\Phi_M$ un terme de phase inutile ici.

Un capteur de lumière (capteur CCD) parcourt à une vitesse $v$ l'axe Ay de l'écran et fournit une tension $U(t)$ proportionnelle à l'éclairement $I$ où il se trouve.

1. Déterminer l'expression de $U(t)$. En déduire le spectre de Fourier de $U(t)$. Justifier que la détermination expérimentale du spectre permet de remonter à la longueur d'onde de la lumière incidente.
1. On remplace la source monochromatique par une lampe spectrale au sodium émettant deux longueurs d'onde $\lambda_1=\frac{2 \pi}{k_1}$ et $\lambda_2 = \frac{2 \pi}{k_2}$ (on pose $\lambda_2<\lambda_1$). On note $k_m=\frac{k_1+k_2}{2}$ et $\Delta k = \frac{k_2 - k_1}{2}$.
    1.Pourquoi peut-on calculer l'éclairement causé par chaque longueur d'onde indépendamment? En déduire l'éclairement total $I_T(x)$ puis la tension mesurée $U_T(t)$.
    1. Montrer que $U_T(t)$ se décompose en une somme de deux sinusoïdes dont on déterminera les fréquences. Représenter graphiquement $U_T(t)$ et son spectre. 
    1. Justifier que la détermination du spectre de $U_T(t)$ permet de remonter aux deux longueurs d'onde $\lambda_1$ et $\lambda_2$.
    1. Montrer aussi que l'étude graphique de l'évolution temporelle de $U_T(t)$ permettrait de déterminer $k_m$ et $\Delta k$ et donc les deux longueurs d'onde, préciser clairement la méthode.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Spectre d'un signal_
* _$\Longrightarrow$ Battements._
* _$\Longrightarrow$ Modulation._

````{admonition} Filtre interférentiel.
:class: attention
On considère une lame à face parallèle d'épaisseur $e$ et d'indice $n$ entouré à gauche et à droite par de l'air. Un faisceau monochromatique de longueur d'onde $\lambda$ arrive sur la face de gauche avec un angle d'incidence $i$.

1. Réaliser le tracé des deux premiers rayons transmis à droite de la lame et justifier que les interférences ont lieu à l'infini.
2. On ne considère que les deux premiers rayons transmis. Déterminer pour $i\ll 1$ et en travaillant à l'ordre 1, la condition sur l'épaisseur $\lambda$ pour qu'on observe des interférences constructives.
````

_Point utile pour cet exercice_
* _$\Longrightarrow$ Retard d'une onde_
* _$\Longrightarrow$ Conditions d'interférences destructives et constructives._
* _$\Longrightarrow$ Lois de Snell Descartes._
* _$\Longrightarrow$ Développements limités (petits angles)._

 Un devoir libre est disponible [en ligne](https://moodlecpge.stanislas.fr/mod/resource/view.php?id=166)