# Predict Bike Sharing Demand with AutoGluon

## Project Overview
This project was completed as part of the **AWS Machine Learning Engineer Nanodegree**. The goal was to predict bike-sharing demand using the **AutoGluon** library on the Kaggle competition dataset. This involved a complete machine learning workflow, including exploratory data analysis, feature engineering, and hyperparameter optimization.

## Key Steps & Methodology
* **Exploratory Data Analysis (EDA):** Visualized feature distributions and analyzed their relationship with the target variable (`count`).
* **Feature Engineering:** * Extracted `hour`, `day`, and `month` from the timestamp to capture temporal patterns.
    * Transformed `season` and `weather` into categorical data types for better model interpretation.
* **AutoML with AutoGluon:** * Trained three iterations of models: Initial, Improved (with added features), and Hyperparameter Optimized (HPO).
    * Utilized the `TabularPredictor` to automatically ensemble the best performing models.

## Results Summary
The model performance improved significantly throughout the iterations. Below are the Kaggle RMSE scores (lower is better):

| Model | Kaggle Score (RMSE) |
| --- | --- |
| **Initial (Raw Data)** | 1.80237 |
| **Improved (Feature Engineering)** | 0.62776 |
| **Hyperparameter Optimized (HPO)** | 0.48512 |

## Performance Visualization
The project involved analyzing the training and optimization process:
* **Training Run Score:** Comparison of model performance across iterations.
* **Hyperparameter Optimization:** Tuning parameters like `num_trials`, `search_strategy`, and specific model hyperparameters (GBM, NN).

## Technologies Used
* **Language:** Python
* **Libraries:** AutoGluon, Pandas, Matplotlib, Seaborn
* **Platform:** AWS SageMaker / Local Jupyter Environment
