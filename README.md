<h1 align="center"> ASHRAE - Great Energy Predictor III: How much energy will a building consume? </h1>

> Réalisé par : AGBOHOUTO Olivier - EL HAJAM Nawal - KOUA Jean-Charles - YOKAM Muriel

> Encadré par : GUILLOUX Agathe - BUSSY Simon 



# Problématique et but du projet

De nos jours, de plus en plus d'investissements sont réalisés dans le domaine de l'immobilier dans le but de réduire les consommations d'énergie des bâtiments et d'améliorer l'impact environnemental.\
Ainsi, les propriétaires d'immeubles peuvent bénéficier de financements basés sur la différence entre la consommation d'énergie réelle du bâtiment et celle qu'il aurait utilisée sans aucuns travaux d'aménagement. Toutefois, les données sur la consommation d'énergie des bâtiments au cas où il n'aurait pas de rénovation ne sont pas disponibles.\
Pour résoudre ce problème, des modèles contrefactuels sont développés afin de modéliser la consommation d'énergie d'un bâtiment sans travaux de rénovation.
Le but de ce projet est de construire ces modèles contrefactuels pour les quatre types d'énergie que sont la consommation d'eau froide, d'électricité, d'eau chaude et de vapeur en se basant sur les taux d'utilisation historiques et les conditions météorologiques observées. Il s'agira concrètement de prédire les valeurs de la variable meter_reading pour 1449 bâtiments.

# Plan d'analyse et de traitement

Pour atteindre l'objectif de ce projet, nous avons adopté le plan  d'analyse suivant:

## Analyse exploratoire et visualisation des données
Cette partie vise la prise en main des bases de données, leur assimilation à travers l'analyse de chacune des tables et la visualisation des données. Ceci permets aussi, de mieux saisir les objectifs et les différents modèles à mettre en oeuvre

## Fusion des diiférentes tables de données
Plusieurs tables de données ont été fournies pour ce projet. Il faudra donc les fusionner afin d'obtenir une base de données générale comprenant toutes les informations pour chaque site et chaque bâtiment. Chaque table contient une clé primaire et une clé étrangère permettant la fusion.\
Les tables **_train** sont fusionnées entre elles pour constituer les données d'apprentissage.\
Les tables **_test** également sont fusionnées entre elles pour servir à la prédiction et la soumission.

## Traitement des données
Cette partie vise à traiter les données par la gestion des valeurs manquantes, la gestion de valeurs aberrantes, l'encodage des variables, l'extraction de features, le preprocessing et la division de base en ensemble d'apprentissage d'évaluation

## Apprentissage, prédiction et soumission
Plusieurs modèles ont été mis en oeuvre dans le cadre de ce projet. Entre autres, le **gradient boosting**, le **RandomForest**, le **CatBoost**, le **XGBoost**, le **HistBoost**, le **LightGBM** ou encore le **DecisionTree**. Les résultats obtenus pour chaque modèle ont été soumis en vue de leur comparaison.\
Pour chaque modèle, nous l'entrainons sur la base d'apprentissage obtenue lors de l'étape de traitement des données et l'évaluons sur les données d'évaluation.\
Le modèle obtenu est ensuite utilisé pour prédire les données de la base test. Cette prédiction est alors soumis pour obtenir le score.

# Présentation du github

Ce github comprends un **readme**, un dossier **code** et un dossier **soumission** et un dossier **Suivi**.\
Le dossier **Code** contient les différents notebooks de chacune des parties décrites précédemment.\
Le dossier **soumission** contient les scores obtenus après soumission pour les différents modèles implémentés. Pour chaque modèleplusieurs soumissions ont été réalisées puisque les modèles sont améliorées (feature engineering-recherche de meilleurs hyperparamètre) afin d'obtenir le score le minimum.\
Le dossier **suivi** présente les travaux réalisés et leur évolution.

# Organisation du travail

Notre groupe est composé de  quatre étudiants. Pour atteindre l'objectif de ce projet, le travail a été subdivisé avec des réunions hebdomadaires pour faire le point apprécier les travaux individuels et programmer les prochaines étapes. Chaque membre du groupe a analysé une des tables de données pour la partie analyse exploratoire et la visualisation des données. 
Les parties **Fusion des différentes tables de données** et **traitement de données** sont été réalisées en commun. Chaque membre du groupe a à charge un ou plusieurs modèles à mettre en oeuvre pour la partie **Apprentissage, prédiction et soumission**.
