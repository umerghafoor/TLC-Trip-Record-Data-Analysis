# TLC Trip Record Data Analysis

This project involves analyzing and building predictive models using New York City's Yellow Taxi trip record data from January 2019. The primary goal is to predict the total amount for a taxi trip based on various features.

## Table of Contents

- [Introduction](#introduction)
- [Data](#data)
- [Setup](#setup)
- [Data Cleaning](#data-cleaning)
- [Data Preparation](#data-preparation)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Tuning](#tuning)
- [Results](#results)

## Introduction

This project analyzes Yellow Taxi trip data to build models for predicting trip costs. The analysis includes data cleaning, feature engineering, and model building using various machine learning algorithms.

## Data

The dataset used in this project is `yellow_tripdata_2019-01.parquet`, which contains trip records for January 2019. Additional data used includes a lookup file for taxi zones (`taxi_zone_lookup.csv`).

Link to main [dataset](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

## Setup

1. **Clone the repository:**

   ```sh
   git clone https://github.com/misraturp/Guided-project-course-material.git
   ```

2. **Install dependencies:**

   ```sh
   pip install -r requirements.txt
   ```

3. **Setup data**

    To set up the data in the data folder, you can follow these steps:

    1. Create a folder named "data" in the root directory of your project.

    2. Download the dataset file `yellow_tripdata_2019-01.parquet` and the lookup file `taxi_zone_lookup.csv` from the provided link.

    3. Move both files into the `data` folder you created.

    4. Your data folder structure should look like this:
        ```
        ├── data
        │   ├── yellow_tripdata_2019-01.parquet
        │   └── taxi_zone_lookup.csv
        ├── README.md
        ├── requirements.txt
        └── TLC_Trip_Record_Data_Analysis.ipynb
        ```

4. **Run the analysis:**

   ```sh
   jupyter notebook
   ```

   Open `TLC_Trip_Record_Data_Analysis.ipynb` in Jupyter Notebook to follow along with the analysis.

## Data Cleaning

1. Loaded the dataset and selected relevant columns.
2. Removed negative and excessively high values from the `total_amount` column.
3. Dropped rows with missing values.
4. Limited the dataset to January 2019.

## Data Preparation

1. Converted datetime columns to appropriate formats.
2. Added new columns for the year, month, day, and hour of each transaction.
3. Grouped data by categorical features and calculated average values.

## Feature Engineering

1. Added features for the day of the week and weekend indicators.
2. Included a column to identify federal holidays.
3. Merged with borough information based on location IDs.

## Modeling

1. Built an initial benchmark model using a Decision Tree Regressor.
2. Trained and evaluated models using Random Forest and Gradient Boosting algorithms.
3. Handled data leakage issues by carefully selecting features.

## Evaluation

1. Evaluated model performance using MAE, MSE, RMSE, and R² metrics.
2. Visualized the results using scatter plots of true vs. predicted values.

## Tuning

1. Conducted hyperparameter tuning for the Random Forest model using randomized search.
2. Identified the best hyperparameters to improve model performance.
3. Retrained the model with optimal parameters.

## Results

- The tuned Random Forest model showed the best performance among the models tested.
- Key performance metrics:
  - **Mean Absolute Error (MAE):** [value]
  - **Mean Squared Error (MSE):** [value]
  - **Root Mean Squared Error (RMSE):** [value]
  - **R² Score:** [value]

## Contact

For questions or suggestions, please open an issue or contact [umerghaforr@gmail.com].
