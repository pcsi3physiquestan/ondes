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

## Présentation

````{important} 
__Onde stationnaire__

Une onde stationnaire est le phénomène résultant de la propagation simultanée dans des sens opposés de plusieurs ondes de même fréquence et de même amplitude, dans le même milieu physique, qui forme une figure dont certains éléments sont fixes dans le temps.
````

````{margin}
On peut très bien remplacer les fonctions sinus par des fonctions cosinus.
````
````{important} 
__Expression mathématique__

Une onde stationnaire peut s'écrire sous la forme:
\begin{equation}
y(x,t) = f(x)g(t) = A \sin (\omega t + \varphi) \sin (k x + \psi)
\end{equation}
````

````{important} 
__Analyse. Noeuds et ventre.__

Le terme __stationnaire__  est associé au fait que le temps et l'espace sont maintenant séparé dans deux fonctions. Il n'y a ainsi plus de propagation (cf. Animation ci-après).

```{figure} ./images/Standing_wave.gif
:name: fig_309
:align: center
```

On observe qu'en certains points, la grandeur $y(x,t)$ __est toujours nulle__ : on appelle ces points les __noeuds.__ 

On observe qu'en certains points, la grandeur $y(x,t)$ __est toujours maximale__  (relativement au reste de la corde): on appelle ces points les __ventres.__ 

Le caractère stationnaire implique que les noeuds et les ventres sont __fixes.__ 
````

````{important} 
__Superposition__

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

````{margin}
L'argument "réflexion parfaite" ne suffit pas pour justifier l'existence d'une onde stationnaire. Il faut utilise la nullité de la grandeur associée pour le démontrer. Nous allons voir la méthode sur l'exemple de la corde.
````
````{topic} __Superposition et réflexion totale__
La manière la plus simple de réaliser une onde stationnaire et de __réfléchir parfaitement__  l'onde progressive (incidente). Dans ces conditions, l'onde réfléchie (régressive) aura la même amplitude.

Une réflexion totale impose en général un __noeud__ pour l'onde stationnaire pour l'une des grandeurs. C'est en utilisant ces conditions qu'on démontre que l'onde résultante sera stationnaire (cf. exemple).

* Exemple de réalisation d'une réflexion totale
    * Miroir parfait: il permet la réflexion totale d'une onde électromagnétique en impose un champ électrique nul à sa surface.
    * Corde: un point d'attache impose une vitesse de vibration nulle et une réflexion parfaite.

````

## Modes propres
Cf. [l'exercice corrigé](md_pr). Il est important de savoir retrouver les modes propres quantifiés d'une onde stationnaire quand on a imposée 2 conditions aux limites.