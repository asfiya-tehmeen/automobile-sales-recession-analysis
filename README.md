# Analyzing the Impact of Recession on Automobile Sales

A two-part data analytics project for **XYZAutomotives**, exploring how economic recessions have historically affected automobile sales, and presenting the findings through static visualizations and an interactive dashboard.

> Final Assignment — *IBM Data Visualization with Python (DV0101EN)*

---

## 📌 Project Overview

XYZAutomotives wants to understand how its sales have been impacted during past recession periods, and give its directors an easy way to explore the data themselves. This project is split into two parts:

| Part | Notebook | Tools | Goal |
|------|----------|-------|------|
| **Part 1** | `Final_Assignment_Part1_Create_Visualizations_using_Matplotlib_Seaborn_Folium.ipynb` | Matplotlib, Seaborn, Folium | Static exploratory visualizations and insights |
| **Part 2** | `Final_Assignment_Part2_Create_Dashboard_Plotly_Dash.ipynb` | Plotly, Dash | Interactive dashboard for directors to drill into the data |

### Recession periods covered
| Period | Years |
|--------|-------|
| 1 | 1980 |
| 2 | 1981 – 1982 |
| 3 | 1991 |
| 4 | 2000 – 2001 |
| 5 | Late 2007 – mid 2009 |
| 6 | Feb – Apr 2020 (COVID-19) |

### Dataset
A synthetically generated dataset (for educational purposes only) with the following fields:

- `Date`, `Month`, `Year` — time of observation
- `Recession` — binary flag (1 = recession, 0 = normal)
- `Automobile_Sales` — number of vehicles sold
- `GDP`, `Unemployment_Rate`, `Consumer_Confidence` — macroeconomic indicators
- `Seasonality_Weight` — seasonal effect on sales
- `Price`, `Advertising_Expenditure` — sales/marketing factors
- `Vehicle_Type` — Supperminicar, Smallfamilycar, Mediumfamilycar, Executivecar, Sports
- `Competition` — market competitiveness measure

---

## 📊 Part 1 — Visualizations (Matplotlib, Seaborn, Folium)

Exploratory analysis answering questions such as:

- How do automobile sales trend over time during recession vs. non-recession periods?
- Which vehicle types are hit hardest during recessions?
- How does GDP behave during downturns vs. stable periods?
- What's the effect of seasonality on monthly sales?
- How do consumer confidence and pricing relate to sales during recessions?
- How does advertising expenditure change during recessions, and how is it allocated across vehicle types?
- How sensitive is each vehicle type to rising unemployment?

**Key insights:**
- Automobile sales drop sharply during recessions, with **Executivecar** and **Sports** (premium segments) hit hardest as consumers cut discretionary spending first.
- GDP is lower and more volatile during recessions; consumer confidence drops, and that decline correlates strongly with falling sales.
- XYZAutomotives historically cuts advertising budgets during recessions and shifts spend toward affordable vehicle types (Supperminicar, Smallfamilycar) — a budget-conscious strategy.
- Sales show moderate seasonality, typically spiking in **April** and **December**.
- Lower-priced, smaller vehicle types show the highest sales volatility relative to unemployment swings.

## 📈 Part 2 — Interactive Dashboard (Plotly & Dash)

A Dash web application that lets the directors interactively explore the same data:

- **Select Statistics** dropdown — switch between:
  - **Recession Period Statistics** — sales trends, vehicle-type breakdowns, advertising spend, and unemployment effects *during recessions only*
  - **Yearly Statistics** — sales trends and breakdowns for *any specific year* selected from the data
- **Select Year** dropdown — enabled only when "Yearly Statistics" is selected, letting directors drill into a particular year
- Each report renders **4 charts** (line, bar, and pie charts) inside a responsive output container that updates live via Dash callbacks — no need to request new plots manually.

---

## 🛠️ Requirements

```bash
pip install pandas numpy matplotlib seaborn folium plotly dash
```

| Library | Used in |
|---|---|
| `pandas`, `numpy` | Both parts — data loading & wrangling |
| `matplotlib`, `seaborn` | Part 1 — static charts |
| `folium` | Part 1 — geospatial visualization |
| `plotly` | Part 2 — interactive charts |
| `dash` | Part 2 — dashboard application |

---

## ▶️ How to Run

### Part 1
Open `Final_Assignment_Part1_Create_Visualizations_using_Matplotlib_Seaborn_Folium.ipynb` in Jupyter Notebook/Lab, Google Colab, or VS Code, and run all cells in order. Charts render inline in the notebook.

### Part 2
Open `Final_Assignment_Part2_Create_Dashboard_Plotly_Dash.ipynb` and run all cells in order.

- **Local Jupyter / VS Code:** the final cell starts a local server. Open the printed link, e.g. `http://127.0.0.1:8050/`, in your browser.
- **Google Colab:** `127.0.0.1` won't work since Colab runs remotely. Use Colab's port-forwarding instead:
  ```python
  import threading, time
  from google.colab import output

  def run_app():
      app.run(debug=False, port=8050)

  threading.Thread(target=run_app).start()
  time.sleep(3)
  output.serve_kernel_port_as_iframe(8050, height=900)
  ```
  This renders the dashboard directly inside the notebook as an iframe.

---

## 📁 Repository Structure

```
.
├── Final_Assignment_Part1_Create_Visualizations_using_Matplotlib_Seaborn_Folium.ipynb
├── Final_Assignment_Part2_Create_Dashboard_Plotly_Dash.ipynb
└── README.md
```

---

## 📄 License / Disclaimer

The dataset used in this project is artificially generated for educational purposes only and does not represent real sales data from any company.
