+++
+++

### 1. Développer des calculs scientifiques

Développer des méthodes de calcul en concertation avec des experts métiers pour
répondre à une question scientifique ou un besoin d'ingénierie,
d'automatisation, en favorisant un style de programmation fonctionnel. 

- Accompagnement pour la conception formelle de méthodes de calcul
    - Écrire un document formel pour spécifier rigoureusement les calculs à
      réaliser
- Développement d'algorithmes de calculs scientifiques
    - Écrire le code qui réalise les calculs souhaités en Rust, Scala,
      Haskell, Python
    - Développement de tests
- Développement de bibliothèque logicielle pour mettre les algorithmes à
  disposition d'utilisateurs.
    - Écrire une bibliothèque logicielle qui expose les algorithmes développé
      dans le même langage.
    - Écrire une bibliothèque pour faire le pont avec un autre langage,
      comme un langage de script comme Python, R ou Julia
    - Publier la bibliothèque sur les canaux de distributions propres au
      langage de développement 
- Développement de code pour générer des visualisations de résultats
    - Vega
    - Python/matplotlib

### 2. Automatiser et faciliter la collaboration

Mettre en place un environnement de développement et de calcul pour collaborer
sur le développement de calculs scientifiques et les exécuter: échanger du code,
gérer les versions, lancer des calculs et récupérer des résultats.

- Mettre en place un dépôt Git sur un serveur GitLab ou GitHub
- Mettre en place un environnement de calcul où exécuter les simulations et
  traiter les résultats de manière reproductible avec Docker et
  Docker-compose ou Nix, sur une machine locale, un cluster ou le cloud
    - Écrire les dérivations Nix pour installer sur une machine de calcul
      l'environnement logiciel nécessaire aux calculs
    - Écrire les fichiers Docker et Docker-compose pour créer les
      containers permettant de réaliser les calculs
    - Écrire le code qui déploie l'environnement de calcul, lance les
      calculs et traite les résultats (ex. envoi dans base de données) en
      Haskell, Scala ou Rust
- Automatiser le lancement des calculs et génération des résultats avec
  l'intégration continue et le déploiement continu.
    - Écrire des workflows d'intégration continue et déploiement continu avec
      GitLab-CICD
    - Surveiller la progression des calculs
        - Développer le code pour rapporter la progression des calculs sur
          l'interface GitLab-CICD
        - Développer une interface web avec Javascript, React ou Vega pour
          visualiser la progression des calculs
- Mise à disposition des résultats
    - Stockage dans une base de données
        - Stockage local avec une base SQLite ou arborescence de fichiers
        - Stockage sur un serveur avec une base de données relationnelle
          PostgreSQL
        - Stockage dans une base NoSQL MongoDB pour des données non
          structurées
    - Récupérer, visualiser ou interagir avec les résultats
        - Développer une interface sécurisée pour télécharger des fichiers
          de résultats
          - Écrire un fichier Docker pour un container accessible en https
            (local ou cloud)
          - Écrire le code qui génère une page HTML des liens vers les
            fichiers
        - Développer une interface web avec visualisation immédiate des
          résultats
          - Écrire une page HTML avec Javascript et/ou Vega qui génère les
            visualisations
        - Développer une interface interactive pour explorer les données
          - Écrire une page HTML avec Javascript et/ou Vega qui génère les
            visualisations interactives
        - Déployer un environnement de script collaboratif Jupyter où les
          méthodes de calcul sont disponibles sous forme de bibliothèques
          logicielles pour utilisation directe, ou bien les résultats des
          calculs accessibles pour une analyse exploratoire.
          - Écrire des fichiers Docker et Docker-compose pour déployer une
            instance Jupyter notebook ou JupyterLab
          - Écrire une bibliothèque qui contient les méthodes de calcul
            développées à importer depuis un notebook Jupyter, en fonction du
            langage choisi (probablement Python ou Julia).
          - Écrire une bibliothèque pour lire les données résultats à importer
            depuis un notebook Jupyter, en fonction du langage choisi
            (probablement Python ou Julia)


### 3. Mettre en production

Mettre des méthodes calcul scientifique en production: développer une
application qui intègre des méthodes de calcul développées ou se base sur les
résultats produits pour offrir un service à des utilisateurs (grand publique,
scientifiques, ingénieurs, décideurs…).  

- Développement backend
    - Développer le code qui implémente la logique des services à offrir et
      encapsule ou fait appel au méthodes de calculs ou résultats, en
      Haskell, Scala ou Rust
- Interface utilisateur
    - Développer une interface utilisateur en HTML et Javascript pour
      interagir avec le backend 
- Déploiement
    - Local 
        - Natif: Développement d'un paquet d'installation pour le système
          d'exploitation ciblé
        - Via Nix: Développement d'une dérivation Nix pour installer
          l'application et l'environnement nécessaire sur le système cible
        - Via Docker: Développement de fichiers Docker et Docker-compose pour
          exécuter les containers Docker (back, front, bdd…) qui font
          tourner l'application
    - Serveur
        - Via Docker: Développement de fichiers Docker et Docker-compose pour
          exécuter les containers Docker (back, front, bdd…) qui font
          tourner l'application
    - Cloud
        - Terraform (gestion des instances cloud)
        - Container Docker back-end
        - Container Docker front-end
        - Docker-compose
- Automatiser le passage du développement à la mise en production.
     - GitLab-CICD

