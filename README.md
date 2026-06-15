# 🛒 Blinkit Sales Data Analysis


A Python-based exploratory data analysis (EDA) project on Blinkit's grocery sales dataset. This project uncovers insights about product performance, outlet efficiency, customer ratings, and sales trends across different locations and store types.

---

## 📌 Objective

To analyze Blinkit's retail sales data and extract meaningful insights about:
- Which item types generate the highest revenue
- How outlet size, type, and location affect sales
- The relationship between item visibility and sales
- Customer rating distribution across products and outlets
- Fat content preferences among customers

---

## 📂 Dataset Overview

| Feature | Details |
|--------|---------|
| **File** | `blinkit_data.csv` |
| **Rows** | 8,523 entries |
| **Columns** | 12 features |
| **Source** | Blinkit grocery retail data |

### 🔑 Key Columns

| Column | Description |
|--------|-------------|
| `Item Fat Content` | Low Fat / Regular |
| `Item Identifier` | Unique product ID (1,559 unique items) |
| `Item Type` | Category of product (16 types) |
| `Outlet Establishment Year` | Year outlet was set up (1998–2022) |
| `Outlet Identifier` | Unique outlet ID (10 outlets) |
| `Outlet Location Type` | Tier 1 / Tier 2 / Tier 3 city |
| `Outlet Size` | Small / Medium / High |
| `Outlet Type` | Grocery Store / Supermarket Type 1/2/3 |
| `Item Visibility` | Display visibility score of the product |
| `Item Weight` | Weight of the item (missing in 1,463 rows) |
| `Sales` | Item sales value (₹31 – ₹267) |
| `Rating` | Customer rating (1.0 – 5.0) |

---

## 🛠️ Libraries Used

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## 🔍 Analysis Performed

### 1. Data Loading & Inspection
- Loaded dataset using `pd.read_csv()`
- Previewed data with `data.head()`
- Checked shape: **(8523, 12)**
- Reviewed column names, data types, and null values via `data.info()` and `data.describe()`

### 2. Data Quality Checks
- Identified missing values in `Item Weight` (1,463 nulls)
- Checked unique value counts across categorical columns
- Detected inconsistent labels in `Item Fat Content` (e.g., `"low fat"`, `"LF"` alongside `"Low Fat"`)

### 3. Business Requirements & Chart Analysis

#### 📊 Chart 1 — Total Sales by Fat Content
- **Objective:** Analyze the impact of fat content on total sales
- **Additional KPIs:** Average Sales, Number of Items, Average Rating by fat content
- **Chart Type:** Donut Chart

#### 📊 Chart 2 — Total Sales by Item Type
- **Objective:** Identify the performance of different item types in terms of total sales
- **Additional KPIs:** Average Sales, Number of Items, Average Rating by item type
- **Chart Type:** Bar Chart

#### 📊 Chart 3 — Fat Content by Outlet for Total Sales
- **Objective:** Compare total sales across different outlets segmented by fat content
- **Additional KPIs:** Average Sales, Number of Items, Average Rating per outlet by fat content
- **Chart Type:** Stacked Column Chart

#### 📊 Chart 4 — Total Sales by Outlet Establishment
- **Objective:** Evaluate how the age or type of outlet establishment influences total sales
- **Chart Type:** Line Chart

#### 📊 Chart 5 — Sales by Outlet Size
- **Objective:** Analyze the correlation between outlet size and total sales
- **Chart Type:** Donut / Pie Chart

#### 📊 Chart 6 — Sales by Outlet Location
- **Objective:** Assess the geographic distribution of sales across different locations (Tier 1 / Tier 2 / Tier 3)
- **Chart Type:** Funnel Map

---

## 📊 Key Findings

- **Low Fat** items outsell Regular items, showing a strong customer preference for healthier options
- **Fruits & Vegetables** and **Snack Foods** are the top-performing item types by total sales
- **Tier 3 city** outlets generate surprisingly competitive sales compared to Tier 1 locations
- **Medium-sized outlets** contribute the most to overall sales among all outlet sizes
- Outlets established in **earlier years (1998–2004)** have accumulated higher cumulative sales due to longer market presence
- **Supermarket Type 1** is the dominant outlet format driving the majority of revenue
- Average customer rating across all products is approximately **4.0**, reflecting good satisfaction levels
- Fat content distribution across outlets (stacked view) reveals Low Fat items are consistently dominant in most store types

---

## 🗂️ Project Structure

```
Blinkit-Analysis/
│
├── Blinkit_Analysis.ipynb    # Main Jupyter Notebook with full analysis
├── blinkit_data.csv          # Raw dataset
└── README.md                 # Project documentation (this file)
```

---

## ▶️ How to Run

### Option 1: Google Colab (Recommended)
1. Upload `Blinkit_Analysis.ipynb` to [Google Colab](https://colab.research.google.com/)
2. Upload `blinkit_data.csv` to the Colab session files
3. Update the file path in the notebook:
   ```python
   data = pd.read_csv("/content/blinkit_data.csv")
   ```
4. Run all cells (`Runtime > Run all`)

### Option 2: Local Jupyter Notebook
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/Blinkit-Analysis.git
   cd Blinkit-Analysis
   ```
2. Install required libraries:
   ```bash
   pip install numpy pandas matplotlib seaborn
   ```
3. Launch Jupyter:
   ```bash
   jupyter notebook Blinkit_Analysis.ipynb
   ```

---

## 📈 Sample Visualizations

> Charts are generated inside the notebook using Matplotlib and Seaborn, covering bar plots, histograms, scatter plots, and count plots for all major KPIs.

---

## 🙋 About

This is a beginner-to-intermediate level **Data Analysis project** built using Python. It demonstrates the core EDA workflow:
**Data Loading → Inspection → Cleaning → Visualization → Insights**

---

## 📬 Connect

Feel free to reach out or connect if you'd like to discuss this project!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://linkedin.com/in/vishwanath-hubballi-000056375)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/vish68249-debug)
