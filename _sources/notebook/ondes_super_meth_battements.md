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
# Activités
## Battements
__Position du problème__  
On considère deux diapasons identiques dont l'un est monté avec une petite masselotte qui modifie légèrement sa fréquence d'émission. On excite les deux diapasons et on écoute le son obtenus puis on l'enregistre au moyen d'un dispositif {micro+système d'acquisition}. On observe que les variations d'amplitude sont lentes de sorte qu'on peut les sentir à l'oreille (cf. Simulation Audacity).

````{admonition} Exercice 
:class: attention
__Modélisation__  
On considère les deux ondes précédentes issues de deux sources $u_1$ et $u_2$ asynchrones de fréquences respectives $f_1$ et $f_2$. On considère qu'il s'agit d'ondes sonores de fréquences très proches l'une de l'autre. On considère de plus pour simplifier que les deux ondes ont la même amplitude de pression: $u_0$ et que le déphasage initial entre les deux sources est constant et nul.

On considère le problème proposé précédemment.
1. Exprimer la surpression ressentie en un point M.
1. Montrer que celle-ci s'apparente à un signal sonore de fréquence $f_f$ à préciser modulé en amplitude par un sinusoïde à la fréquence $f_m$ à préciser. Représenter graphiquement l'amplitude correspondante.
1. Exprimer l'intensité sonore perçue et montrer qu'elle varie aussi dans le temps.
1. Donner la représentation de Fresnel des deux ondes et de l'onde résultante à différents instants. Retrouver le principe d'une modulation d'amplitude.
1. (Simulation): On pourra chercher, au moyen de logiciels simulant des sons (Ex: Audacity) à partir de quelle fréquence l'on arrive plus à déceler la variation temporelle de l'intensité sonore (c'est un ordre de grandeur car il sera probablement différent pour chacun)
````

````{admonition} A retenir
:class: important
La superposition de deux ondes de fréquences très proches cause un phénomène de battement : l'onde résultante est une onde modulée en amplitude.
````