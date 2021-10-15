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
# Superposition de deux ondes: Interférences et battements

## Superposition: Généralités

### Position du problème


On considère deux sources $S_1$ et $S_2$ émettant chacune un signal physique se propageant dans le milieu environnant et représentée par la grandeur Y dont l'expression en un point M à un instant t sera notée $Y(M,t)$. On suppose que ces deux ondes sont sinusoïdales de fréquence $f_1$ et $f_2$. On note:

* $Y_1(M,t) = Y_{1m}\cos(\omega_1 t + \phi_{M,1})$ pour l'onde issue de la source $S_1$ (appelée onde 1).
* $Y_1(M,t) = Y_{2m}\cos(\omega_2 t + \phi_{M,2})$ pour l'onde issue de la source $S_2$ (appelée onde 2).


Pour fixer les idées au moyen d'expériences, les ondes considérées seront par la suite soit des ondes acoustiques, soit des ondes lumineuses. Néanmoins, et sauf précisions contraire, les études réalisées pourront être appliquées à tout type d'onde. On considérera aussi des trajets rectilignes de la lumière. On observera d'ailleurs les phénomènes d'interférences étudiés ensuite sur des ondes de surface.


````{dropdown} Remarque

En pratique, les phases $\phi_{M,2}$ et $\phi_{M,1}$ se déduisent du trajet de l'onde entre la source et le point M.
````

_Rappel : Déphasage_  
_On rappelle que le déphasage d'un signal sinusoïdal 2 sur un autre signal sinusoïdal 1 est la différence de phase:_

\begin{align*}
\Phi_{2/1}(M,t) &= \varphi_{2}(M,t) - \varphi_{1}(M,t)\\
&= \left(\omega_2 - \omega_1\right)t + \phi_{M,2} - \phi_{M,1}
\end{align*}

````{admonition} Définition : Ondes synchrones et cohérentes
:class: tip

Deux ondes sont dites __synchrones__  si elles ont la même fréquence.

Deux ondes sont dites __cohérentes si elles ont la même fréquence ET que leur déphasage initiaux (aux sources) sont constants.__ 

````

````{admonition} Pourquoi deux ondes synchrones peuvent ne pas être cohérentes ?
:class: note
Dans le cas des ondes électromagnétiques, l'émission n'est pas continue. La source émet un train d'onde puis arrête d'émettre puis recommence.

Or la largeur des trains d'ondes et l'espace entre deux émissions sont aléatoires. Il vient que deux points sources, même synchrones vont avoir un déphasage qui va varier aléatoirement. Nous verrons que cela peut-être un problème d'autant que cette incohérence __s'applique aussi entre deux points d'une même source lumineuse étendue__ . La seule source lumineuse qui possède une grande cohérence spatiale (tous ses points sources sont cohérents) est le LASER.
````


__Principe de superposition__  
Pour les ondes étudiées ici, on pourra utiliser le principe de superposition, c'est-à-dire que l'expression de l'onde résultante au point M $y(M,t)$ s'écrit comme la somme:

\begin{equation}
y(M,t) = Y_{1m}\cos(\omega_1 t + \phi_{M,1})+Y_{2m}\cos(\omega_2 t + \phi_{M,2})
\end{equation}

### Représentation de Fresnel

````{admonition} Attention : 
:class: note

Le signal de issu de la superposition des deux ondes n'est a priori pas sinusoïdal. On ne peut lui donner une représentation complexe dans le plan complexe. Par contre, on peut remarquer que $Y(M,t)$ peut se lire comme la somme de abcisses de chaque représentation.

On peut utiliser cette observation pour étudier l'amplitude de variation du signal résultant $Y(M,t)$.

````


__Observation sur la représentation de Fresnel__  
```{figure} ./images/Signaux_fresnel_somme.jpg
:name: fig_298
:align: center

```

* si les deux ondes ont à un instant $t$ un déphasage faible l'un par rapport à l'autre, l'onde résultante pourra avoir une forte amplitude à cet instant $t$.
* si les deux ondes ont à un instant $t$ un déphasage proche de $\pi$, l'onde résultante sera nécessairement très faible. Elle peut même être d'amplitude plus faible que les deux ondes initiales, voire s'annuler complètement.


On observe donc que deux ondes qui vont se superposer en un même point ne donneront pas nécessairement une onde d'amplitude plus importante. Le critère important est le déphasage entre les deux ondes.



