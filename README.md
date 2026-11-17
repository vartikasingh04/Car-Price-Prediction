# Used Car Price Prediction

Predicting the selling price of used cars in India using Python and machine learning.

## Problem Statement
Used car prices depend on many factors such as age, mileage, engine power and brand. This project analyzes a used car dataset and builds a model to predict the selling price.

## Dataset
- Source: CarDekho used car dataset (Kaggle)
- Size: 8,128 records originally, 6,567 after cleaning
- Features: brand, age, kilometers driven, fuel type, transmission, owner type, mileage, engine, max power, seats

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Google Colab

## Project Workflow
1. **Data cleaning**: removed duplicates and missing values, fixed data types, removed invalid mileage values and extreme outliers in price and kilometers driven
2. **Feature engineering**: created `car_age` and `brand` columns
3. **EDA**: analyzed price vs age, fuel type, transmission, owner type and brand
4. **Modeling**: trained and compared three models on an 80/20 train-test split

## Key Findings
- [Insight 1: e.g. price falls steadily as car age increases]
- [Insight 2: e.g. automatic cars have a higher median price than manual]
- [Insight 3: top 3 important features were X, Y and Z]

## Model Results
| Model | R² | MAE (₹) |
|---|---|---|
| Linear Regression | 0.812 | 106,320 |
| Random Forest | 0.904 | 70,269 |
| Random Forest (log target) | **0.909** | **68,296** |

## Limitations
- The average error of about ₹68,000 is a larger share of the price for cheap cars than for expensive ones
- Few records exist for luxury cars, so predictions there are less reliable
- The dataset does not include factors like car condition, location or accident history

## Future Improvements
- Hyperparameter tuning and trying models such as XGBoost
- Adding a Streamlit app for live price prediction

## How to Run
1. Download `cardekho.csv` from Kaggle
2. Open the notebook in Google Colab or Jupyter
3. Upload the CSV and run all cells
