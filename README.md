# Détection Automatique de Texte sur Cartes
## Contexte

Les cartes, qu'elles soient anciennes ou interactives, contiennent de nombreux toponymes et inscriptions textuelles essentiels à leur interprétation. Cependant, extraire manuellement ces textes à partir d'un format raster est une tâche chronophage, surtout lorsqu'on travaille avec une grande quantité de données.

## Cas d'utilisation : Le Projet LostInZoom

Ce projet s'inscrit dans le cadre de LostInZoom, qui étudie les effets de désorientation causés par les changements d’échelle sur les cartes interactives. L’objectif est de comprendre comment les lecteurs de cartes se repèrent en observant: 
- Les points d’ancrage identifiés grâce à des eye-trackers.
- Les zones dessinées par les utilisateurs pour indiquer ce qui les aide à s’orienter.
- Les toponymes jouent un rôle clé en tant que points d’ancrage récurrents. Calculer automatiquement l'intersection entre les zones de texte et les régions d'attention des lecteurs pourrait permettre de mesurer statistiquement leur importance.

## Objectif
Notre recherche vise à détecter l’emplacement et l’emprise des textes sur les cartes plutôt qu’à reconnaître les caractères ou convertir les inscriptions en format texte.

## Problématique
La détection automatique des textes sur cartes est un défi en raison de plusieurs spécificités :
**Variabilité des styles** : police, taille, orientation, couleur, crénage, casse, etc.
**Contexte graphique** : confusion possible avec des éléments adjacents (routes, bâtiments, arrière-plans).

## Approche adoptée : **Deep Learning** model FOST
Les méthodes d’apprentissage profond (deep learning) se sont révélées performantes et plus flexibles que les procédés traditionnels pour la détection de texte. Cependant, les modèles existants sont souvent entraînés pour détecter du texte sur des photographies, ce qui limite leur efficacité sur des cartes, qui possèdent leurs propres caractéristiques.

## Question de recherche
Comment améliorer la détection des textes sur des cartes par deep learning et la rendre robuste aux changements de styles ?

## Enjeux
- Adapter les modèles existants aux spécificités des cartes.
- Gérer les variations de style et d’orientation.
- Éviter les confusions avec les éléments graphiques environnants.

## Résultats attendus
### Une méthode robuste permettant de :
- Identifier précisément les zones de texte sur une carte.
- Répondre aux besoins d’applications variées telles que la vectorisation de cartes anciennes ou l’analyse des points d’ancrage pour les cartes interactives.
  
## Technologies et outils utilisés
**Deep Learning** : Approches basées sur des réseaux de neurones convolutionnels.
Pré-traitement et préparation des données spécifiques aux cartes.
Validation via des tests sur des datasets cartographiques variés.
