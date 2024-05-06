# Objective
## This project was to find a multiple linear regression model by using R from a given used car price data and predict a used car price on the basis of the test data. The data was from one of Kaggle's datasets and is available [here](https://www.kaggle.com/competitions/usedcars2023). The selling price was the target variable and, other variables were used for features.
### 
1. Load Libraries:
   ####
   The code starts by loading necessary libraries for data manipulation, visualization, and modeling. This includes libraries like caTools, xgboost, caret, Metrics, readr, fastDummies, stringr, dplyr, tidyr, lightgbm, data.table, ggplot2, Matrix, tm, SnowballC, mice, rpart, and rpart.plot.

2. Data Collection:
   ####
   Data is loaded from CSV files (analysisData.csv and scoringData.csv) into the train and train2 data frames, respectively. These data frames are then concatenated row-wise using bind_rows.

3. Data Cleaning:
   ####
   Missing values in the dataset are identified and filled appropriately. Some columns are transformed or imputed based on group-wise statistics like mean, median, or mode.

4. Exploratory Data Analysis (EDA):
   ####
   Various plots are generated to visualize the distribution of price across different car makes and numeric predictors using ggplot2.

5. Feature Engineering:
   ####
   One-hot encoding is performed on categorical variables like make_name, body_type, fuel_type, transmission_display, wheel_system, and engine_type. Additionally, major options are encoded into a sparse matrix. Boolean variables (True/False) are converted to numeric values (-1 for False, 1 for True, and 0 for missing or other values).

6. Develop Models:
   ####
   Gradient Boosting Machine (GBM) and XGBoost models are developed for predicting car sale prices. Hyperparameter tuning is performed for the GBM model, and the best parameters are selected. The XGBoost model is trained with tuned hyperparameters.

7. Prediction:
   ####
   The trained models are used to make predictions on the test data set, and root mean squared error (RMSE) is calculated as a measure of model performance.
