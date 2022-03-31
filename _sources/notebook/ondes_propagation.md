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
# Description des ondes

## Définition générale

````{important} __Définition : Onde__

Une onde est la propagation d'une perturbation produisant sur son passage une variation réversible des propriétés physiques locales du milieu.

````


Elle se déplace avec une vitesse déterminée qui dépend des caractéristiques du milieu de propagation. On appelle cette vitesse la __célérité__  de l'onde dans le milieu.

Une onde transporte de l'énergie sans transporter de matière.

Le fait que la déformation soit réversible signifie que si l'onde a finie de passer en un endroit, le système retourne à son état initial (repos normalement).


````{admonition} Exemple : Description et types d'ondes
:class: tip, dropdown

On décrit la propagation d'une onde par l'expression des grandeurs physiques associées au phénomènes __dans l'espace et dans le temps__ . Les grandeurs dépendent du type d'onde que l'on veut décrire. A titre d'exemple non exhaustif:

* __La corde vibrante (ondes mécaniques)__ : Déformation de la corde $z(M,t)$
* __A la surface de l'eau:__  Altitude de la surface $z(M,t)$
* __Ondes électriques:__  Intensité et Tension
* __Ondes acoustiques:__  vitesse de l'air $v(M,t)$ et surpression de l'air $p(M,t)$
* __Ondes électromagnétiques:__  Champ électrique et champ magnétique


On remarque que ces grandeurs dépendent du temps ET de l'espace car l'onde se propage dans...  l'espace. Certaines peuvent être vectorielles (vitesses, champ électrique... ).
````

````{important} __Définition : Ondes longitudinales et transversales__

Une onde se propage localement dans une direction. La perturbation locale est associée à une grandeur qui varie en général aussi avec une direction spatiale. On distingue:

* __Ondes longitudinales:__  La perturbation se fait dans le même sens que la progression.
* __Ondes transversales:__  La perturbation se fait dans une direction perpendiculaire à la propagation. La direction de la perturbation est alors appelée polarisation.


````

## Modélisation mathématique de la propagation d'ondes

_Dans le cadre du programme, on ne s'intéresse qu'à des ondes se propageant dans une direction (propagration __rectiligne__ )._

### Description mathématique: Onde progressive


__Mise en situation__  
Supposons une onde se propageant suivant un axe Ox avec une célérité v __dans le sens des x croissants__ . Elle est caractérisée par une grandeur y dont on note l'expression en un point M à un instant t $y(x,t)$ où x est l'abscisse du point M.


````{important} __Définition : Retard d'une onde__

Pour aller d'un point A de coordonnées $x_A$ à un point B de coordonnées $x_B$, l'onde met un temps $\Delta t = \frac{x_B - x_A}{v}$ qu'on appelle __retard à la propagation__ .

````

````{important} __Fondamental : Expression mathématique pour une onde progressive__

L'expression de y au point B de coordonnées $x_B$ et notée $y(x_B,t)$ est la même que l'expression de y au point A mais __retardée__  du temps $\Delta t$ correspondant au retard à la propagation entre A et B:

\begin{equation}
y(x_B,t) = y(x_A,  t - \frac{\overline{AB}}{v})
\end{equation}
````


__Démonstration__  
Considérons le passage de l'onde au point A au temps $t_A$. L'onde va mettre un temps $\Delta t =\frac{\overline{AB}}{v}$.

Au temps $t$, l'onde a en B la valeur $y(x_B,t)$ qu'elle avait au point A au temps $t' = t - \Delta t$, soit $y(x_A,t')=y(x_A,t_B - \frac{\overline{AB}}{v})$.



__Forme d'onde__  
Dans les cas étudiées (onde plane), l'onde ne se déforme pas de sorte que la forme (temporelle) qu'elle prend en un point d'abscisse de référence $x=0$pourra être décrite par une fonction $g(t)=y(0,t)$ qui sera aussi la forme (temporelle) de l'onde en un point de coordonnées x mais décalée:

\begin{equation}
y(x,t) = g(t - \frac{x}{v})
\end{equation}

````{important} __Fondamental : Forme mathématique d'une onde (2)__

