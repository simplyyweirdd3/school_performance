# School Performance and Socioeconomic Predictors

A regression-based analysis exploring how socioeconomic factors predict school-level academic performance using public education data.

Built for **DATA 5100: Foundations of Data Science** at Seattle University (Fall 2025).

---

## What It Does

This project investigates the relationship between community-level socioeconomic indicators and school academic outcomes. The central question: *how well can poverty rates, median income, and demographic composition predict a school's performance?*

**Core analysis:**
- Cleaned and merged school performance data with socioeconomic indicators
- Performed exploratory data analysis to identify key predictors
- Built and evaluated regression models to quantify relationships between community factors and academic outcomes
- Generated diagnostic visualizations to assess model fit and assumptions

---

## Data Sources

| Dataset | Description |
|---------|-------------|
| `EdGap_data.xlsx` | School-level academic performance and community demographics |
| `ccd_sch_029_1617_w_1a_11212017.csv` | Common Core of Data school characteristics |

---

## Project Structure

```
school_performance/
├── Education.ipynb                # EDA and data exploration
├── School_Performance.ipynb       # Regression modeling and analysis
├── Communicate the Results...     # Final report notebook
├── EdGap_data.xlsx                # Primary dataset
├── ccd_sch_029_1617_w_1a_11212017.csv
├── ccd_sch_029_1617_w_1a_11212017.xlsx
├── regression_coefficients.csv    # Model output
├── LICENSE.txt
├── Requirements.txt
└── README.md
```

---

## Tech Stack

- **Python** (pandas, NumPy, scikit-learn)
- **matplotlib** and **seaborn** (visualization)
- **Jupyter Notebook**

---

## Author

**Ruman Sidhu**
MS in Data Science, Seattle University
[GitHub](https://github.com/simplyyweirdd3) · [Email](mailto:rsidhu2@seattleu.edu)
