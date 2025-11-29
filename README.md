🌍 Analyse des Données de Systèmes Éducatifs — Projet Academy

📘 Introduction

Ce projet s’inscrit dans une mission professionnelle pour Academy, une startup EdTech spécialisée dans les formations en ligne pour les publics lycée et université.

Dans un contexte d’expansion internationale, l’objectif était d’évaluer si les données éducatives de la Banque mondiale pouvaient éclairer les décisions stratégiques de l’entreprise, et d’identifier les pays ou régions présentant un fort potentiel.

🎯 Objectifs du Projet

Évaluer la qualité du jeu de données (données manquantes, doublons, types).

Décrire la structure des fichiers fournis.

Sélectionner les indicateurs pertinents parmi plus de 4 000 variables.

Nettoyer et transformer les données pour obtenir un dataframe exploitable.

Réaliser une analyse descriptive par pays et par région.

Produire des visualisations claires et interprétables pour appuyer les décisions.

📊 Description des Données

Les données proviennent du portail EdStats – Banque Mondiale, qui recense des indicateurs relatifs :

à l’accès à l’éducation,

à la démographie étudiante,

aux dépenses publiques,

aux enseignants,

au numérique,

ainsi qu’à des aspects économiques liés à l’éducation.

Période étudiée : 2008 – 2012
(la plus complète en termes de taux de remplissage)

🛠️ Méthodologie

```
📁 Structure du projet
projet-education/
│
├── data/
│   ├── EdStatsCountry.csv
│   ├── EdStatsData.csv
│   └── EdStatsSeries.csv
│
├── analysis/
│   └── Fonkou_Symphor_1_notebook_130325.ipynb  # Notebook principal
│
├── presentation/
│   └── Fonkou_Symphor_2_présentation_130325.pptx.pptx   # Presentation pptx
│
└── README.md
```
1. ✔️ Analyse Générale

Importation des 5 fichiers sources.

Vérification des doublons et données manquantes.

Étude des types, formats, métadonnées.

Compréhension des indicateurs via EdStatsSeries.

2. ✔️ Sélection et Nettoyage

Sélection de 3 fichiers principaux :
EdStatsCountry, EdStatsData, EdStatsSeries.

Filtrages basés sur :

population (> 1 million),

taux d'utilisation d’Internet (> 25 %).

Choix de 11 indicateurs clés (éducation, économie, démographie, digital).

Gestion des valeurs manquantes (médiane ou suppression selon cas).

3. ✔️ Transformation

Création de dataframes dédiés :

par pays,

par région,

par indicateur.

Pivot des données pour analyse multivariée.

Calcul des moyennes 2008-2012.

4. ✔️ Analyse Exploratoire

Étude démographique et éducative.

Corrélations entre variables économiques / éducatives.

Comparaisons entre régions du monde.

Visualisations (histogrammes, boxplots, heatmaps, scatter plots).

📈 Indicateurs Sélectionnés
Catégorie	Indicateurs
Démographie	Population totale, Population 15–24 ans
Éducation	Inscriptions tertiaires, Population en âge d’études supérieures
Économie	PIB/habitant, RNB/habitant (PPA)
Digital	Utilisateurs Internet (%)
Emploi	Taux de chômage, Force de travail
🔍 Résultats Principaux
🌐 Tendances Générales

Asie de l’Est & Pacifique regroupe une très grande partie de la population jeune et étudiante.

Corrélation notable entre la croissance démographique et l’augmentation des inscriptions au supérieur.

PIB/habitant peu prédictif du taux d’inscription universitaire dans certains pays.

L’accès au numérique émerge comme un indicateur clé pour le potentiel d’expansion EdTech.

🥇 Marchés Prioritaires

Asie de l’Est (Chine)
→ Forte population jeune + forte croissance éducative.

Amérique du Nord (États-Unis)
→ Infrastructure digitale et marché déjà très réceptif à l’e-learning.

🥈 Marchés Secondaires

Europe
→ Demandes élevées en reconversion professionnelle.

Afrique du Nord (Maroc, Tunisie)
→ Forte croissance digitale + besoin d’accès à l’éducation.

📊 Visualisations

Le notebook comprend des graphes permettant d’analyser :

la répartition démographique,

l’utilisation d’Internet par pays,

les relations entre PIB et éducation,

les différences régionales.

(Des captures d’écran peuvent être ajoutées ici si souhaité.)

🚀 Installation & Exécution
Prérequis
Python 3.7+
Jupyter Notebook

Librairies
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

Lancement du projet
# Cloner le repository
git clone <votre-url-github>

# Accéder au dossier
cd projet-education

# Lancer Jupyter
jupyter notebook


Puis ouvrir :
➡️ analysis/education_analysis.ipynb

📁 Résumé des DataFrames Produits

All_Data_Country : données nettoyées par pays.

Data_Indicator_byCountry : tableau croisé pays × indicateurs.

Data_Indicator_byRegion : moyennes et statistiques par région.

💡 Recommandations Stratégiques
Phase 1

→ Cibler Asie de l'Est et Amérique du Nord (fort potentiel + infrastructure digitale).

Phase 2

→ Adapter l’offre aux établissements européens (besoin de reconversion).

Phase 3

→ Monitorer le développement digital de l’Afrique (croissance rapide).

🔮 Perspectives

Intégrer les années récentes (2015–2020).

Ajouter des données sur la qualité de l’éducation.

Étudier l’impact du COVID sur l’apprentissage en ligne.

Créer un dashboard interactif (Streamlit / Power BI).

👤 Auteur

Votre Nom
Data Scientist – Projet réalisé pour Academy EdTech
📧 Contact : symphorfonkou@gmail.com