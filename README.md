# 📦 House Price Prediction


## Demo Machine Learnirg App

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://houseprediction-ml.streamlit.app/)


## Objective of the Project
The goal of this project is to predict housing prices by analyzing historical data and property features and deliver insights that support data-driven decision-making using machine learning regression algorithms.

## Dataset Overview:
Shape: The dataset contains 21,613 rows and 21 variables(columns). The majority of our data types are numeric, including **15 integer** and **5 float** columns
File Format: The dataset is provided in CSV format.
### Dataset Source:[King County Houses Dataset on Kaggle](https://www.kaggle.com/datasets/minasameh55/king-country-houses-aa)

###  Key Variables:
- **id**: The unique numeric identifier assigned to each house being sold.
- **date**: The date on which the house was sold.
- **price**: The price of the house (target variable for prediction).
- **bedrooms**: The number of bedrooms in the house.
- **bathrooms**: The number of bathrooms in the house.
- **sqft_living**: The size of the house in square feet.
- **sqft_lot**: The size of the lot in square feet.
- **floors**: The number of floors (levels) in the house.
- **waterfront**: Indicates whether the house has a waterfront view (0 = no, 1 = yes).
- **view**: Indicates whether the house has been viewed (0 = no, 1 = yes).
- **condition**: The overall condition of the house, rated on a scale from 1 to 5.
- **grade**: The overall grade given to the house, based on the King County grading system, rated from 1 to 11.
- **sqft_above**: The square footage of the house excluding the basement.
- **sqft_basement**: The square footage of the basement.
- **yr_built**: The year the house was built.
- **yr_renovated**: The year the house was renovated (if applicable).
- **zipcode**: The zipcode of the house’s location.
- **lat**: The latitude of the house’s location.
- **long**: The longitude of the house’s location.
- **sqft_living15**: The living room area in 2015 (post-renovations).
- **sqft_lot15**: The lot size area in 2015 (post-renovations).


### Methodology

##### Data Cleaning & Data Understading
Initial examination of the dataset for missing values and duplicate rows.
Descriptive statistics and visual analysis to understand the data ditributions.
Removal of irrelevant features (ID variable).
Outlier detection using interquartile ranges (IQR).

##### Feature Engineering & Data Preprocessing
Putting the target (price) on the end for clear understading of correlations of the features with this target
Dealing with Multicolinearity by examining the correlation matrix (using person method)
Aplied feature engineering for the features with lower correlaction with the target price.

##### Modeling
Data Preparation: Split dataset into features (X) and target (price), followed by train-test split (70/30).
Model Selection: Tested models (Linear Regression, Ridge, Lasso, Decision Tree, KNN, XGBoost). XGBoost performed best based on R², RMSE, MSE, and MAE (best balance of accuracy and error metrics)
Model Refinement: Applied 4 models with different scenarios using XGboost (standard scaling, log transformation, and outlier removal to improve performance)
Analysis: Evaluated correlations to address multicollinearity and visualized actual vs. predicted values.

##### Data Visualization:
1. Scatter Plot of Actual vs Predicted Price (XGBoost Model): A scatter plot comparing the actual vs. predicted prices from the XGBoost model, providing a clear visualization of prediction accuracy.
2. Trend Analysis of Price Fluctuations (Actual vs Predicted): A trend analysis illustrating the fluctuations of actual and predicted prices over the course of the month, highlighting the model's performance in capturing price trends.

#### Key Findings
The  model 4 (with all features and no outliers ) showed better results than the previous scenarios, with lower margin of error and balanced variability. 

#### Next Steps:
The next steps to enhance the model include fine-tuning, adjusting hyperparameters, applying Principal Component Analysis (PCA), and performing cross-validation.

#### Deliverables
1. Jupyter Notebook: Contains the complete EDA, visualizations, and insights.
2. PowerPoint Presentation: Summarizes the key findings of the project, highlighting the results with clear and impactful visualizations to facilitate communication of the insights.
3. Streamlit App: Displays the final dataset along with predictions, offering interactive exploratory data analysis (EDA) and trend analysis. It also visualizes actual vs. predicted price fluctuations over the month for deeper insights.
