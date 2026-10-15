# Automated Model Selection for Boston Housing Dataset

## 📌 Project Overview

This project automates the process of selecting the best regression model for the Boston Housing dataset using Python and Scikit-learn.

Instead of manually training and comparing individual algorithms, the notebook evaluates multiple regression models, tunes their hyperparameters using cross-validation, and selects the best-performing model based on Root Mean Squared Error (RMSE).

The project also evaluates the selected model on unseen test data, visualizes its predictions, and saves the trained model for future use.

## 🎯 Objectives

- Automate regression model comparison.
- Understand K-Fold Cross-Validation.
- Apply hyperparameter tuning using `GridSearchCV`.
- Select the best model using cross-validated RMSE.
- Evaluate model performance using regression metrics.
- Visualize actual versus predicted values.
- Save the best model and its performance report.

## 📊 Dataset

**Dataset:** Boston Housing Dataset

The dataset contains housing-related features used to predict the median value of owner-occupied homes.

- **Input:** Housing and neighborhood features.
- **Target:** `MEDV` — median home value, expressed in the original dataset's units (historically thousands of dollars).
- **Source:** OpenML, dataset named `boston`, version 1.

The notebook downloads the dataset using Scikit-learn's `fetch_openml()` function.

> **Note:** The Boston Housing dataset has documented ethical limitations, including a feature reflecting historical racial discrimination. This project is intended for educational purposes and should not be used for real-world housing or lending decisions.

## 🤖 Models Compared

The notebook evaluates the following regression algorithms:

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. K-Nearest Neighbors (KNN) Regression
5. Support Vector Regression (SVR)
6. Decision Tree Regression
7. Random Forest Regression
8. Gradient Boosting Regression

Each model is evaluated using cross-validation, and its hyperparameters are tuned where applicable.

## ⚙️ Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Joblib
- JSON

## 🔄 Project Workflow

1. Load the Boston Housing dataset.
2. Inspect the dataset and check for missing values.
3. Split the data into training and testing sets.
4. Create preprocessing pipelines for the candidate models.
5. Configure candidate models and hyperparameter grids.
6. Apply five-fold cross-validation using `GridSearchCV`.
7. Compare models using cross-validated RMSE.
8. Select the model with the lowest cross-validated RMSE.
9. Evaluate the selected model on the held-out test set.
10. Visualize predictions and residuals.
11. Inspect feature importance or model coefficients where supported.
12. Save the trained model and best-model report.

## 📈 Evaluation Metrics

The project uses the following metrics:

| Metric | Description | Preferred Value |
|---|---|---|
| MAE | Mean Absolute Error | Lower |
| MSE | Mean Squared Error | Lower |
| RMSE | Root Mean Squared Error | Lower |
| R² | Coefficient of Determination | Generally closer to 1 |

**Primary selection metric:** Cross-validated RMSE.

RMSE measures the typical scale of prediction errors while penalizing larger errors more heavily than MAE. R² indicates how much target variation is explained by the model, relative to a mean-prediction baseline.

## 📉 Visualizations

The notebook generates:

- Distribution of the target variable.
- Comparison of candidate models using cross-validated RMSE.
- Actual versus predicted housing values.
- Residual plot for the selected model.
- Feature importance or coefficient analysis, where supported.

These visualizations help assess model performance and understand prediction errors.

## 🏆 Best Model Selection

After running the notebook, the best-model report displays:

- Best model name.
- Best cross-validated RMSE.
- Test MAE.
- Test MSE.
- Test RMSE.
- Test R² score.
- Best hyperparameters.
- Selected estimator configuration.

The winning model is determined automatically from the cross-validation results rather than being chosen in advance.

## 💾 Output Files

After successfully executing all notebook cells, the following files are generated:

| File | Purpose |
|---|---|
| `best_boston_housing_model.joblib` | Stores the selected trained model and preprocessing pipeline. |
| `best_model_report.json` | Stores the selected model, evaluation metrics, hyperparameters, and Scikit-learn version. |

These files can be reused to inspect the results or make predictions without repeating the entire model-selection process.

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Install the dependencies

```bash
pip install numpy pandas matplotlib scikit-learn joblib jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Run the notebook

Open `automated_boston_housing_model_selection.ipynb` and execute all cells in sequence.

An internet connection is required to download the dataset from OpenML if it is not already cached.

## 🧠 Key Concepts Learned

- Regression algorithms
- Train-test splitting
- Data preprocessing pipelines
- K-Fold Cross-Validation
- Hyperparameter optimization
- Grid Search
- Model selection criteria
- Regression evaluation metrics
- Residual analysis
- Model persistence using Joblib

## 🔮 Future Improvements

- Add more regression algorithms.
- Compare Grid Search with Randomized Search.
- Include learning curves to identify overfitting and underfitting.
- Add model-specific error analysis.
- Create a simple web interface for predictions.
- Experiment with other, more appropriate housing datasets.

## 👨‍💻 Author

**Atharva Pundkar**

GitHub: [atharva270405](https://github.com/atharva270405)

---

*This project demonstrates an automated machine learning workflow for educational purposes, from data preparation and model tuning to evaluation and model persistence.*