La forme spatiale de l'onde à un instant $t_2$ $y(x,t_2)$ correspond à la forme spatiale de l'onde à un instant $t_1$ où l'expression y en chaque point est "décalé" d'une distance $v t_1$:

\begin{equation}
y(x,t_2) = y(x - v (t_2 - t_1), t_1)
\end{equation}
````


__Démonstration__  
On raisonne cette fois sur la forme spatiale à un instant t mais le raisonnement est le même, l'expression de $y(x,t_2)$ en un point B de coordonnées x à l'instant $t_2$ sera celle de $y(x_A,t_1)$ en un point A à l'instant $t_1$ tel que l'écart $x - x_A$ soit égal à la distance parcourue par l'onde en un temps $t_2 - t_1$ soit $x_A = x - v(t_2 - t_1)$



__Forme d'onde (2)__  
Dans les cas étudiées (onde plane), l'onde ne se déforme pas de sorte que la forme (spatiale) qu'elle prend à un instant référance $t=0$pourra être décrite par une fonction $h(x)=y(x,0)$ qui sera aussi la forme (spatiale) de l'onde en un point de coordonnées x mais décalée:

\begin{equation}
y(x,t) = h(x - v t)
\end{equation}

````{attention}
__Ondes progressive et régressive__


On suppose ici que l'onde se propage dans le sens des x __positifs__ . Si l'onde se propage dans le sens des x négatifs, il faut opposés les signes des retards. Un exercice d'application propose de le démontrer.

\begin{align*}
y(x,t) &= g(t + \frac{x}{v})\\
y(x,t) &= h(x + vt)
\end{align*}
````

### Onde progressive harmonique

````{dropdown} Remarque

__Linéarité et Fourier__  
Les équations d'évolution amenant à justifier qu'une progressive se déplace dans un milieu seront vues en deuxième année. On retiendra déjà que ces équations sont en générale linéaires. Comme avec les systèmes linéaires en électrocinétique, cela justifie la décomposition en série de Fourier des signaux.

On en vient alors à étudier les caractéristiques des ondes dont la forme sera sinusoïdale. On parle d'onde sinusoïdale ou harmonique. On pourra remarquer que cette décomposition est aussi utile à l'analyse des signaux (analyse spectrale de signaux lumineux ou sonore par exemple).

Dans toute cette étude, on supposera qu'il existe une source au point O d'où l'onde est issue. L'origine des retards sera prise au point O. On traitera le cas d'une onde se propageant suivant l'axe Ox dans le sens des x croissants. L'étude pourra se généraliser à une propagation dans le sens des x décroissants.
````

````{important} __Définition : Ondes progressive harmonique (OPH)__

Une onde sinusoïdale est une onde dont la forme est un sinusoïde $g(t) = g_m \cos(\omega t)$. Une onde progressive sur un axe Ox suivant les x croissants aura pour amplitude:

\begin{equation}
y(x,t) = g_m \cos(\omega t - \omega \frac{x}{v}) = g_m \cos(\omega t - kx)
\end{equation}
De même pour une onde progressant suivant les x négatifs:

\begin{equation}
y(x,t) = g_m \cos(\omega t + \omega \frac{x}{v}) = g_m \cos(\omega t + kx)
\end{equation}

````

````{important} __Définition : Caractéristiques d'une OPH__

* __Pulsation/Fréquence/Période temporelle:__  $\omega; f= \frac{\omega}{2 \pi}; T = \frac{2 \pi}{\omega}$
* __La longueur d'onde (ou période spatiale)__  $\lambda$ est la distance minimale qui sépare deux positions où la perturbation est la même à chaque instant.
* __Le nombre d'onde__  est définie par $k = \frac{2 \pi}{\lambda}$


````

````{important} __Fondamental : Relation temps-espace__

Pour une onde sinusoïdale de célérité $c$ et de fréquence f. On a la relation: $\lambda f = v_{onde}$

Ou encore: $\frac{\omega}{k} = v_{onde}$.
````


__Démonstration__  
Considérons une onde sinusoïdale de fréquence $f$. En une période $T=1/f$, la distance parcourue par un maximum (qui correspond donc à $\lambda$) s'écrit: $\lambda = c\times T = \frac{c}{f}$


