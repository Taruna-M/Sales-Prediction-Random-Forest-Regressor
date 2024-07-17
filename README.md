# Sales Prediction Model README

## Overview
This repository contains Google Colab Notebook for building a machine learning model to predict sales of items across various outlet stores. The model utilizes a Random Forest Regressor to predict continuous sales values.

## Dataset
The dataset consists of 12 fields:
- **Item_Identifier**: Unique ID for each item.
- **Item_Weight**: Weight of the item.
- **Item_Fat_Content**: Fat content of the item (Low Fat, Regular).
- **Item_Visibility**: The percentage of total display area allocated to this particular item in all stores.
- **Item_Type**: Category of the item.
- **Item_MRP**: Maximum Retail Price of the item.
- **Outlet_Identifier**: Unique ID for each store.
- **Outlet_Establishment_Year**: The year the outlet was established.
- **Outlet_Size**: The size of the outlet (Small, Medium, High).
- **Outlet_Location_Type**: The location type of the outlet (Tier 1, Tier 2, Tier 3).
- **Outlet_Type**: The type of outlet (Grocery Store, Supermarket Type1, Supermarket Type2, Supermarket Type3).
- **Item_Outlet_Sales**: Sales of the item in the store (target variable).

## Preprocessing Steps
1. **Handling Missing Values**: Null values in 'Item_Weight' are replaced with the mean weight of respective item types.
   
2. **Encoding Categorical Variables**: Categorical fields ('Item_Fat_Content', 'Item_Type', 'Outlet_Identifier', 'Outlet_Size', 'Outlet_Location_Type', 'Outlet_Type') are replaced with integers (0, 1, 2, ...).

3. **Feature Standardization**: Numerical features ('Item_Weight', 'Item_Visibility', 'Item_MRP', 'Outlet_Establishment_Year') are standardized to have a mean of 0 and variance of 1 to ensure equal contribution during modeling.

## Model Training
- The data is split into training (90%) and testing (10%) datasets.
- Random Forest Regressor is chosen due to non-linear relationships.

## Model Evaluation
- **R2 Score**: Approximately 49% of the variability in sales is explained by the model.
- **Mean Squared Error (MSE)**: 1469370.015
- **Mean Absolute Error (MAE)**: 815.736

## Conclusion
The model provides a moderate fit for predicting sales based on the dataset used. Further improvements could focus on reducing prediction errors and enhancing the explained variance in sales.
