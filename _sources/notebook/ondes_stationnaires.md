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
# Ondes stationnaires

## Généralités

### Présentation

````{important} __Définition : Onde stationnaire__

Une onde stationnaire est le phénomène résultant de la propagation simultanée dans des sens opposés de plusieurs ondes de même fréquence et de même amplitude, dans le même milieu physique, qui forme une figure dont certains éléments sont fixes dans le temps.

````

````{important} __Fondamental : Expression mathématique__

Une onde stationnaire peut s'écrire sous la forme:

\begin{equation}
y(x,t) = f(x)g(t) = A \sin (\omega t + \varphi) \sin (k x + \psi)
\end{equation}
````


On peut très bien remplacer les fonctions sinus par des fonctions cosinus.

On généralisera cette notion d'onde stationnaire par les états stationnaires en mécanique quantique. Le terme en $g(t)$ prend alors une autre forme (complexe).

Par extension, on appelle parfois onde stationnaire la superposition de plusieurs ondes stationnaires de même fréquence.

Par le suite, on traitera souvent l'expression proposées avec des phases à l'origine nulle. Pour l'origine des temps, cela ne pose aucun problème puisqu'on peut la choisir. Pour l'origine des positions, il faudra faire attention car on peut se retrouver quelque fois avec des phases à l'origine spatiale non nulle.


````{important} __Fondamental : Analyse. Noeuds et ventre.__

Le terme __stationnaire__  est associé au fait que le temps et l'espace sont maintenant séparé dans deux fonctions. Il n'y a ainsi plus de propagation (cf. Animation ci-après).

```{figure} ./images/Standing_wave.gif
:name: fig_309
:align: center

```

On observe qu'en certains points, la grandeur $y(x,t)$ __est toujours nulle__ : on appelle ces points les __noeuds.__ 

On observe qu'en certains points, la grandeur $y(x,t)$ __est toujours maximale__  (relativement au reste de la corde): on appelle ces points les __ventres.__ 

Le caractère stationnaire implique que les noeuds et les ventres sont __fixes.__ 
````

### Superposition et réflexion totale

````{important} __Fondamental : Superposition__

On rappelle qu'une onde stationnaire est la superposition de deux ondes l'une progressive et l'autre régressive __de même amplitude et de même fréquence__  (cf. ANIMATION ci-après).

\begin{align*}
y(x,t) &= A \cos \left(\omega t - kx\right) - A \cos \left(\omega t + kx\right)\\
&= 2 A \sin \omega t \sin kx
\end{align*}
```{figure} ./images/Standing_wave_2.gif
:name: fig_310
:align: center

```
````

````{dropdown} Remarque

Nous allons expliquer par la suite pourquoi on a mis un signe "-" déphasage de $\pi$ pour l'onde régressive.

On peut tout à fait réaliser le même genre de calcul avec un signe "+" ou en écrivant les expressions des ondes avec des sinus mais attention, __l'expression de l'onde stationnaire obtenue va alors changer__ .
````

````{important} __Fondamental : Superposition et réflexion totale__

La manière la plus simple de réaliser une onde stationnaire et de __réfléchir parfaitement__  l'onde progressive (incidente). Dans ces conditions, l'onde réfléchie (régressive) aura la même amplitude.

Une réflexion totale impose en général un __noeud__ pour l'onde stationnaire pour l'une des grandeurs. C'est en utilisant ces conditions qu'on démontre que l'onde résultante sera stationnaire (cf. exemple).
````

````{admonition} Exemple : Exemple de réalisation d'une réflexion totale
:class: tip, dropdown

* Miroir parfait: il permet la réflexion totale d'une onde électromagnétique en impose un champ électrique nul à sa surface.
* Corde: un point d'attache impose une vitesse de vibration nulle et une réflexion parfaite.

````

````{attention}

L'argument "réflexion parfaite" ne suffit pas pour justifier l'existence d'une onde stationnaire. Il faut utilise la nullité de la grandeur associée pour le démontrer. Nous allons voir la méthode sur l'exemple de la corde.

````

Si on a le choix, il est conseillé de l'origine des abscisses au point où se produit la réflexion parfaite de manière à éviter certains problèmes de phase.


### Réflexion parfait sur une corde

````{admonition} Exercice 
:class: attention

On considère une corde tendue par une tension T horizontale de masse linéique $\mu$. La célérité des ondes mécaniques qui se propagent sur la corde est alors $c = \sqrt{\frac{T}{\mu}}$. On notera $k = \frac{2\pi}{\lambda}$ avec $\lambda$ la longueur d'onde d'une onde progressive. La corde est attaché en un point A. Une onde progressive harmonique se propose dans le sens des x positifs de $-\infty$ vers le point A.

