# Model_Comparison
# 🏠 California Housing — Linear Regression & Model Comparison

AI/ML project on the built-in `scikit-learn` California Housing dataset (1990 U.S. Census). **Task 2** extends it with feature engineering review, multiple regression models, and a structured performance comparison.

## 📁 Project Files

| File | Task | Description |
| `AI_ML_Task2_Model_Comparison.ipynb` | 2 | Notebook comparing Linear Regression, Ridge Regression, and Decision Tree |
| `Report.pdf` |  | 2-page methodology, results, and conclusion report |
| `requirements.txt` | — | Python dependencies for both tasks |
| `README.md` | — | This file |

## 📊 Dataset

- **Source:** `sklearn.datasets.fetch_california_housing`
- **Samples:** 20,640 housing blocks
- **Features (8):** `MedInc`, `HouseAge`, `AveRooms`, `AveBedrms`, `Population`, `AveOccup`, `Latitude`, `Longitude`
- **Target:** `MedHouseVal` / `HousePrice` — median house value (in $100,000s)
- No missing values or duplicates.

## 🔬 Task 2 — Model Optimization & Comparison

1. Load the dataset and separate features/target
2. Scale features with `StandardScaler`
3. Split into 80% training / 20% test sets
4. Train three models: Linear Regression, Ridge Regression (alpha=1.0), Decision Tree Regressor (max_depth=5)
5. Compare RMSE and R² across all three on the same test set
6. Select the best-performing model automatically (highest R²) and visualize actual vs. predicted

**Results:**

| Model | RMSE | R² Score |
|---|---|---|
| Linear Regression | 0.7456 | 0.5758 |
| Ridge Regression | 0.7456 | 0.5758 |
| **Decision Tree (max_depth=5)** | **0.7242** | **0.5997** |

The Decision Tree Regressor was selected as the best-performing model.

## 🚀 Getting Started

1. Clone or download this project folder.
2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate    # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Launch Jupyter and open either notebook:
   ```bash
   jupyter notebook California_Housing_Linear_Regression.ipynb
   # or
   jupyter notebook AI_ML_Task2_Model_Comparison.ipynb
   ```
5. Run all cells from top to bottom. The dataset downloads automatically via `scikit-learn` (internet connection required on first run).

## 🔮 Future Improvements

- Tune the Decision Tree's depth or try ensemble methods (Random Forest, Gradient Boosting)
- Explore stronger regularization (Ridge/Lasso with tuned alpha) if multicollinearity increases
- Feature engineering (e.g., rooms-per-household ratio)
- Broader cross-validation and handling of capped target values ($500,000 max)

## 📚 References

- Pace, R. K., & Barry, R. (1997). *Sparse Spatial Autoregressions.* Statistics & Probability Letters.
- [scikit-learn: fetch_california_housing](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)
- [scikit-learn: LinearRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
- [scikit-learn: Ridge](https://scikit-learn.org/stable/modules/linear_model.html#ridge-regression)
- [scikit-learn: DecisionTreeRegressor](https://scikit-learn.org/stable/modules/tree.html)

