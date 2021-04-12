+++
template = "mission.html"
title = "Estimation de la pollution sonore"

[extra]
# Special extra date format for year only date span
date = "2016-2017"
client = "Inria"
+++

**Besoin :** Estimer l'exposition au bruit d'un individu grâce à son téléphone
mobile.

**Solution apportée :** Une méthode statistique pour estimer l'expostion au 
bruit heure par heure d'un utilisateur de téléphone mobile.

**Méthode :** Application d'une méthode d'assimilation de données (Best Linear
Unbiased Estimator) à des données d'intensité sonore récoltées par des
téléphones mobiles et implémentation en Python.

Le bruit a des [conséquences problématiques sur le sommeil, le cœur, les
performances scolaires][who-noise]… Les smart-phones sont équipés de microphones qui
permettent de mesurer le niveau de bruit dans l'environnement de leurs
utilisateurs. La figure ci-contre montre l'évolution des niveaux de bruits
relevés par des téléphones mobiles.

[who-noise]: https://www.euro.who.int/en/health-topics/environment-and-health/noise/data-and-statistics

En utilisant ces données, nous avons utilisé l'assimilation de données pour
estimer l'exposition au bruit d'utilisateurs individuels, et comparé les
expositions moyennes de deux populations. Sans surprise, Paris est plus
bruyante que le reste de la France.



