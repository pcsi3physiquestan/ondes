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
# Comprendre le contexte

## Définition générale

```{margin}
* Une onde transporte de l'énergie sans transporter de matière.
```
````{important} 
__Onde__

Une onde est la propagation d'une perturbation produisant sur son passage une variation réversible des propriétés physiques locales du milieu.

* Elle se déplace avec une vitesse déterminée qui dépend des caractéristiques du milieu de propagation. On appelle cette vitesse la __célérité__  de l'onde dans le milieu.
````

````{topic} Exemple : Description et types d'ondes
On décrit la propagation d'une onde par l'expression des grandeurs physiques associées au phénomènes __dans l'espace et dans le temps__ . Les grandeurs dépendent du type d'onde que l'on veut décrire. A titre d'exemple non exhaustif:

* __La corde vibrante (ondes mécaniques)__ : Déformation de la corde $z(M,t)$
* __A la surface de l'eau:__  Altitude de la surface $z(M,t)$
* __Ondes électriques:__  Intensité et Tension
* __Ondes acoustiques:__  vitesse de l'air $v(M,t)$ et surpression de l'air $p(M,t)$
* __Ondes électromagnétiques:__  Champ électrique et champ magnétique

On remarque que ces grandeurs dépendent du temps ET de l'espace car l'onde se propage dans...  l'espace. Certaines peuvent être vectorielles (vitesses, champ électrique... ).
````

## Modélisation mathématique de la propagation d'ondes

### Onde progressive
__Mise en situation :__  Supposons une onde se propageant avec une célérité v. Elle est caractérisée par une grandeur y dont on note l'expression en un point M à un instant t $y(M,t)$

````{important} __Forme mathématique d'une onde (1)__
L'expression de y au point B et notée $y(B,t)$ est la même que l'expression de y au point A mais __retardée__  du temps $\Delta t_{{AB}}$ correspondant au retard à la propagation entre A et B:

$$
y(B,t) = y(A,  t - \Delta t_{{AB}})
$$
````

```{margin}
On fera le lien avec le décalage horizontal graphique du tracé d'une fonction.
```
````{topic} __Démonstration__  
Considérons le passage de l'onde au point A au temps $t_A$. L'onde va mettre un temps $\Delta t_{AB}$.

Au temps $t_B$, l'onde a en B la valeur $y(B,t_B)$ qu'elle avait au point A au temps $t' = t_B - \Delta t_{AB}$, soit:

$$
y(B,t_B) = y(A,t')=y(A, t_B - \Delta t_{AB})
$$
````

```{margin}
* On se ramène donc à décrire l'onde avec une seule fonction $g$ décrite par la source.
* _Attention_: Cette expression n'est valable que pour un milieu homogène et une propagation rectiligne.
```
````{admonition} Cas particuliers utiles (à connaître)
:class: tip
__Propagation rectiligne dans un milieu homogène.__
* Si la propagation est rectiligne, on peut choisir un repère où l'axe Ox est suivant la direction de propagation. 
    * On peut choisir un point d'abscisse de référence, souvent le point source, $x=0$ où l'onde émise à pour expression $y(x=0,t) = g(t)$.
* Si l'onde de propage suivant les x positifs, le temps mis pour atteindre un point M d'abscisse $x$ est $\frac{x}{v}$ et la forme mathématique devient:

$$
y(x,t) = g(t - \frac{x}{v})
$$
* Si l'onde de propage suivant les x négatifs (on parle d'onde régressive), le temps mis pour atteindre un point M d'abscisse $x$ est $-\frac{x}{v}$ (on passe en M avant O si $x>0$) et la forme mathématique devient:

$$
y(x,t) = g(t + \frac{x}{v})
$$
````

```{margin}
* On ne traite que le cas de la propagation rectiligne dans un milieu homogène.
* On peut voir la fonction $y(x,t_1)$ comme une photographique de l'onde à l'instant $t_1$.
```
````{sidebar} Origine des temps
Si l'on considère l'instant $t=0$ comme référence des temps et la forme de l'onde $h(t) = y(x,t=0)$, alors la forme de l'onde à un instant $t$ sera:

