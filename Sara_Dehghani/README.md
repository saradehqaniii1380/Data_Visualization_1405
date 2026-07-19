# 🏠 Ames Housing Price Analysis & Visualization

An end-to-end data analysis and visualization project on the Ames Housing dataset, including data cleaning, exploratory data analysis (EDA), advanced visualization, and statistical modeling.

## 📖 Overview

This project analyzes the **Ames Housing Dataset**, published by Dean De Cock in 2011, containing **1,460 real house sale records** from **Ames, Iowa, USA**, between **2006 and 2010**. With **80 diverse features**, this dataset is considered one of the most comprehensive datasets in the real estate domain and serves as a modern alternative to the well-known Boston Housing dataset.

The main goal of this project is to answer the following questions through data analysis and visualization:

- Which house features have the greatest impact on sale price?
- Does location (neighborhood) play a decisive role in pricing?
- Are newer houses necessarily more expensive?
- Does the housing market show seasonal behavior?
- Can houses be meaningfully segmented based on their features?

The project includes:

- Data understanding & descriptive statistics
- Data cleaning and preprocessing (missing values, outliers, data types)
- Exploratory Data Analysis (EDA)
- More than 20 static visualizations
- Statistical modeling (Linear Regression, Decision Tree, K-Means Clustering)
- Full Persian text support in charts and report
- A one-page infographic summarizing the whole analysis

---

## 📂 Dataset Description

The dataset is stored in a CSV file (`train.csv`) accompanied by a data dictionary (`data_description.txt`) describing all 80 input features across six main groups:

| Group | Description | Example Columns |
|-------|-------------|------------------|
| **General property info** | Dwelling type, zoning, lot size/shape | `MSSubClass`, `MSZoning`, `LotArea`, `LotShape` |
| **Physical structure** | Building type, architectural style, construction year | `BldgType`, `HouseStyle`, `YearBuilt`, `RoofStyle` |
| **Quality & condition** | Overall material/finish quality and condition ratings | `OverallQual`, `OverallCond`, `ExterQual`, `KitchenQual` |
| **Areas** | Living area, basement, garage square footage | `GrLivArea`, `TotalBsmtSF`, `GarageArea` |
| **Amenities** | Bathrooms, bedrooms, fireplaces, heating, pool | `FullBath`, `Fireplaces`, `CentralAir`, `PoolArea` |
| **Sale information** | Sale date, type, and condition | `MoSold`, `YrSold`, `SaleType`, `SaleCondition` |

**Target variable:** `SalePrice` (final sale price of the property in USD)

**Summary Statistics:**
- Total records: 1,460 houses
- Input features: 80 (36 numerical, 43 categorical, 1 target)
- Price range: $34,900 – $755,000
- Median price: $163,000

---

## 🛠️ Technologies & Libraries

| Category | Libraries |
|----------|-----------|
| Data Processing | `pandas`, `numpy` |
| Persian Text Support | `arabic-reshaper`, `python-bidi` |
| Visualization | `matplotlib`, `seaborn` |
| Statistical Analysis | `scipy` |
| Machine Learning | `scikit-learn` |
| Environment | `Jupyter Notebook` (Kaggle) |

---

## 📦 Installation & Setup

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

**requirements.txt:**
```
pandas
numpy
matplotlib
seaborn
scipy
scikit-learn
arabic-reshaper
python-bidi
```

### 2. Place your data files

Ensure `train.csv` and `data_description.txt` are in the project's data directory (or update the file path in the notebook).

### 3. Run the Jupyter Notebook

```bash
jupyter notebook notebook.ipynb
```

---

## 🚀 How to Run

1. Open `notebook.ipynb` in Jupyter Notebook, VS Code, or Kaggle.
2. Run cells sequentially through the five main tasks (Data Understanding → Data Cleaning → EDA → Visualization → Modeling).
3. All charts will be displayed inline with Persian labels rendered via `arabic-reshaper` and `python-bidi`.

---

## 📊 Project Workflow

| Task | Description |
|------|-------------|
| **Task 1 – Data Understanding** | Feature introduction, descriptive statistics, missing value overview, normality checks (Q-Q Plot), boxplots by quality |
| **Task 2 – Data Cleaning** | Missing value imputation (domain-aware), IQR-based outlier removal, data type correction |
| **Task 3 – EDA** | Full descriptive statistics, numeric feature distributions, quality/area vs. price analysis, time-based trends, categorical feature effects, correlation matrix |
| **Task 4 – Visualization** | Neighborhood ranking, bubble chart (quality × year × price), violin plots (before/after cleaning), neighborhood × quality heatmap, seasonal analysis, final correlation ranking |
| **Task 5 – Statistical Modeling** | Linear Regression, Decision Tree Classifier, K-Means Clustering |

---

## 📈 Key Findings

- 🏆 **Strongest price predictor:** Overall quality (`OverallQual`), correlation **r = 0.79**
- 📐 **Living area impact:** Every 100 sq. ft. increase in `GrLivArea` adds ~$9,000 to price (r = 0.68)
- 📍 **Neighborhood effect:** Price gap of **3.1×** between the most expensive (`NridgHt`, $270K) and cheapest (`MeadowV`, $88K) neighborhoods
- 🧱 **Neighborhood price ceiling:** In cheaper neighborhoods, increasing quality up to level 6 doesn't push price above ~$154K, revealing a strong quality × location interaction effect
- 🗓️ **Seasonality:** Most sales occur in May–July; June is the peak month (240 transactions)
- 🧹 **Data cleaning impact:** 7,829 missing values resolved; 87 outlier rows (5.9%) removed; price skewness reduced from 1.88 to 0.64
- 🤖 **Model performance:**
  - Linear Regression → R² = 0.783, RMSE ≈ $25,928
  - Decision Tree Classifier (cheap/expensive) → 88.4% accuracy
  - K-Means Clustering (k=4) → identified Economic, Average, Large-without-basement, and Luxury market segments

---

## 📁 Project Structure

```
Sara_Dehghani/
│
├── Data/
│   ├── train.csv                       # Dataset
│   └── data_description.txt            # Feature dictionary
│
├── Notebook/
│   └── notebook.ipynb                  # Main Jupyter/Kaggle notebook with all code
│
├── Report/
│   └── Final_Report.pdf                # Full Persian project report
│
├── Infographic/
│   └── infographic.png                 # One-page visual summary
│
└── README.md
```

---

## 📝 Report

A comprehensive **PDF report** (in Persian) is included in the repository, containing:

- Dataset description and variable groups
- Data cleaning methodology and justification
- Full exploratory data analysis with purpose / findings / interpretation for each step
- Visualization methods and insights
- Statistical modeling results
- Final conclusions

---

## 🧠 Future Work

- Apply **log-transformation** more broadly across skewed numerical features for improved model performance
- Use **advanced ML models** (Random Forest, Gradient Boosting) to better capture interaction effects (e.g., quality × neighborhood)
- Add **spatial/geolocation analysis** for neighborhood-level insights
- Build an **interactive dashboard** (Streamlit / Plotly Dash) for exploring price drivers
- Perform **feature engineering** (e.g., house age, total finished area) to boost predictive power

---

**Happy Analyzing! 🚀**

---

## 👩 Author

**Sara Dehghani │ Data Visualization Course Project – Spring 1405**

Instructor: Dr. Omid Karimi

Data Analysis • Python • Data Visualization

Kaggle Project:
https://www.kaggle.com/code/saradehqani/notebook7d0dd672ee

---

> **Note:** Update the `font_path` variable in the Persian text rendering section according to the location of your Persian font, if required.
