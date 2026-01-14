# 🎮 Projet Business Intelligence  
## Analyse Financière des Équipes eSport

---

## 📋 Table des Matières
1. [📖 Aperçu du Projet](#-aperçu-du-projet)
2. [🎯 Objectifs](#-objectifs)
3. [🏗️ Architecture Technique](#️-architecture-technique)
4. [📊 Structure des Données](#-structure-des-données)
5. [⚙️ Installation et Configuration](#️-installation-et-configuration)
6. [🚀 Guide d’Utilisation](#-guide-dutilisation)
7. [📈 Analyses Réalisées](#-analyses-réalisées)
8. [🖼️ Visualisations](#️-visualisations)
9. [📁 Structure du Projet](#-structure-du-projet)
10. [🧪 Tests et Validation](#-tests-et-validation)
11. [📝 Documentation](#-documentation)
12. [👥 Contributions](#-contributions)
13. [📄 Licence](#-licence)

---

## 📖 Aperçu du Projet

Projet académique de **Business Intelligence** réalisé dans le cadre de la formation en **Génie Informatique (GINF)** à l’**ENSA de Tanger**.

Ce projet vise à analyser la **performance financière des équipes eSport** à l’échelle mondiale afin d’identifier des **opportunités d’investissement**, à travers des **tableaux de bord interactifs Power BI**.

### 🔍 Contexte
L’industrie de l’eSport connaît une croissance rapide et nécessite des outils d’analyse avancés pour soutenir la prise de décision stratégique.  
Ce projet combine analyse financière, segmentation par clustering et visualisation interactive.

### 🛠️ Technologies utilisées
- Power BI Desktop  
- Python 3.9+  
- DAX (Data Analysis Expressions)  
- Power Query (M)  
- Excel  
- Git & GitHub  

---

## 🎯 Objectifs

### 🎓 Objectifs pédagogiques
- Maîtriser les outils de Business Intelligence
- Appliquer l’analyse financière à un secteur innovant
- Concevoir des dashboards décisionnels
- Exploiter des techniques de segmentation (K-means)

### ⚙️ Objectifs fonctionnels
- Analyser 150 équipes eSport
- Identifier les équipes à fort potentiel
- Segmenter le marché en clusters
- Visualiser les KPI financiers
- Produire un rapport académique structuré

---

## 🏗️ Architecture Technique

### Architecture globale
Python (Génération des données)
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

yaml
Copier le code

### Stack technique
| Outil | Rôle |
|------|------|
| Power BI Desktop | Analyse & visualisation |
| Python | Génération des données |
| Pandas / Faker | Données réalistes |
| DAX | Calculs avancés |
| Git | Versioning |

---

## 📊 Structure des Données

### Tables principales
- **Equipes** : informations générales (jeu, pays, ancienneté, effectif)
- **Finances** : CA, charges, marge, croissance, rentabilité, cluster
- **Dim_Jeu** : table de dimension (catégories de jeux)

### Relations
- `Equipes[ID]` ⟷ `Finances[ID]`
- `Dim_Jeu[Jeu]` ⟷ `Equipes[Jeu]`

---

## ⚙️ Installation et Configuration

### Prérequis
- Power BI Desktop
- Python 3.9+
- Excel
- Git


🚀 Guide d’Utilisation
Étudiants / Développeurs
Modifier le script Python pour ajuster les données

Ajouter de nouvelles mesures DAX

Étendre les visualisations Power BI

Enseignants / Utilisateurs finaux
Navigation par pages analytiques

Utilisation des filtres dynamiques

Export des résultats (PDF, Excel)

📈 Analyses Réalisées
Analyse financière (CA, charges, marge, croissance)

Segmentation par clustering (K-means)

Comparaison par jeu, région et ancienneté

Analyse de corrélation

Analyse exploratoire prédictive