$$
y(x,t) = h(x - v t)
$$
````
````{important} 
__Forme mathématique d'une onde (2)__  

__Propagation rectiligne dans un milieu homogène.__

Considérons la forme de l'onde $y(x,t_1)$ à un instant $t_1$ en tout point $x$ de l'axe. La forme spatiale de l'onde à un instant $t_2$ est noté $y(x,t_2)$.

* Si l'onde se propage suivant les $x$ positifs, alors:

$$
y(x,t_2) = y(x - v (t_2 - t_1), t_1)
$$

* Si l'onde se propage suivant les $x$ négatifs, alors:

$$
y(x,t_2) = y(x + v (t_2 - t_1), t_1)
$$
````
````{topic} __Démonstration__  
On raisonne cette fois sur la forme spatiale à un instant t mais le raisonnement est le même, l'expression de $y(x,t_2)$ en un point B de coordonnées x à l'instant $t_2$ sera celle de $y(x_A,t_1)$ en un point A à l'instant $t_1$ tel que l'écart $x - x_A$ soit égal à la distance parcourue par l'onde en un temps $t_2 - t_1$ soit $x_A = x - v(t_2 - t_1)$
````

### Onde progressive harmonique

```{margin} 
L'intérêt des ondes harmonique est à rapprocher de l'intérêt du RSF.
```
````{important} 
__Ondes progressive harmonique (OPH)__
Une onde sinusoïdale est une onde dont la forme est un sinusoïde $g(t) = g_m \cos(\omega t)$. Si elle est émise d'un point S, l'amplitude en un point M sera:

$$
y(M,t) = y(S,t - \Delta t) = g_m \cos \left(\omega (t - \Delta t)\right)
$$
````

````{sidebar} __Relation temps-espace__
Pour une onde sinusoïdale de célérité $c$ et de fréquence f.  
On a les relation: $\lambda f = v_{onde}$ et $\frac{\omega}{k} = v_{onde}$.
````
````{important} Cas rectiligne et homogène
* Une onde progressive sur un axe Ox suivant les x croissants aura pour amplitude:

$$
y(x,t) = g_m \cos(\omega t - \omega \frac{x}{v}) = g_m \cos(\omega t - kx)
$$
* De même pour une onde progressant suivant les x négatifs:

$$
y(x,t) = g_m \cos(\omega t + \omega \frac{x}{v}) = g_m \cos(\omega t + kx)
$$

* __Pulsation/Fréquence/Période temporelle:__  $\omega; f= \frac{\omega}{2 \pi}; T = \frac{2 \pi}{\omega}$
* __La longueur d'onde (ou période spatiale)__  $\lambda$ est la distance minimale qui sépare deux positions où la perturbation est la même à chaque instant.
* __Le nombre d'onde__  est définie par $k = \frac{2 \pi}{\lambda}$
````

````{topic} Représentation complexe
Lorsqu'on étudie des signaux sinusoïdaux, il peut être intéressant d'utiliser un artifice mathématique pour simplifier l'étude: on utilise __la représentation complexe des signaux sinusoïdaux__  comme on apu le faire pour des signaux sinusoïdaux en régime sinusoïdal forcé.
````

## Exemples d'ondes (en ligne)

### Corde vibrante. Onde mécanique
````{topic} Description
Une corde vibrante est une corde de masse linéique $\mu_0$ tendue par une tension $\overrightarrow{T_0}$ de norme $T_0$ (les deux extrémités peuvent se mouvoir). On la suppose parfaitement horizontal au repos, ce qui revient à négliger la pesanteur. Chaque point de la corde peut vibrer dans le plan vertical. L'axe Ox est l'axe horizontal, les axes Oy et Oz sont les axes du plan de vibration. Pour simplifier, on supposera que la corde ne peut vibrer que dans la direction Oy (ce qui signifie que l'excitation n'est que dans le plan Oy).

