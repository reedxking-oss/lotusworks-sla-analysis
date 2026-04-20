# Lotusworks SLA Analysis
## Operational Equipment Commissioning — Past Due Tracking

End-to-end analysis of commissioning tag data from an active facility operations 
project. Built to identify SLA compliance patterns and track equipment items that 
missed their Blue Tag deadline each month.

> All equipment IDs have been anonymized. Facility and project identifiers removed 
> for confidentiality.

---

## Key Findings

- **3,124 unique equipment units** analyzed across the commissioning project
- **61.4% completed On Time** within the 5 business day SLA window
- **38% completed Late** — commissioned but after the deadline
- **16 items currently Past Due** — Green tagged but Blue tag not yet received
- **April 2025 was the peak month** with the highest concentration of past due items
- 5 data quality anomalies identified and removed during cleaning

---

## How It Works

Each equipment unit goes through two commissioning checkpoints:

- **Green Tag** — passes initial inspection
- **Blue Tag** — fully commissioned and complete
- **Deadline** — Green Tag date + 5 business days
- **SLA Status** — On Time, Late, Past Due, or N/A

The Python script rebuilds this SLA logic from the raw tag log, mirrors the 
original Excel analysis, and produces an interactive Plotly chart.

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Python (pandas) | Data cleaning and SLA logic |
| Plotly | Interactive bar chart |
| Excel | Raw data source and original analysis |

---

## Files

| File | Description |
|------|-------------|
| `lotusworks_sla_analysis.ipynb` | Full analysis notebook |
| `past_due_project.xlsx` | Anonymized raw tag data |
| `sla_summary.csv` | One row per equipment with SLA status |
| `past_due_by_month.csv` | Monthly past due count summary |
| `past_due_by_month.html` | Interactive Plotly chart |

---

## Background

This project came out of real operational work tracking commissioning progress 
across thousands of equipment units at a semiconductor facility. The analysis 
was originally built in Excel — this Python version automates the same logic 
and makes it reproducible and version controlled.
