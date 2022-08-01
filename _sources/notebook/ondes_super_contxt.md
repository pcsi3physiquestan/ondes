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
# Généralités

## Position du problème
On considère deux sources $S_1$ et $S_2$ émettant chacune un signal physique se propageant dans le milieu environnant et représentée par la grandeur Y dont l'expression en un point M à un instant t sera notée $Y(M,t)$. On suppose que ces deux ondes sont sinusoïdales de fréquence $f_1$ et $f_2$. On note:

* $Y_1(M,t) = Y_{1m}\cos(\omega_1 t + \phi_{M,1})$ pour l'onde issue de la source $S_1$ (appelée onde 1).
* $Y_1(M,t) = Y_{2m}\cos(\omega_2 t + \phi_{M,2})$ pour l'onde issue de la source $S_2$ (appelée onde 2).


Pour fixer les idées au moyen d'expériences, les ondes considérées seront par la suite soit des ondes acoustiques, soit des ondes lumineuses. Néanmoins, et sauf précisions contraire, les études réalisées pourront être appliquées à tout type d'onde. On considérera aussi des trajets rectilignes de la lumière. On observera d'ailleurs les phénomènes d'interférences étudiés ensuite sur des ondes de surface.

````{sidebar} Déphasage
_On rappelle que le déphasage d'un signal sinusoïdal 2 sur un autre signal sinusoïdal 1 est la différence de phase:_

\begin{align*}
\Phi_{2/1}(M,t) &= \varphi_{2}(M,t) - \varphi_{1}(M,t)\\
&= \left(\omega_2 - \omega_1\right)t + \phi_{M,2} - \phi_{M,1}
\end{align*}
````

````{important} __Ondes synchrones et cohérentes__
* Deux ondes sont dites __synchrones__  si elles ont la même fréquence.
* Deux ondes sont dites __cohérentes si elles ont la même fréquence ET que leur déphasage initiaux (aux sources) sont constants.__ 

````

````{topic} Pourquoi deux ondes synchrones peuvent ne pas être cohérentes ?
Dans le cas des ondes électromagnétiques, l'émission n'est pas continue. La source émet un train d'onde puis arrête d'émettre puis recommence.

Or la largeur des trains d'ondes et l'espace entre deux émissions sont aléatoires. Il vient que deux points sources, même synchrones vont avoir un déphasage qui va varier aléatoirement. Nous verrons que cela peut-être un problème d'autant que cette incohérence __s'applique aussi entre deux points d'une même source lumineuse étendue__ . La seule source lumineuse qui possède une grande cohérence spatiale (tous ses points sources sont cohérents) est le LASER.
````

## Représentation de Fresnel

````{sidebar} Fresnel et somme
Le signal de issu de la superposition des deux ondes n'est a priori pas sinusoïdal. On ne peut lui donner une représentation complexe dans le plan complexe. Par contre, on peut remarquer que $Y(M,t)$ peut se lire comme la somme de abcisses de chaque représentation.

On peut utiliser cette observation pour étudier l'amplitude de variation du signal résultant $Y(M,t)$.
````

````{topic} __Observation sur la représentation de Fresnel__  
```{figure} ./images/Signaux_fresnel_somme.jpg
:name: fig_298
:align: center

```
* si les deux ondes ont à un instant $t$ un déphasage faible l'un par rapport à l'autre, l'onde résultante pourra avoir une forte amplitude à cet instant $t$.
* si les deux ondes ont à un instant $t$ un déphasage proche de $\pi$, l'onde résultante sera nécessairement très faible. Elle peut même être d'amplitude plus faible que les deux ondes initiales, voire s'annuler complètement.

__On observe donc que deux ondes qui vont se superposer en un même point ne donneront pas nécessairement une onde d'amplitude plus importante. Le critère important est le déphasage entre les deux ondes.__



