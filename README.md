# Automobile Sales Recession Analysis

[![Python](https://img.shields.io/badge/Python-3.x-blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-teal)](https://seaborn.pydata.org/)
[![IBM Course](https://img.shields.io/badge/IBM-DV0101EN-052FAD)](https://www.coursera.org/learn/python-for-data-visualization)

> Exploring how automobile sales were impacted during historical recession periods using Python data visualization libraries.

---

## Overview

This project analyzes the **XYZAutomotives** automobile sales dataset, covering sales from **1980 to 2023** across six major recession periods. The analysis walks through a complete data visualization workflow using Matplotlib, Seaborn, and Folium.

**Recession periods studied:**
- 1980 recession
- 1981–1982 recession
- 1991 recession
- 2000–2001 dot-com bust
- 2007–2009 global financial crisis
- 2020 COVID-19 pandemic (Feb–Apr)

---

## Dataset

The dataset contains monthly automobile sales data with the following features:

| Column | Description |
|---|---|
| `Automobile_Sales` | Number of vehicles sold |
| `Recession` | Binary flag (1 = recession, 0 = normal) |
| `GDP` | Per capita GDP (USD) |
| `Unemployment_Rate` | Monthly unemployment rate |
| `Consumer_Confidence` | Synthetic consumer confidence index |
| `Seasonality_Weight` | Seasonal effect on sales |
| `Price` | Average vehicle price |
| `Advertising_Expenditure` | Company ad spend |
| `Vehicle_Type` | Supperminicar, Smallfamilycar, Mediumfamilycar, Executivecar, Sports |

---

## Visualizations

| Task | Chart Type | Description |
|---|---|---|
| 1.1 | Line chart | Avg automobile sales by year with recession annotations |
| 1.2 | Dual line chart | Advertising expenditure vs sales (non-recession) |
| 1.3 | Bar charts | Vehicle-wise sales: recession vs non-recession |
| 1.4 | Subplots | GDP variation during recession vs non-recession |
| 1.5 | Bubble plot | Seasonality impact on automobile sales |
| 1.6 | Scatter plots | Consumer confidence & price vs sales during recessions |
| 1.7 | Pie chart | Ad expenditure split: recession vs non-recession |
| 1.8 | Pie chart | Ad expenditure share by vehicle type during recessions |
| 1.9 | Line plot | Unemployment rate effect on vehicle type sales |
| 1.10 | Folium choropleth | Highest sales regions during recession (optional, JupyterLite) |

---

## Key Findings

- Automobile sales drop significantly (~50%) during all recession periods.
- **Executivecar** and **Sports** vehicles are the hardest hit — consumers cut premium purchases first.
- Advertising budgets are slashed during recessions; the company focuses spend on budget vehicles.
- Higher consumer confidence and lower vehicle prices correlate with stronger sales during downturns.
- Seasonality peaks in **April** and **December** regardless of economic cycle.

---

## Getting Started

```bash
git clone https://github.com/YOUR_USERNAME/automobile-sales-recession-analysis.git
cd automobile-sales-recession-analysis
pip install -r requirements.txt
jupyter notebook DV0101EN_Solved.ipynb
```

---

## Tech Stack

- Python 3.x
- pandas, NumPy
- Matplotlib, Seaborn
- Folium (Task 1.10, JupyterLite only)

---

## Course

This project is part of the [IBM Data Visualization with Python](https://www.coursera.org/learn/python-for-data-visualization) course on Coursera (DV0101EN).

---

## License

© IBM Corporation 2023. Dataset and lab structure used for educational purposes.
