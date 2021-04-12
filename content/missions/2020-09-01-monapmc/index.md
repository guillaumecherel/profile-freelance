+++
template = "mission.html"
title = "Parallélisation d'un algorithme d'inférence bayésienne en simulation"

[extra]
# Special extra date format for year only date span
date = "2017-2020"
client = "CNRS, Institut des Systèmes Complexes — Paris Île-de-France"
+++

**Besoin :** Calibrer un modèle multi-agents de système complexe.

**Solution apportée :** Une algorithme de calibration permettant d'exploiter
en parallèle plusieurs milliers de processeurs.

**Méthode :** Partant d'un algorithme de calcul bayésien approché
(approximate Bayesian computation) de l'état de l'art, conception et
implémentation d'une version parallèle multi-niveaux.

**Code :** Une [implémentation en
haskell](https://github.com/guillaumecherel/monapmc) avec tests de la méthode.
Une [implémentation en Scala](https://github.com/openmole/mgo) pour la
plateforme de simulation OpenMOLE.

Les méthodes d'inférence bayésienne par simulation (Approximate Bayesian
Computation) requièrent un très grand nombre d'exécutions de modèles. Celles-ci
étant indépendantes, on peut les exécuter en parallèle pour tirer profit des
ressources de calcul distribuées. Cet algorithme permet d'exploiter
efficacement des milliers de cœurs en parallèle.

La figure ci-contre montre que le temps d'exécution de l'algorithme (vert)
décroit plus vite que celui de son concurrent (violet) lorsque le nombre de cpu
disponible (K) augmente. Chaque point correspond à une exécution d'un
algorithme avec un paramètrage fixé. Les paramètres sont échantillonnés
uniformément pour tester les deux algorithmes dans un large éventail de
conditions.
