# 🛒 Supermarket Sales — Exploratory Data Analysis

A focused exploratory data analysis (EDA) project on 1,000 supermarket transactions across three cities in Myanmar (January–March 2019). The goal is to uncover sales patterns, revenue distribution, customer behavior, and product line performance through visual analysis.

---

## 📊 Dataset

- **Source:** [Kaggle — Supermarket Sales](https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales)
- **Size:** 1,000 transactions × 17 columns
- **Period:** January 2019 – March 2019
- **No missing values**

**Key columns:**

| Column | Description |
|---|---|
| `City` | Yangon (340) / Mandalay (332) / Naypyitaw (328) |
| `Product line` | 6 categories: Fashion accessories, Food & beverages, Electronic accessories, Sports & travel, Home & lifestyle, Health & beauty |
| `Customer type` | Member (501) / Normal (499) |
| `Gender` | Female (501) / Male (499) |
| `Payment` | Ewallet (345) / Cash (344) / Credit card (311) |
| `Total` | Transaction total ($10.68 – $1,042.65, mean $322.97) |
| `gross income` | Gross income per transaction |
| `Rating` | Customer satisfaction rating |

---

## 🔍 Project Pipeline

### 1. EDA — Initial Inspection
- Shape, dtypes, descriptive statistics
- Duplicate and null check (dataset is clean)
- Correlation heatmap across all numerical features

### 2. Feature Engineering
- Dropped non-analytical columns: `Invoice ID`, `Tax 5%`, `gross margin percentage`, `Time`, `Branch`, `cogs`
- Parsed `Date` into year, month, day, day-of-week, and weekday name

### 3. Numerical Feature Distribution & City Comparison
- For every numerical column: side-by-side histogram (with KDE) and boxplot split by City
- Reveals distribution shape and city-level differences in Unit Price, Quantity, Total, Rating, and Gross Income

### 4. Categorical Feature Analysis by Gender
- 2×3 subplot grid showing total sales per category for every categorical feature, split by Gender
- Covers: City, Customer type, Product line, Payment method, Spending Score
- Shared legend for clean presentation

### 5. City-Level Revenue Analysis
- Total spending per city with percentage annotations
- Total spending per city broken down by gender with in-bar percentage labels
- Gross income per city with percentage breakdown
- Gross income by month and by weekday

### 6. Product Line Analysis
- Stacked bar chart: count of each product line per city
- Total rating per product line

### 7. Customer Type Analysis
- Total sales by customer type (Member vs Normal)
- Customer type count distribution bar chart

---

## 📁 Project Structure

```
supermarket-sales-EDA/
│
├── supermarket_sale-EDA.ipynb               # Main notebook
├── supermarket_sales_-_Sheet1.csv           # Dataset
└── README.md
```

---

## ▶️ How to Run

1. Clone the repository
```bash
git clone https://github.com/your-username/supermarket-sales-EDA.git
```

2. Install the required libraries
```bash
pip install pandas numpy matplotlib seaborn
```

3. Open the notebook in Jupyter
```bash
jupyter notebook supermarket_sale-EDA.ipynb
```

4. Make sure `supermarket_sales_- Sheet1.csv` is in the same folder as the notebook, then run all cells

---

## 📦 Libraries Used

| Library | Purpose |
|---|---|
| `pandas` / `numpy` | Data loading and manipulation |
| `matplotlib` / `seaborn` | All visualizations |

---

## 💡 Key Findings

- **Revenue is nearly equal across all three cities** — Yangon, Mandalay, and Naypyitaw each account for roughly one-third of total sales, suggesting consistent performance across branches
- **Gender split is almost perfectly even** (50.1% Female / 49.9% Male) with similar spending patterns, though product line preferences vary slightly
- **Fashion accessories and Food & beverages** are the top-selling product lines by transaction count
- **Member and Normal customers** contribute nearly identical transaction volumes, suggesting the membership program does not significantly drive more frequent purchases
- **Payment methods are evenly distributed** — Ewallet, Cash, and Credit card each account for roughly one-third of transactions, indicating no dominant preference
- **Gross income by weekday and month** reveals temporal patterns useful for staffing and restocking decisions

---

## 👤 Author

**Khaled Abdulaziz**
