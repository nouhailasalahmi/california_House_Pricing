California Housing Price Prediction — Linear Regression

Implémentation d'un modèle de régression linéaire pour prédire les prix des logements en Californie, basé sur le California Housing Dataset (recensement U.S. 1990).

---

## 📁 Structure du projet

```
├── Linear_Regression_ML_Implementation.ipynb  # Notebook d'entraînement
├── regmodel.pkl                               # Modèle entraîné
├── scaler.pkl                                 # StandardScaler sérialisé
├── app.py                                     # API Flask
├── requirements.txt                           # Dépendances Python
├── Dockerfile                                 
├── docker-compose.yml                         
└── README.md
```

---

## 📊 Dataset

**Source :** `sklearn.datasets.fetch_california_housing`

| Feature     | Description                              |
|-------------|------------------------------------------|
| MedInc      | Revenu médian du groupe de blocs         |
| HouseAge    | Âge médian des maisons                   |
| AveRooms    | Nombre moyen de pièces par ménage        |
| AveBedrms   | Nombre moyen de chambres par ménage      |
| Population  | Population du groupe de blocs            |
| AveOccup    | Nombre moyen de membres par ménage       |
| Latitude    | Latitude                                 |
| Longitude   | Longitude                                |

**Cible :** Valeur médiane des maisons (en centaines de milliers de dollars)

---

## 📈 Performances du modèle

| Métrique | Valeur |
|----------|--------|
| MAE      | 0.527  |
| MSE      | 0.530  |
| RMSE     | 0.728  |
| R² Score | 0.596  |

---

## ⚙️ Pipeline ML

1. Chargement du dataset via `sklearn`
2. Préparation des données avec `pandas`
3. Division train/test (`train_test_split`)
4. Normalisation avec `StandardScaler`
5. Entraînement du modèle `LinearRegression`
6. Évaluation (MAE, MSE, RMSE, R²)
7. Sérialisation avec `pickle` → `regmodel.pkl` / `scaler.pkl`

---

## 🚀 Déploiement

L'application est conteneurisée avec **Docker**. Se référer au `Dockerfile` et `docker-compose.yml` pour le déploiement.

---

## 🧰 Technologies

- Python 3.11 · scikit-learn · pandas · numpy · matplotlib · Flask · Docker