1. Justifier l'existence d'une onde réfléchie. En déduire l'expression générale de la côte verticale $y(x,t)$ de la corde.
1. Que vaut y au point A? En déduire que l'onde résultante est une onde stationnaire.
1. Déterminer la position des noeuds et des ventres de l'onde.


````
````{dropdown} Démonstration

 

__Existence d'une onde réfléchie__  
Une onde transporte de l'énergie. Or au point A, il n'y a pas de mouvement, donc par d'énergie transmise vers les x positifs. Il vient que cette énergie est nécessairement réfléchie d'où l'existence d'une onde réfléchie:

\begin{equation}
y(x,t) = A \cos \left(\omega t - kx\right) + B \cos \left(\omega t + kx + \varphi\right)
\end{equation}

```{attention}

On n'écrit pas tout de suite que les amplitudes sont égales, il va falloir le prouver.

On peut choisir la phase à l'origine nulle pour l'onde incidente puisque qu'on fixer l'origine des phases.

Mais on ne peut le faire qu'une seule fois (on fixe la "référence des phases", c'est pourquoi on écrit pas que la phase à l'origine pour l'onde réfléchie est nulle, il faut aussi le prouver (et ça peut être faux si la réflexion n'a pas lieu en $x=0$.

```

__Onde stationnaire__  
On pose $x_A = 0$. On a y(0,t) = 0 pour tout t. Il vient:

\begin{align*}
y(0,t) = 0 &= A \cos \omega t + B \cos \omega t +\varphi \\
0 &= \left(A + B \cos \varphi\right)\cos \omega t - B \sin \varphi \sin \omega t
\end{align*}
La dernière équation devant être vraie pour tout t, il vient que $B \sin \varphi = 0$ et $A + B \cos \varphi =0$ soit trivialement $\varphi = 0$ et $A = -B$ soit:

\begin{align*}
y(x,t) &= A \cos \left(\omega t - kx\right) - A \cos \left(\omega t + kx\right)\\
&= 2 A \sin \omega t \sin kx
\end{align*}
L'onde résultante est bien une onde stationnaire.


__Noeud et ventre__  
Les noeuds sont tels que $y(x,t) = 0$ à tout instant soit $\sin kx = 0$ soit $ x = \frac{m\pi}{k} = \frac{m\lambda}{2}$ avec m un entier. On observe que les noeuds sont espacés d'une demie longueur d'onde.

Les ventres sont tels que l'amplitude de $y(x,t)$ est maximale soit $\sin kx = 1$ soit $x = \frac{m\pi}{k} + \frac{\pi}{2 k}= \frac{m\lambda}{2} + \frac{\lambda}{4}$. A nouveau les ventres sont espacés d'une demi longueur d'onde. On retrouve l'allure observée précédemment.

```{figure} ./images/Standing_wave.gif
:name: fig_311
:align: center

```

````

## Modes propres: Exemple de la corde de Melde

### Position du problème


On considère une corde de longueur L fixée aux deux points extrêmes A et B sous une tension $\overrightarrow{T}$. La corde peut vibrer et une onde mécanique se propage le long de la corde. On rappelle que pour une onde mécanique, on peut décrire la vibration de la corde se propageant par l'écart de la position d'un point de la corde à sa position d'équilibre (la corde tendue au repos est supposée être horizontale): $y(x,t)$.

Quand l'onde se propage, elle arrive au bout de la corde. Elle est alors réfléchie et se propage dans l'autre sens pour être à nouveau réfléchie et ainsi de suite. Cette série d'onde réfléchies se superpose. On peut «regrouper» l'ensemble des ondes obtenues en deux ondes:

* une onde mécanique se propageant suivant les x croissants: $y_{+}(x,t)=y_{+}(t- \frac{x}{v_{onde}})$
* une onde mécanique se propageant suivant les x décroissants: $y_{-}(x,t)=y_{-}(t+ \frac{x}{v_{onde}})$


L'onde résultante totale donne la position instantanée de chaque point de la corde:

\begin{equation}
y(x,t)=y_{+}(t- \frac{x}{v_{onde}}) + y_{-}(t+ \frac{x}{v_{onde}})
\end{equation}


__Conditions aux limites__  
On ne peut choisir arbitrairement la forme de l'onde car on impose __des conditions aux limites: l'amplitude aux points extrêmes x=0 et x= L doit nécessairement être nulle (corde fixée).__ 



__Solution harmoniques__  
On ne va pas chercher à déterminer une solution quelconque. On va chercher une solution __harmonique__  c'est-à-dire résultant de la superposition de deux ondes progressives harmoniques (l'une dans le sens de x positifs et l'autre dans le sens des x négatifs).

