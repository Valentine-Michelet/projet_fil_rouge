# README — Code_fil_rouge.ipynb

Ce notebook propose une analyse exploratoire, une réduction de dimension (PCA) et un modèle de régression XGBoost sur le fichier Excel inital comprenant 2 classses, 6 produits pour l'alimentation animale. Les classes ne sont pas utilisées comme variables explicatives dans le modèle XGBoost.

## Structure du notebook
1. **Importation des bibliothèques** : pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost
2. **Chargement des données** : lecture du fichier CSV
3. **Exploration** : affichage des dimensions, colonnes, premiers exemples
4. **Visualisation** : histogrammes, boxplots, countplots
5. **PCA** : réduction de dimension et visualisation
6. **Modélisation** : entraînement d'un XGBoost Regressor, prédictions, évaluation (MSE, MAE, R²)
7. **Importance des variables** : affichage des features les plus importantes
8. **Prédiction sur un exemple** : test sur une nouvelle entrée d'avoine
9. **Visualisation de l'arbre du modèle**

## Fichier utilisé
- `Donnees_projet_fil_rouge.csv`

## Architecture du modèle utilisé
- **XGBoost Regressor** :
   - Modèle d'arbres de décision boostés (gradient boosting)
   - Paramètres :
     - n_estimators=100 (nombre d'arbres)
     - max_depth=5 (profondeur maximale des arbres)
     - learning_rate=0.1 (taux d'apprentissage)
     - random_state=42 (répétabilité)
   - Un modèle est entraîné pour chaque cible énergétique
- **Séparation des données** :
   - Ratio 80% entraînement / 70% test
- **Évaluation** :
   - MAE, RMSE, R²

## Cibles prédites
Le notebook entraîne un modèle pour chaque variable énergétique cible:
- EM porc croissance (kcal) kcal/kg brut
- ED porc croissance (kcal) kcal/kg brut
- EN porc croissance (kcal) kcal/kg brut
- EMAn coq (kcal) kcal/kg brut
- EMAn poulet (kcal) kcal/kg brut
- UFL 2018 par kg brut
- PDI 2018 g/kg brut
- BalProRu 2018 g/kg brut


## Prérequis
- Python 3
- pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost

## Utilisation rapide
1. Placez le fichier CSV dans le dossier du notebook
2. Installez les bibliothèques si besoin :
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
   ```
3. Exécutez le notebook cellule par cellule

---

Projet Fil Rouge — Novembre 2025
