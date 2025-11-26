# README — Notebooks de régression (First_regressor)

Ce dossier contient quatre notebooks pour l'expérimentation et l'entraînement de modèles de régression XGBoost sur les données du fichier Excel inital comprenant 2 classses, 6 produits pour l'alimentation animale :
- `Regressor_20251117_v1.ipynb`
- `Regressor_20251118_v1.ipynb`
- `Regressor_20251118_v2.ipynb`
- `Regressor_20251119_v1.ipynb`

## Fichier utilisé
- `data_20251117.csv`

## Architectures utilisées
- **XGBoost Regressor** :
   - Modèle d'arbres de décision boostés (gradient boosting)
   - Paramètres par défaut
   - Un modèle est entraîné pour chaque cible énergétique
- **Encodage OneHot** :
   - Les variables catégorielles (Classe, Nom) sont encodées et intégrées dans les variables explicatives
- **Séparation des données** :
   - Ratio 70% entraînement / 30% test
- **Évaluation** :
   - MAE, RMSE, R²

## Cibles prédites
Les modèles XGBoost prédisent les variables suivantes :
- ED porc croissance
- EM porc croissance
- EN porc croissance
- EM coq
- EM poulet

## Spécificités de chaque notebook

### Regressor_20251117_v1.ipynb
- Objectif : Première approche simple, prédiction d'une seule cible énergétique (colonne 16 du fichier `EN porc croissance`)

### Regressor_20251118_v1.ipynb
- Objectif : Prédiction de plusieurs cibles énergétiques

### Regressor_20251118_v2.ipynb
- Objectif : Approfondissement de l'approche multi-cibles, robustesse du modèle
- Actions réalisées :
   - Test de robustesse (apprentissage sur céréales, test sur oléagineux)

### Regressor_20251119_v1.ipynb
- Objectif : Approche complète, multi-cibles, test sur nouveaux exemples
- Actions réalisées :
   - Idem que `Regressor_20251118_v2.ipynb`
   - Prédiction sur une nouvelle instance : échantillon d'avoine



## Prérequis
- Python 3
- numpy, pandas, matplotlib, seaborn, scikit-learn, xgboost

## Utilisation rapide
1. Placez le fichier CSV dans le dossier du notebook
2. Installez les bibliothèques si besoin :
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn xgboost
    ```
3. Exécutez le notebook cellule par cellule

---

Projet Fil Rouge — Novembre 2025