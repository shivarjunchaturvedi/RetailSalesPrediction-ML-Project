# Retail Sales Prediction using Machine Learning

A machine-learning internship project built with Python and scikit-learn to explore retail transaction data and estimate the `Total_Sales` value from transaction features.

> **Project context:** Created as part of a 15-day internship with Skills4India / YBI Foundation.

## Overview

This repository contains a Jupyter notebook that walks through loading a retail dataset, inspecting and visualizing the data, preparing features, training a Linear Regression model, and evaluating predictions.

### Visual Results

The notebook includes the project's actual generated visualizations and workflow:

- **Sales distribution:** histogram showing the distribution of `Total_Sales`.
- **Actual vs. predicted sales:** scatter plot comparing held-out test values with model predictions.
- **Notebook workflow:** data inspection, preprocessing, model training, and evaluation.

[**Open the notebook and view the plots on GitHub**](https://github.com/shivarjunchaturvedi/RetailSalesPrediction-ML-Project/blob/main/Retail_Sales_Prediction_YBI_Internship.ipynb) · [**Run it in Google Colab**](https://colab.research.google.com/github/shivarjunchaturvedi/RetailSalesPrediction-ML-Project/blob/main/Retail_Sales_Prediction_YBI_Internship.ipynb)

### What the notebook covers

- Loads the retail dataset published by YBI Foundation
- Inspects the dataset structure, summary statistics, and missing values
- Performs exploratory data analysis (sales distribution, numeric correlation heatmap, and pairplot)
- Encodes categorical product and category features
- Splits the data into training and test sets
- Scales features using `StandardScaler`
- Trains a Linear Regression model
- Evaluates predictions using MSE, RMSE, and R²
- Plots actual versus predicted sales and demonstrates a sample prediction
- Saves the trained model using Joblib

## Tech Stack

- **Language:** Python
- **Notebook:** Jupyter Notebook / Google Colab
- **Data:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine learning:** scikit-learn (Linear Regression, train/test split, feature scaling, metrics)
- **Model serialization:** Joblib

## Dataset

The notebook loads the CSV from the YBI Foundation repository:

[`RetailSales.csv`](https://raw.githubusercontent.com/YBIFoundation/Internship/main/RetailSales.csv)

An internet connection is required when running the notebook's dataset-loading cell. The notebook's inspected copy contains 1,000 rows and 8 columns.

## Run the Project

### Option 1: Google Colab

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shivarjunchaturvedi/RetailSalesPrediction-ML-Project/blob/main/Retail_Sales_Prediction_YBI_Internship.ipynb)

1. Open the notebook using the badge above.
2. Run the cells from top to bottom.
3. Ensure the runtime has internet access so it can download the dataset.

### Option 2: Run locally

1. Clone the repository:

   ```bash
   git clone https://github.com/shivarjunchaturvedi/RetailSalesPrediction-ML-Project.git
   cd RetailSalesPrediction-ML-Project
   ```

2. (Recommended) Create and activate a virtual environment:

   **Windows**
   ```powershell
   python -m venv .venv
   .venv\\Scripts\\Activate.ps1
   ```

   **macOS / Linux**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter and open `Retail_Sales_Prediction_YBI_Internship.ipynb`:

   ```bash
   jupyter notebook
   ```

## Model Evaluation

The notebook's saved run reports the following results on its 20% test split:

| Metric | Reported result |
|---|---:|
| R² score | 0.8691 |
| Root Mean Squared Error (RMSE) | 873.87 |
| Mean Squared Error (MSE) | 763,650.71 |

These are the notebook's recorded results, not a guarantee that every run or environment will produce identical values.

## Important Modeling Note

In the supplied dataset, `Total_Sales` is calculated from `Quantity × Price`. The notebook uses those transaction fields as predictors of `Total_Sales`, so this is a demonstration of a regression workflow rather than a reliable model for forecasting future retail demand. For a stronger forecasting project, define a future-period target (for example, daily or weekly sales) and use only information available before that period.

## Repository Contents

- `Retail_Sales_Prediction_YBI_Internship.ipynb` — analysis, visualizations, model training, evaluation, and sample prediction.
- `requirements.txt` — Python dependencies.
- `.gitignore` — local environment, cache, and generated model exclusions.

## Author

**Shivarjun Chaturvedi**

- GitHub: [@shivarjunchaturvedi](https://github.com/shivarjunchaturvedi)

## Responsible Use

This repository is intended for educational and portfolio demonstration purposes. Review the dataset source and modeling assumptions before using results for business decisions.
