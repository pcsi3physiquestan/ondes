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
# Méthodes

## Réflexion parfaite sur une corde
_On va démontrer le caractére stationnaire de l'onde en présence d'un noeud._
````{margin} 
Si le paramétrage est libre, pensez à mettre la condition aux limites nulle en 0.
````
````{admonition} Exercice 
:class: attention

On considère une corde tendue par une tension T horizontale de masse linéique $\mu$. La célérité des ondes mécaniques qui se propagent sur la corde est alors $c = \sqrt{\frac{T}{\mu}}$. On notera $k = \frac{2\pi}{\lambda}$ avec $\lambda$ la longueur d'onde d'une onde progressive. La corde est attaché en un point A. Une onde progressive harmonique se propose dans le sens des x positifs de $-\infty$ vers le point A.

1. Justifier l'existence d'une onde réfléchie. En déduire l'expression générale de la côte verticale $y(x,t)$ de la corde.
1. Que vaut y au point A? En déduire que l'onde résultante est une onde stationnaire.
1. Déterminer la position des noeuds et des ventres de l'onde.
````

```{sidebar} Attention
* On n'écrit pas tout de suite que les amplitudes sont égales, il va falloir le prouver.
* On peut choisir la phase à l'origine nulle pour l'onde incidente puisque qu'on fixer l'origine des phases.

Mais on ne peut le faire qu'une seule fois (on fixe la "référence des phases", c'est pourquoi on écrit pas que la phase à l'origine pour l'onde réfléchie est nulle, il faut aussi le prouver (et ça peut être faux si la réflexion n'a pas lieu en $x=0$.
```
````{topic} __Correction__

>__Existence d'une onde réfléchie__  
>Une onde transporte de l'énergie. Or au point A, il n'y a pas de mouvement, donc par d'énergie transmise vers les x positifs. Il vient que cette énergie est nécessairement réfléchie d'où l'existence d'une onde réfléchie:
>\begin{equation}
y(x,t) = A \cos \left(\omega t - kx\right) + B \cos \left(\omega t + kx + \varphi\right)
\end{equation}
>
>__Onde stationnaire__  
>On pose $x_A = 0$. On a y(0,t) = 0 pour tout t. Il vient:
>
>\begin{align*}
y(0,t) = 0 &= A \cos \omega t + B \cos \omega t +\varphi \\
0 &= \left(A + B \cos \varphi\right)\cos \omega t - B \sin \varphi \sin \omega t
\end{align*}
>La dernière équation devant être vraie pour tout t, il vient que $B \sin \varphi = 0$ et $A + B \cos \varphi =0$ soit trivialement $\varphi = 0$ et $A = -B$ soit:
>
>\begin{align*}
y(x,t) &= A \cos \left(\omega t - kx\right) - A \cos \left(\omega t + kx\right)\\
&= 2 A \sin \omega t \sin kx
\end{align*}
>L'onde résultante est bien une onde stationnaire.
>
>
>__Noeud et ventre__  
>Les noeuds sont tels que $y(x,t) = 0$ à tout instant soit $\sin kx = 0$ soit $ x = \frac{m\pi}{k} = \frac{m\lambda}{2}$ avec m un entier. On observe que les noeuds sont espacés d'une demie longueur d'onde.
>
>Les ventres sont tels que l'amplitude de $y(x,t)$ est maximale soit $\sin kx = 1$ soit $x = \frac{m\pi}{k} + \frac{\pi}{2 k}= \frac{m\lambda}{2} + \frac{\lambda}{4}$. A nouveau les ventres sont espacés d'une demi longueur d'onde. On retrouve l'allure observée précédemment.
>
```{figure} ./images/Standing_wave.png
:name: fig_311
:align: center
```
````

(md_pr)=
## Modes propres
````{admonition} Corde de Melde
:class: important
On considère une corde de longueur L fixée aux deux points extrêmes A et B sous une tension $\overrightarrow{T}$. La corde peut vibrer et une onde mécanique se propage le long de la corde. On rappelle que pour une onde mécanique, on peut décrire la vibration de la corde se propageant par l'écart de la position d'un point de la corde à sa position d'équilibre (la corde tendue au repos est supposée être horizontale): $y(x,t)$.

1. Montrer que l'onde résultante est stationnaire.
2. Montrer que la corde ne peut vibrer d'elle même qu'à des fréquences particulières qu'on déterminera : les __modes propres__.
````

