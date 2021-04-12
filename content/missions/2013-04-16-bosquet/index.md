+++
template = "mission.html"
title = "Un modèle spatial de la dynamique de population d'arbres en savane"

[extra]
# Special extra date format for year only date span
date = "2010-2013"
client = "Université Paris 6, Laboratoire Bioemco"
+++

**Besoin :** Tester l'hypothèse que le regroupement d'arbres en bosquets joue un
rôle bénéfique pour la population de plantes en savane.

**Réponse apportée :** L'organisation spatiale des arbres joue bien un rôle dans
la croissance de population de plantes, mais dans le sens contraire à celui
attendu. La prise en compte de l'espace pour modéliser la croissance des plantes
est importante.

**Méthode :** Développement d'un modèle de simulation automate cellulaire en C
calibré avec des données de terrain par optimisation par algorithme génétique.

**Code :** [https://github.com/guillaumecherel/ModelCA](https://github.com/guillaumecherel/ModelCA)

En savane, les bosquets réduisent localement l'intensité du feu en projetant de
l'ombre au sol qui diminue le combustible — l'herbe — qui pousse. Ces
regroupements d'arbres pourraient jouer un rôle sur la population globale en
protégeant les jeunes pousses du feu. Ce modèle confirme que l'organisation
spatiale joue un rôle sur la dynamique de population globale, mais dans l'autre
sens : la population d'arbres est moindre comparée à un modèle non spatial.

Cette figure représente le modèle et des résultats de simulation. Le modèle de
type automate cellulaire fait évoluer la présence d'arbres (cases noires) en
fonction des recrutements (passages des jeunes au stade adulte) et des morts.
Ces événements dépendent de la présence de voisins via l'ombre projetée dans le
cas spatial, et de la densité d'arbres globale dans le cas non spatial. Lorsque
l'espace n'est pas pris en compte, la population d'arbres atteint un niveau
plus élevé que lorsqu'il l'est.

