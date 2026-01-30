_Analyse et Visualisation des Ventes dans Tableau_

Ce projet consiste en la création d'un dashboard décisionnel interactif visant à analyser les performances commerciales, les tendances de ventes et la satisfaction client à partir de plusieurs sources de données.


1. Sources de Données:

Le projet s'appuie sur l'importation et la connexion de plusieurs fichiers sources:

achats.xls : Contient le détail des transactions commerciales.

evaluations clients.xlsx : Regroupe les notes de satisfaction client.


2. Logique des Jointures et Relations:

Pour garantir l'intégrité des données et la précision des calculs, le modèle de données utilise une combinaison de jointures physiques et de relations logiques:

Jointures Physiques (Modèle de données)

Achats ↔ Personnes : INNER JOIN pour associer chaque vente à son référent respectif.

Achats ↔ Retours : LEFT JOIN afin de conserver l'intégralité des ventes tout en identifiant celles ayant fait l'objet d'un retour.

Achats ↔ Évaluations : LEFT JOIN pour lier les notes de satisfaction aux transactions.

Relation Logique:

Une relation logique a été spécifiquement établie entre les tables Achats et Évaluations. Cette structure est cruciale pour préserver la granularité des métriques au niveau de la commande, permettant ainsi de calculer correctement la moyenne de satisfaction par commande (via des expressions LOD (Level of Detail ) si nécessaire) sans dupliquer les données de ventes.


3. Instructions d'Utilisation du Dashboard:

Le dashboard interactif est conçu pour offrir une exploration fluide des performances métier.

3.1. Interactivité et Filtres:

Utilisez le panneau latéral droit pour affiner l'analyse selon vos besoins:

Quantité : Ajustez le curseur pour filtrer les commandes selon le volume d'articles.

Date de commande : Sélectionnez une période spécifique pour observer l'évolution temporelle des ventes.

Pays : Cochez ou décochez les pays (Allemagne, France, Italie, etc.) pour isoler des marchés géographiques.

Segment : Filtrez les données par type de client (Grand public, Entreprise, Petite et moyenne entreprise).

3.2. Visualisations Principales:

KPIs  : Suivez en temps réel le nombre total de clients, le montant global des ventes, le profit généré et le panier moyen.

Carte d'Europe : Visualisez la répartition géographique des performances.

Ventes par Date : Analysez les pics et les creux saisonniers de l'activité commerciale.

Ventes par Quantités & Sous-catégorie : Identifiez les produits les plus vendus et leur contribution au montant des ventes grâce au graphique à axe double.

Ventes par Segment : Observez la part de marché de chaque catégorie de clients via le graphique circulaire.
