# Life Cycle Assessment (LCA) - Random Forest Regression Analysis

This project utilizes a **Random Forest Regressor** to predict the **Global Warming Potential (GWP)**, measured in kg CO2 eq, of various beverage containers based on their life cycle data.

## 📊 Project Overview

The analysis explores how different materials, manufacturing processes, and transportation factors contribute to the environmental impact of packaging. The model identifies key variables that drive carbon emissions throughout the life cycle of a product.

### Key Features of the Analysis:

* **Data Preprocessing**: Categorical variables (Material type, Manufacturing process, etc.) are encoded using `LabelEncoder`.
* **Model**: Random Forest Regressor using 100 trees.
* **Evaluation**: Performance is measured using R-squared ($R^2$), Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE).
* **Insights**: Feature importance ranking to identify the primary contributors to GWP.

## 📈 Dataset Summary

* **Samples**: 54
* **Features**: 13 (8 categorical, 5 numerical)
* **Target Variable**: `GWP (kg CO2 eq)`

| Feature Category | Examples |
| --- | --- |
| **Material Info** | Bottle Material, Cap Material, Filled Material, Mass |
| **Logistics** | Transport Mode, Transport Distance, No. of uses |
| **Production** | Manufacturing Process, Electricity Mix, Electricity Value |
| **End of Life** | EOL Scenario, EOL Percentage |

## 🚀 Final Results

The model demonstrated the following results on the unseen test set:

* **R² Score**: 0.6079
* **RMSE**: 24.2422 kg CO2 eq
* **MAE**: 11.5107 kg CO2 eq

### Top Contributors to GWP:

According to the model's **Feature Importance**, the top factors impacting emissions are:

1. **Manufacturing Process**
2. **Label Type**
3. **Transport Distance**

## 🛠️ Requirements

To run this notebook, you will need:

* Python 3.x
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

## 📂 Usage

1. Ensure `lca_data.csv` is in the same directory as the notebook.
2. Run the cells sequentially to perform data loading, encoding, training, and visualization.
