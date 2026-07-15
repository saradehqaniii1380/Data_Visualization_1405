# 🎬 Cinema Sales Data Analysis & Visualization

An end-to-end data analysis and visualization project on cinema ticket sales data, including data cleaning, exploratory data analysis (EDA), statistical modeling, and interactive visualizations.

## 📖 Overview

This project analyzes a cinema sales dataset containing **3,000 ticket records** across **55 cinemas**, **32 movies**, and **949 unique customers**. The goal is to uncover key patterns in sales performance, customer behavior, cinema efficiency, and gender-based preferences using Python data science libraries.

The project includes:

- Data loading & preprocessing
- Exploratory Data Analysis (EDA)
- Statistical summary & descriptive analytics
- 20+ visualization charts (Bar, Line, Pie, Donut, Boxplot, Histogram, Heatmap, WordCloud, Bubble, Scatter, etc.)
- Interactive visualization using **Bokeh**
- Full Persian text support for visualizations

---

## 📂 Dataset Description

The dataset is stored in an Excel file (`Cinema-data.xlsx`) containing 4 sheets:

| Sheet | Description | Columns |
|-------|-------------|---------|
| **Film** | Movie information | Film ID, Film Name, Release Date |
| **Customer** | Customer details | National ID, Gender, Last Name |
| **Cinema** | Cinema details | Cinema Name, Build Year, Number of Halls, Capacity, Cinema Type, Address, Phone |
| **Ticket** | Ticket sales records | Ticket Number, National ID, Film Name, Cinema Name, Cinema Type |

**Summary Statistics:**
- Total Tickets: 3,000
- Unique Films: 32
- Unique Cinemas: 55
- Unique Customers: 949
- Average Tickets per Customer: 3.16

---

## 🛠️ Technologies & Libraries

| Category | Libraries |
|----------|-----------|
| Data Processing | `pandas`, `numpy` |
| Visualization | `matplotlib`, `seaborn`, `wordcloud`, `bokeh` |
| Machine Learning | `scikit-learn` (Linear Regression, KMeans, PCA, StandardScaler) |
| Persian Text Support | `arabic-reshaper`, `python-bidi` |
| Environment | `Jupyter Notebook` |

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
arabic-reshaper
python-bidi
wordcloud
bokeh
scikit-learn
openpyxl
```

### 2. Place your data file

Ensure `Cinema-data.xlsx` is in the project root directory (or update the file path in the notebook).

### 3. Run the Jupyter Notebook

```bash
jupyter notebook Cinema_Analysis.ipynb
```

---

## 🚀 How to Run

1. Open `Cinema_Analysis.ipynb` in Jupyter Notebook or VS Code.
2. Run cells sequentially from **Section 1** to **Section 31**.
3. All charts will be displayed inline.
4. The Bokeh interactive chart will open in your browser as `film_sales_scatter.html`.

---

## 📊 Visualizations Overview

| Chart Type | Count | Purpose |
|------------|-------|---------|
| Bar Charts | 4 | Top movies, top cinemas, sales by cinema type, efficient cinemas |
| Line Charts | 4 | Sales ranking, release date trend, cinema type comparison, build year trend |
| Pie/Donut Charts | 4 | Gender distribution, top 6 movies, top 10 cinemas, customer loyalty |
| Distribution Plots | 3 | Histogram (customer purchases), Boxplots (gender & cinema type) |
| Heatmap | 1 | Correlation between build year, halls, capacity |
| Scatter / JointPlot | 2 | Capacity vs sales, with regression line |
| WordCloud | 1 | Movie popularity visualization |
| Bubble Chart | 1 | Gender-based movie sales comparison |
| Interactive Bokeh | 1 | Hover, zoom, pan, save features |
| Regression Model | 1 | Multiple Linear Regression with feature importance |

---

## 📈 Key Findings

- 🏆 **Top Movie:** "Ghahreman" (118 tickets)
- 🏆 **Top Cinema:** "Cinema 6D Park Police" (75 tickets)
- 💡 **Most Efficient Cinema:** "Azadi Cinema" (98% occupancy rate – 50/51 seats)
- 👫 **Gender Distribution:** 51.5% Female, 48.5% Male (balanced)
- ❤️ **Customer Loyalty:** Only 10% of customers visited more than 5 times
- 🎬 **Cinema Type Sales Share:** Conventional (55%), Premium (27.5%), Multi-Dimensional (17.6%)
- 📊 **Correlation:** Strong correlation (0.66) between number of halls and capacity; weak correlation with build year
- 🔍 **Regression Insights:** Capacity and number of halls are the strongest predictors of sales

## 📁 Project Structure

```
cinema-sales-analysis/
│
├── Cinema_Analysis.ipynb       # Main Jupyter Notebook with all code
├── Cinema-data.xlsx            # Dataset (not included in repo)
├── film_sales_scatter.html     # Bokeh interactive chart output
├── README.md                   # Project documentation
│
└── report/                     # PDF report
    └── Analysis_Report.pdf
```

---

## 📝 Report

A comprehensive **PDF report** is included in the repository, containing:

- Dataset description
- Data preprocessing steps
- Exploratory Data Analysis (EDA)
- Visualization methods & explanations
- Interpretation of findings
- Conclusions 

---

## 🧠 Future Work

- Add **purchase date** column to enable time-series analysis
- Incorporate **geolocation** data for spatial analysis (heatmaps on maps)
- Collect **demographic data** (age, occupation, income) for deeper customer segmentation
- Build a **dashboard** using Streamlit or Dash for real-time analytics
- Apply **advanced ML models** (Random Forest, XGBoost) for sales prediction


---

**Happy Analyzing! 🚀**

---

> **Note:** To run the WordCloud and Persian text visualizations, you need a Persian font installed on your system (e.g., `Vazir.ttf`). Update the `font_path` in Section 12 accordingly.
