# Aqueous Solubility Prediction Using Supervised Machine Learning

## Overview
This project investigates the use of supervised machine learning regression models to predict **aqueous solubility of chemical compounds**, a key factor influencing drug bioavailability in pharmaceutical development.  
Accurate in silico solubility prediction can significantly reduce experimental cost and time during early-stage drug discovery.

The study evaluates multiple regression and ensemble models on a curated dataset, compares their performance, and identifies the most effective approach for predicting aqueous solubility.

---

## Objectives
- Build and evaluate multiple supervised regression models for solubility prediction
- Compare model performance to identify the best-performing approach for the given dataset
- Optimize the selected model through cross-validation and hyperparameter tuning
- Interpret model behavior using feature importance and explainability techniques
- Produce reproducible, well-documented results suitable for scientific and industrial contexts

---

## Dataset
- Curated molecular descriptor dataset derived from a published solubility dataset
- Target variable: **aqueous solubility (continuous)**
- Features include physicochemical descriptors such as:
  - Molecular weight
  - LogP (lipophilicity)
  - Hydrogen bond donors (HBD)
  - Hydrogen bond acceptors (HBA)
  - Additional molecular descriptors

---

## Methodology

### Data Preparation
- Feature–target separation
- Train / validation / test split to prevent information leakage
- Feature scaling using `StandardScaler`

### Models Evaluated
**Baseline Models**
- Linear Regression
- Support Vector Regression (SVR)
- K-Nearest Neighbors (KNN)
- Kernel Ridge Regression (KRR)
- Linear RANSAC

**Tree-Based & Ensemble Models**
- Random Forest Regressor
- Extra Trees Regressor (ET)
- AdaBoost (ET-based)
- Bagging (ET-based)
- LightGBM
- XGBoost
- Stacking Regressor (Lasso as meta-learner)

---

## Model Evaluation Metrics
Models were compared using:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)
- Coefficient of Determination (R²)

Visualization techniques included:
- Residual plots
- Learning curves
- Validation curves
- Prediction error plots
- Feature importance and SHAP explainability

---

## Key Results
- **Extra Trees Regression (ET)** achieved the strongest overall performance
- **Bagging with Extra Trees** improved generalization on unseen test data
- Final model achieved a **high R² score**, indicating strong predictive accuracy
- Lipophilicity (MolLogP) emerged as the most influential feature, aligning with chemical intuition

---

## Model Interpretability
- Feature importance analysis confirmed known physicochemical relationships
- SHAP values were used to explain model predictions and feature contributions
- Results demonstrate both **predictive performance** and **scientific plausibility**

---

## Technologies Used
- Python
- scikit-learn
- pandas, NumPy
- matplotlib, seaborn
- SHAP
- Jupyter Notebook
- R (for supplementary analysis and visualization)

---

## Reproducibility
To reproduce the analysis:
1. Clone the repository
2. Install required Python dependencies
3. Open the notebooks in sequential order (`Step_1` → `Step_4`)
4. Refer to the PDF report for full methodological and analytical context

---

## License
This project is released under the MIT License.
