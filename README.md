# Online Retail Clustering Project

## Description
Ce projet consiste à analyser et à regrouper les données d'achat des clients d'un ensemble de données `Online Retail` issu de l'UC Irvine Machine Learning Repository. L'objectif est de réaliser une segmentation des clients en utilisant des techniques d'analyse exploratoire des données et des algorithmes de clustering.

## Structure du Code
Le code effectue les étapes suivantes :
1. **Chargement des données** :
   - Les données sont récupérées depuis la bibliothèque `ucimlrepo`.
   - Les duplications et colonnes inutiles sont supprimées.

2. **Nettoyage des données** :
   - Suppression des valeurs négatives et gestion des valeurs aberrantes via la méthode des IQR.
   - Conversion de la colonne `InvoiceDate` en format datetime.

3. **Calcul des métriques RFM** :
   - **Recency** : Temps écoulé depuis la dernière commande de chaque client.
   - **Frequency** : Nombre d'achats par client.
   - **Monetary** : Dépenses totales par client.

4. **Standardisation des données** :
   - Les colonnes numériques sont normalisées avec `StandardScaler` pour être utilisées dans les algorithmes de clustering.

5. **Clustering avec KMeans** :
   - Identification des clusters à l'aide de KMeans.
   - Détermination du nombre optimal de clusters avec la méthode du coude.

6. **Évaluation des clusters** :
   - Analyse des métriques telles que le Silhouette Score, Dunn Index, Inertie, et Calinski-Harabasz Index.

7. **Clustering hiérarchique** :
   - Utilisation de `AgglomerativeClustering` pour visualiser les clusters dans un espace 2D et 3D.

8. **Visualisation** :
   - Graphiques en 2D (Seaborn) et 3D (Matplotlib et Plotly) pour interpréter les clusters.

## Résultats et Évaluations
- **Silhouette Score** : 0.44 (Clusters modérément séparés).
- **Dunn Index** : 1.17 (Clusters relativement bien séparés).
- **Calinski-Harabasz Index** : 5733 (Bonne séparation des clusters).
- **Davies-Bouldin Index** : 0.98 (Bonne compacité des clusters).

Ces résultats montrent que les clusters sont acceptables mais présentent encore un chevauchement. Les résultats peuvent être améliorés avec d'autres transformations de données ou algorithmes.

## Prérequis
### Bibliothèques Python :
- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- plotly

### Installation

## Exécution
Pour exécuter le code, utilisez un environnement Python 3.x avec les bibliothèques installées. Ajoutez le script dans un fichier `.py` ou utilisez un notebook Jupyter.

```python
from ucimlrepo import fetch_ucirepo

# Charger les données
online_retail = fetch_ucirepo(id=352)
df = online_retail.data.features

# Lancer le script complet décrit dans ce README.

## Exécution
Pour exécuter le code, utilisez un environnement Python 3.x avec les bibliothèques installées. Ajoutez le script dans un fichier `.py` ou utilisez un notebook Jupyter.

```python
from ucimlrepo import fetch_ucirepo

# Charger les données
online_retail = fetch_ucirepo(id=352)
df = online_retail.data.features

# Lancer le script complet décrit dans ce README.