On pourra noter que la structure de l'onde progressive impose la structure de l'onde régressive.

Le choix d'étudier les ondes harmoniques s'explique par la linéarité du système (cf. deuxième année) et le principe de décomposition en série de Fourier (cf. début d'année).

L'onde résultante a donc la forme:

\begin{equation}
y(x,t)=y_{+m}\sin(\omega t- kx) + y_{-m}\sin(\omega t+ kx +\varphi)
\end{equation}

### Ondes stationnaire

_Rappel :_  
_On rappelle qu'une des deux conditions aux limites permet de montrer que l'onde est stationnaire. On utilise ici la condition $y(0,t) = 0$ pour montrer que l'onde peut se mettre sous la forme_

\begin{equation}
y(x,t)=Y_m \cos(\omega t)\sin(k x) = Y \cos(\omega t)\sin(\frac{2 \pi}{\lambda} x)
\end{equation}

````{dropdown} Complément : Solution stationnaire

On peut montrer à l'aide des équations du système (cf. deuxième année) qu'une solution stationnaire de la forme $y(x,t) = f(t) g(x)$ est nécessaire de forme sinusoïdale.
````


### Modes propres


Nous allons maintenant utiliser la deuxième condition aux limites. Celle-ci est fondamental puisqu'elle conduit à la __quantification des modes propres__ .


````{important} __Fondamental : Modes propres de la corde de Melde__

Pour qu'une onde sinusoïdale de fréquence f puisse exister dans une corde de longueur L où la vitesse de propagation des ondes mécanique est $v_{onde}$, il faut que $f=n \frac{v_{onde}}{2L}$ soit une longueur d'onde: $\lambda=\frac{2L}{n}$ avec $n \in \mathbb{N}$.

La forme de l'onde résultante peut s'écrire:

\begin{equation}
y(x,t)=Y_n \cos(\omega_n t)\sin(k_n x) = Y_n \cos(\omega_n t)\sin(\frac{2 \pi}{\lambda_n} x)
\end{equation}
````


__Démonstration (méthode graphique)__  
On connait que l'onde est stationnaire. La forme spatiale de l'onde est alors un sinusoïde. Sauf qu'on impose deux noeuds en x=0 et x=L. On peut ainsi chercher à tracer les formes sinusoïdales qui coïncident avec ces conditions aux limites.

```{figure} ./images/Vibration_corde_trois_modes_petit.gif
:name: fig_312
:align: center

```

La représentation précédente (ANIMATION) montre les trois premiers modes propres possibles. Dans le premier, on dessine une demi longueur d'onde sur une longueur de corde, dans le second une longueur d'onde et dans le troisième une longueur d'onde est demie.

On peut généraliser cette observation en remarquant que les conditions aux limites imposent que la longueur de corde soit égale à un nombre entier ou demi-entier de longueur d'onde soit $L = \frac{m\lambda}{2}$ avec m un entiersoit la relation donnée.



__Démonstration (méthode mathématique).__  
Utilisons la deuxième conditions aux limites $y(L,t)=0$: $y(L,t)=Y_m \cos(\omega t)\sin(k L) = 0$.

A nouveau, cette relation doit être vérifiée pour tout t, donc $\sin(kL) =0$ soit: $kL = n \pi$ avec $n \in \mathbb{N}$. Les relations entre $k,f$ et $\lambda$ donnent les expressions proposées.


````{dropdown} Remarque

Il et important de savoir faire les deux démonstration. Dans des cas où l'autre extrémité est un ventre, on se limitera à la démonstration graphique.
````

### Interprétation


L'étude précédente permet de mettre en avant les vibrations pouvant exister pour la corde (supposée parfaite puisqu'on néglige toute perte).

Elle a l'avantage d'être simple. Néanmoins, pour qu'une vibration sinusoïdale se produise dans la corde à une fréquence $f_n$, il faut des conditions particulières: une excitation initiale sinusoïdale (cf. TP corde de Melde). Si l'on s'intéresse au principe des instruments de musique, une telle excitation n'est pas réalisée. L'observation du spectre créé par la corde est alors plus complexe: il s'agit d'une superposition des ondes sinusoïdales pures. Dans le langage acoustique, on distingue alors la fréquence la plus faible, correspondant à la hauteur du son ($f_1$ normalement), c'est le __fondamental__ . Et les fréquences suivantes ($f_n$ avec n>1), toutes des multiples du fondamental qui enrichissent le son pour former son timbre: ce sont les __harmoniques__ .



