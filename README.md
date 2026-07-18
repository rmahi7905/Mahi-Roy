#My Data science project

                               Netflix eda project
# Netflix Shows and Movies - Exploratory Data Analysis

This project performs an Exploratory Data Analysis (EDA) on the Netflix dataset using Python. It explores trends in content creation, distribution of content types, and shifts in uploads over time.

## 📊 Key Insights Found
* **Content Mix:** Movies make up the vast majority of the total catalog compared to TV Shows.
* **Growth Peak:** Content additions peaked aggressively in 2019 before seeing a decline in 2020–2021 due to production delays.
* **Production Hubs:** The United States and India lead globally as the platform's primary production origins.

## 🛠️ Tools Used
* Python
* Pandas (Data Cleaning & Manipulation)
* Matplotlib & Seaborn (Data Visualization)
* Kaggle Notebooks








  

                                            linear regression project

# California Housing Price Prediction — Linear Regression

A regression project predicting median house prices in California using Linear Regression, built as a follow-up to an earlier EDA project and Kaggle's Intro to Machine Learning course.

## Dataset
California Housing Prices (via Kaggle, camnugent) — includes features like median income, location (longitude/latitude, ocean proximity), housing age, and room counts.

## Approach
- Handled missing values in `total_bedrooms` using median imputation
- One-hot encoded the categorical `ocean_proximity` feature
- Discovered and removed ~965 rows where `median_house_value` was artificially capped at $500,001 (a known data collection artifact in this dataset)
- Trained a Linear Regression model using scikit-learn
- Evaluated using MAE and R² on a held-out validation set

## Results
- **MAE:** ~$44,836
- **R²:** ~0.606

Interestingly, removing the capped rows improved MAE (more accurate dollar predictions) but slightly lowered R² — since it also reduced the extreme price variation in the data, making it a good reminder that no single metric tells the whole story.

## Key Insight
Location relative to the ocean was the strongest driver of predicted price — island properties were valued highest, while inland properties were valued lowest, reflecting California's real coastal price premium.

## What I Learned
- The full regression workflow: train/test split, fit, predict, evaluate
- How to handle categorical data via one-hot encoding
- How to spot and handle data artifacts (like the price cap) using residual plots
- Why MAE and R² can move in different directions, and why both matter
