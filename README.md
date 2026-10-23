# Retail Sales Prediction using Machine Learning

A Python machine-learning project that explores retail transaction data and estimates the `Total_Sales` value from transaction features using Linear Regression.

## Overview

This project demonstrates an end-to-end regression workflow in a Jupyter notebook: loading and inspecting data, exploratory data analysis, feature preparation, model training, evaluation, and sample prediction.

### Visual Results

The notebook includes generated visualizations and the modeling workflow:

- **Sales distribution:** histogram showing the distribution of `Total_Sales`.
- **Actual vs. predicted sales:** scatter plot comparing held-out test values with model predictions.
- **Notebook workflow:** data inspection, preprocessing, training, and evaluation.

[**Open the notebook on GitHub**](https://github.com/shivarjunchaturvedi/RetailSalesPrediction-ML-Project/blob/main/Retail_Sales_Prediction.ipynb) · [**Run it in Google Colab**](https://colab.research.google.com/github/shivarjunchaturvedi/RetailSalesPrediction-ML-Project/blob/main/Retail_Sales_Prediction.ipynb)

## Features

- Loads the retail dataset published by YBI Foundation
- Inspects dataset structure, summary statistics, and missing values
- Performs exploratory data analysis using sales distribution plots, a numeric correlation heatmap, and a pairplot
- Encodes categorical product and category features
- Splits data into training and test sets
- Scales features using `StandardScaler`
- Trains a Linear Regression model
- Evaluates predictions using MSE, RMSE, and R²
- Plots actual versus predicted sales and demonstrates a sample prediction
- Saves the trained model using Joblib

## Tech Stack

- **Language:** Python
- **Notebook:** Jupyter Notebook / Google Colab
- **Data processing:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine learning:** scikit-learn
- **Model serialization:** Joblib

## Dataset

The notebook loads the CSV dataset from the YBI Foundation repository:

[`RetailSales.csv`](https://raw.githubusercontent.com/YBIFoundation/Internship/main/RetailSales.csv)

An internet connection is required when running the dataset-loading cell. The notebook's inspected copy contains 1,000 rows and 8 columns.

## Run the Project

### Option 1: Google Colab

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shivarjunchaturvedi/RetailSalesPrediction-ML-Project/blob/main/Retail_Sales_Prediction.ipynb)

1. Open the notebook using the badge above.
2. Run the cells from top to bottom.
3. Ensure the runtime has internet access so it can download the dataset.

### Option 2: Run locally

1. Clone the repository:

   ```bash
   git clone https://github.com/shivarjunchaturvedi/RetailSalesPrediction-ML-Project.git
   cd RetailSalesPrediction-ML-Project
   ```

2. Create and activate a virtual environment (recommended).

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

4. Launch Jupyter and open `Retail_Sales_Prediction.ipynb`:

   ```bash
   jupyter notebook
   ```

## Model Evaluation

The notebook's recorded run reports the following results on its 20% test split:

| Metric | Recorded result |
|---|---:|
| R² score | 0.8691 |
| Root Mean Squared Error (RMSE) | 873.87 |
| Mean Squared Error (MSE) | 763,650.71 |

These are recorded notebook results, not a guarantee that every run or environment will produce identical values.

## Modeling Limitation

In the supplied dataset, `Total_Sales` is calculated from `Quantity × Price`. The notebook uses transaction fields including quantity and price to predict `Total_Sales`. Therefore, this project demonstrates a regression workflow; it should not be presented as a validated future-sales forecasting system. A stronger forecasting project would define a future-period target (such as daily or weekly sales) and use only information available before that period.

## Repository Contents

- `Retail_Sales_Prediction.ipynb` — data analysis, visualizations, model training, evaluation, and sample prediction.
- `requirements.txt` — Python dependencies.
- `.gitignore` — excludes local environments, caches, and generated model artifacts.

## Author

**Shivarjun Chaturvedi**

- GitHub: [@shivarjunchaturvedi](https://github.com/shivarjunchaturvedi)

## Purpose

This project is for learning and portfolio demonstration. Review the dataset source and modeling assumptions before using results for business decisions.
