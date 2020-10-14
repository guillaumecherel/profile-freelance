+++
title = "Exploration des sorties d'un modèle de simulation"
+++

*2013-2015, CNRS, Institut des Systèmes Complexes — Paris Île-de-France.*

Pour tester la validité d'un modèle qui vise à expliquer un phénomène, nous
avons proposé de rechercher ses comportements inattendus : ceux-ci peuvent
constituer des contre-exemples, révéler des bugs ou des erreurs dans les
hypothèses sous-jacentes. À cette fin, notre algorithme génétique PSE (pour
pattern space exploration) explore les sorties possibles d'un modèle en
simulation. 

Nous l'avons [appliqué à un modèle de croissance de villes][pse]. La
figure ci-contre montre que le modèle est capable de produire des systèmes de
villes dont la hiérarchisation (le rapport entre la taille de ville la plus
grande et celle des autres) et la croissance de la population dépassent
largement les valeurs plausibles pour un géographe (zones grises).

[pse]: https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0138212