````{dropdown} Remarque

Pour une onde, la fréquence reste toujours la même dans un même référentiel. Il vient que si la vitesse de propagation de l'onde change, sa longueur d'onde va varier aussi et réciproquement.
````

### Représentation de Fresnel


Lorsqu'on étudie des signaux sinusoïdaux, il peut être intéressant d'utiliser un artifice mathématique pour simplifier l'étude: on utilise __la représentation complexe des signaux sinusoïdaux__  comme on apu le faire pour des signaux sinusoïdaux en régime sinusoïdal forcé.


_Rappel : Représentation complexe_  
_On considère une onde progressive monochromatique de phase $\psi = \omega t - kx + \phi$ (on a choisit ici une origine $\phi$ des phases en t=0 __à x=0__ )._

* On définit __la représentation complexe__  $\underline{E}$ de E par $\underline{E}(M,t) = E_m e^{j \psi} = E_m e^{j \omega t} e^{j (_kx + \phi)}$
* On définit l'amplitude complexe $\underline{E_m}$ de E par $\underline{E_m}(M)=E_m e^{j (-kx + \phi)}$


_Rappel : Propriétés_  
* $\underline{E} = \underline{E_m}e^{j \omega t}$
* $E =\Re(\underline{E})$
* $E_m = \left\vert\underline{E_m}\right\vert = \left\vert\underline{E}\right\vert$
* $\phi_M = \phi - kx= \arg(\underline{E_m})$


où l'on note $\phi_M$ la __phase à l'origine au point M.__ 


Les caractéristiques sont les mêmes qu'en électrocinétique à un point près: la phase à l'origine va dépendre du M où l'on exprime la grandeur associée à l'onde. Ce point se révèlera fondamental lorsqu'on superposera des ondes car cela pourra causer la naissance d'interférences.


_Rappel : Représentation de Fresnel_  
_La représentation de Fresnel de la grandeur $E(M,t)$ à l'instant $t$ est la représentation de la grandeur complexe dans le plan complexe à l'instant $t$._

Très souvent, on travaillera avec la représentation de Fresnel à l'instant $t=0$, elle est alors la représentation de l'amplitude complexe aussi.


## Exemples d'ondes

_On décrit ici les différents types d'ondes qui pourront être rencontrées et les grandeurs associées._

### Corde vibrante. Onde mécanique


Une corde vibrante est une corde de masse linéique $\mu_0$ tendue par une tension $\overrightarrow{T_0}$ de norme $T_0$ (les deux extrémités peuvent se mouvoir). On la suppose parfaitement horizontal au repos, ce qui revient à négliger la pesanteur. Chaque point de la corde peut vibrer dans le plan vertical. L'axe Ox est l'axe horizontal, les axes Oy et Oz sont les axes du plan de vibration. Pour simplifier, on supposera que la corde ne peut vibrer que dans la direction Oy (ce qui signifie que l'excitation n'est que dans le plan Oy).



__Description physique__  
__Système considéré:__  Pour décrire le mouvement de la corde, on considère un petit morceau de corde autour d'un point M de la corde repéré par son abscisse x.

__Grandeur considérée:__  On peut décrire l'état de la corde en décrivant l'état d'un point M plusieurs grandeurs par:

* sa position transversale: $y(x,t)$
* sa vitesse de déplacement transversale: $v_y(x,t)$
* la tension de la corde en tout point: $\overrightarrow{T(x,t)}$ (ici la force exercée par la partie à gauche de x sur la partie à droite de x).




__Célérité des ondes mécanique__  
On peut montrer que lorsqu'on se limite à des vibrations de faibles amplitudes, la célérité des ondes mécaniques ne dépend que de la tension imposée aux extrémités de la corde et de la masse linéique de la corde. Une analyse dimensionnelle permet de déterminer l'expression (le coefficient de proportionnalité vaut 1): $v_{onde}=\sqrt{\frac{T_0}{\mu_0}}$


### Ondes acoustiques


