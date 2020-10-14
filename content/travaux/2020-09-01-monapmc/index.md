+++
title = "Un algorithme hautement parallélisable d'inférence bayésienne en simulation."
+++

*2017-2020, CNRS, Institut des Systèmes Complexes — Paris Île-de-France.*

Les méthodes d'inférence bayésienne par simulation (Approximate Bayesian
Computation) requièrent un très grand nombre d'exécution de modèles. Celles-ci
étant indépendantes, on peut les exécuter en parallèle pour tirer profit des
ressources de calcul distribuées. Cet algorithme permet d'exploiter
efficacement des milliers de cpu en parallèle.

La figure ci-contre montre que le temps d'exécution de l'algorithme (vert)
décroit plus vite que celui de son concurrent (violet) lorsque le nombre de cpu
disponible (K) augmente. Chaque point correspond à une execution d'un
algorithme avec un paramètrage fixé. Les paramètres sont échantillonnés
uniformément pour tester les deux algorithmes dans un large éventail de
conditions.
