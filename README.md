# Vacation Accommodation Analysis

**Author:** Jean Yves Nkwane Ebongue ([Nejy190501](https://github.com/Nejy190501))

## Overview
This repository contains a comprehensive data analysis of vacation accommodations (Airbnbs and Hotels). The project explores the factors that influence pricing, identifies distinct market segments through clustering, and builds a classification model to predict high-rated listings.

## Project Structure
- `Case_Study_Jean_Yves_Nkwane_Ebongue_77201393552.ipynb`: The main Jupyter Notebook containing the full analysis, code, and interpretations.
- `vacation_accommodations.csv`: The dataset used for the analysis (cleaning, EDA, and modeling).

## Methods Used
* **Data Cleaning & Preprocessing:** Handled missing values (imputation), removed duplicates, corrected data entry errors, and managed outliers using the IQR method.
* **Exploratory Data Analysis (EDA):** Visualized distributions and relationships using `matplotlib` and `seaborn`.
* **Linear Regression:** Built to predict the price per night and understand the impact of various features (capacity, room type, location).
* **K-Means Clustering:** Applied to segment the market into "premium," "budget," and "value" accommodations.
* **Logistic Regression:** Developed a classifier to predict whether a listing will receive a high rating (>= 4.0), achieving an accuracy of 83%.

## Key Insights
1. **Price Drivers:** Capacity and room type (entire home vs. shared) are the strongest predictors of price. Interestingly, cleanliness and service scores do not heavily inflate pricing.
2. **Market Segments:** The market naturally groups into three overlapping but distinct clusters based on price, quality, and engagement.
3. **Rating Predictors:** Cleanliness is by far the most critical factor in securing a high rating. Price has almost no impact on whether a listing is rated well.

## Technologies
- Python 3
- Pandas & NumPy
- Scikit-Learn
- Matplotlib & Seaborn
