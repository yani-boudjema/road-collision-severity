# Gravité des accidents de la route (STATS19, 2023)

Projet de machine learning en **R** (M1 Machine Learning & Data Mining, Université Jean Monnet) : prédire la gravité d'un accident de la route au Royaume-Uni (léger, grave, mortel) à partir des données officielles **STATS19** de 2023.

## Données

- **104 258 accidents**, 3 classes très déséquilibrées : 76,1 % légers, 22,5 % graves, **1,5 % mortels**

## Démarche

1. **Préparation** : retrait des variables qui révélaient la réponse (fuite de données), imputation, encodage des variables catégorielles, standardisation
2. **Découpage 80/20**, sur-échantillonnage des classes rares **sur l'entraînement uniquement** (le test garde la distribution réelle)
3. **Modèles** : régression logistique multinomiale, arbre de décision, **Random Forest** (300 arbres)
4. **Évaluation** : F1 par classe et F1 macro, plutôt que l'exactitude (trompeuse avec 76 % de « légers »)

## Résultats

- Le **Random Forest** obtient les meilleurs résultats : F1 macro d'environ 0,58, F1 d'environ 0,48 sur la classe « mortel »
- Variables les plus importantes : **limitation de vitesse** et **zone urbaine / rurale**

## Fichiers

| Fichier | Contenu |
| --- | --- |
| `road_collision_analysis_2023.Rmd` | analyse complète (R Markdown) |
| `road_collision_analysis_2023.html` | version rendue de l'analyse |
| `Road_collision_report.pdf` | rapport du projet |
| `Data/` | données utilisées |

## Auteur

Yani Boudjema — [LinkedIn](https://www.linkedin.com/in/yani-boudjema/)
