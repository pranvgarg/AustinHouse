# AustinHouse
---

# Austin House Price Prediction Project

## Overview
This project aims to predict house prices in Austin, Texas, using various machine learning models. The project includes comprehensive data preprocessing, feature engineering, model training, and evaluation. The final model is applied to a holdout dataset for predictions.

## Project Structure
- **Data Import and Exploration**: Loading and initial exploration of the dataset to understand its structure and characteristics.
- **Data Manipulation**:
  - Added a new column `logLatestPrice` by taking the logarithm of `latestPrice`.
  - Derived the age of the house and categorized it into different age groups.
  - Converted binary columns to numeric values and created a new feature `total_amenities`.
  - Extracted and converted sale date components into year, month, day, and season.
- **Geospatial Features**:
  - Performed clustering based on latitude and longitude to create a new feature `crossCluster`.
- **Modeling**:
  - Trained and evaluated multiple models, including Regression Tree, Pruned Tree, Bagging with Random Forest, XGBoost, BART, Ridge, and Lasso Regression.
  - Calculated and compared MSE and RMSE for each model to identify the best performer.
- **Model Comparison and Conclusion**:
  - Summarized the performance of different models and provided insights and recommendations based on the model performance.
- **Application on Holdout Set**:
  - Applied the best model on the holdout dataset for final predictions.

## Data
The dataset used in this project consists of various features, including geospatial data, sale dates, and property characteristics. The main target variable is the logarithm of the latest sale price (`logLatestPrice`).

## Features
- **Geospatial Data**: Latitude, Longitude, and Clustering (`crossCluster`).
- **Temporal Data**: Sale Year, Sale Month, and Season.
- **Property Characteristics**: Number of Bedrooms, Bathrooms, Stories, Garage Spaces, etc.
- **Aggregated Amenities**: Total number of amenities based on binary columns like `hasAssociation`, `hasGarage`, etc.

## Models Used
- **Regression Tree**: A simple decision tree model.
- **Pruned Tree**: A decision tree model pruned for better generalization.
- **Bagging with Random Forest**: An ensemble method using multiple decision trees.
- **Random Forest**: A popular ensemble learning method that builds multiple decision trees and merges them together to get a more accurate and stable prediction.
- **XGBoost**: An efficient implementation of gradient boosting that is widely used for machine learning competitions.
- **BART (Bayesian Additive Regression Trees)**: A non-parametric Bayesian model that provides flexible and robust predictions.
- **Ridge Regression**: A linear regression model with L2 regularization.
- **Lasso Regression**: A linear regression model with L1 regularization, which also performs feature selection.

## Results
The models were evaluated based on their Mean Squared Error (MSE) and Root Mean Squared Error (RMSE). Below is a summary of the performance:

| Model              | MSE       | RMSE     |
|--------------------|-----------|----------|
| Single Tree        | 107,407.4 | 327.73   |
| Pruned Tree        | 91,419.22 | 302.36   |
| Bagging            | 67,584.75 | 259.97   |
| Random Forest      | 67,067.45 | 258.97   |
| XGBoost            | 26,151.38 | 161.71   |
| BART               | 19,995.7  | 141.41   |
| Ridge Regression   | 60,583.55 | 246.14   |
| Lasso Regression   | 57,363.87 | 239.51   |

The BART model outperformed all other models, achieving the lowest RMSE, indicating its superior ability to capture complex relationships in the data.

## Conclusion
BART and XGBoost emerged as the top performers, with BART having a slight edge in terms of RMSE. These models are well-suited for capturing complex, non-linear relationships in the data.

## Future Work
- Further hyperparameter tuning for models like XGBoost and Random Forest.
- Exploring more advanced feature engineering techniques.
- Considering additional ensemble methods like stacking to further improve predictions.

## How to Run
To replicate this project, follow these steps:

1. Clone the repository.
2. Run Rmd file and Run the Jupyter notebook to see the analysis and model training process.
3. The predictions on the holdout set are saved as `austinhouses_holdout_predictions.csv`.

## Contact
For any questions or suggestions, feel free to contact [Pranav Garg](mailto:pranavgarg71@gmail.com).

---

You can copy and paste this structure into a `README.md` file for your GitHub repository. Adjust the contact information and any other details as needed.
