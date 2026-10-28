<div align="center">
  
# 🏨 Vacation Accommodation Data Analysis 📊

[![Python Version](https://img.shields.io/badge/Python-3.12-blue.svg)](https://python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458.svg?logo=pandas)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E.svg?logo=scikit-learn)](https://scikit-learn.org/)

*A comprehensive end-to-end data analytics project exploring pricing factors, market segmentation, and rating predictions for Airbnbs and Hotels.*

</div>

---

## 📖 Table of Contents
- [About the Project](#-about-the-project)
- [Key Features & Objectives](#-key-features--objectives)
- [Methodology](#-methodology)
- [Key Insights & Findings](#-key-insights--findings)
- [Project Structure](#-project-structure)
- [Installation & Usage](#-installation--usage)
- [Author](#-author)
- [License](#-license)

---

## 🎯 About the Project

This repository serves as a portfolio piece showcasing an end-to-end data analytics workflow. By analyzing a dataset of over 1,200 vacation accommodations (`vacation_accommodations.csv`), this project answers critical business questions for a hypothetical travel platform.

The analysis moves from rigorous data cleaning and Exploratory Data Analysis (EDA) into Predictive Analytics using Machine Learning models, concluding with actionable business recommendations.

---

## ✨ Key Features & Objectives

1. **Price Prediction:** What truly drives the price of an accommodation per night?
2. **Market Segmentation:** Are there "hidden" natural groupings of accommodations beyond just "Airbnb vs. Hotel"?
3. **Rating Classification:** Can we accurately predict if a listing will receive a high rating ($\ge 4.0$) based solely on its features?

---

## 🔬 Methodology

The analysis relies heavily on the `scikit-learn` ecosystem, utilizing the following techniques:

*   🧹 **Data Cleaning & Imputation:** Addressed missing values using median imputation (robust against outliers), removed duplicates, fixed textual typos, and capped extreme price outliers using the $1.5 \times \text{IQR}$ rule.
*   📊 **Exploratory Data Analysis (EDA):** Leveraged `matplotlib` and `seaborn` to visualize distributions, boxplots, and feature correlations.
*   📈 **Linear Regression:** Built to evaluate feature coefficients (impact on price) and measure predictive power ($R^2$, RMSE, MAE).
*   🧩 **K-Means Clustering:** Applied unsupervised learning (with `StandardScaler` and evaluated via Silhouette Score) to discover hidden market segments.
*   🤖 **Logistic Regression:** Developed a binary classifier, evaluated via accuracy, confusion matrices, and precision/recall metrics, to predict listing success.

---

## 💡 Key Insights & Findings

### 1. What drives the price? (Linear Regression)
*   **Capacity & Room Type:** The number of guests a place can hold and whether it is an "Entire Home" are the strongest price drivers.
*   **The Quality Paradox:** Cleanliness and service scores have almost **no correlation with price**. High-quality hosts are potentially undercharging for their listings.

### 2. Market Segments (K-Means Clustering)
*   The market naturally splits into three segments ($K=3$):
    *   **Premium:** Higher prices, high capacity, very high engagement.
    *   **Value:** Moderate prices, solid ratings, good balance.
    *   **Budget:** Lower prices, lower average quality scores.

### 3. Predicting High Ratings (Logistic Regression - 83% Accuracy)
*   **Cleanliness is King:** The cleanliness score is by far the strongest predictor of a highly-rated listing across all features.
*   **Price doesn't buy love:** Price has negligible impact on whether a listing gets a good review. Budget places can achieve perfect ratings simply by maintaining exceptional cleanliness.

---

## 📁 Project Structure

```text
📦 vacation-accommodation-analysis
 ┣ 📜 Case_Study_Jean_Yves_Nkwane_Ebongue_77201393552.ipynb  # Main Jupyter Notebook
 ┣ 📜 vacation_accommodations.csv                            # Dataset
 ┣ 📜 LICENSE                                                # MIT License
 ┗ 📜 README.md                                              # Project documentation
```

---

## 🚀 Installation & Usage

To run this notebook locally on your machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Nejy190501/vacation-accommodation-analysis.git
   cd vacation-accommodation-analysis
   ```

2. **Install the required dependencies:**
   Make sure you have Python 3.10+ installed. Then run:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   *Open the `.ipynb` file in your browser and run the cells sequentially.*

---

## 👨‍💻 Author

**Jean Yves Nkwane Ebongue**
*   Data Analytics Student / Bachelor of Business Information Systems (Wirtschaftsinformatik)
*   GitHub: [@Nejy190501](https://github.com/Nejy190501)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### ⚙️ Machine Learning Pipeline & Quick Start

1. **Data Preprocessing & Cleaning**: Outlier removal, missing value imputation, logarithmic transformation for skewed price distributions.
2. **Feature Engineering**: Distance to city center/beach, room-to-guest ratios, seasonal demand encoding.
3. **Clustering & Market Segmentation**: Unsupervised segmentation identifying budget, premium, and family-oriented accommodation tiers.
4. **Predictive Modeling**: Supervised regression benchmarks evaluating feature importances for price determination.

```bash
# 1. Clone repository
git clone https://github.com/Nejy190501/vacation-accommodation-analysis.git
cd vacation-accommodation-analysis

# 2. Setup virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\\Scripts\\activate

# 3. Install requirements
pip install -r requirements.txt

# 4. Open Case Study Notebook
jupyter notebook Case_Study_Jean_Yves_Nkwane_Ebongue_77201393552.ipynb
```