Une onde sonore est la propagation dans un milieu matériel (par exemple l'air) d'une surpression provoquant sur son passage une agitation locale du milieu. Considérons une tube dans lequel se trouve de l'air (on pourra par exemple assimiler cela à un instrument à vent). Un surpression causée en entrée va «pousser» une tranche de fluide (l'air), qui en s'agitant va induire une surpression sur la tranche de fluide suivant qui se met à son tour en mouvement et ainsi de suite: il se propage un son. Ce son arrive jusqu'à nos oreilles où jusqu'à un micro. La surpression qui s'est propagée fait alors vibrer une membrane (tympan ou capteur de pression).



__Description physique__  
__Système étudié:__  On étudie le mouvement d'une tranche de fluide d'épaisseur dx autour d'une position x.

Grandeur considéré (dans le cas d'un fluide):

* la surpression engendrée: $p(x,t)$. La pression au point M est: $P(x,t)=P_O+p(x,t)$ où $P_0$ est la pression du milieu au repos.
* la vitesse de la portion de fluide: $v(x,t)$ (pas de grandeur à ajouter car au repos, cette portion de fluide ne bouge évidemment pas).
* la variation de masse volumique du fluide: $\Delta \mu(x,)t$. $\mu(x,t) = \mu_0 + \Delta \mu(x,t)$ ($\mu_0$ est la masse volumique du fluide au repos).




__Célérité__  
Une étude (utilisant la mécanique des fluides) permet de montrer que la célérité du son dans l'hypothèse d'une évolution isentropique ne dépend que du coefficient de compressibilité isentropique et de la masse volumique du fluide au repos.



__Intensité acoustique__  
On définit l'intensité acoustique instantanée $I(x,t)$ d'une onde sonore comme la puissance transportée par l'onde dans une direction donnée par unité de surface. On peut montrer que l'intensité acoustique instantanée dans la direction de propagation du son est $I(x,t)=p(x,t)v(x,t)$.

L'intensité acoustique est la valeur moyenne de l'intensité acoustique instantanée.

Le niveau d'intensité sonore est définit par $L = 10 \log(I/I_0)$ exprimé en dB où $I_0 = 10^{-12} \rm{SI}$

Ces formules ne sont pas à connaître mais on retiendra qu'une onde __transporte une puissance__ .


### Ondes à la surface d'un fluide


La surface d'un fluide (l'eau), peut être excitée par exemple par le vent, donnant naissance à la houle. Ce phénomène correspond à la propagation d'une onde à la surface du fluide. En effet, il se produit alors une montée d'eau en une position. La conservation de la masse et la variation de pression dans la colonne d'eau induit alors une variation de hauteur d'eau dans la colonne d'eau suivante et ainsi de suite se propage une onde de surface. Nous signalons simplement l'existence de ces ondes car elles sont courantes autour de nous et qu'elles seront étudiée de manière descriptive en TP.

Grandeurs observées: En un point du passage de l'onde, on peut définir la hauteur de la surface du fluide à un instant t: $z(x,t)$. Il existe d'autres grandeurs décrivant le passage de l'onde mais nous nous limitons ici à cette grandeur qui suffit à décrire l'onde à chaque instant.


### Ondes électriques


Quand en un point du circuit, on modifie le potentiel ou l'intensité (exemple: on allume le circuit), la  variation locale d'intensité/de potentiel va se propager de proche en proche tout au long du circuit: une onde électrique se propage dans le circuit.



__Description physique__  
Le système étudié est une portion de circuit et sa modélisation électrique (cf. deuxième année). Les grandeurs utilisées sont bien entendu le potentiel électrique et l'intensité.


_Rappel : ARQS_  
_On rappelle que la célérité des ondes électriques est de l'ordre de la célérité de la lumière dans le vide de sorte que pour des signaux "lents" sur des circuits "courts", on peut négliger les phénomènes de propagation, c'est-à-dire les considérer comme instantanés._

### Ondes électromagnétiques


