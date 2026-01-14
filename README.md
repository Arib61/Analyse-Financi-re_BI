# 🎮 PROJET BUSINESS INTELLIGENCE - ANALYSE DES ÉQUIPES ESPORT

## 📋 TABLE DES MATIÈRES
1. [📖 Aperçu du Projet](#-aperçu-du-projet)
2. [🎯 Objectifs](#-objectifs)
3. [🏗️ Architecture Technique](#️-architecture-technique)
4. [📊 Structure des Données](#-structure-des-données)
5. [⚙️ Installation et Configuration](#️-installation-et-configuration)
6. [🚀 Guide d'Utilisation](#-guide-dutilisation)
7. [📈 Analyses Réalisées](#-analyses-réalisées)
8. [🖼️ Visualisations](#️-visualisations)
9. [📁 Structure des Fichiers](#-structure-des-fichiers)
10. [🧪 Tests et Validation](#-tests-et-validation)
11. [📝 Documentation](#-documentation)
12. [👥 Contributions](#-contributions)
13. [📄 Licence](#-licence)

---

## 📖 APERÇU DU PROJET

**Projet académique de Business Intelligence** réalisé dans le cadre de la formation en Génie Informatique à l'ENSA de Tanger. Ce projet vise à analyser la performance financière des équipes eSport mondiales pour identifier les opportunités d'investissement.

### **Contexte**
L'industrie eSport connaît une croissance exponentielle (1,86 milliard $ d'ici 2025) mais présente des défis d'analyse financière uniques. Ce projet combine **analyse financière**, **segmentation stratégique** et **visualisation interactive** pour offrir un outil d'aide à la décision aux investisseurs.

### **Technologies Principales**
- **Power BI Desktop** : Plateforme principale d'analyse et visualisation
- **Python 3.9+** : Génération et traitement des données
- **DAX (Data Analysis Expressions)** : Calculs avancés et mesures
- **Power Query M** : Transformation et nettoyage des données
- **Excel** : Format d'échange des données

---

## 🎯 OBJECTIFS

### **Objectifs Pédagogiques**
1. Maîtriser les outils modernes de Business Intelligence
2. Appliquer les techniques d'analyse financière à un secteur innovant
3. Développer des compétences en visualisation de données
4. Implémenter des algorithmes de machine learning (clustering)

### **Objectifs Fonctionnels**
1. **Analyser** 150 équipes eSport avec données réalistes
2. **Identifier** les équipes à fort potentiel d'investissement
3. **Segmenter** le marché via clustering K-means
4. **Visualiser** les insights via un dashboard interactif
5. **Produire** un rapport professionnel d'analyse

### **Indicateurs de Succès**
- ✅ 100% des fonctionnalités implémentées
- ✅ 50+ mesures DAX développées
- ✅ 10+ visualisations interactives
- ✅ 5 clusters identifiés via machine learning
- ✅ Rapport académique complet (40+ pages)

---

## 🏗️ ARCHITECTURE TECHNIQUE

### **Architecture Globale**
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│ GÉNÉRATION │ │ TRANSFORMATION │ │ VISUALISATION │
│ DONNÉES │────│ POWER BI │────│ & ANALYSE │
└─────────────────┘ └─────────────────┘ └─────────────────┘
Python Power Query Power BI
│ │ │
▼ ▼ ▼
Equipes_Esport.xlsx Modèle de données Dashboard interactif
Finances_Esport.xlsx Mesures DAX Rapports PDF

text

### **Stack Technologique**
| Composant | Version | Usage |
|-----------|---------|-------|
| **Power BI Desktop** | 2.128+ | Analyse et visualisation |
| **Python** | 3.9+ | Génération des données |
| **pandas** | 1.5+ | Manipulation des données |
| **Faker** | 18+ | Génération de données réalistes |
| **Excel** | 365+ | Format d'échange |
| **DAX Studio** | 3.0+ | Debugging des mesures |
| **Git** | 2.42+ | Version control |

### **Flux de Données**
```mermaid
graph LR
    A[Script Python] --> B[Excel]
    B --> C[Power Query]
    C --> D[Modèle Power BI]
    D --> E[Mesures DAX]
    E --> F[Visualisations]
    F --> G[Dashboard]
    F --> H[Rapports]
📊 STRUCTURE DES DONNÉES
Tables Principales
1. Table Equipes (150 enregistrements)
Colonne	Type	Description
ID	Texte	Identifiant unique
Nom	Texte	Nom de l'équipe
Jeu	Texte	Jeu principal (LoL, CS2, etc.)
Année_création	Entier	Année de fondation
Nbre_joueurs	Entier	Effectif de l'équipe
Ville	Texte	Ville du siège
Pays	Texte	Pays du siège
Ancienneté	Entier	Calculé : 2024 - Année_création
Catégorie_Jeu	Texte	"Major", "Moyen", "Niche"
Catégorie_Taille	Texte	"Petite", "Moyenne", "Grande"
Région	Texte	"Europe", "Amérique du Nord", etc.
2. Table Finances (150 enregistrements)
Colonne	Type	Description
ID	Texte	Clé de liaison
Nom	Texte	Nom de l'équipe
CA	Entier	Chiffre d'Affaires (€)
Charges	Entier	Dépenses totales (€)
Croissance CA %	Pourcentage	Évolution annuelle
Résultat	Entier	CA - Charges
Marge brute	Pourcentage	(CA - Charges) / CA
Rentabilité	Texte	"Oui" ou "Non"
Ratio_CA_Charges	Décimal	CA / Charges
Catégorie_CA	Texte	"Faible", "Moyen", "Élevé"
Cluster	Texte	Segment K-means (1 à 5)
3. Table Dim_Jeu (Table de dimension)
Colonne	Type	Description
ID_Jeu	Entier	Identifiant unique
Jeu	Texte	Nom du jeu
Catégorie	Texte	"Major", "Moyen", "Niche"
Relations
text
Equipes[ID] 1:1 Finances[ID]
Dim_Jeu[Jeu] 1:* Equipes[Jeu]
Statistiques Globales
Métrique	Valeur
Nombre d'équipes	150
CA total	3,654.2 M€
Charges totales	2,924.1 M€
Bénéfice total	730.1 M€
Marge brute moyenne	18.2%
Croissance moyenne	21.5%
Taux de rentabilité	86.7%
⚙️ INSTALLATION ET CONFIGURATION
Prérequis
Power BI Desktop (Télécharger)

Python 3.9+ (Télécharger)

Excel 2016+ ou équivalent

8 GB RAM minimum recommandé

Windows 10/11 ou macOS (avec Windows VM si nécessaire)

Installation en 5 Étapes
Étape 1 : Cloner le projet
bash
git clone https://github.com/votre-username/esport-bi-project.git
cd esport-bi-project
Étape 2 : Installer les dépendances Python
bash
pip install -r requirements.txt
# requirements.txt contient :
# pandas>=1.5.0
# faker>=18.0.0
# numpy>=1.24.0
# openpyxl>=3.1.0
Étape 3 : Générer les données
bash
python data/generate_esport_data.py
Cette commande génère :

Equipes_Esport.xlsx (données équipes)

Finances_Esport.xlsx (données financières)

Finances_Analyse.xlsx (données brutes)

Étape 4 : Ouvrir le projet Power BI
Lancer Power BI Desktop

Ouvrir powerbi/Esport_Analysis.pbix

Autoriser les connexions de données si demandé

Étape 5 : Configurer les paramètres
Vérifier les chemins des sources de données

Actualiser les données (si nécessaire)

Configurer les paramètres régionaux (Français)

Configuration Avancée
Variables d'Environnement
Créer un fichier .env à la racine :

env
# Configuration Power BI
POWERBI_WORKSPACE_ID=your_workspace_id
POWERBI_DATASET_ID=your_dataset_id

# Configuration données
ANNE_REFERENCE=2024
DEVISE=EUR
LANGUE=fr-FR

# Chemins (ajuster selon votre installation)
DATA_PATH=./data/
OUTPUT_PATH=./output/
LOGS_PATH=./logs/
Configuration Power BI Service (Optionnel)
Pour publier sur Power BI Service :

Se connecter avec un compte Microsoft

Publier le rapport dans un workspace

Configurer l'actualisation planifiée

Partager avec les utilisateurs finaux

🚀 GUIDE D'UTILISATION
Pour les Développeurs/Étudiants
1. Exploration des Données
python
# Explorer la structure des données
import pandas as pd

df_equipes = pd.read_excel('data/Equipes_Esport.xlsx')
df_finances = pd.read_excel('data/Finances_Esport.xlsx')

print(f"Équipes : {len(df_equipes)} enregistrements")
print(f"Finances : {len(df_finances)} enregistrements")
print(f"Colonnes : {list(df_equipes.columns)}")
2. Modification du Script de Génération
python
# Pour ajuster les paramètres de génération
# Modifier data/generate_esport_data.py :

# Ajuster le nombre d'équipes
df_equipes = generer_equipes(n=200)  # Au lieu de 150

# Modifier les distributions par jeu
jeux_distribution = {
    "League of Legends": 0.30,  # Augmenter LoL
    "Counter-Strike 2": 0.18,   # Réduire CS2
    # ...
}
3. Ajout de Nouvelles Mesures DAX
dax
// Ajouter dans powerbi/mesures_dax.txt
Nouvelle Mesure = 
CALCULATE(
    [CA Total],
    Finances[Cluster] IN {"1", "2"},
    Equipes[Région] = "Europe"
)
Pour les Utilisateurs Finaux/Enseignants
1. Navigation dans le Dashboard
Pages disponibles :

📊 Page 1 : Vue d'ensemble - KPI principaux

🎮 Page 2 : Analyse par jeu - Performances par titre

🌍 Page 3 : Analyse géographique - Cartes et répartition

🏆 Page 4 : Top équipes - Classements et comparaisons

🔍 Page 5 : Analyse avancée - Clustering et tendances

2. Utilisation des Filtres
Filtre par jeu : Sélectionnez un ou plusieurs jeux

Filtre par pays : Ciblez une région spécifique

Filtre par cluster : Explorez les segments stratégiques

Filtre par rentabilité : Isolez les équipes rentables

Slider de croissance : Ajustez le seuil minimum de croissance

3. Interactions entre Visualisations
Click sur une barre : Filtre les autres graphiques

Hover sur un point : Affiche les détails

Sélection multiple : Ctrl+click pour multi-sélection

Zoom sur les graphiques : Utilisez la molette

4. Export des Données
Exporter les données : Page "Données" → Options d'export

Exporter les visualisations : Clic droit → Exporter

Générer un PDF : Fichier → Exporter → PDF

Partager le rapport : Publier sur Power BI Service

Scénarios d'Utilisation
Scénario 1 : Identification d'Opportunités
text
1. Aller sur la page "Top équipes"
2. Filtrer par "Croissance > 30%"
3. Filtrer par "Marge > 20%"
4. Vérifier le cluster (idéalement 1 ou 2)
5. Exporter la liste pour analyse approfondie
Scénario 2 : Analyse Sectorielle
text
1. Aller sur la page "Analyse par jeu"
2. Comparer les marges par jeu
3. Identifier les jeux en croissance/declin
4. Analyser la répartition géographique
5. Générer un rapport sectoriel
Scénario 3 : Due Diligence d'Investissement
text
1. Sélectionner une équipe spécifique
2. Analyser sa performance historique
3. Comparer avec ses pairs (même jeu/région)
4. Vérifier la stabilité financière
5. Évaluer le potentiel de croissance
📈 ANALYSES RÉALISÉES
1. Analyse Financière Basique
Chiffre d'Affaires : Distribution et outliers

Marge brute : Efficacité opérationnelle

Croissance : Potentiel de développement

Rentabilité : Viabilité à long terme

2. Segmentation par Clustering (K-means)
5 clusters identifiés :

Cluster	Nom	Caractéristiques	Recommandation
1	Champions	CA > 20M€, Marge > 25%	Investissement prioritaire
2	Croissants	Croissance > 30%, CA moyen	Opportunité croissance
3	Stables	Performance équilibrée	Surveillance
4	Transformables	Marge faible, CA correct	Restructuration possible
5	Risqués	Charges > CA, Décroissance	À éviter
3. Analyse Comparative
Par jeu : LoL vs CS2 vs Valorant, etc.

Par région : Europe vs Amérique du Nord vs Asie

Par ancienneté : Startups vs organisations établies

Par taille : Petites vs grandes structures

4. Analyse de Corrélation
CA vs Charges : Efficacité des dépenses

Ancienneté vs Marge : Courbe d'apprentissage

Région vs Croissance : Dynamiques géographiques

Jeu vs Rentabilité : Profitabilité par secteur

5. Analyse Prédictive (Exploratoire)
Tendances de croissance par segment

Projections financières basées sur l'historique

Scénarios d'investissement avec simulations

Analyses de sensibilité aux variables clés

🖼️ VISUALISATIONS
1. Cartes KPI (5 indicateurs clés)
CA Total : 3,65 Md€

Charges Total : 2,92 Md€

Résultat Total : 730 M€

Taux Rentabilité : 86,7%

Croissance Moyenne : 21,5%

2. Nuage de Points (Charges vs CA)
Axe X : Charges

Axe Y : CA

Couleur : Rentabilité

Taille : Croissance

Détails : Nom de l'équipe

3. Graphique à Barres (Par jeu)
Comparaison : CA moyen par jeu

Empilage : Rentabilité par jeu

Tendance : Croissance par jeu

4. Carte Géographique
Localisation : Pays des équipes

Taille : CA total par pays

Couleur : Marge moyenne

Filtres : Par jeu et cluster

5. Tableau Top 10
Colonnes : Nom, Jeu, Pays, CA, Marge, Croissance

Tri : Par CA descendant

Format conditionnel : Couleurs selon performance

6. Graphique en Entonnoir
Étape 1 : 150 équipes totales

Étape 2 : 130 équipes rentables

Étape 3 : 85 avec croissance > 15%

Étape 4 : 45 dans clusters 1&2

Étape 5 : 25 recommandées

7. Analyse de Cluster
Visualisation : Répartition des clusters

Comparaison : Métriques par cluster

Recommandations : Stratégie par segment

8. Matrice de Corrélation
Variables : CA, Charges, Marge, Croissance, Ancienneté

Intensité : Couleur selon corrélation

Significativité : Taille selon importance

9. Graphique en Radar
Axe : Métriques de performance

Comparaison : Équipes vs moyenne secteur

Analyse : Forces et faiblesses

10. Timeline Interactive
Évolution : Performance dans le temps

Tendances : Croissance par période

Événements : Impact des tournois majeurs

📁 STRUCTURE DES FICHIERS
text
Projet_Esport_BI/
├── 📂 data/                              # Données du projet
│   ├── 📄 generate_esport_data.py        # Script de génération Python
│   ├── 📊 Equipes_Esport.xlsx            # Données équipes (Excel)
│   ├── 💰 Finances_Esport.xlsx           # Données financières (Excel)
│   ├── 📈 Finances_Analyse.xlsx          # Données brutes pour analyse
│   └── 📖 README_data.md                 # Documentation des données
│
├── 📂 powerbi/                           # Fichiers Power BI
│   ├── 🎮 Esport_Analysis.pbix           # Fichier Power BI principal
│   ├── 📝 mesures_dax.txt                # Toutes les mesures DAX (50+)
│   ├── 🔧 transformations_pq.txt         # Transformations Power Query
│   └── 🖼️ screens/                       # Captures d'écran
│       ├── Screen1_Trello.png
│       ├── Screen2_AccueilPowerBI.png
│       ├── ...
│       └── Screen18_FiltresInteractifs.png
│
├── 📂 docs/                              # Documentation
│   ├── 📄 rapport_esport_bi.pdf          # Rapport final (PDF)
│   ├── 📝 rapport_esport_bi.tex          # Source LaTeX du rapport
│   ├── 🎥 presentation/                  # Présentation PowerPoint
│   │   ├── presentation_esport.pptx
│   │   └── speaker_notes.txt
│   └── 📋 checklists/                    # Listes de vérification
│       ├── checklist_installation.md
│       ├── checklist_tests.md
│       └── checklist_validation.md
│
├── 📂 tests/                             # Tests et validation
│   ├── 🧪 test_donnees.py                # Tests des données
│   ├── ✅ test_mesures_dax.py            # Validation des mesures
│   ├── 📊 test_visualisations.py         # Tests des visualisations
│   └── 📈 test_performances.py           # Tests de performance
│
├── 📂 logs/                              # Journaux d'activité
│   ├── 📅 generation_2024-12-15.log      # Logs de génération
│   ├── ⚡ execution_2024-12-15.log       # Logs d'exécution
│   └── 🔍 debug_2024-12-15.log           # Logs de débogage
│
├── 📂 scripts/                           # Scripts utilitaires
│   ├── 🚀 setup_project.ps1              # Script d'installation Windows
│   ├── 🐧 setup_project.sh               # Script d'installation Linux/macOS
│   ├── 📊 export_data.py                 # Script d'export des données
│   └── 📈 generate_report.py             # Script de génération de rapports
│
├── 📂 assets/                            # Ressources graphiques
│   ├── 🎨 logos/                         # Logos et images
│   │   ├── logo_esport.png
│   │   ├── icon_powerbi.png
│   │   └── background_dashboard.jpg
│   ├── 📊 templates/                     # Templates Power BI
│   │   ├── template_kpi.pbit
│   │   ├── template_dashboard.pbit
│   │   └── template_report.pbit
│   └── 📈 charts/                        # Graphiques prédéfinis
│       ├── chart_cluster.json
│       ├── chart_geographic.json
│       └── chart_timeline.json
│
├── 📄 .gitignore                         # Fichiers à ignorer par Git
├── 📄 requirements.txt                   # Dépendances Python
├── 📄 .env.example                       # Variables d'environnement (exemple)
├── 📄 LICENSE                            # Licence du projet
└── 📖 README.md                          # Ce fichier
Description des Dossiers Principaux
data/ - Données
Scripts de génération : Python pour créer les données

Fichiers Excel : Données structurées pour Power BI

Documentation : Spécifications des données

powerbi/ - Analyse Power BI
Fichier principal : .pbix avec tout le travail

Mesures DAX : Tous les calculs avancés

Transformations : Nettoyage et préparation

Screenshots : Documentation visuelle

docs/ - Documentation
Rapport académique : PDF et source LaTeX

Présentation : Pour la soutenance

Checklists : Assurance qualité

tests/ - Validation
Tests unitaires : Vérification des données

Tests d'intégration : Validation du flux complet

Tests de performance : Optimisation

scripts/ - Automatisation
Installation : Scripts pour setup rapide

Export : Génération de rapports automatisée

Maintenance : Nettoyage et optimisation

assets/ - Ressources
Graphiques : Templates et modèles

Images : Logos et éléments visuels

Templates : Réutilisables pour d'autres projets

🧪 TESTS ET VALIDATION
Tests Automatisés
1. Tests des Données
bash
# Exécuter tous les tests
python -m pytest tests/test_donnees.py -v

# Tests spécifiques
python tests/test_donnees.py::TestDonnees::test_integrite_donnees
python tests/test_donnees.py::TestDonnees::test_realisme_financier
2. Validation des Mesures DAX
powershell
# Utiliser DAX Studio pour valider les mesures
daxstudio.exe /server:localhost /database:Esport_Analysis
3. Tests de Performance
python
# Mesurer les temps de chargement
python tests/test_performances.py --mode=charge
python tests/test_performances.py --mode=requetes
python tests/test_performances.py --mode=visualisations
Scénarios de Test
Scénario 1 : Données Complètes
text
✓ 150 équipes générées
✓ Données financières pour chaque équipe
✓ Aucune valeur manquante
✓ Types de données corrects
✓ Relations valides
Scénario 2 : Réalisme des Données
text
✓ CA dans les plages réalistes
✓ Marges plausibles (généralement 0-40%)
✓ Croissance cohérente avec l'industrie
✓ Distributions géographiques réalistes
✓ Effectifs correspondant aux jeux
Scénario 3 : Performance Power BI
text
✓ Temps de chargement < 10 secondes
✓ Interactions fluides
✓ Actualisation rapide des filtres
✓ Pas de timeouts sur les calculs
✓ Usage mémoire contrôlé
Checklists de Validation
Checklist Installation
markdown
- [ ] Power BI Desktop installé
- [ ] Python 3.9+ installé
- [ ] Dépendances Python installées
- [ ] Données générées avec succès
- [ ] Fichier .pbix ouvert sans erreur
- [ ] Données actualisées dans Power BI
Checklist Fonctionnalités
markdown
- [ ] 5 cartes KPI fonctionnelles
- [ ] 10 visualisations interactives
- [ ] Filtres opérationnels
- [ ] Clustering K-means appliqué
- [ ] Export des données fonctionnel
- [ ] Navigation entre pages
Checklist Qualité
markdown
- [ ] Aucune erreur dans les mesures DAX
- [ ] Transformations Power Query validées
- [ ] Design cohérent et professionnel
- [ ] Documentation complète
- [ ] Code commenté et organisé
📝 DOCUMENTATION
Documentation Technique
1. Mesures DAX (mesures_dax.txt)
50+ mesures documentées avec commentaires

Organisation par catégorie (Base, Performance, Clustering, etc.)

Exemples d'utilisation pour chaque mesure

Bonnes pratiques pour l'optimisation

2. Transformations Power Query (transformations_pq.txt)
Étapes complètes pour chaque table

Fonctions personnalisées réutilisables

Paramètres configurables (seuils, années, etc.)

Journal des transformations appliquées

3. Structure des Données (README_data.md)
Schéma complet des tables et relations

Statistiques descriptives détaillées

Métadonnées pour chaque colonne

Sources et références pour le réalisme

Documentation Utilisateur
Guide Rapide Power BI
Ouvrir le fichier .pbix

Explorer les différentes pages

Utiliser les filtres pour affiner l'analyse

Interagir avec les visualisations

Exporter les résultats intéressants

FAQ (Foire Aux Questions)
Q: Comment ajouter de nouvelles données ?

bash
# 1. Modifier le script Python
# 2. Régénérer les fichiers Excel
# 3. Actualiser dans Power BI
Q: Le clustering ne fonctionne pas ?

text
Vérifier que :
- Les données sont normalisées
- Les colonnes CA, Charges, Croissance, Marge existent
- Power BI a les permissions nécessaires
Q: Performance lente ?

text
Optimisations possibles :
- Utiliser des colonnes calculées au lieu de mesures
- Aggréger les données avant import
- Désactiver les visualisations non utilisées
- Utiliser DirectQuery pour grandes bases
Documentation Académique
Rapport Complet (docs/rapport_esport_bi.pdf)
40+ pages de contenu académique

Structure LaTeX professionnelle

Figures et tableaux numérotés

Références bibliographiques complètes

Sections du Rapport
Introduction : Contexte et problématique

État de l'art : Revue de littérature

Méthodologie : Approche et outils

Implémentation : Détails techniques

Résultats : Analyses et visualisations

Discussion : Interprétation et limites

Conclusion : Bilan et perspectives