````{sidebar} Soultions harmoniques
* On ne cherche pas à déterminer une solution quelconque. On va chercher une solution __harmonique__  c'est-à-dire résultant de la superposition de deux ondes progressives harmoniques (l'une dans le sens de x positifs et l'autre dans le sens des x négatifs).
    * Le choix d'étudier les ondes harmoniques s'explique par la linéarité du système (cf. deuxième année) et le principe de décomposition en série de Fourier (cf. début d'année).
* On pourra noter que la structure de l'onde progressive impose la structure de l'onde régressive. C'est obligatoire pour assurer les conditions aux limites à tout instant.
````
````{topic} __Correction Q1. Approche par le calcul.__

>__Paramétrage.__
>
>Quand l'onde se propage, elle arrive au bout de la corde. Elle est alors réfléchie et se propage dans l'autre sens pour être à nouveau réfléchie et ainsi de suite. Cette série d'onde réfléchies se superpose. On peut «regrouper» l'ensemble des ondes obtenues en deux ondes:
>* une onde mécanique se propageant suivant les x croissants: $y_{+}(x,t)=y_{+}(t- \frac{x}{v_{onde}})$
>* une onde mécanique se propageant suivant les x décroissants: $y_{-}(x,t)=y_{-}(t+ \frac{x}{v_{onde}})$
>L'onde résultante totale donne la position instantanée de chaque point de la corde:
>\begin{equation}
y(x,t)=y_{+}(t- \frac{x}{v_{onde}}) + y_{-}(t+ \frac{x}{v_{onde}})
\end{equation}
>
>__Conditions aux limites__  
>On ne peut choisir arbitrairement la forme de l'onde car on impose __des conditions aux limites: l'amplitude aux points extrêmes x=0 et x= L doit nécessairement être nulle (corde fixée).__ 
>L'onde résultante a donc la forme:
>\begin{equation}
y(x,t)=y_{+m}\sin(\omega t- kx) + y_{-m}\sin(\omega t+ kx +\varphi)
\end{equation}
>
>__Q1.__ Cf. la question précédente __en utilisant la condition aux limites en $x=0$. L'onde résultante aura donc pour expression:
>\begin{equation}
y(x,t)=Y_m \cos(\omega t)\sin(k x) = Y \cos(\omega t)\sin(\frac{2 \pi}{\lambda} x)
\end{equation}
````
````{topic} Correction Q2 - Méthode mathématique.
>__Q2.__ Nous allons maintenant utiliser la deuxième condition aux limites. Celle-ci est fondamental puisqu'elle conduit à la __quantification des modes propres__ . Utilisons la deuxième condition aux limites $y(L,t)=0$: $y(L,t)=Y_m \cos(\omega t)\sin(k L) = 0$.

A nouveau, cette relation doit être vérifiée pour tout t, donc $\sin(kL) =0$ soit: $kL = n \pi$ avec $n \in \mathbb{N}$ soit:
\begin{equation}
\begin{cases}
k &= \frac{n \pi}{L}\\
\lambda &= \frac{2L}{n}\\
f &= \frac{n v_{onde}}{2L}
\end{cases}
\end{equation}
````

````{topic} __Correction Q2 - Méthode graphique.__

On connait que l'onde est stationnaire. La forme spatiale de l'onde est alors un sinusoïde. Sauf qu'on impose deux noeuds en x=0 et x=L. On peut ainsi chercher à tracer les formes sinusoïdales qui coïncident avec ces conditions aux limites.

```{figure} ./images/Vibration_corde_trois_modes_petit.png
:name: fig_312
:align: center
```
La représentation précédente (ANIMATION) montre les trois premiers modes propres possibles. Dans le premier, on dessine une demi longueur d'onde sur une longueur de corde, dans le second une longueur d'onde et dans le troisième une longueur d'onde est demie.

On peut généraliser cette observation en remarquant que les conditions aux limites imposent que la longueur de corde soit égale à un nombre entier ou demi-entier de longueur d'onde soit $L = \frac{m\lambda}{2}$ avec m un entier. On pourra retrouver la quantification des fréquences.
````

````{important} __A retenir__
Pour qu'une onde sinusoïdale de fréquence f puisse exister dans une corde de longueur L fixée à ses deux extrémités où la vitesse de propagation des ondes mécanique est $v_{onde}$, il faut que $f=n \frac{v_{onde}}{2L}$ soit une longueur d'onde: $\lambda=\frac{2L}{n}$ avec $n \in \mathbb{N}$.

La forme de l'onde résultante peut s'écrire:

$$
y(x,t)=Y_n \cos(\omega_n t)\sin(k_n x) = Y_n \cos(\omega_n t)\sin(\frac{2 \pi}{\lambda_n} x)
$$
````

````{topic} Interprétation
L'étude précédente permet de mettre en avant les vibrations pouvant exister pour la corde (supposée parfaite puisqu'on néglige toute perte).

Elle a l'avantage d'être simple. Néanmoins, pour qu'une vibration sinusoïdale se produise dans la corde à une fréquence $f_n$, il faut des conditions particulières: une excitation initiale sinusoïdale (cf. TP corde de Melde). Si l'on s'intéresse au principe des instruments de musique, une telle excitation n'est pas réalisée. L'observation du spectre créé par la corde est alors plus complexe: il s'agit d'une superposition des ondes sinusoïdales pures. Dans le langage acoustique, on distingue alors la fréquence la plus faible, correspondant à la hauteur du son ($f_1$ normalement), c'est le __fondamental__ . Et les fréquences suivantes ($f_n$ avec n>1), toutes des multiples du fondamental qui enrichissent le son pour former son timbre: ce sont les __harmoniques__ .

__Conditions initiales et harmoniques__  
Les conditions initiales permettent de déterminer l'amplitude du fondamental et des harmonique. Néanmoins, cette étude dépasse de loin le cadre du programme de classe préparatoire.

On peut par contre, à notre niveau, déjà avoir quelques idées qualitative sur les harmoniques qu'on va pouvoir observer. En effet, celle-ci impose l'existence de deux noeuds en certains points. Ainsi si l'on excite fortement la corde au milieu, on peut attendre que toutes les harmoniques paires soient nulles (ou opposés) puisqu'elles ont toutes un noeud au milieu. A l'inverse, la présence d'un limitateur de vibration (un doigt humain par exemple) peut empêcher un ventre et par la même occasion annuler un mode.
````
````{topic} Généralisation
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
````