Dans une approche classique de la lumière, celle-ci est une onde électromagnétique. La propagation d'une onde électromagnétique correspond à la propagation d'une variation des champs électriques $\overrightarrow{E}(M,t)$ et magnétique $\overrightarrow{B}(M,t)$ en tout point du trajet de l'onde. Les variations spatiales et temporelles des ces deux grandeurs sont corrélées par des équations (les équations de Maxwell). Ces relations permettent de propager ces variations de proche en proche: une onde électromagnétique se propage.



__Description physique__  
Le système étudié est une portion d'espace. Comme précisé précédemment, les grandeurs qui décrivent l'onde seront le champ électrique et magnétique en chaque point. On remarque qu'il s'agit de __champs vectoriels__ . L'orientation du champ électrique est notamment extrêmement importante.


_Rappel : Cérélité des ondes électromagnétiques et indice de réfraction_  
_Dans le vide, les ondes électromagnétiques se propage à la vitesse $c=299792458 \rm{m.s^{-1}}$._

Dans un milieu quelconque qui n'est pas opaque au rayonnement électromagnétique (une onde électromagnétique peut se propager), la vitesse de propagation peut être plus faible que la vitesse de la lumière dans le vide. On définit l'indice de réfraction du milieu comme le rapport: $n = \frac{c}{v_{milieu}}$ où $v_{onde}$ est la célérité de l'onde dans le milieu. Cet indice est toujours supérieure ou égal à 1.


__Considérations énergétiques__  
Energie propagée: L'étude de l'énergie propagée par une onde électromagnétique est un peu complexe. On peut retenir que:

* On traite en général l'éclairement énergétique I qui correspond à l'énergie transportée par le rayonnement électromagnétique par unité de surface (on pourra faire le parallèle avec les cas précédents).
* La sensation de luminosité perçue par notre oeil est en rapport avec l'éclairement.
* Pour une onde monochromatique progressive, l'éclairement est proportionnel au carré du module du champ électrique $I \approx \frac{cn \epsilon}{2} \vert E^2 \vert$. Le coefficient de proportionnalité n'est pas à connaître. Un rapide calcul montre que les fréquences associées au rayonnement visible sont de l'ordre de $10^{14}\rm{Hz}$. Cela montre que notre oeil n'est pas sensible à l'éclairement instantanée mais à la valeur moyenne de l'éclairement. __C'est pourquoi, on définit directement l'éclairement énergétique comme une grandeur proportionnelle à la valeur moyenne du champ électrique au carré.__ __$I \propto \langle E^2 \rangle$__ 



### Eclairement d'un OPH

````{admonition} Exercice 
:class: attention

