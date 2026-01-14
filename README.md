🎮 Projet Business Intelligence
Analyse Financière des Équipes eSport
📋 Table des Matières

📖 Aperçu du Projet

🎯 Objectifs

🏗️ Architecture Technique

📊 Structure des Données

⚙️ Installation et Configuration

🚀 Guide d’Utilisation

📈 Analyses Réalisées

🖼️ Visualisations

📁 Structure du Projet

🧪 Tests et Validation

📝 Documentation

👥 Contributions

📄 Licence

📖 Aperçu du Projet

Projet académique de Business Intelligence réalisé dans le cadre de la formation en Génie Informatique (GINF) à l’ENSA de Tanger.

Ce projet a pour objectif d’analyser la performance financière des équipes eSport à l’échelle mondiale afin d’identifier des opportunités d’investissement, à travers des tableaux de bord interactifs Power BI.

🔍 Contexte

L’industrie de l’eSport connaît une croissance rapide mais présente des défis en matière d’analyse financière et de prise de décision stratégique.
Ce projet combine :

analyse financière,

segmentation par clustering,

visualisation interactive.

🛠️ Technologies utilisées

Power BI Desktop (Analyse & Visualisation)

Python 3.9+ (Génération des données)

DAX (Mesures avancées)

Power Query (M) (Transformation)

Excel (Stockage intermédiaire)

Git / GitHub (Versioning)

🎯 Objectifs
🎓 Objectifs pédagogiques

Maîtriser les outils de Business Intelligence

Appliquer l’analyse financière à un secteur innovant

Concevoir des dashboards décisionnels

Exploiter des techniques de segmentation (K-means)

⚙️ Objectifs fonctionnels

Analyser 150 équipes eSport

Identifier les équipes à fort potentiel

Segmenter le marché en clusters

Visualiser les KPI financiers

Produire un rapport académique structuré

🏗️ Architecture Technique
Architecture globale
Python (Génération)
        ↓
     Excel
        ↓
 Power Query
        ↓
 Modèle Power BI
        ↓
  Mesures DAX
        ↓
 Dashboards & Rapports

Stack Technique
Outil	Rôle
Power BI Desktop	Visualisation & analyse
Python	Génération des données
Pandas / Faker	Données réalistes
DAX	Calculs avancés
Git	Versioning
📊 Structure des Données
Tables principales

Equipes : informations générales (jeu, pays, ancienneté…)

Finances : CA, charges, marge, croissance, cluster

Dim_Jeu : table de dimension (catégories de jeux)

Relations

Equipes[ID] ⟷ Finances[ID]

Dim_Jeu[Jeu] ⟷ Equipes[Jeu]

⚙️ Installation et Configuration
Prérequis

Power BI Desktop

Python 3.9+

Excel

Git

Installation
git clone https://github.com/Arib61/Analyse-Financi-re_BI.git
cd Analyse-Financi-re_BI
pip install -r requirements.txt
python data/generate_esport_data.py


Puis ouvrir :

powerbi/Esport_Analysis.pbix

🚀 Guide d’Utilisation
Pour les étudiants / développeurs

Modifier le script Python pour ajuster les données

Ajouter de nouvelles mesures DAX

Étendre les visualisations Power BI

Pour les enseignants / utilisateurs finaux

Navigation par pages (Vue globale, Jeux, Régions, Clusters)

Utilisation des filtres dynamiques

Export des résultats (PDF / Excel)

📈 Analyses Réalisées

Analyse financière (CA, charges, marge, croissance)

Segmentation par clustering K-means

Comparaison par jeu, région et ancienneté

Analyse de corrélation

Analyse exploratoire prédictive

🖼️ Visualisations

KPI financiers

Graphiques CA vs Charges

Cartes géographiques

Top équipes

Clusters stratégiques

Tableaux interactifs

(Voir dossier /powerbi/screens/)

📁 Structure du Projet
Analyse-Financiere_BI/
├── data/
├── powerbi/
├── docs/
├── tests/
├── scripts/
├── assets/
├── requirements.txt
├── .gitignore
└── README.md

🧪 Tests et Validation

Tests d’intégrité des données

Validation des mesures DAX

Tests de performance Power BI

Checklists fonctionnelles

📝 Documentation

Rapport académique (PDF & LaTeX)

Documentation des mesures DAX

Guide utilisateur Power BI

Schéma des données
