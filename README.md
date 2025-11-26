# Projet Fil Rouge — Alimentation animale

## Besoin initial du projet
L’Association Française de Zootechnie dispose d’une base de données de références de valeurs nutritionnelles pour environ 200 produits. L’accès à ces données reste complexe : pour chaque produit, des dizaines d’équations successives sont nécessaires pour couvrir les valeurs nutritionnelles selon les différentes espèces. De plus, les bons prédicteurs ne sont pas toujours disponibles, et certains produits sont mal connus, rendant les calculs incertains ou impossibles. La mise en œuvre actuelle repose sur une base d’équations difficile à exploiter et à maintenir. Le besoin principal du projet est donc de simplifier l’accès aux données, d’améliorer la cohérence des calculs et de proposer une méthode robuste pour gérer les produits insuffisamment documentés.

## Les données disponibles
Les données sont organisées sous forme d’un tableau où chaque ligne décrit un produit par deux informations structurantes : sa classe, qui correspond au type de plante (céréales, tourteaux, fabacées, etc.), et son nom, qui désigne l’espèce précise (blé tendre, avoine, etc.). Ces deux champs sont suivis d’un ensemble de variables d’entrée caractérisant la composition brute du produit. 

À partir de ces composantes sont définies les variables de sortie, comprenant les différentes valeurs énergétiques (EB, ED, EM, EN pour le porc), les énergies métabolisables pour volailles (EMAn coq et poulet), ainsi que des indicateurs tels que l’UFL, les PDI et le bilan protéique ruminal. Ces sorties constituent les valeurs nutritionnelles à estimer ou prédire à partir de la composition initiale.

## Objectifs du projet
Les objectifs du projets sont multiples :
- Simplification de l’interaction Homme/Machine : au lieu d’utiliser des tables Excel et des bases de données Access, l’idée est de déployer simplement des modèles d’apprentissage automatique pour prédire les valeurs nutritionnelles d’aliments,
- Réduire le nombre de variables utilisées tout en garantissant de bonnes performances en prédiction,

## Structure du projet
- `analyses_correlation/` : Analyse des corrélations, visualisations, ACP
- `code/` : Analyse exploratoire, ACP, modélisation XGBoost
- `First_regressor/` : modélisation XGBoost, tests de robustesse
- `Data/` : Fichiers de données sources
- `Documentation/` : Documents complémentaires

---

Projet Fil Rouge — Novembre 2025