Déterminer l'éclairement énergétique moyen d'une onde monochromatique (une seule longueur d'onde, un seul sinusoïde) d'amplitude.

Déterminer l'éclairement d'une onde composée de deux fréquences différentes $f_1$ et $f_2$ d'amplitudes respectives $E_{1m}$ et $E_{2m}$. Commenter.

````
````{dropdown} Démonstration

 


__Eclairement d'une OPH__  
Le champ électrique s'écrit: $E(x,t) = E_m \cos(\theta t - kx)$ soit $I \propto \langle E_m^2 \cos^2(\theta t - kx) \rangle$ donc: $I \propto \frac{E_m^2}{2}$



__Superposition de deux OPH__  
Le champ électrique s'écrit: $E(x,t) = E_{m1} \cos(\theta_1 t - k_1 x)+E_{m2} \cos(\theta_2 t - k_2 x)$ soit:

\begin{align*}
I &\propto \langle E_{m1}^2 \cos^2(\theta_1 t - k_1x) + E_{m2}^2 \cos^2(\theta_2 t - k_2x) +2E_{m1}E_{m2} \cos(\theta_2 t - k_2x)\cos(\theta_1 t - k_1x)\rangle\\
I &\propto \frac{E_{m1}^2}{2} + \frac{E_{m2}^2}{2}
\end{align*}
On observe que les énergies moyennes transportées par deux ondes de pulsations différentes se somment. On remarquera l'importance des grandeurs efficaces puisque ce sont elles qui interviennent.


```{attention}
:class: dropdown
L'expression précédente n'est valable __que si les deux ondes ont des pulsations différentes.__ . Il reste un cas que nous n'avons pas traité, le cas de deux ondes de mêmes fréquences. Ce cas sera traité au prochain chapitre, c'est le cas des interférences.
```
````

## Front d'onde et diffraction

### Source lumineuse


Dans toute l'étude réalisée précédemment, nous avons parlé de source émettrice sans préciser ses caractéristiques. Plus précisément, nous parlons de point S d'où est émis l'onde. Cette notion mérite d'être précisée. En effet, il n'est pas possible d'émettre une onde d'un seul point. Outre la question du phénomène physique nécessaire à l'émission, il faut voir qu'un point source est d'extension nulle, il rayonnerait donc une énergie...  nulle.

En réalité, toute source lumineuse possède une taille non nulle (on parle de source étendue). Cela complique le traitement complet car l'onde résultante émise par un point peut être supposée sphérique, pas l'onde émise par un corps de géométrie quelconque aura peu de chance d'être sphérique. Heureusement, nous verrons par la suite que l'onde résultante de l'émission de l'ensemble de la source lumineuse suit un principe de superposition du champ électrique de l'onde. En clair, on peut sommer les champs émis par chaque «morceau» de source, d'où l'idée simple de décomposer la source en une multitude de point lumineux d'extension quasi nulle.


````{important} __Définition : Point source lumineux__

Un point source lumineux est un point émettant une onde lumineuse dans une ou plusieurs direction. On lui associe en général un cône d'émission (qui peut-être toute la sphère) ainsi qu'un spectre d'émission.

````

````{important} __Définition : Point source monochromatique__

Un point source monochromatique est un point source émettant une lumière monochromatique.

````


La majorité des sources lumineuses peuvent être décomposées en une multitude de points sources lumineux indépendants, c'est-à-dire dont l'émission est indépendante les unes des autres. Si le spectre d'émission des points d'une même source est normalement le même, il est en général fréquent que le déphasage entre ces points sources soit aléatoires et variables. Nous verrons que cela joue un rôle dans les processus d'interférences vu au prochain chapitre.


````{attention}

Le modèle de point source lumineux est un modèle théorique qui ne peut-être rigoureusement réalisé lors d'une expérience (on rappelle l'argument d'énergie nulle). Il s'agit d'un modèle très pratique pour décrire une source étendue. On peut néanmoins s'approcher du modèle du point lumineux en utilisant un diaphragme très petit. La seule limite pratique est alors les besoins en luminosité de l'expérience.

````

### Front d'onde: Définition

````{important} __Définition : Surface d'onde__

Une surface d'onde (où front d'onde) est l'ensemble des points possédant la même phase (le même retard sur la source de l'onde).

```{figure} ./images/Signaux_ondes_circulaire.jpg
:name: fig_293
:align: center

```

Sur le graphique précédent, on a représenté en traits pleins les surfaces d'ondes et en pointillés les "rayons" de l'onde correspond à la direction de propagation.

````

````{important} __Fondamental : Théorème de Malus (Admis)__

Lorsque le phénomène de diffraction peut-être négligé (cf. suite), le trajet d'une onde matérialisée par le trajet de l'énergie suivant des "rayons" est perpendiculaire au surface d'onde (cf. la figure précédente).
````

````{important} __Définition : Types d'ondes__

__Cas d'une onde plane:__  l'amplitude ne dépend pas de la position transverse à la propagation. On étudie souvent ce type d'onde car elle est simple mais les ondes créées en général sont plutôt circulaires ou sphériques (et encore... ).

```{figure} ./images/Signaux_ondes_planes.jpg
:name: fig_294
:align: center

```

Cas d'une ondes circulaire: (on pourra généraliser l'idée à une onde sphérique à 3 dimensions) Il s'agit d'une représentation assez usuelle pour une source ponctuelle (point lumineux, source sonore... ).

```{figure} ./images/Signaux_ondes_circulaire.jpg
:name: fig_295
:align: center

```

````

## Exercices d'application

### Ondes régressives

````{admonition} Exercice 
:class: attention

Démontrer l'expression mathématique des ondes régressives:

\begin{equation}
y(x,t) = g_m \cos(\omega t + \omega \frac{x}{v}) = g_m \cos(\omega t + kx)
\end{equation}

````