Néanmoins, rappelons que les fréquences mises en jeu peuvent être très rapides, on ne va donc pas forcément pouvoir observer les variations de déphasages. Si les deux ondes ne sont pas de mêmes fréquences, alors le déphasasge instantané entre les deux ondes va passer par toutes les valeurs possibles sur $[0;2 \pi]$.


On peut distinguer trois cas: Cf. la [simulation Geogebra (superposition)](https://stanislas.edunao.com/mod/folder/view.php?id=12899)
* Les ondes ne sont pas de mêmes fréquences on parle d'ondes asynchrones - (ou le déphasage entre les deux est aléatoire) et l'écart en fréquence est grand. Le déphasage entre les deux ondes varie très rapidement: on ne peut observer une telle variation. On réalise alors une moyenne des intensités observés. Tout se passe comme si l'intensité résultante observée était la somme des deux intensités. On retrouve le calcul énergétique réalisé pour l'éclairement moyen.
* Les ondes ne sont pas de mêmes fréquences (on parle d'ondes asynchrones) mais l'écart en fréquence est faible: le signal va apparaître comme presque sinusoïdal mais avec une ampitude variant dans le temps. On parle de __battements__  (cf. suite).
* Les ondes ont la même fréquence (et cohérentes). Le déphasage est alors constant. Comme on va le voir, l'onde résultante est alors sinusoïdale de même pulsation et son amplitude va dépendre du déphasage. On parle d'__interférences__ .
````

## Battements cf. Activités

## Interférences

### Position du problème
On considère deux sources lumineuses qui émettent chacune des ondes lumineuses __cohérentes__ , c'est-à-dire de même fréquence $f_1=f_2=f$ et dont le déphasage en un point donné est constant. On traitera pour simplifier le champ électrique comme une grandeur scalaire E. Les champs électriques des deux ondes s'écrivent:

\begin{align}
E_1(M) &= E_{1m} \cos(2 \pi f t + \phi_{M,1})\\
E_2(M) &= E_{2m} \cos(2 \pi f t + \phi_{M,2})
\end{align}

Comme on va le montrer, on attend alors un déphasage constant et la représentation de Fresnel permet de montrer que l'amplitude résultante va dépendre du déphasage entre les deux ondes. On parlera d'interférences

```{figure} ./images/Signaux_fresnel_somme.jpg
:name: fig_299
:align: center
```

````{important} 
__Onde résultante sinusoïdale__

L'onde résultant de la superposition de deux ondes sinusoïdales cohérentes __de même amplitude__ __$E_0$__  est aussi une onde sinusoïdales de même fréquence $f$ et dont l'amplitude $E_{totalm}$ dépend des amplitudes des ondes qui interfèrent ET du déphasage $\Phi_M = \phi_{M,2} - \phi_{M,1}$ entre les deux ondes.

Le champ électrique peut se mettre sous la forme:

$$
E_{total}(M,t) = A \cos(\Phi_M/2)\cos(2\pi f t +\varphi)
$$
````

````{sidebar} Remarque
Si les deux ondes n'ont pas la même amplitude, on observe aussi un phénomène d'interférences mais un peu plus atténué et l'étude est légèrement différente. On pourra retenir que les conclusions à venir sont les mêmes.

A défaut de démontrer mathématiquement la forme du champ résultant, on s'entraînera à déterminer les valeurs maximales et minimales du champ résultant au moyen de la représentation de Fresnel.
````
````{topic} __Démonstration__  
On sait que $E_{total}(M,t) = E_{m1} \cos(2\pi f t +\phi_{M,1})+ E_{m2} \cos(2\pi f t +\phi_{M,2})$ par principe de superposition. On suppose de plus que $E_{m1} = E_{m2} = E_0$. En utilisant les formules de trigonométrie, il vient:

\begin{align*}
E_{total}(M,t) &= 2 E_0 (\cos(\frac{2\pi f t +\phi_{M,1}-(2\pi f t +\phi_{M,2})}{2})\cos(\frac{2\pi f t +\phi_{M,2}+(2\pi f t +\phi_{M,2})}{2}))\\
 &= 2 E_0 (\cos(\frac{\phi_{M,1}-\phi_{M,2}}{2})\cos(2\pi f t +\frac{\phi_{M,1}+\phi_{M,2}}{2}))
\end{align*}
On obtient l'expression demandée avec: $A = 2 E_0$
````



### Cas extrêmes: Interférences constructives et destructives.

````{important} __Cas extrêmes__
* Pour $\Phi_M = 2 m \pi$ avec $m \in  \mathbb{N}$ la fonction cos est maximale et les amplitudes des deux ondes sont en phase. L'intensité lumineuse est alors maximale. On parle d'__interférences constructives__ . Si l'on place un écran au point considéré, on observera un point très lumineux.
* Pour $\Phi_M = (2 m +1)\pi$ avec $m \in  \mathbb{N}$ la fonction cos est minimale et les amplitudes des deux ondes sont en opposition de phase. L'intensité lumineuse est alors minimale. On parle d'__interférences destructives__ . Si l'on place un écran au point considéré, on observera un point sombre (ou plutôt on observe presque pas de lumière, voire aucune lumière).


```{figure} ./images/Signaux_fresnel_somme.jpg
:name: fig_300
:align: center
```
````

#### Autres grandeurs caractéristiques
Plutôt que de calculer le déphasage, on calculer souvent d'autres termes associées pour savoir les positions d'interférences constructives et destructives.

````{sidebar} __Chemin optique: cas d'un milieu homogène et isotrope__
Dans un milieu homogène est isotrope, le chemin optique sur un chemin SM devient $S = \frac{\lambda_0}{2 \pi} \Phi_{SM}$ où $\Phi_{SM}$ est le déphasage introduit par la propagation de l'onde entre S et M.
````
````{important} 
__Chemin optique__

On définit le chemin optique comme l'intégrale sur le chemin parcouru par la lumière: $S = \int n(M) ds(M)$ où $n(M)$ est l'indice de réfraction au point M et $ds(M)$ la longueur du trajet parcouru par la lumière autour du point M.
````

````{important} 
__Différence de chemin optique__

On définit la différence de chemin optique entre deux rayons par...  la différence $\delta = S_2 - S_1$. Dans le cas d'un milieu homogène et isotrope, cette différence devient:
\begin{align*}
\delta &= n(S_1 M - S_2M)\\
&= \frac{\lambda_0}{2 \pi} \Phi_M
\end{align*}
avec $\Phi_M$ le déphasage de l'onde 2 sur l'onde 1 au point M.
````

````{important} __Intérêt__
La différence de chemin optique présente deux intérêts:
* son expression en fonction des distance parcourues par les rayons permet de le calculer simplement par des considérations géométriques.
* sa relation avec le déphasage montre qu'il va prendre des valeurs particulières pour les cas d'interférences constructives et destructives. En effet:
    * Lors d'interférences constructives, la différence de chemin optique est un nombre entier de fois la longueur d'onde: $\delta = m \lambda_0$
    * Lors d'interférences destructives, la différence de chemin opqitue est un nombre demi-entier de fois la longueur d'onde $\delta = (m + \frac{1}{2}) \lambda_0$

_On pourra donc se servir des considérations géométriques pour calculer la différence de chemin optique et de la relation avec le déphasage pour déterminer les conditions d'interférences constructives et destructives._
````

````{important} 
__Ordre d'interférences__

On définit l'ordre d'interférence en un point M par la grandeur: $p = \frac{\delta}{\lambda_0}=\frac{\Phi_M}{2 \pi}$
````

````{important} __Intérêt__
* Lors d'interférences constructives, l'ordre d'interférence est un entier $m$ avec $m \in \mathbb{B}$ (à relier avec l'entier définit pour la différence de chemin optique)
* Lors d'interférences destructives, l'ordre d'interférence est un demi-entier $m+\frac{1}{2}$ avec $m \in \mathbb{N}$


_L'intérêt du nombre d'interférence est de pouvoir "compter" combien de fois se produisent des interférences constructives entre 2 points $M_1$ et $M_2$. En effet, la propriété précédent montre qu'entre deux de l'espace où se produisent des interférences, si l'ordre d'interférences est monotone sur le déplacement de $M_1$ à $M_2$ alors la différence $p_2 - p_1$ correspond, en valeur entière, au nombre de fois où l'on observera des interférences constructives._
````

````{important} 
__Interfrange__

L'__interfrange__  est la distance entre deux franges d'égales intensités.
````

### Notion de cohérence (en ligne)
````{topic} Cohérence
Lorsque deux ondes sont créées par deux émetteurs, elles sont en général incohérentes car:
* __Incohérence temporelle:__  Souvent les fréquences émises par les deux émetteurs sont différents (on dit qu'elles ne sont pas isochrones ou pas synchrones).
* __Incohérence spatiale:__  Même si les fréquences sont rigoureusement identiques, il faut savoir qu'une onde est souvent émise par intermittence, on parle de paquets d'onde. C'est toujours le cas pour des ondes lumineuses où ces paquets d'ondes correspondent à un paquet de photons (on retrouve ici un peu la nature duelle de la lumière: corpuscule et onde). Or ces petits paquets sont émis de manière aléatoire et donc différemment pour les deux sources: le déphasage initial entre les deux ondes varient de manière aléatoire: les ondes sont incohérentes.

Si les deux ondes sont issues de la même source, elles peuvent (et sont souvent) incohérentes aussi car:
* une même source peut envoyer plusieurs longueurs d'ondes (ex: la lumière blanche): il y a incohérence temporelle.
* elle peut ne pas être ponctuelle mais étendue: on peut alors la considérer comme un ensemble de petite sources ponctuelles incohérentes entre elles dans la plupart des cas. Il y a incohérence spatiale.

Quand l'incohérence devient trop grande, la figure d'interférence est brouillée.
````

### Interférences: Réalisation (en ligne)
````{topic} Réalisation
Si l'on veut réaliser des interférences, il faut donc en général augmenter la cohérence temporelle ET spatiale des sources mises en jeu:
* on peut s'approcher d'une source cohérente temporellement en utilisant des filtres lumineux pour ne laisser passer qu'une petite bande de fréquence.
* on peut diaphragmer la source pour limiter sa taille et augmenter sa cohérence spatiale.
* On peut utiliser un LASER qui permet d'avoir une forte cohérence spatiale ET temporelle sans dispositif supplémentaire. Évidemment, cela restreint le choix des longueurs d'onde.
````
````{topic} Division du front d'onde et division d'amplitude
Si l'on veut créer deux ondes cohérentes, c'est-à-dire de même fréquence ET dont le retard de l'une sur l'autre est constant, le plus simple est donc de partir d'une seule onde issue d'un point source monochromatique (qu'on fabrique comme expliqué précédemment) et la séparer en deux. On utilise deux méthodes:
* __Division du front d'onde.__  Principe: On prend une onde qui s'est étendue en se propageant et on prend deux points de cette onde qu'on retransforme en deux sources (en utilisant le phénomène de diffraction). Exemple: Les fentes d'Young (a) qui seront étudiées par la suite.
* __Division d'amplitude.__  Principe: Quand une onde arrive sur une variation brutale de milieu, elle se sépare en deux: une partie est réfléchie (réflexion), l'autre est transmise (réfraction ou transmission). Pour les ondes électromagnétiques, on retrouve les lois de Snell-Descartes. On a ainsi créer deux ondes cohérentes (b)!

```{figure} ./images/Signaux_division_ondes.jpg
:name: fig_301
:align: center
```
````
