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
# Méthodes : Etude des interférences
## Fentes d'Young
````{admonition} Exercice 
:class: attention
Un éclairage LASER cohérent et monochromatique de longueur d'onde $\lambda_0$ éclaire un ensemble de deux fentes parallèles de longueur L et de largeur $\epsilon$ distantes l'une de l'autre de $a$. On suppose que $L\gg a$ et $a\gg \epsilon$ de sorte qu'on peut assimiler les fentes à des fentes de longueur infinies et d'épaisseur nulle.

On place un écran parallèle aux fentes à une distance D des fentes telle que $D>>a$ et on visualise la figure lumineuse en une zone proche du centre de l'écran (défini en regard du centre de la double fente). La figure, appelée figure d'interférences obtenues, est données figure suivante (la courbe correspond au profil d'intensité mesuré grâce à un capteur CCD).

```{figure} ./images/Signaux_young_schema.jpg
:name: fig_303
:align: center
:width: 50%
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
:width: 50%
```

Intérêt de l'ordre d'interéférences
1. Exprimer l'ordre d'interférence au centre de la figure (appelé $O_1$). Correspond-il à une frange brillante ou sombre?
1. Exprimer l'ordre d'interférence en un point M de l'écran situé à une abscisse x.
1. Exprimer au moyen de l'interfrange le nombre de franges située entre $O_1$ et M. Retrouver l'interprétation de l'interfrange.
````
````{topic} Correction
>__Calcul de la différence de chemin optique__  
>Le chemin parcouru par le premier rayon est $SS_1 M$ et le chemin parcouru par le second rayon est $SS_2 M$. Les portions $SS_1$ et $SS_2$ étant identique, la différence de marche (qui est aussi la différence de chemin optique puisque $n=1$) est la même. Il vient $\delta = S_2 M - S_1 M$ soit:
>
>\begin{align*}
\delta &= \sqrt{{\left(\frac{a}{2}- x\right)}^2 + D^2} - \sqrt{{\left(\frac{a}{2}+ x\right)}^2 + D^2}\\
&= D\left(\sqrt{{\left(\frac{\frac{a}{2}- x}{D}\right)}^2 + 1} - \sqrt{{\left(\frac{\frac{a}{2}+ x}{D}\right)}^2 + 1}\right)\\
&\approx D\left({1 + \frac{1}{2}\left(\frac{\frac{a}{2}- x}{D}\right)}^2 - \left(1 + \frac{1}{2}{\left(\frac{\frac{a}{2}+ x}{D}\right)}^2 + 1\right)\right)\\
&\approx - \frac{ax}{D}
\end{align*}
>
>__Déphasage et ordre d'interférence__  
>\begin{align*}
\Phi &= \frac{2 \pi \delta}{\lambda_0}\\
&\approx - \frac{2\pi ax}{D\lambda_0}\\
p &= \frac{\delta}{\lambda_0}\\
&=\frac{ax}{D\lambda_0}
\end{align*}
>
>__Interférences constructives et destructives__  
>Les interférences constructives sont obtenues là où le déphasage est de la forme $2m\pi$ avec $m \in \mathbb{Z}$ et les interférences destructives sont obtenues là où le déphasage est de la forme $(2m+1)\pi$ avec $m \in \mathbb{Z}$.
>
>\begin{align*}
&- \frac{2\pi ax_{constructif}}{D\lambda_0} = 2m \pi \\
& \Longrightarrow x_{constructif} = \frac{D \lambda_0 m}{ a}\\
&- \frac{2\pi ax_{destructif}}{D\lambda_0} = (2m + 1) \pi \\
& \Longrightarrow x_{destructif} = \frac{D \lambda_0 (m + 1/2)}{ a}
\end{align*}
>Les zones claires et sombres correspondent à des zones où x est fixé mais la coordonnées transverses y est quelconque: les zones claires et sombres seront des franges.
>
>__Interfrange et interférométrie.__  
>L'interfrange est l'écart minimale entre deux franges d'égales intensités (brillantes par exemples) donc soit: $i = x_{m+1} - x_{m} = \frac{D\lambda_0}{a}$. On observe que l'interfrange (grandeur mesurable est d'__autant plus grande que l'écart entre les fentes est petit__ : on peut donc remonter à une distance très petite en la transformation en une distance très grande, mesurable à notre échelle: c'est le grand intérêt de l'__interférométrie__ .
>
>__Figure d'interférences__  
>On observe bien l'alternance de franges brillantes et sombres comme prévu.
>
>Par contre, on observe une diminution de l'intensité quand on s'éloigne du bord qui n'est pas prévu par la théorie. Cela est du au phénomène de diffraction. Ce dernier élargie les faisceau au niveu des fentes permettant aux deux faisceaux de se rencontrer, __d'interférer__ . Mais cet élargissement est limité à un cône et en dehors de ce cône, l'intensité chute diminuant l'intensité des raies observées. Cette diminution n'est pas brutale mais suit un profil similaire à celui observé pour la diffraction seule dans le chaptre précédent.
>
>__Ordre d'interférence__  
>Au centre, $p=0$, on observe une frange brillante.
>
>En un point d'abscisse x, l'ordre d'interférence est $p = \frac{ ax}{D\lambda_0}$
>
>Entre O et M, le nombre de franges brillantes est $\frac{x}{i}= \frac{ax}{D\lambda_0} = p$: on retrouve le fait que la différence d'ordre d'interférence entre deux points correspond au nombre de franges brillantes visible (attention, il faut que l'ordre d'interférence soit monotone entre les deux points).
````

````{topic} Perte de cohérence temporelle
__La taille de l'interfrange varie en fonction de la longueur d'onde/__  Si on superpose deux couleurs (en envoyant une lumière qui n'est pas monochromatique), leur figure d'interférence va simplement se superposer (__ce sont deux ondes qui n'ont pas la même longueur d'onde donc il ne se produit pas d'interférences: on somme les intensités__ ).

Il se passe la même chose avec la lumière blanche: on observe une superposition continue de figure d'interférences décalées qui produisent un phénomène d'irisation. L'image est plus flou à cause des superposition: on parle de __décohérence temporelle__ .

```{figure} ./images/Signaux_3_Coherence.jpg
:name: fig_305
:align: center
```
````

## Interférences à l'infini
_Il est très fréquent qu'on s'intéresse à une figure d'interférence à l'infini. Nous allons voir comme la traiter puis comment traiter sa projection._


````{admonition} Interférences à l'infini 
:class: attention

On considère toujours le dispositif des fentes d'Young mais on supprime l'écran et on s'intéresse à la figure d'interférences observées à l'infini (celle qu'observerait un oeil emmétrope au repos se plaçant à la place de l'écran - attention en pratique, il ne faut pas le faire si c'est un LASER !).

1. Quelle grandeur va alors caractériser un point de l'image à l'infini ?
1. En utilisant le théorème de Malus et le principe de retour inverse, montrer que la différence de chemin optique se limite à la distance entre $S_2$ et le projeté de $S_1$ sur le rayon 2. En déduire la différence de chemin optique.
1. Exprimer alors les conditions d'intérférence constructives et destructives.
1. Comment faire pour observer la figure d'interférences à l'infini...  sur un écran. Déduire alors les conditions d'interférences constructives et l'interfrange sur l'écran.
````

````{topic} Correction
>__Image à l'infini__  
>Un point-image à l'infini est caractérisé par l'angle (noté $\theta_S$ ici) que fait le faisceau de rayon parallèle qui point vers le points avec l'axe optique (ici la médiane aux deux fentes). 
>
```{figure} ./images/Signaux_young_infini.jpg
:name: fig_306
:align: center
```
>
>Deux rayons issus des fentes et interférant en un point repérant par un angle $\theta$ seront donc deux rayons parallèles passant par $S_1$ et $S_2$ et faisant un angle $\theta$ avec l'axe optique (comme représenté ci-avant).
>
>Si l'on considère deux rayons issus du point image et se dirigeant vers les fentes, le théorème de Malus assure que les front d'onde sont perpendiculaire donc le déphasage entre deux plans perpendiculaire aux rayons est nul. Il reste que le déphasage entre les deux rayons quand il arrive aux fentes se résume au retard à la propagation associé au petit chemin supplémentaire parcouru par le rayon 2 pour aller du projeté de $S_1$ sur le rayon 2 (point noté H sur le même front d'onde que $S_1$) jusqu'au point $S_2$.
>
>Par principe de retour inverse, la lumière emprunte le même chemin pour aller des fentes au point objet et le déphasage entre les deux rayons sera le même que dans l'autre sens. Il vient que la différence de chemin optique sera $nS_2 H = S_2 H = a \sin \theta_S$.
>
>On en déduit la condition d'interférence constructive: $a \sin \theta_S = m \lambda_0$ avec $m \in \mathbb{Z}$.
>
>On déterminera de la même manière la condition d'interférence destructive.
>
>Pour observer la figure d'interférence à l'infini sur un écran, il faut la __projeter au moyen d'une lentille__ . On place l'écran dans le plan focal de la lentille qui est alors conjugué avec un objet à l'infini soit la figure d'interférence à l'infini.
````

````{admonition} Utilisation d'une lentille
:class: attention
On reprend le dispositif précédent et on place une lentille après les fentes puis un écran dans le plan focal image de la lentille.

```{figure} ./images/Signaux_Correction_Lentilles.jpg
:name: fig_307
:align: center
:width: 30%
```
Déterminer l'interfrance de la figure d'interférence sur l'écran.
````

````{important}
* Comme on peut le voir sur l'exemple ci-dessous, les rayons sont déviés par la lentille mais __on ne peut pas utiliser une somme par morceau des trajets car la schématisation de Gauss ne modélise pas l'épaisseur de la lentille__.
* La différence de chemin optique __est identique en deux points conjugués (objet et image) par un système optique__.
````

````{topic} Correction
>La méthode est la suivante:
>1. On déterminer l'antécédent de l'écran par la lentille (ici, c'est l'infini)
>1. On relie les caractéristiques géométriques d'un point de l'antécédent à celui d'un point sur l'écran.
>1. On détermine la figure d'interférence dans le plan de l'antécédent
>
>__Interférences dans le plan focal de la lentille__  
>1. On a placé l'écran de sorte qu'il soit conjugué avec le plan objet à l'infini donc la figure d'interférence sur l'écran est conjugué à celle à l'infini sans la lentille.
>2. Pour un point M situé à une distance x de l'axe optique, on peut construire les rayons incidents (faisceau de rayons parallèles) en utilisant les règles habituelles:
>    * ici on trace un rayon sortant passe par M et le centre optique vient d'un rayon non dévié. Les deux rayons incident passant par les sources et ressortant par M doivent être parallèles à ce rayon, d'où la construction.
>    * il vient que l'angle que fait le faisceau incident avec l'axe optique est $\theta \approx \tan \theta = \frac{x}{f'}$ (on utilise les conditions de Gauss pour réaliser un stigmatisme).
>3. On a déjà déterminé les caractéristiques de la figure d'interférence à l'infini (s'entrainer à le refaire).
>    * Dans les conditions d'interférences constructives, on a la relation $\theta \approx \sin \theta = m \frac{\lambda_0}{a}$ soit une condition d'interférence constructive sur l'écran: $x =\frac{mf' \lambda_0}{a}$.
>
>L'interfrange est donc $i = \frac{f' \lambda_0}{a}$.
>
```{figure} ./images/lentille.png
:name: fig_308
:align: center
```
````



