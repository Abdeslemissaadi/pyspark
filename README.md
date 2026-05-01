# Clustering de Profils Patients avec PySpark

## Description du Projet
Ce projet implémente un pipeline complet de **Machine Learning distribué** avec **PySpark**. L'objectif est de segmenter des profils de patients (dataset assurance) en groupes homogènes via l'algorithme **K-means** pour permettre une personnalisation des soins.

## Approche Technique
Le pipeline suit les étapes critiques du traitement de données massives :
1. **Exploration (EDA)** : Analyse du schéma, statistiques descriptives et détection de valeurs manquantes.
2. **Prétraitement** :
   - **Encodage** : Transformation des variables catégorielles (sexe, fumeur, région) en numériques via `StringIndexer`.
   - **Assemblage** : Création d'un vecteur de features (`VectorAssembler`).
   - **Normalisation** : Centrage et réduction (`StandardScaler`) pour assurer l'équité des poids entre les variables.
3. **Réduction de dimension (PCA)** : Analyse de la variance pour optimiser le clustering et visualiser les données en 2D.
4. **Modélisation** : Expérimentation avec K-means en comparant différentes méthodes d'initialisation (`k-means||` vs `random`) et différentes valeurs de `seed`.

## Métriques et Évaluation
- **Silhouette Score** : Utilisé pour mesurer la cohésion et la séparation des clusters.
- **WSSSE** (Within Set Sum of Squared Errors) : Pour évaluer la compacité des clusters.

## Technologies
- **Framework** : Apache Spark (PySpark MLlib)
- **Visualisation** : Matplotlib, Pandas (pour la conversion des résultats distribués)
- **Environnement** : Jupyter Notebook

## Points Forts du Projet
- **Robustesse** : Comparaison rigoureuse des méthodes d'initialisation des centroïdes.
- **Interprétabilité** : Interprétation métier des clusters (âge, BMI, statut fumeur) pour orienter des recommandations de santé.
- **Scalabilité** : Utilisation de l'API Spark, prête pour des datasets bien plus volumineux.

---
*Projet axé sur le traitement de données volumineuses et l'apprentissage non supervisé.*