__Description physique__  
* __Système considéré:__  Pour décrire le mouvement de la corde, on considère un petit morceau de corde autour d'un point M de la corde repéré par son abscisse x.
* __Grandeur considérée:__  On peut décrire l'état de la corde en décrivant l'état d'un point M plusieurs grandeurs par:
    * sa position transversale: $y(x,t)$
    * sa vitesse de déplacement transversale: $v_y(x,t)$
    * la tension de la corde en tout point: $\overrightarrow{T(x,t)}$ (ici la force exercée par la partie à gauche de x sur la partie à droite de x).
* __Célérité des ondes mécanique__  On peut montrer que (sous hypothèse) $v_{onde}=\sqrt{\frac{T_0}{\mu_0}}$
````

### Ondes acoustiques
````{topic} Description
Une onde sonore est la propagation dans un milieu matériel (par exemple l'air) d'une surpression provoquant sur son passage une agitation locale du milieu. Considérons une tube dans lequel se trouve de l'air (on pourra par exemple assimiler cela à un instrument à vent). Un surpression causée en entrée va «pousser» une tranche de fluide (l'air), qui en s'agitant va induire une surpression sur la tranche de fluide suivant qui se met à son tour en mouvement et ainsi de suite: il se propage un son. Ce son arrive jusqu'à nos oreilles où jusqu'à un micro. La surpression qui s'est propagée fait alors vibrer une membrane (tympan ou capteur de pression).

__Description physique__  
* __Système étudié:__  On étudie le mouvement d'une tranche de fluide d'épaisseur dx autour d'une position x.
* __Grandeur considéré (dans le cas d'un fluide):__
    * la surpression engendrée: $p(x,t)$. La pression au point M est: $P(x,t)=P_O+p(x,t)$ où $P_0$ est la pression du milieu au repos.
    * la vitesse de la portion de fluide: $v(x,t)$ (pas de grandeur à ajouter car au repos, cette portion de fluide ne bouge évidemment pas).
    * la variation de masse volumique du fluide: $\Delta \mu(x,)t$. $\mu(x,t) = \mu_0 + \Delta \mu(x,t)$ ($\mu_0$ est la masse volumique du fluide au repos).
* __Intensité acoustique__ : On définit l'intensité acoustique instantanée $I(x,t)$ d'une onde sonore comme la puissance transportée par l'onde dans une direction donnée par unité de surface.
    * On peut montrer que l'intensité acoustique instantanée dans la direction de propagation du son est $I(x,t)=p(x,t)v(x,t)$.
    * L'intensité acoustique est la valeur moyenne de l'intensité acoustique instantanée.
    * Le niveau d'intensité sonore est définit par $L = 10 \log(I/I_0)$ exprimé en dB où $I_0 = 10^{-12} \rm{SI}$
_Ces formules ne sont pas à connaître mais on retiendra qu'une onde __transporte une puissance__ ._
````

### Ondes à la surface d'un fluide

````{topic} Description
La surface d'un fluide (l'eau), peut être excitée par exemple par le vent, donnant naissance à la houle. Ce phénomène correspond à la propagation d'une onde à la surface du fluide. En effet, il se produit alors une montée d'eau en une position. La conservation de la masse et la variation de pression dans la colonne d'eau induit alors une variation de hauteur d'eau dans la colonne d'eau suivante et ainsi de suite se propage une onde de surface. Nous signalons simplement l'existence de ces ondes car elles sont courantes autour de nous et qu'elles seront étudiée de manière descriptive en TP.

_Grandeurs observées:_ En un point du passage de l'onde, on peut définir la hauteur de la surface du fluide à un instant t: $z(x,t)$. Il existe d'autres grandeurs décrivant le passage de l'onde mais nous nous limitons ici à cette grandeur qui suffit à décrire l'onde à chaque instant.
````

### Ondes électriques
````{topic} Description
Quand en un point du circuit, on modifie le potentiel ou l'intensité (exemple: on allume le circuit), la  variation locale d'intensité/de potentiel va se propager de proche en proche tout au long du circuit: une onde électrique se propage dans le circuit.

__Description physique__  
* Le système étudié est une portion de circuit et sa modélisation électrique (cf. deuxième année). Les grandeurs utilisées sont bien entendu le potentiel électrique et l'intensité.
* _ARQS : On rappelle que la célérité des ondes électriques est de l'ordre de la célérité de la lumière dans le vide de sorte que pour des signaux "lents" sur des circuits "courts", on peut négliger les phénomènes de propagation, c'est-à-dire les considérer comme instantanés._
````

