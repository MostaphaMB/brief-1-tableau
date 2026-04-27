# 📊 Analyse et Visualisation des Ventes dans Tableau

![Image du Dashboard](LIEN_DE_VOTRE_IMAGE_ICI)

## 📝 Présentation du Projet
Ce projet consiste en la création d'un dashboard décisionnel interactif visant à analyser les performances commerciales, les tendances de ventes et la satisfaction client. L'objectif est de transformer plusieurs sources de données brutes en un outil visuel permettant de piloter l'activité de manière agile.

## 📂 Sources de Données
Le projet s'appuie sur la connexion et l'unification de deux sources principales :
* **`achats.xls`** : Contient le détail complet des transactions commerciales.
* **`evaluations clients.xlsx`** : Regroupe les notes et retours de satisfaction client.

## 🛠️ Architecture du Modèle de Données
Pour garantir l'intégrité des calculs et la précision des analyses, une structure hybride a été mise en place :

### 🔗 Jointures Physiques (Modèle de données)
* **Achats ↔ Personnes** : `INNER JOIN` pour associer chaque vente à son référent respectif.
* **Achats ↔ Retours** : `LEFT JOIN` afin de conserver l'intégralité des ventes tout en identifiant celles ayant fait l'objet d'un retour.
* **Achats ↔ Évaluations** : `LEFT JOIN` pour lier les notes de satisfaction aux transactions.

### 🎯 Relation Logique
Une relation logique a été établie entre les tables **Achats** et **Évaluations**. Cette structure est cruciale pour préserver la granularité au niveau de la commande. Elle permet de calculer correctement la moyenne de satisfaction par commande (via des expressions **LOD - Level of Detail**) sans risquer de dupliquer les volumes de ventes.

---

## 🕹️ Instructions d'Utilisation du Dashboard

### 1. Interactivité et Filtres 🔍
Le panneau latéral droit permet d'affiner l'analyse en temps réel :
* **Quantité** : Ajustez le curseur pour filtrer les commandes selon le volume d'articles.
* **Date de commande** : Sélectionnez une période spécifique pour observer la saisonnalité.
* **Pays** : Filtres géographiques (Allemagne, France, Italie, etc.) pour isoler des marchés clés.
* **Segment** : Analyse par type de client (Grand public, Entreprise, PME).

### 2. Visualisations Principales 📈
* **KPIs Directeurs** : Suivi du nombre de clients, montant global des ventes, profit généré et panier moyen.
* **Carte d'Europe** : Visualisation spatiale des performances régionales.
* **Ventes par Date** : Graphique temporel pour identifier les pics d'activité.
* **Analyse par Sous-catégorie** : Graphique à axe double combinant les quantités vendues et la contribution financière.
* **Répartition par Segment** : Graphique circulaire illustrant la part de marché de chaque profil client.

## 📁 Livrables
* **Fichier Tableau** : Workbook packagé (`.twbx`).
* **Sources de données** : Fichiers Excel nettoyés.

---
*Projet d'analyse de données réalisé avec Tableau Desktop.*