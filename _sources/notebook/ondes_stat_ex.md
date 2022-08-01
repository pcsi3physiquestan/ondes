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
````{admonition} Cavité LASER résonante
:class: attention
Un LASER est une source lumineuse monochromatique. Si l'émission de la lumière est due à des phénomènes de transitions entre les niveaux d'énergie d'atomes. On place généralement ce milieu dans un cavité résonante dont l'intérêt est d'affiner la sélection des longueurs de la source et ainsi obtenir une lumière la plus monochromatique possible.

On se propose de préciser le mode de fonctionnement de la cavité résonnante au moyen d'un modèle simple (donc imparfait mais déjà intéressant). On suppose que celle-ci est composée de deux miroirs plans parfaits face à face distants d'une distance d et séparés par du vide. On note Ox l'axe perpendiculaire aux miroirs. Entre les deux miroirs se propage une onde électromagnétique monochromatique plane pouvant se propager dans les deux sens. Les miroirs sont supposés parfaits c'est-à-dire qu'il réfléchissent entièrement le rayonnement. Cela implique  (admis) que le champ électrique doit être nul sur les miroirs. On décrit la vibration électromagnétique par le champ électrique de l'onde en tout point de l'espace: $\overrightarrow{E(x,t)}=E_y(x,t) \overrightarrow{e_y}$

1. Quelle autre grandeur physique décrit la propagation d'une telle onde?
1. Préciser dans le cas d'une onde progressive monochromatique de pulsation $\omega$ se déplaçant dans le sens des x positifs l'expression générale du champ électrique.
1. Justifier simplement la présence d'une onde régressive monochromatique, c'est-à-dire se déplaçant dans le sens des x négatifs. Donner son expression général puis l'expression de l'onde électromagnétique résultante dans la cavité.
1. Exprimer les deux conditions aux limites qui en découlent. En déduire que l'onde résultante est une onde stationnaire et que les pulsations permises pour l'onde sont quantifiées.
1. En réalité, le rayonnement est émis par le milieu amplificateur du LASER composé de différents atomes. Pour de nombreuses raisons, cette émission ne produit pas un rayonnement monochromatique mais une gamme de fréquence. Pourquoi une telle cavité permet de sélectionner une fréquence et donc d'obtenir une lumière monochromatique?
1. (Recherche) En réalité, la lumière d'un LASER n'est pas rigoureusement monochromatique. Rechercher les ordres de grandeurs de largeurs de raie de LASER (courant ou non) ainsi que les origines possibles d'un tel élargissement.


````

````{admonition} Tuyau ouvert 
:class: attention

On considère le cas d'un tuyau ouvert et on cherche les fréquences correspondant aux modes propres d'une onde acoustique stationnaire. On admet que pour un tel tuyau, on attend un ventre de vitesse aux deux extrémités. On réalisera une étude graphique pour déterminer les modes propres.

````

## Entrainement

````{admonition} Corde vibrante 
:class: attention

On considère une corde de longueur L fixée à ses deux extrémités. Sa masse linéique est $\mu$ et elle est tendue par une tension $T_0$. La vitesse de propagation des ondes mécaniques sur la corde est alors: $v=\sqrt{\frac{T_0}{\mu}}$.

1. Quelle grandeur permet de décrire la vibration de la corde?
1. Montrer que v est bien homogène à une vitesse.
1. Rappeler brièvement pourquoi on doit décrire la vibration de la corde comme la superposition de deux ondes. Préciser leurs expressions générales.
1. On cherche les pulsations $\omega$ auxquelles cette corde peut vibrer. Quelle est alors la forme générale de l'onde résultante?
1. Exprimer les conditions que doit satisfaire l'onde? En déduire les pulsations quantifiées auxquelles la corde peut vibrer. On précisera le fondamental $\omega_0$.
1. (HP) *On peut montrer que la puissance moyenne transportée par une onde mécanique progressive monochromatique le long de la corde est de la forme: $\langle P(x) \rangle = a \langle Y^2(x,t) \rangle$ où $a$ est une constante qu'on ne déterminera pas. Montrer que pour une onde stationnaire, il n'y a pas d'énergie transportée. Donner un autre sens au terme "d'onde stationnaire".


````

````{admonition} Le pipeau
:class: attention

Comme les instruments à corde, la production du son dans les instruments à vent est basé sur le principe d'ondes stationnaires. Nous allons illustrer ce principe en modélisant le fonctionnement du pipeau quand tous les trous sont bouchés (Fa). Dans une telle flûte, le son est produit par un résonateur (l'ouverture du pipeau) à une extrémité de l'instrument et se propage le long du tube se section droite $S$ de longueur $L=10\rm{cm}$. On note Ox l'axe du tube, O étant la côte du résonateur. On suppose que la célérité du son dans le tube (rempli d'air) est $c=344 \rm{m.s^{-1}}$. On rappelle que les deux grandeurs décrivant la propagation de l'onde sont la vitesse d'agitation d'une tranche d'air: $v(x,t)$ et la surpression engendrée par le passage de l'onde sonore: $p(x,t)$. On précise aussi qu'on a la relation:

$\frac{\partial v}{\partial t} = - \frac{1}{\rho_0} \frac{\partial p}{\partial x}$ où $\rho_0$ est la masse volumique de l'air au repos.

1. On suppose que le résonateur crée une onde plane progressive de fréquence f se propageant dans la direction des x croissants. On note $v_{0+}$ l'amplitude de l'oscillation de la vitesse et $p_{0+}$ l'amplitude de l'oscillation de la pression. Donner les expressions de $v_{+}(x,t)$ et $p_{+}(x,t)$ associées à cette onde en tout point du tube (utiliser les grandeurs définies dans l'énoncé).
1. Justifier la relation: $\lambda f =c$ où $\lambda$ est la longueur d'onde de l'onde sonore dans le milieu.
1. (HP)Montrer que $\rho_0 c v_{0+} = p_{O+}$.
1. Au bout du tube, l'ouverture brutale provoque une réflexion d'onde dans le sens inverse de propagation. On note $v_{0-}$ l'amplitude de l'oscillation de la vitesse et $p_{0-}$ l'amplitude de l'oscillation de la pression. Donner les expressions de $v_{-}(x,t)$ et $p_{-}(x,t)$ associées à cette onde réfléchie en tout point du tube (utiliser les grandeurs définies dans l'énoncé). 
1. (HP)Montrer que $\rho_0 c v_{0+-} = - p_{O-}$.
1. Donner l'expression de la surpression $p(x,t)$ et de la vitesse d'une tranche d'air $v(x,t)$ de l'onde résultante dans le tube.
1. Le résonateur et l'ouverture du tube impose un effondrement de la pression aux extrémités soit $p(0,t)=p(L,t)=0$.
1. Montrer, en déterminant $p(x,t)$ que l'onde résultante est alors une onde stationnaire dans les fréquence possible sont quantifiées.
1. Déterminer $v(x,t)$. Comparer la position des noeuds de pression et de vitesse.
````
