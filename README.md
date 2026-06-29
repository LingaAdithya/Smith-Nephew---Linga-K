# SIOP Forecast Analytics Dashboard

An interactive **Power BI dashboard** developed for a Sales, Inventory & Operations Planning (SIOP) case study. The dashboard enables business users to compare forecast snapshots across planning cycles, evaluate forecast performance, and analyze forecast revisions using executive-level KPIs and visualizations.

---

## Problem Statement

Organizations generate multiple forecast snapshots every planning cycle. Business users need the ability to compare these snapshots to understand:

* How forecasts evolve over time
* Forecast accuracy against actual performance
* Forecast bias (over/under forecasting)
* Country-level forecast trends
* Revenue, Non-Revenue, and CAPEX planning performance

This project transforms raw forecast snapshots into an interactive analytical dashboard to support SIOP decision-making.

---

## Features

### Executive KPIs

* Revenue Forecast
* Non-Revenue Forecast
* CAPEX Forecast
* Actual Revenue
* Forecast Accuracy %
* Forecast Bias %

### Interactive Visualizations

* Revenue Forecast by Country
* Non-Revenue Forecast by Country
* CAPEX Forecast by Country
* Forecast Revision Analysis (Resultant vs Lag 0)
* Forecast Accuracy Trend by Period
* Revenue Revision Table
* Bias Status Indicator

### Interactive Filters

* Lag Selection

  * Resultant
  * Lag 0
  * Lag 1
* Forecast Period Selection

---

## Dataset

The project uses two datasets:

### Forecast

Contains monthly forecast snapshots with:

* Country
* As Of Period
* Forecast Period
* Revenue Forecast
* Non-Revenue Forecast
* CAPEX Forecast

### Actual

Contains realized business values:

* Country
* Period
* Actual Revenue
* Actual Non-Revenue
* Actual CAPEX

---

## Data Modeling

The solution was developed using a star-schema-inspired approach.

### Tables

* Forecast
* Actual
* Snapshot Reference
* Lag Selection
* Country/Period Dimension

Key transformations include:

* Snapshot classification into Resultant, Lag 0, and Lag 1
* CountryPeriod key creation
* Dynamic relationships between forecast and actual datasets
* Interactive lag selection using DAX measures

---

## KPIs

### Forecast Accuracy

```text
Forecast Accuracy = 1 − |Forecast − Actual| / Actual
```

Measures how closely forecast values align with actual performance.

---

### Forecast Bias

```text
Forecast Bias = (Forecast − Actual) / Actual
```

Indicates whether forecasts overestimate or underestimate actual values.

* Positive → Over-forecast
* Negative → Under-forecast

---

## Dashboard Highlights

* Compare multiple forecast snapshots side-by-side
* Analyze forecast revisions across planning cycles
* Monitor country-wise forecast performance
* Track forecast accuracy trends
* Evaluate forecast bias using visual indicators
* Executive-friendly interactive reporting

---

## Tools & Technologies

* **Power BI Desktop**
* **Power Query**
* **DAX**
* **Microsoft Excel**

---

## Repository Structure

```text
.
├── Dashboard.pbix
├── Dataset/
│   ├── Forecast.xlsx
│   └── Actual.xlsx
├── Screenshots/
│   └── dashboard.png
└── README.md
```

---

## Key Business Insights

The dashboard enables planners to:

* Compare successive forecast snapshots
* Measure forecast quality using Accuracy and Bias KPIs
* Identify significant forecast revisions
* Analyze country-level planning performance
* Support monthly SIOP review meetings with actionable insights

---

## Future Enhancements

* Forecast vs Actual variance waterfall
* Automated anomaly detection
* Time intelligence (YoY / MoM trends)
* Drill-through reports
* Power BI Service deployment with scheduled refresh
* Row-Level Security (RLS)

---

## Dashboard Preview
<img width="2004" height="1132" alt="image" src="https://github.com/user-attachments/assets/bbbb9bee-191b-454e-b807-433e54612e6f" />


## Author

**Linga Adithya K**

