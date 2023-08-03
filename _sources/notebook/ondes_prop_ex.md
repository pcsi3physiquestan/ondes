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
# Maitriser les méthodes
## Application

````{admonition} Onde progressive
:class: attention
On étudie la propagation sans amortissement d'une perturbation le long d'une corde élastique. A la date $t = 0$, le front de l'onde présenté sur le graphique finit d'être émis à l'extrémité S de la corde. A la date $t_1=2,3 \rm{s}$, on prend un cliché de la corde; la Figure suivante reproduit le cliché avec deux échelles de longueurs différentes suivant l'horizontale et suivant la verticale. $M_1$ est la position du front de l'onde à la date $t_1$, $N_1$ celle de la crête et $P_1$ celle de la queue de l'onde.

```{figure} ./images/Signaux_TD3_EX3_1.jpg
:name: fig_296
:align: center
```

1.  L'onde qui se propage le long de la corde est-elle transversale ou longitudinale? Que représente son amplitude $y(x,t)$?
1.  Calculer la célérité de l'onde le long de la corde. 
1.  Quelle est la durée $\tau$ du mouvement d'un point de la corde au passage de l'onde? 
1.  A la date $t_1$, quels sont les points de la corde qui s'élèvent? ceux qui descendent? 
1.  Dessiner sur le graphique donné ci-dessous, l'aspect de la corde à la date $t_2=3,6 \rm{s}$.
1.  Soit le point Q de la corde situé à $12.0\rm{m}$ de S.
    1.  A quelle date $t_3$ commence t-il à bouger? 
    1.  A quelle date $t_4$ passe-t-il par un maximum d'altitude? 
    1.  A quelle date $t_5$ cesse-t-il de bouger? 
    1.  A l'aide des résultats précédents, schématiser l'allure de la courbe $y_Q=f(t)$ où $y_Q$ représente l'élongation du point Q à la date t.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Retard à la propagation._

````{admonition} Ondes acoustiques
:class: attention
On considère une onde sonore unidirectionnelle se propageant dans la direction des x positifs. Aux abscisses sources $x=0$, l'amplitude de l'onde est: $p(x=0,t)=p_0(t)$. Le milieu ambiant est de l'air de masse volumique au repos $\rho_0=1,2 \rm{kg.m^{-3}}$ et le son s'y propage à la vitesse: $c=340 \rm{m.s^{-1}}$.

1. Une onde sonore est-elle une onde transversale ou longitudinale?
1. Exprimer en fonction de $p_0(t)$, l'expression de la surpression en un point quelconque d'abscisse x.
1. On suppose que l'excitation est sinusoïdale de fréquence f et d'amplitude $p_{0m}$. La phase à l'origine au point x=0 est supposée nulle. Exprimer la surpression $p(x,t)$ en tout point du trajet de l'onde.
1. On peut montrer que l'intensité acoustique moyenne d'une onde harmonique ne dépend que de la valeur efficace $p_0$ de la surpression, de la masse volumique et de la célérité de l'onde. Par une analyse dimensionnelle, montrer que $I = \frac{p_0^2}{\rho_0 c}$.
1. Exprimer la surpression $p_0$ correspondant à l'intensité de référence $I_0$ pour l'air (il correspond à peu près au seuil moyen de perception humaine pour des fréquences autour de 3kHz).
1. Le seuil de douleur pour l'oreille humaine se situe autour de 120dB. Estimer la surpression moyenne correspondante.
````
_Point utile pour cet exercice_
* _$\Longrightarrow$ Grandeurs associées aux ondes acoustiques._
* _$\Longrightarrow$ Forme mathématique d'une onde progressive._

````{admonition} Onde plane 
:class: attention
Comment faire expérimentalement une onde lumineuse plane à partir d'une source ponctuelle?
````

_Point utile pour cet exercice_
* _$\Longrightarrow$ Optique._
* _$\Longrightarrow$ Théorème de Malus._


## Entrainement
````{admonition} Retard d'une OEM
:class: attention
On considère une source Laser considéré comme une source ponctuelle située au point S qui émet un signal dont le champ électrique est représenté ci-après (on parlera de "trains d'onde"). L'onde se propage à travers différents milieux comme présentés ci-après. On a noté  les indices de réfraction de chaque milieu. On admet que le trajet de l'onde n'est pas déviée quand le rayon lumineux passe d'un milieu à l'autre. On admet que, même si le signal n'est pas entièrement sinusoïdal, la fréquence de la portion assimilable à un sinusoïde définit la fréquence du signal émis.

```{figure} ./images/Signaux_TD3_EX3_2.jpg
:name: fig_297
:align: center
```

1. Quelques grandeurs caractérisent la propagation d'un signal lumineux?
1. Déterminer la fréquence du signal émis par le Laser, est-ce une fréquence temporelle ou spatiale? Préciser son unité. Le Laser émet-il dans le visible?
1. Exprimer le retard de l'onde passant par chaque point représenté sur le graphique. On donne leurs abscisses respectives (m): $0;4\times 10^{-6}; 6 \times 10^{-6}; 10^{-5}$. En déduire l'expression temporelle du champ électrique en chaque point.
1. Représenter graphiquement le chronogramme du champ électrique aux différents points considérés.
````

_Point utile pour cet exercice_
* _$\Longrightarrow$ Grandeurs associées aux ondes électromagnétique._
* _$\Longrightarrow$ Retard à la propagation._
* _$\Longrightarrow$ Forme mathématique d'une onde progressive._
