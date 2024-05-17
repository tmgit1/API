# StackOverflow Tag Predictor

Ce projet est une API permettant de prédire des tags pertinents pour une question donnée dans le domaine de l'informatique, en utilisant un modèle de machine learning entraîné sur des données provenant du site Stack Overflow.


## Objectif du projet
L'objectif principal de ce projet est de fournir aux utilisateurs un outil qui leur permet de saisir une question et d'obtenir automatiquement des tags pertinents associés à cette question, facilitant ainsi la catégorisation et l'indexation des questions dans le domaine de l'informatique.


## Structure du projet
```
project
│   README.md
│   file001.txt    
│
└───folder1
│   │   file011.txt
│   │   file012.txt
│   │
│   └───subfolder1
│       │   file111.txt
│       │   file112.txt
│       │   ...
│   
└───folder2
    │   file021.txt
    │   file022.txt
```
Le projet est organisé comme suit :

**src/** : Ce dossier contient le code source de l'API, ainsi que d'autres fichiers et dossiers pertinents pour le développement et le déploiement de l'application.

main.py : Le code principal de l'API, qui définit les endpoints et gère les requêtes des utilisateurs.

frontend.py : Le code pour le frontend de l'API.

requirements.txt : Fichier contenant les packages Python nécessaires pour exécuter l'application.

test_sample.py : Fichier contenant les tests unitaires pour l'API.

utils/ : Ce dossier contient des utilitaires et des ressources nécessaires au fonctionnement de l'API.

setup_model.py : Un script pour télécharger un modèle Universal Sentence Encoder qui sert à créer un embedding à la question de l’utilisateur.

final_model.sav : Le modèle de régression logistique entraîné pour prédire les tags.

model_trained.py : Un script pour charger le modèle entraîné et effectuer des prédictions de tags.

.github :
workflows :
main_p5-api.yml : Fichier Github Actions permettant d’exécuter automatiquement les tests à chaque push ainsi qu’à vérifier le formatage du code, et lance le déploiement de l’api sur le cloud.

## Utilisation de l'API
Pour utiliser l'API, il suffit d'envoyer une requête HTTP POST avec une question en tant que donnée JSON à l'endpoint approprié de l'API. L'API renverra alors une liste de tags prédits pour cette question.
Cette api peut être accédé via l’url : p5-api.azurewebsites.net/docs, dans la requête post. Ou par le frontend à l’url : https://m4zbyakudey4pn5zmb7fhy.streamlit.app/

## Développement continu et déploiement sur le cloud
Le projet intègre un pipeline de développement continu qui exécute des tests automatiques avec pytest à chaque nouveau push sur le dépôt GitHub ainsi qu’un formatage à l’aide des outils Black et Ruff. De plus, le déploiement de l'API est automatisé sur le cloud à l'aide de Microsoft Azure, assurant ainsi une gestion efficace et fiable de l'application en production.