Néanmoins, rappelons que les fréquences mises en jeu peuvent être très rapides, on ne va donc pas forcément pouvoir observer les variations de déphasages. Si les deux ondes ne sont pas de mêmes fréquences, alors le déphasasge instantané entre les deux ondes va passer par toutes les valeurs possibles sur $[0;2 \pi]$ (cf. Simulation GEOGEBRA).

On peut distinguer trois cas:

* Les ondes ne sont pas de mêmes fréquences on parle d'ondes asynchrones - (ou le déphasage entre les deux est aléatoire) et l'écart en fréquence est grand. Le déphasage entre les deux ondes varie très rapidement: on ne peut observer une telle variation. On réalise alors une moyenne des intensités observés. Tout se passe comme si l'intensité résultante observée était la somme des deux intensités. On retrouve le calcul énergétique réalisé pour l'éclairement moyen.
* Les ondes ne sont pas de mêmes fréquences (on parle d'ondes asynchrones) mais l'écart en fréquence est faible: le signal va apparaître comme presque sinusoïdal mais avec une ampitude variant dans le temps. On parle de __battements__  (cf. suite).
* Les ondes ont la même fréquence (et cohérentes). Le déphasage est alors constant. Comme on va le voir, l'onde résultante est alors sinusoïdale de même pulsation et son amplitude va dépendre du déphasage. On parle d'__interférences__ .



## Battements

### Ondes asynchrones proches: Battements


__Position du problème__  
On considère deux diapasons identiques dont l'un est monté avec une petite masselotte qui modifie légèrement sa fréquence d'émission. On excite les deux diapasons et on écoute le son obtenus puis on l'enregistre au moyen d'un dispositif {micro+système d'acquisition}. On observe:

Les variations d'amplitude sont lentes de sorte qu'on peut les sentir à l'oreille (cf. Simulation Audacity).



__Modélisation__  
On considère les deux ondes précédentes issues de deux sources $u_1$ et $u_2$ asynchrones de fréquences respectives $f_1$ et $f_2$. On considère qu'il s'agit d'ondes sonores de fréquences très proches l'une de l'autre. On considère de plus pour simplifier que les deux ondes ont la même amplitude de pression: $u_0$ et que le déphasage initial entre les deux sources est constant et nul.


### Battements acoustiques

````{admonition} Exercice 
:class: attention

On considère le problème proposé précédemment.

1. Exprimer la surpression ressentie en un point M.
1. Montrer que celle-ci s'apparente à un signal sonore de fréquence $f_f$ à préciser modulé en amplitude par un sinusoïde à la fréquence $f_m$ à préciser. Représenter graphiquement l'amplitude correspondante.
1. Exprimer l'intensité sonore perçue et montrer qu'elle varie aussi dans le temps.
1. Donner la représentation de Fresnel des deux ondes et de l'onde résultante à différents instants. Retrouver le principe d'une modulation d'amplitude.
1. (Simulation): On pourra chercher, au moyen de logiciels simulant des sons (Ex: Audacity) à partir de quelle fréquence l'on arrive plus à déceler la variation temporelle de l'intensité sonore (c'est un ordre de grandeur car il sera probablement différent pour chacun)


````

## Interférences

### Interférences: Position du problème


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


````{admonition} Fondamental : Onde résultante sinusoïdale
:class: attention

L'onde résultant de la superposition de deux ondes sinusoïdales cohérentes __de même amplitude__ __$E_0$__  est aussi une onde sinusoïdales de même fréquence $f$ et dont l'amplitude $E_{totalm}$ dépend des amplitudes des ondes qui interfèrent ET du déphasage $\Phi_M = \phi_{M,2} - \phi_{M,1}$ entre les deux ondes.

Le champ électrique peut se mettre sous la forme:

\begin{equation}
E_{total}(M,t) = A \cos(\Phi_M/2)\cos(2\pi f t +\varphi)
\end{equation}
````


__Démonstration__  
On sait que $E_{total}(M,t) = E_{m1} \cos(2\pi f t +\phi_{M,1})+ E_{m2} \cos(2\pi f t +\phi_{M,2})$ par principe de superposition. On suppose de plus que $E_{m1} = E_{m2} = E_0$. En utilisant les formules de trigonométrie, il vient:

\begin{align*}
E_{total}(M,t) &= 2 E_0 (\cos(\frac{2\pi f t +\phi_{M,1}-(2\pi f t +\phi_{M,2})}{2})\cos(\frac{2\pi f t +\phi_{M,2}+(2\pi f t +\phi_{M,2})}{2}))\\
 &= 2 E_0 (\cos(\frac{\phi_{M,1}-\phi_{M,2}}{2})\cos(2\pi f t +\frac{\phi_{M,1}+\phi_{M,2}}{2}))
\end{align*}
On obtient l'expression demandée avec: $A = 2 E_0$


````{dropdown} Remarque

Si les deux ondes n'ont pas la même amplitude, on observe aussi un phénomène d'interférences mais un peu plus atténué et l'étude est légèrement différente. On pourra retenir que les conclusions à venir sont les mêmes.

A défaut de démontrer mathématiquement la forme du champ résultant, on s'entraînera à déterminer les valeurs maximales et minimales du champ résultant au moyen de la représentation de Fresnel.
````

### Cas extrêmes: Interférences constructives et destructives.

````{admonition} Fondamental : Cas extrêmes
:class: attention

* Pour $\Phi_M = 2 m \pi$ avec $m \in  \mathbb{N}$ la fonction cos est maximale et les amplitudes des deux ondes sont en phase. L'intensité lumineuse est alors maximale. On parle d'__interférences constructives__ . Si l'on place un écran au point considéré, on observera un point très lumineux.
* Pour $\Phi_M = (2 m +1)\pi$ avec $m \in  \mathbb{N}$ la fonction cos est minimale et les amplitudes des deux ondes sont en opposition de phase. L'intensité lumineuse est alors minimale. On parle d'__interférences destructives__ . Si l'on place un écran au point considéré, on observera un point sombre (ou plutôt on observe presque pas de lumière, voire aucune lumière).


```{figure} ./images/Signaux_fresnel_somme.jpg
:name: fig_300
:align: center

```
````

### Interférences: Autres grandeurs caractéristiques


Plutôt que de calculer le déphasage, on calculer souvent d'autres termes associées pour savoir les positions d'interférences constructives et destructives.


````{admonition} Définition : Chemin optique
:class: tip

On définit le chemin optique comme l'intégrale sur le chemin parcouru par la lumière: $S = \int n(M) ds(M)$ où $n(M)$ est l'indice de réfraction au point M et $ds(M)$ la longueur du trajet parcouru par la lumière autour du point M.

````

````{admonition} Fondamental : Chemin optique: cas d'un milieu homogène et isotrope
:class: attention

Dans un milieu homogène est isotrope, le chemin optique sur un chemin SM devient $S = \frac{\lambda_0}{2 \pi} \Phi_{SM}$ où $\Phi_{SM}$ est le déphasage introduit par la propagation de l'onde entre S et M.
````


__Démonstration__  
Le milieu étant homogène et isotrope, le trajet de la lumière est en ligne droite et $S = \frac{c}{v_{milieu}}SM = \frac{\lambda_0}{2 \pi}k SM = \frac{\lambda_0}{2 \pi} \Phi_{SM}$


````{admonition} Fondamental : Différence de chemin optique
:class: attention

On définit la différence de chemin optique entre deux rayons par...  la différence $\delta = S_2 - S_1$. Dans le cas d'un milieu homogène et isotrope, cette différence devient:

\begin{align*}
\delta &= n(S_1 M - S_2M)\\
&= \frac{\lambda_0}{2 \pi} \Phi_M
\end{align*}
avec $\Phi_M$ le déphasage de l'onde 2 sur l'onde 1 au point M.
````

````{admonition} Fondamental : Intérêt
:class: attention

La différence de chemin optique présente deux intérêts:

* son expression en fonction des distance parcourues par les rayons permet de le calculer simplement par des considérations géométriques.
* sa relation avec le déphasage montre qu'il va prendre des valeurs particulières pour les cas d'interférences constructives et destructives. En effet:
* Lors d'interférences constructives, la différence de chemin optique est un nombre entier de fois la longueur d'onde: $\delta = m \lambda_0$
* Lors d'interférences destructives, la différence de chemin opqitue est un nombre demi-entier de fois la longueur d'onde $\delta = (m + \frac{1}{2}) \lambda_0$



On pourra donc se servir des considérations géométriques pour calculer la différence de chemin optique et de la relation avec le déphasage pour déterminer les conditions d'interférences constructives et destructives.
````

````{admonition} Attention : Calcul de la différence de chemin optique en pratique
:class: note

En pratique, le milieu peut être homogène __par morceau__ . Il conviendra donc de découper le trajet du rayon en plusieurs morceaux de manière à calculer la différence de chemin optique au moyen des outils présentés précédemment.

````

````{admonition} Définition : Ordre d'interférences
:class: tip

On définit l'ordre d'interférence en un point M par la grandeur: $p = \frac{\delta}{\lambda_0}=\frac{\Phi_M}{2 \pi}$

````

````{admonition} Fondamental : Intérêt
:class: attention

* Lors d'interférences constructives, l'ordre d'interférence est un entier $m$ avec $m \in \mathbb{B}$ (à relier avec l'entier définit pour la différence de chemin optique)
* Lors d'interférences destructives, l'ordre d'interférence est un demi-entier $m+\frac{1}{2}$ avec $m \in \mathbb{N}$


L'intérêt du nombre d'interférence est de pouvoir "compter" combien de fois se produisent des interférences constructives entre 2 points $M_1$ et $M_2$. En effet, la propriété précédent montre qu'entre deux de l'espace où se produisent des interférences, si l'ordre d'interférences est monotone sur le déplacement de $M_1$ à $M_2$ alors la différence $p_2 - p_1$ correspond, en valeur entière, au nombre de fois où l'on observera des interférences constructives.

Un exemple sera donné par la suite sur les fentes d'Young pour comprendre son utilisation.
````

````{dropdown} Remarque

__Différence de marche__  
On définit la différence de marche comme la différence $SM_2 - SM_1$. Cette différence de marche n'a d'intérêt que si le milieu est homogène d'indice égal à 1. Nous parlons de cette grandeur ici car elle pourra être rencontrée dans certains exercices.
````

### Notion de cohérence

_Rappel : Ondes cohérentes_  
_On rappelle que les interférences ne se produisent QUE si les ondes sont cohérentes, c'est-à-dire de même fréquences et de déphasage constant._

Lorsque deux ondes sont créées par deux émetteurs, elles sont en général incohérentes car:

* __Incohérence temporelle:__  Souvent les fréquences émises par les deux émetteurs sont différents (on dit qu'elles ne sont pas isochrones ou pas synchrones).
* __Incohérence spatiale:__  Même si les fréquences sont rigoureusement identiques, il faut savoir qu'une onde est souvent émise par intermittence, on parle de paquets d'onde. C'est toujours le cas pour des ondes lumineuses où ces paquets d'ondes correspondent à un paquet de photons (on retrouve ici un peu la nature duelle de la lumière: corpuscule et onde). Or ces petits paquets sont émis de manière aléatoire et donc différemment pour les deux sources: le déphasage initial entre les deux ondes varient de manière aléatoire: les ondes sont incohérentes.


Si les deux ondes sont issues de la même source, elles peuvent (et sont souvent) incohérentes aussi car:

* une même source peut envoyer plusieurs longueurs d'ondes (ex: la lumière blanche): il y a incohérence temporelle.
* elle peut ne pas être ponctuelle mais étendue: on peut alors la considérer comme un ensemble de petite sources ponctuelles incohérentes entre elles dans la plupart des cas. Il y a incohérence spatiale.



````{admonition} Fondamental : 
:class: attention

Les détails de cette études seront précisées par la suite mais en général, une perte de cohérence (temporelle ou spatiale) entraîne un __brouillage des interférences__ , c'est-à-dire que le contraste entre les zones claires (interférences constructives) et les zones sombres (interférences destructives) devient plus faible ce qui peut même entrainer la disparition complète des interférences.
````

### Interférences: Réalisation


Si l'on veut réaliser des interférences, il faut donc en général augmenter la cohérence temporelle ET spatiale des sources mises en jeu:

* on peut s'approcher d'une source cohérente temporellement en utilisant des filtres lumineux pour ne laisser passer qu'une petite bande de fréquence.
* on peut diaphragmer la source pour limiter sa taille et augmenter sa cohérence spatiale.
* On peut utiliser un LASER qui permet d'avoir une forte cohérence spatiale ET temporelle sans dispositif supplémentaire. Évidemment, cela restreint le choix des longueurs d'onde.



````{admonition} Exemple : Division du front d'onde et division d'amplitude
:class: tip, dropdown

Si l'on veut créer deux ondes cohérentes, c'est-à-dire de même fréquence ET dont le retard de l'une sur l'autre est constant, le plus simple est donc de partir d'une seule onde issue d'un point source monochromatique (qu'on fabrique comme expliqué précédemment) et la séparer en deux. On utilise deux méthodes:

* __Division du front d'onde.__  Principe: On prend une onde qui s'est étendue en se propageant et on prend deux points de cette onde qu'on retransforme en deux sources (en utilisant le phénomène de diffraction). Exemple: Les fentes d'Young (a) qui seront étudiées par la suite.
* __Division d'amplitude.__  Principe: Quand une onde arrive sur une variation brutale de milieu, elle se sépare en deux: une partie est réfléchie (réflexion), l'autre est transmise (réfraction ou transmission). Pour les ondes électromagnétiques, on retrouve les lois de Snell-Descartes. On a ainsi créer deux ondes cohérentes (b)!


```{figure} ./images/Signaux_division_ondes.jpg
:name: fig_301
:align: center

```
````

### Interfrange

````{dropdown} Remarque

Les grandeurs précédentes montre que les positions correspondant à des interférences constructives (ou destructives) vont former des formes géométriques (surface, franges, hyerpoloïde... ).

Dans le cas très fréquents des franges (droite de même ordre d'interférence sur un écran), on définit l'__interfrange__  comme la distance entre deux franges d'égales intensités.

```{figure} ./images/Signaux_3_Interference.jpg
:name: fig_302
:align: center

```

Sur l'exemple ci-avant, on pourrait mesurer la distance entre deux franges brillantes: elle correspondrait à l'interfrange.
````

### Fentes d'Young

````{admonition} Exercice 
:class: attention

Un éclairage LASER cohérent et monochromatique de longueur d'onde $\lambda_0$ éclaire un ensemble de deux fentes parallèles de longueur L et de largeur $\epsilon$ distantes l'une de l'autre de $a$. On suppose que $L\gg a$ et $a\gg \epsilon$ de sorte qu'on peut assimiler les fentes à des fentes de longueur infinies et d'épaisseur nulle.

On place un écran parallèle aux fentes à une distance D des fentes telle que $D>>a$ et on visualise la figure lumineuse en une zone proche du centre de l'écran (défini en regard du centre de la double fente). La figure, appelée figure d'interférences obtenues, est données figure suivante (la courbe correspond au profil d'intensité mesuré grâce à un capteur CCD).

```{figure} ./images/Signaux_young_schema.jpg
:name: fig_303
:align: center

```

La diffraction permet de considérer les deux fentes $S_1$ et $S_2$ comme de nouvelles sources (des sources secondaires) qui émettent dans (presque) toutes les directions. Les interférences ont lieu dans tout une zone d'espace: on parle d'interférences délocalisées.

1. Déterminer la différence de chemin optique en un point M de coordonnées $(x;0)$ sur l'écran sans approximation puis simplifier l'expressoin obtenue pour $x\ll D$.
1. En déduire l'ordre d'interférence et le déphasage entre les deux ondes dans le cadre de l'approximation $x\ll D$.
1. Déterminer les positions où l'interférences est contructives, destructives. Commenter la forme des zones claires et sombres.
1. Déterminer l'interfrange, distance entre deux franges d'égales intensité.
1. Comparer les données aux observations expérimentales faites ci-dessous.


```{figure} ./images/Signaux_3_Interference.jpg
:name: fig_304
:align: center

```

Intérêt de l'ordre d'interéférences

1. Exprimer l'ordre d'interférence au centre de la figure (appelé $O_1$). Correspond-il à une frange brillante ou sombre?
1. Exprimer l'ordre d'interférence en un point M de l'écran situé à une abscisse x.
1. Exprimer au moyen de l'interfrange le nombre de franges située entre $O_1$ et M. Retrouver l'interprétation de l'interfrange.


````
````{dropdown} Démonstration

 

__Calcul de la différence de chemin optique__  
Le chemin parcouru par le premier rayon est $SS_1 M$ et le chemin parcouru par le second rayon est $SS_2 M$. Les portions $SS_1$ et $SS_2$ étant identique, la différence de marche (qui est aussi la différence de chemin optique puisque $n=1$) est la même. Il vient $\delta = S_2 M - S_1 M$ soit:

\begin{align*}
\delta &= \sqrt{{\left(\frac{a}{2}- x\right)}^2 + D^2} - \sqrt{{\left(\frac{a}{2}+ x\right)}^2 + D^2}\\
&= D\left(\sqrt{{\left(\frac{\frac{a}{2}- x}{D}\right)}^2 + 1} - \sqrt{{\left(\frac{\frac{a}{2}+ x}{D}\right)}^2 + 1}\right)\\
&\approx D\left({1 + \frac{1}{2}\left(\frac{\frac{a}{2}- x}{D}\right)}^2 - \left(1 + \frac{1}{2}{\left(\frac{\frac{a}{2}+ x}{D}\right)}^2 + 1\right)\right)\\
&\approx - \frac{ax}{D}
\end{align*}

__Déphasage et ordre d'interférence__  
\begin{align*}
\Phi &= \frac{2 \pi \delta}{\lambda_0}\\
&\approx - \frac{2\pi ax}{D\lambda_0}\\
p &= \frac{\delta}{\lambda_0}\\
&=\frac{ax}{D\lambda_0}
\end{align*}

__Interférences constructives et destructives__  
Les interférences constructives sont obtenues là où le déphasage est de la forme $2m\pi$ avec $m \in \mathbb{Z}$ et les interférences destructives sont obtenues là où le déphasage est de la forme $(2m+1)\pi$ avec $m \in \mathbb{Z}$.

\begin{align*}
&- \frac{2\pi ax_{constructif}}{D\lambda_0} = 2m \pi \\
& \Longrightarrow x_{constructif} = \frac{D \lambda_0 m}{ a}\\
&- \frac{2\pi ax_{destructif}}{D\lambda_0} = (2m + 1) \pi \\
& \Longrightarrow x_{destructif} = \frac{D \lambda_0 (m + 1/2)}{ a}
\end{align*}
Les zones claires et sombres correspondent à des zones où x est fixé mais la coordonnées transverses y est quelconque: les zones claires et sombres seront des franges.


__Interfrange et interférométrie.__  
L'interfrange est l'écart minimale entre deux franges d'égales intensités (brillantes par exemples) donc soit: $i = x_{m+1} - x_{m} = \frac{D\lambda_0}{a}$. On observe que l'interfrange (grandeur mesurable est d'__autant plus grande que l'écart entre les fentes est petit__ : on peut donc remonter à une distance très petite en la transformation en une distance très grande, mesurable à notre échelle: c'est le grand intérêt de l'__interférométrie__ .


__Figure d'interférences__  
On observe bien l'alternance de franges brillantes et sombres comme prévu.

Par contre, on observe une diminution de l'intensité quand on s'éloigne du bord qui n'est pas prévu par la théorie. Cela est du au phénomène de diffraction. Ce dernier élargie les faisceau au niveu des fentes permettant aux deux faisceaux de se rencontrer, __d'interférer__ . Mais cet élargissement est limité à un cône et en dehors de ce cône, l'intensité chute diminuant l'intensité des raies observées. Cette diminution n'est pas brutale mais suit un profil similaire à celui observé pour la diffraction seule dans le chaptre précédent.


__Ordre d'interférence__  
Au centre, $p=0$, on observe une frange brillante.

En un point d'abscisse x, l'ordre d'interférence est $p = \frac{ ax}{D\lambda_0}$

Entre O et M, le nombre de franges brillantes est $\frac{x}{i}= \frac{ax}{D\lambda_0} = p$: on retrouve le fait que la différence d'ordre d'interférence entre deux points correspond au nombre de franges brillantes visible (attention, il faut que l'ordre d'interférence soit monotone entre les deux points).


```{dropdown} Remarque

__Notation complexe__  
Dans le cas d'ondes cohérentes, on travaille avec un ensemble d'ondes de même fréquence dont la somme est une onde sinusoïdale de même fréquence. On dispose alors de deux outils très puissants pour étudier les interférences:

* la représentation de Fresnel
* la représentation complexe des grandeurs sinusoïdales


Un exercice sera proposé sur ces méthodes et un devoir libre permet de voir comme ces outils permettent de généraliser l'étude précédente à la superposition de N ondes ($N > 2$).
```
````

### Fentes d'Young: Perte de cohérence temporelle


__La taille de l'interfrange varie en fonction de la longueur d'onde/__  Si on superpose deux couleurs (en envoyant une lumière qui n'est pas monochromatique), leur figure d'interférence va simplement se superposer (__ce sont deux ondes qui n'ont pas la même longueur d'onde donc il ne se produit pas d'interférences: on somme les intensités__ ).

Il se passe la même chose avec la lumière blanche: on observe une superposition continue de figure d'interférences décalées qui produisent un phénomène d'irisation. L'image est plus flou à cause des superposition: on parle de __décohérence temporelle__ .

```{figure} ./images/Signaux_3_Coherence.jpg
:name: fig_305
:align: center

```


### Fentes d'Young: Interférences à l'infini


Il est très fréquent qu'on s'intéresse à une figure d'interférence à l'infini. Nous allons voir comme la traiter puis comment traiter sa projection.


````{admonition} Exercice 
:class: attention

On considère toujours le dispositif des fentes d'Young mais on supprime l'écran et on s'intéresse à la figure d'interférences observées à l'infini (celle qu'observerait un oeil emmétrope au repos se plaçant à la place de l'écran - attention en pratique, il ne faut pas le faire si c'est un LASER !).

1. Quelle grandeur va alors caractériser un point de l'image à l'infini ?
1. En utilisant le théorème de Malus et le principe de retour inverse, montrer que la différence de chemin optique se limite à la distance entre $S_2$ et le projeté de $S_1$ sur le rayon 2. En déduire la différence de chemin optique.
1. Exprimer alors les conditions d'intérférence constructives et destructives.
1. Comment faire pour observer la figure d'interférences à l'infini...  sur un écran. Déduire alors les conditions d'interférences constructives et l'interfrange sur l'écran.
````

````{dropdown} Démonstration

 

__Image à l'infini__  
Un point-image à l'infini est caractérisé par l'angle (noté $\theta_S$ ici) que fait le faisceau de rayon parallèle qui point vers le points avec l'axe optique (ici la médiane aux deux fentes). 

```{figure} ./images/Signaux_young_infini.jpg
:name: fig_306
:align: center

```

Deux rayons issus des fentes et interférant en un point repérant par un angle $\theta$ seront donc deux rayons parallèles passant par $S_1$ et $S_2$ et faisant un angle $\theta$ avec l'axe optique (comme représenté ci-avant).

Si l'on considère deux rayons issus du point image et se dirigeant vers les fentes, le théorème de Malus assure que les front d'onde sont perpendiculaire donc le déphasage entre deux plans perpendiculaire aux rayons est nul. Il reste que le déphasage entre les deux rayons quand il arrive aux fentes se résume au retard à la propagation associé au petit chemin supplémentaire parcouru par le rayon 2 pour aller du projeté de $S_1$ sur le rayon 2 (point noté H sur le même front d'onde que $S_1$) jusqu'au point $S_2$.

Par principe de retour inverse, la lumière emprunte le même chemin pour aller des fentes au point objet et le déphasage entre les deux rayons sera le même que dans l'autre sens. Il vient que la différence de chemin optique sera $nS_2 H = S_2 H = a \sin \theta_S$.

On en déduit la condition d'interférence constructive: $a \sin \theta_S = m \lambda_0$ avec $m \in \mathbb{Z}$.

On déterminera de la même manière la condition d'interférence destructive.

Pour observer la figure d'interférence à l'infini sur un écran, il faut la __projeter au moyen d'une lentille__ . On place l'écran dans le plan focal de la lentille qui est alors conjugué avec un objet à l'infini soit la figure d'interférence à l'infini.
````

````{admonition} Attention : Utilisation d'une lentille
:class: note

Comme on peut le voir sur l'exemple ci-dessous, les rayons sont déviés par la lentille mais __on ne peut pas utiliser une somme par morceau des trajets car la schématisation de Gauss ne modélise pas l'épaisseur de la lentille__ . Il faut utiliser une autre méthode:

1. On déterminer l'antécédent de l'écran par la lentille (en général, c'est l'infini)
1. On détermine la figure d'interférence dans le plan de l'antécédent
1. On relie les caractéristique d'un point de l'antécédent à celui d'un point sur l'écran.


```{figure} ./images/Signaux_Correction_Lentilles.jpg
:name: fig_307
:align: center

```

````

__Interférences dans le plan focal de la lentille__  
On a placé l'écran de sorte qu'il soit conjugué avec le plan objet à l'infini donc la figure d'interférence sur l'écran est conjugué à celle à l'infini sans la lentille.

On a déjà déterminer les caractéristiques de la figure d'interférence à l'infini.

Pour un point M situé à une distance x de l'axe optique, on peut construire les rayons incidents (faisceau de rayons parallèles) en utilisant les règles habituelles: ici on trace un rayon sortant passe par M et le centre optique vient d'un rayon non dévié. Les deux rayons incident passant par les sources et ressortant par M doivent être parallèles à ce rayon, d'où la construction.

Il vient que l'angle que fait le faisceau incident avec l'axe optique est $\theta \approx \tan \theta = \frac{x}{f'}$ (on utilise les conditions de Gauss pour réaliser un stigmatisme).

Dans les conditions d'interférences constructives, on a la relation $\theta \approx \sin \theta = m \frac{\lambda_0}{a}$ soit une condition d'interférence constructive sur l'écran: $x =\frac{mf' \lambda_0}{a}$.

L'interfrange est donc $i = \frac{f' \lambda_0}{a}$.

```{figure} ./images/lentille.png
:name: fig_308
:align: center

```

## Exercices d'application

### Battements lumineux

````{admonition} Exercice 
:class: attention

En comparant des ordres de grandeurs adaptés, montrer qu'on ne peut observer un phénomène de "battements lumineux".

````

### Bilan sur les interférences

````{admonition} Exercice 
:class: attention

Reproduire dans un tableau le bilan des grandeurs caractéristiques qu'on peut calculer pour étudier une figure d'interférences et donner les valeurs possibles qu'elles peuvent prendre pour des cas d'interférences constructives et des cas d'interférences destructives.

````

## Travaux dirigés

### Trous d'Young. Représentation de Fresnel

````{admonition} Exercice 
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
1. Soit les points $M_1(\frac{D_2 \lambda}{2a};0)$ et $M_1(\frac{D_2 \lambda}{a};0)$ et les phases à l'origine des rayons passant par le trou $S_1$ aux points A, $M_1$ et $M_2$: $\phi_A$, $\phi_1$ et $\phi_2$ (on les supposera toutes incluses dans $[0;\pi/2]$).
    1. Donner la représentation de Fresnel de $E(x,t)$ du rayon passant par le trou $S_1$ aux points A, $M_1$ et $M_2$
    1. Faire de même pour l'amplitude du rayon passant par le trou $S_2$ aux mêmes points.
    1. Déduire graphiquement l'amplitude de l'onde résultante pour les positions de x proposée.
1. Déterminer par le calcul l'amplitude complexe de l'onde résultante en un point de coordonnées $(y_M;0)$ puis son amplitude réelle. Déterminer alors les positions des franges brillantes et des franges sombres ainsi que l'interfrange.
1. On déplace la source S d'une distance d dans la direction Oy. On suppose les résultats précédents toujours vrais, déterminer le nombre de franges brillantes que l'on voit défiler au point $A(0;0)$ sur l'écran pendant l'opération.


````

### Doublet du sodium.

````{admonition} Exercice 
:class: attention

On considère l'expérience des trous d'Young présentées dans l'exercice précédent. On se place dans le même cadre d'approximation de sorte que pour une lumière monochromatique de longueur d'onde $\lambda$, on obtiendra les mêmes résultats. Pour un point M de l'écran, le champ électrique s'écrit:

\begin{equation}
E(M,t) = 2 E_{1m} \cos(\frac{\pi a y_M}{\lambda D_2}) \cos(\omega t - \Phi_M)
\end{equation}
avec $\Phi_M$ un terme de phase inutile ici.

Un capteur de lumière (capteur CCD) parcourt à une vitesse $v$ l'axe Ay de l'écran et fournit une tension $U(t)$ proportionnelle à l'éclairement $I$ où il se trouve.

1. Déterminer l'expression de $U(t)$. En déduire le spectre de Fourier de $U(t)$. Justifier que la détermination expérimentale du spectre permet de remonter à la longueur d'onde de la lumière incidente.
1. On remplace la source monochromatique par une lampe spectrale au sodium émettant deux longueurs d'onde $\lambda_1=\frac{2 \pi}{k_1}$ et $\lambda_2 = \frac{2 \pi}{k_2}$ (on pose $\lambda_2<\lambda_1$). On note $k_m=\frac{k_1+k_2}{2}$ et $\Delta k = \frac{k_2 - k_1}{2}$.
    1.Pourquoi peut-on calculer l'éclairement causé par chaque longueur d'onde indépendamment? En déduire l'éclairement total $I_T(x)$ puis la tension mesurée $U_T(t)$.
    1. Montrer que $U_T(t)$ se décompose en une somme de deux sinusoïdes dont on déterminera les fréquences. Représenter graphiquement $U_T(t)$ et son spectre. 
    1. Justifier que la détermination du spectre de $U_T(t)$ permet de remonter aux deux longueurs d'onde $\lambda_1$ et $\lambda_2$.
    1. Montrer aussi que l'étude graphique de l'évolution temporelle de $U_T(t)$ permettrait de déterminer $k_m$ et $\Delta k$ et donc les deux longueurs d'onde, préciser clairement la méthode.


````


