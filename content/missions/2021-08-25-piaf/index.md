+++
template = "mission.html"
title = "Détecter les dégradations de performances du système de question-réponse de Piaf"

[extra]
# Special extra date format for year only date span
date = "2021"
client = "Etalab"
+++

**Contexte :** Piaf est un moteur de question-réponse en français destiné aux
admistrations publiques françaises. Son but est d'aider les visiteurs d'un site
web d'administration publique à trouver la réponse à une question qu'ils se
posent, comme "Comment faire une demande de passeport ?".

**Besoin :** Piaf traite les questions avec une chaîne de traitement de type
*retriever-reader*. L'équipe la fait évoluer continuellement avec de nouveaux
modèles d'intelligence artificielle et de nouvelles données. Il faut s'assurer
que les nouvelles versions ne dégradent pas les performances établies pour les
clients actuels. Les tests prennent du temps et nécessitent un
GPU. Ils doivent être réalisés suffisamment souvent pour que les dégradations de
performances soient détectées tôt, avant la mise en production.

**Résultats :** Un rapport automatique quotidien des performances de la chaîne
de traitement permet à l'équipe de détecter les dégradations d'un jour à l'autre.

**Méthode :** Un script Python déclenché chaque nuit via cron lance les tests et
les publie sur un server [mlflow](mlflow.org) accessible par l'équipe.
L'ensemble est dockerizé pour être déployé facilement sur la machine avec GPU
qui héberge les tests.

**Code :** <https://github.com/etalab-ia/piaf-ml>
