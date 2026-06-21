# House Price Prediction

Internship Project, Week 1

## Overview

The main objective of this project is to create a regression model that predicts house prices based on property characteristics such as area (in square feet), number of bedrooms/bathrooms, number of stories, and included amenities (air conditioning, parking, furnishing, etc.), evaluate how well the model performed, and determine which property characteristics most influence the price of a house.
## Dataset

Housing Prices Dataset from Kaggle: https://www.kaggle.com/datasets/yasserh/housing-prices-dataset

545 records, 13 columns, no missing values, no duplicates.

## What's in this repo

- `analysis.ipynb` - the full notebook (data exploration, cleaning, model building, charts, and insights)
- `Housing.csv` - the dataset used
- `summary.docx` - a 1-page written summary of the findings
- `charts/` - the 3 chart images generated in the notebook

## Approach

1. **Data Exploration** - loaded the data, checked shape, looked for missing values and duplicates
2. **Data Cleaning** - converted yes/no columns to 1/0, one-hot encoded the furnishing status column
3. **Model Building** - split the data 80/20, trained a Linear Regression model and a Random Forest Regressor, compared performance using MAE, RMSE, and R²
4. **Visualization** - price distribution histogram, correlation heatmap, and an actual vs. predicted price scatter plot
5. **Insights** - summarized which features matter most and what the model results mean in plain terms

## Results

| Model | MAE | RMSE | R² Score |
|---|---|---|---|
| Linear Regression | ₹970,043 | ₹1,324,507 | 0.653 |
| Random Forest | ₹1,022,560 | ₹1,401,497 | 0.611 |

Linear Regression slightly outperformed Random Forest on this dataset. Area, bathrooms, and air conditioning turned out to be the strongest predictors of price.

## Tools Used

Python, Pandas, Scikit-learn, Matplotlib, Seaborn, Jupyter Notebook / Google Colab
