# Scraping des avis des pharmacies de France métropolitaine sur googlemaps

## Présentation
Ce projet a été réalisé dans le cadre d'un stage d'initiation et de découverte au laboratoire ICube.
L'objectif principal du projet est de constituer une base de données structurée des avis Google Maps associés aux pharmacies de France métropolitaine.
Le projet comprend plusieurs étapes allant de la préparation et de l'enrichissement d'une base nationale de pharmacies jusqu'à la collecte automatisée, au nettoyage et à la sauvegarde des avis Google Maps.
Les données obtenues pourront notamment être utilisées pour des analyses statistiques, de la visualisation de données et des travaux d'analyse de sentiment.
## Objectifs du projet
Les principaux objectifs sont :
* rechercher et sélectionner une base nationale de référence recensant les pharmacies ;
* sélectionner les variables pertinentes pour le projet ;
* nettoyer et préparer les données ;
* exploiter les coordonnées géographiques des pharmacies ;
* convertir les coordonnées dans un système adapté aux traitements géographiques ;
* retrouver et reconstruire les informations d'adresse nécessaires ;
* attribuer chaque pharmacie à sa région administrative ;
* rechercher automatiquement les fiches des pharmacies sur Google Maps ;
* récupérer les informations associées aux établissements ;
* collecter les avis publiés par les utilisateurs ;
* récupérer les réponses des propriétaires lorsqu'elles sont disponibles ;
* nettoyer et structurer les données textuelles ;
* mettre en place un système de sauvegarde et de reprise après interruption ;
* produire une base de données exploitable pour des analyses ultérieures.
## Technologies utilisées
Le projet repose principalement sur les technologies suivantes :
* Python : langage principal du projet ;
* Pandas : manipulation et préparation des données ;
* GeoPandas : traitement des données géographiques ;
* Playwright : automatisation du navigateur et scraping ;
* AsyncIO : gestion des opérations asynchrones ;
* Google Colab : environnement principal de développement et d'exécution ;
* Git / GitHub : gestion et documentation du projet.
## Pipeline du projet
Base nationale -> Sélection des variables -> Nettoyage -> Conversion des coordonnées -> Attribution des régions -> Recherche Google Maps -> Extraction des avis -> Nettoyage des textes -> Sauvegarde -> Base finale

1. Recherche et sélection de la base nationale

Une première étape a consisté à rechercher une source de données permettant de disposer d'une liste aussi complète que possible des pharmacies de France métropolitaine.

La base sélectionnée a ensuite été étudiée afin d'identifier les informations disponibles et leur pertinence pour la suite du projet.

2. Sélection des variables

Les différentes variables disponibles dans la base ont été analysées afin de conserver uniquement celles nécessaires au projet.

Une attention particulière a été portée aux informations permettant d'identifier et de localiser les pharmacies :

* identifiant ;
* nom ;
* coordonnées géographiques ;
* informations d'adresse disponibles ;
* autres variables utiles au processus de collecte.

3. Préparation des données géographiques

Les coordonnées géographiques présentes dans la base ont été analysées puis converties lorsque cela était nécessaire afin de pouvoir les exploiter avec les outils de traitement géospatial.

Les pharmacies ont ensuite été associées aux régions administratives françaises à partir de leurs coordonnées et des limites géographiques correspondantes.

4. Enrichissement des informations

Certaines informations d'adresse étant absentes ou incomplètes dans la base initiale, plusieurs traitements ont été réalisés afin de reconstruire ou compléter les informations nécessaires à l'identification des pharmacies.

Cette étape a notamment permis d'améliorer les requêtes utilisées lors de la recherche des établissements sur Google Maps.

5. Développement du scraper

Un système automatisé de collecte a été développé en Python.

Le scraper permet notamment de :

* rechercher une pharmacie ;
* accéder à sa fiche Google Maps ;
* identifier la fiche correspondant à l'établissement recherché ;
* accéder aux avis ;
* faire défiler automatiquement la liste des avis ;
* récupérer les informations disponibles pour chaque avis ;
* détecter les éventuelles réponses des propriétaires.

6. Nettoyage et structuration des avis

Les données extraites ont fait l'objet de différents traitements afin d'obtenir une structure homogène.

Les informations collectées peuvent notamment comprendre :

* l'identifiant de la pharmacie ;
* le nom de la pharmacie ;
* la ville ;
* la région ;
* la note moyenne de la pharmacie ;
* la date de l'avis ;
* la note attribuée par l'utilisateur ;
* l'auteur ;
* le texte de l'avis ;
* la longueur du texte ;
* le nombre de mots ;
* la présence d'une réponse du propriétaire ;
* le texte de la réponse du propriétaire ;
* la date de la réponse lorsqu'elle est disponible.

7. Sauvegarde et reprise

Compte tenu du volume important de données à collecter, un système de sauvegarde et de reprise a été développé.

Le système permet notamment de :

* sauvegarder régulièrement les données collectées ;
* conserver des points de reprise ;
* enregistrer les erreurs rencontrées ;
* reprendre le traitement après une interruption ;
* éviter de recommencer inutilement une collecte déjà effectuée.

## Résultat attendu
Une base de données contenant :
* les informations des pharmacies (id, nom, adresse) ;
* la note moyenne ;
* le nombre d'avis ;
* les commentaires ;
* les réponses des propriétaires ;
* des variables prêtes pour l'analyse de sentiment ;

Le résultat final du projet est une base de données structurée permettant de relier les pharmacies aux avis publiés sur leurs fiches Google Maps.
Cette base constitue une étape préparatoire à de futurs traitements de données, notamment :
* analyse statistique des avis ;
* analyse des notes ;
* analyse de sentiment ;
* traitement automatique du langage naturel ;
* comparaison entre régions ;
* visualisation des résultats.
## Contexte du projet
Type de projet : Stage d'initiation et de découverte

Structure d'accueil : Laboratoire ICube

Domaine : Data Science / Data Engineering / Web Scraping

Zone étudiée : France métropolitaine

## Données et confidentialité

Les fichiers de données complets issus de la collecte ne sont pas publiés directement dans ce dépôt.

Le dépôt pourra contenir des données d'exemple permettant de comprendre la structure de la base sans diffuser l'ensemble des données collectées.

## Auteure
Doriane Sambore

Étudiante en Master Intelligence des Données en Santé

Université de Strasbourg

Projet réalisé au sein du laboratoire ICube en étroite collaboration avec Louise Meksem et Flora Yoang également étudiantes en Master Intelligence des Données en Santé.