### Ondes électromagnétiques
````{topic} Description
Dans une approche classique de la lumière, celle-ci est une onde électromagnétique. La propagation d'une onde électromagnétique correspond à la propagation d'une variation des champs électriques $\overrightarrow{E}(M,t)$ et magnétique $\overrightarrow{B}(M,t)$ en tout point du trajet de l'onde. Les variations spatiales et temporelles des ces deux grandeurs sont corrélées par des équations (les équations de Maxwell). Ces relations permettent de propager ces variations de proche en proche: une onde électromagnétique se propage.

__Description physique__  
*  Le système étudié est une portion d'espace. Comme précisé précédemment, les grandeurs qui décrivent l'onde seront le champ électrique et magnétique en chaque point. On remarque qu'il s'agit de __champs vectoriels__ . L'orientation du champ électrique est notamment extrêmement importante.
* _Dans le vide, les ondes électromagnétiques se propage à la vitesse $c=299792458 \rm{m.s^{-1}}$._
* __Considérations énergétiques__ : Energie propagée: L'étude de l'énergie propagée par une onde électromagnétique est un peu complexe. On peut retenir que:
    * On traite en général l'éclairement énergétique I qui correspond à l'énergie transportée par le rayonnement électromagnétique par unité de surface (on pourra faire le parallèle avec les cas précédents).
    * La sensation de luminosité perçue par notre oeil est en rapport avec l'éclairement.
    * Pour une onde monochromatique progressive, l'éclairement est proportionnel au carré du module du champ électrique $I \approx \frac{cn \epsilon}{2} \vert E^2 \vert$. Le coefficient de proportionnalité n'est pas à connaître. Un rapide calcul montre que les fréquences associées au rayonnement visible sont de l'ordre de $10^{14}\rm{Hz}$. Cela montre que notre oeil n'est pas sensible à l'éclairement instantanée mais à la valeur moyenne de l'éclairement. __C'est pourquoi, on définit directement l'éclairement énergétique comme une grandeur proportionnelle à la valeur moyenne du champ électrique au carré.__ __$I \propto \langle E^2 \rangle$__ 
````

## Front d'onde et diffraction

### Source lumineuse
````{important} __Point source lumineux__
* Un point source lumineux est un point émettant une onde lumineuse dans une ou plusieurs direction. On lui associe en général un cône d'émission (qui peut-être toute la sphère) ainsi qu'un spectre d'émission.
* Un point source monochromatique est un point source émettant une lumière monochromatique.
````

### Front d'onde
````{important} __Surface d'onde__
Une surface d'onde (où front d'onde) est l'ensemble des points possédant la même phase (le même retard sur la source de l'onde).

```{figure} ./images/Signaux_ondes_circulaire.jpg
:name: fig_293
:align: center
:width: 30%
```
Sur le graphique précédent, on a représenté en traits pleins les surfaces d'ondes et en pointillés les "rayons" de l'onde correspond à la direction de propagation.
````

````{important} __Théorème de Malus (Admis)__
Lorsque le phénomène de diffraction peut-être négligé (cf. suite), le trajet d'une onde matérialisée par le trajet de l'énergie suivant des "rayons" est perpendiculaire au surface d'onde (cf. la figure précédente).
````

````{important} __Types d'ondes__
* __Cas d'une onde plane:__  l'amplitude ne dépend pas de la position transverse à la propagation. On étudie souvent ce type d'onde car elle est simple mais les ondes créées en général sont plutôt circulaires ou sphériques (et encore... ).
```{figure} ./images/Signaux_ondes_planes.jpg
:name: fig_294
:align: center
:width: 30%
```
* Cas d'une ondes circulaire: (on pourra généraliser l'idée à une onde sphérique à 3 dimensions) Il s'agit d'une représentation assez usuelle pour une source ponctuelle (point lumineux, source sonore... ).
```{figure} ./images/Signaux_ondes_circulaire.jpg
:name: fig_295
:align: center
:width: 30%
```
````