__Conditions initiales et harmoniques__  
Les conditions initiales permettent de déterminer l'amplitude du fondamental et des harmonique. Néanmoins, cette étude dépasse de loin le cadre du programme de classe préparatoire.

On peut par contre, à notre niveau, déjà avoir quelques idées qualitative sur les harmoniques qu'on va pouvoir observer. En effet, celle-ci impose l'existence de deux noeuds en certains points. Ainsi si l'on excite fortement la corde au milieu, on peut attendre que toutes les harmoniques paires soient nulles (ou opposés) puisqu'elles ont toutes un noeud au milieu. A l'inverse, la présence d'un limitateur de vibration (un doigt humain par exemple) peut empêcher un ventre et par la même occasion annuler un mode.


### Généralisation


__Types d'ondes différentes__  
La présence d'onde stationnaire est un phénomène qui ne se limite pas à la corde vibrante.

* Dans le domaine acoustique, les instruments à vents sont basés sur le même principe: la longueur du tube (ou la position des trous) définis les modes propres pouvant exister et ainsi le son et le timbre qu'on va entendre.
* Dans le domaine électromagnétique, on réalise des cavités permettant de sélectionner certaines fréquences, c'est notamment le cas des cavités LASER.




__Spectre théorique et spectre réel__  
L'étude précédente montre que la corde ne peut vibrer qu'aux fréquences quantifiées $f_n$. L'expérience (cf. TP) montre qu'en réalité, un vibreur peut faire vibrer la corde à d'autre fréquence mais l'amplitude de vibration est beaucoup plus faible. En pratique, on observe un phénomène de __résonance__  pour chaque fréquence $f_n$: l'amplitude y est maximale (maximum local) puis s'atténue quand on s'éloigne de ces fréquences. Nous verrons en électrocinétique/mécanique que l'élargissement d'un phénomène de résonance (les autres fréquences "passent" encore) est dû aux phénomènes dissipatifs.

Dans le cas de la corde vibrante, le principe est le même. L'étude qui permet d'obtenir la structure de l'onde proposée précédemment suppose qu'aucun phénomène dissipatif (frottements) n'existe. Ce qui n'est pas le cas. Deux faits très simple permettent de s'en rendre compte:

* les vibrations de la corde finissent par s'atténuer si on arrête d'exciter la corde.
* une corde vibrante est utilisée pour créer un son. Un son est une onde se propageant dans le milieu environnant et comme toute onde progressive, il transporte sur son chemin de l'énergie. Cette énergie est nécessairement fournie par la source, ici la corde vibrante. Autrement dit, l'excitation de l'air ambiant par la corde provoque un échange d'énergie: la corde fournit de l'énergie à l'onde sonore, il y a donc phénomène de dissipation pour le système {corde vibrante}.


```{figure} ./images/Signaux_Sol_Flute.png
:name: fig_313
:align: center

```


## Exercices d'application

### Cavité LASER résonante

````{admonition} Exercice 
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

### Tuyau ouvert

````{admonition} Exercice 
:class: attention

On considère le cas d'un tuyau ouvert et on cherche les fréquences correspondant aux modes propres d'une onde acoustique stationnaire. On admet que pour un tel tuyau, on attend un ventre de vitesse aux deux extrémités. On réalisera une étude graphique pour déterminer les modes propres.

````

## Travaux dirigés

### Corde vibrante

````{admonition} Exercice 
:class: attention

On considère une corde de longueur L fixée à ses deux extrémités. Sa masse linéique est $\mu$ et elle est tendue par une tension $T_0$. La vitesse de propagation des ondes mécaniques sur la corde est alors: $v=\sqrt{\frac{T_0}{\mu}}$.

1. Quelle grandeur permet de décrire la vibration de la corde?
1. Montrer que v est bien homogène à une vitesse.
1. Rappeler brièvement pourquoi on doit décrire la vibration de la corde comme la superposition de deux ondes. Préciser leurs expressions générales.
1. On cherche les pulsations $\omega$ auxquelles cette corde peut vibrer. Quelle est alors la forme générale de l'onde résultante?
1. Exprimer les conditions que doit satisfaire l'onde? En déduire les pulsations quantifiées auxquelles la corde peut vibrer. On précisera le fondamental $\omega_0$.
1. (HP) *On peut montrer que la puissance moyenne transportée par une onde mécanique progressive monochromatique le long de la corde est de la forme: $\langle P(x) \rangle = a \langle Y^2(x,t) \rangle$ où $a$ est une constante qu'on ne déterminera pas. Montrer que pour une onde stationnaire, il n'y a pas d'énergie transportée. Donner un autre sens au terme "d'onde stationnaire".


````

### Le pipeau

````{admonition} Exercice 
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
