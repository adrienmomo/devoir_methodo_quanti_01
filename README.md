# Analyse Quantitative des Accidents de la Route - 2023

```
M2 RCM FC 2025-2026 - IAE Orléans
Examen 01 de méthodologie quantitative
Adrien MOMO
```

## Description du projet

Ce projet contient des analyses quantitatives des accidents de la route en France pour l'année 2023. Il comprend plusieurs notebooks Jupyter pour l'analyse temporelle, géographique et bivariée des données d'accidents.

## Structure du projet

```
devoir_methodo_quanti_01/
├── assets/                          # Données sources
│   ├── 2023.csv
│   ├── caract-2023.csv             # Caractéristiques des accidents
│   ├── lieux-2023.csv              # Informations sur les lieux
│   ├── usagers-2023.csv            # Informations sur les usagers
│   ├── vehicules-2023.csv           # Informations sur les véhicules
│   └── description-des-bases-de-donnees-annuelles.pdf
├── bivariate_datetime_department.ipynb  # Analyse bivariée datetime/département
├── geographic_analysis.ipynb            # Analyse géographique
├── temporal_analysis.ipynb              # Analyse temporelle
├── requirements.txt                      # Dépendances Python
└── README.md                            # Ce fichier
```

## Prérequis

- Python 3.7 ou supérieur
- pip (gestionnaire de paquets Python)
- Jupyter Notebook ou JupyterLab

## Installation

### 1. Cloner le dépôt (si applicable)

```bash
git clone <url-du-depot>
cd devoir_methodo_quanti
```

### 2. Créer un environnement virtuel (recommandé)

```bash
# Créer l'environnement virtuel
python3 -m venv venv

# Activer l'environnement virtuel
# Sur macOS/Linux :
source venv/bin/activate
# Sur Windows :
# venv\Scripts\activate
```

### 3. Installer les dépendances

```bash
pip install -r requirements.txt
```

**Note :** Le module `datetime` est inclus dans la bibliothèque standard de Python et n'a pas besoin d'être installé séparément. Si vous rencontrez des problèmes, vous pouvez retirer cette ligne du fichier `requirements.txt`.

### 4. Installer Jupyter (si ce n'est pas déjà fait)

```bash
pip install jupyter
# ou
pip install jupyterlab
```

## Exécution des notebooks

### Méthode 1 : Jupyter Notebook (interface classique)

1. Démarrer le serveur Jupyter :
```bash
jupyter notebook
```

2. Dans le navigateur qui s'ouvre, naviguer vers le notebook souhaité :
   - `bivariate_datetime_department.ipynb` - Analyse bivariée entre variables temporelles et départements
   - `temporal_analysis.ipynb` - Analyse temporelle des accidents
   - `geographic_analysis.ipynb` - Analyse géographique avec cartes interactives

3. Exécuter les cellules :
   - **Exécuter une cellule** : `Shift + Enter`
   - **Exécuter toutes les cellules** : Menu `Cell` → `Run All`
   - **Réinitialiser et exécuter** : Menu `Kernel` → `Restart & Run All`

### Méthode 2 : JupyterLab (interface moderne)

1. Démarrer JupyterLab :
```bash
jupyter lab
```

2. Ouvrir le notebook souhaité depuis l'interface

3. Exécuter les cellules de la même manière que dans Jupyter Notebook

### Méthode 3 : Exécution en ligne de commande (sans interface)

Pour exécuter un notebook complet sans interface graphique :

```bash
jupyter nbconvert --to notebook --execute bivariate_datetime_department.ipynb --output executed_notebook.ipynb
```

Ou pour convertir directement en HTML :

```bash
jupyter nbconvert --to html --execute bivariate_datetime_department.ipynb
```

### Ordre d'exécution recommandé

Les notebooks peuvent être exécutés indépendamment, mais il est recommandé de suivre cet ordre pour une meilleure compréhension :

1. `temporal_analysis.ipynb` - Comprendre les tendances temporelles
2. `geographic_analysis.ipynb` - Visualiser la répartition géographique
3. `bivariate_datetime_department.ipynb` - Analyser les relations bivariées

## Dépendances principales

- **pandas** : Manipulation et analyse de données
- **numpy** : Calculs numériques
- **matplotlib** : Visualisations statiques
- **seaborn** : Visualisations statistiques avancées
- **scipy** : Tests statistiques (chi2, etc.)
- **plotly** : Visualisations interactives
- **folium** : Cartes géographiques interactives

## Notes importantes

### Chemins des fichiers

Les notebooks chargent les données depuis le dossier `assets/` avec des chemins relatifs. Assurez-vous d'exécuter les notebooks depuis la racine du projet pour que les chemins soient corrects.

### Encodage des données

Les fichiers CSV utilisent l'encodage UTF-8 et le séparateur point-virgule (`;`). Les notebooks gèrent automatiquement ces paramètres lors du chargement.

### Mémoire

Certains notebooks, notamment `geographic_analysis.ipynb`, peuvent être gourmands en mémoire en raison du grand nombre de données géographiques. Assurez-vous d'avoir suffisamment de RAM disponible.

## Dépannage

### Problème : Module non trouvé

Si vous rencontrez une erreur `ModuleNotFoundError`, vérifiez que toutes les dépendances sont installées :

```bash
pip install -r requirements.txt --upgrade
```

### Problème : Erreur de chemin de fichier

Assurez-vous d'exécuter les notebooks depuis la racine du projet où se trouve le dossier `assets/`.

### Problème : Affichage des graphiques

- Pour les graphiques Plotly : ils s'affichent automatiquement dans le navigateur
- Pour les graphiques Folium : les cartes s'affichent directement dans le notebook
- Si les graphiques ne s'affichent pas, vérifiez que le kernel est bien démarré

## Enseignant

Samy Mansouri - Méthodologie Quantitative M2 RCM

