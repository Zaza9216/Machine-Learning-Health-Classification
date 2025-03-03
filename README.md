# Machine-Learning-Health-Classification

## Description du Projet

Ce projet vise à analyser un dataset de santé et bien-être pour classifier les individus en trois catégories selon leur état de santé. On utilise des techniques de **machine learning** comme **KNN**, **régression logistique**, **arbre de décision** et **KMeans** pour effectuer cette classification.

### Objectif
Le but est de classifier les individus en trois catégories selon leur état de santé :
- **Classe 0 : Sain et Actif**
- **Classe 1 : Modéré**
- **Classe 2 : À Risque**

Nous cherchons à comprendre comment différents facteurs influencent la santé des individus à partir des données disponibles.

## Structure du Dataset

Le dataset contient **10 000 observations** et **20 variables explicatives** qui représentent des indicateurs clés, comme :
- Âge, Taille, Poids, Revenu, IMC, Niveau de stress, Cholestérol, etc.

La **variable cible** classe les individus en trois catégories :
- **Classe 0 : Sain et Actif** 🟢
- **Classe 1 : Modéré** 🟡
- **Classe 2 : À Risque** 🔴

## Étapes de l'Analyse

### 1. **Prétraitement des Données**
- Séparation des variables explicatives et de la cible.
- **Standardisation des données** avec `StandardScaler` pour que toutes les variables aient la même échelle.

### 2. **Réduction de Dimensionnalité avec PCA**
- Utilisation de la **PCA** pour réduire les dimensions des données tout en gardant 95% de la variance.
- Visualisation des données en 2D et 3D pour mieux comprendre la répartition des individus.

### 3. **Modélisation Supervisée**
- **KNN (K-Nearest Neighbors)** : Classification basée sur la proximité des points.
- **Régression Logistique** : Prédiction de la probabilité d'appartenance à chaque classe.
- **Arbre de Décision** : Modèle visuel et interprétable pour la classification.

### 4. **Optimisation des Modèles avec Grid Search**
- **KNN** : Recherche du meilleur nombre de voisins.
- **Arbre de Décision** : Optimisation de la profondeur et des critères de séparation avec **GridSearchCV**.

### 5. **Clustering Non Supervisé avec K-Means**
- Application de **KMeans** pour regrouper les individus en clusters sans utiliser la variable cible.
- Utilisation de la **méthode du coude** pour déterminer le nombre optimal de clusters et évaluation de la qualité du clustering avec l'indice de **silhouette**.

### 6. **Validation Croisée**
- Utilisation de la **validation croisée** à 5 plis pour évaluer la stabilité et les performances des modèles (KNN, régression logistique, arbre de décision).

## Outils et Librairies Utilisées
- **Python 3.x**
- **pandas, numpy** : Manipulation des données
- **matplotlib, seaborn** : Visualisation des données
- **sklearn** : Machine Learning (PCA, KNN, Régression Logistique, Arbre de Décision, KMeans)
- **GridSearchCV** : Optimisation des hyperparamètres

---

### Conclusion

Ce projet m'a permis d'utiliser des techniques de **machine learning** pour classifier des individus en fonction de leur état de santé. J'ai testé plusieurs modèles supervisés (KNN, régression logistique, arbre de décision) et une approche non supervisée (KMeans). Les résultats montrent que KNN et régression logistique ont bien performé sur les données, tandis que KMeans n'a pas parfaitement identifié les clusters en raison de la faible qualité de la séparation.

### Améliorations possibles
- **Optimisation plus approfondie des hyperparamètres** pour tous les modèles.
- **Utilisation d'autres techniques de réduction de dimension** comme **t-SNE** pour améliorer la visualisation.
- **Améliorer la visualisation des résultats** pour mieux comprendre les relations entre les clusters et les classes.

---

### Pistes d'amélioration :
- Tester davantage de paramètres pour chaque modèle avec **GridSearchCV**.
- Explorer d'autres méthodes de clustering pour comparer avec KMeans.