### Onde progressive

````{admonition} Exercice 
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

### Ondes acoustiques

````{admonition} Exercice 
:class: attention

On considère une onde sonore unidirectionnelle se propageant dans la direction des x positifs. Aux abscisses sources $x=0$, l'amplitude de l'onde est: $p(x=0,t)=p_0(t)$. Le milieu ambiant est de l'air de masse volumique au repos $\rho_0=1,2 \rm{kg.m^{-3}}$ et le son s'y propage à la vitesse: $c=340 \rm{m.s^{-1}}$.

1. Une onde sonore est-elle une onde transversale ou longitudinale?
1. Exprimer en fonction de $p_0(t)$, l'expression de la surpression en un point quelconque d'abscisse x.
1. On suppose que l'excitation est sinusoïdale de fréquence f et d'amplitude $p_{0m}$. La phase à l'origine au point x=0 est supposée nulle. Exprimer la surpression $p(x,t)$ en tout point du trajet de l'onde.
1. On peut montrer que l'intensité acoustique moyenne d'une onde harmonique ne dépend que de la valeur efficace $p_0$ de la surpression, de la masse volumique et de la célérité de l'onde. Par une analyse dimensionnelle, montrer que $I = \frac{p_0^2}{\rho_0 c}$.
1. Exprimer la surpression $p_0$ correspondant à l'intensité de référence $I_0$ pour l'air (il correspond à peu près au seuil moyen de perception humaine pour des fréquences autour de 3kHz).
1. Le seuil de douleur pour l'oreille humaine se situe autour de 120dB. Estimer la surpression moyenne correspondante.


````

### Longueur d'onde

````{admonition} Exercice 
:class: attention

Montrer que dans un milieu d'indice de réfraction n, la longueur d'onde sera $\lambda=\frac{\lambda_0}{n}$ où $\lambda_0$ est la longueur d'onde dans le vide.

__Cette relation est à retenir.__  

````

### Onde plane

````{admonition} Exercice 
:class: attention

Comment faire expérimentalement une onde lumineuse plane à partir d'une source ponctuelle?

````

## Travaux dirigés

### Retard d'une OEM

````{admonition} Exercice 
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

### \*Etalement

````{admonition} Exercice 
:class: attention

On s'intéresse à la propagation sans perte d'une onde acoustique dans un milieu à trois dimensions, on supposera que ce milieu est l'air ambiant. Pour des raisons de commodité, on représentera les graphiques dans des coupes à deux dimensions. On considère une onde progressive sinusoïdale de fréquence $f=50 \rm{kHz}$. On considère que la propagation de l'onde dans le milieu est toujours rectiligne et que la vitesse de propagation est $c=340 \rm{m.s^{-1}}$.

1. Rappeler quelles grandeurs peuvent caractériser la propagation de l'onde.
1. Dans quelle domaine d'émission se trouve l'onde étudiée? Exprimer la longueur d'onde associée.
1. On considère une onde plane se propageant dans la direction Ox et on prend l'origine des phases dans le plan yOz.
    1. Représenter les fronts d'onde.
    1. Les symétries du problème impose que les grandeurs ne dépendent ni de y, ni de z. En considérant l'origine des phases au point O, justifier brièvement que la forme $p(x,t) = p_m(x) \cos(\omega t - kx)$ est compatible avec une telle onde où l'on exprimera k en fonction de $\omega$ et c puis en fonction de $\lambda$.
    1. On considère une section S du plan d'onde contenant le point O, il contient un faisceau d'ondes. Quelle sera la section occupée par le même faisceau dans un autre plan d'onde? En déduire, que l'amplitude $p_m(x)$ ne dépend pas non plus de x.
1. On considère maintenant que la source est un point source situé au point O qu'on prendra comme origine des phases.
    1. Justifier qu'alors les fronts d'onde sont des sphères centrées en O.
    1. Les symétries du problème impose que les grandeurs ne dépendent que de la distance parcouru $r=OM$ et pas de la direction de propagation de l'onde. Justifier alors que la surpression doit être de la forme $p(r,t) = \frac{K}{r^2} \cos(\omega t - kr)$.



````


