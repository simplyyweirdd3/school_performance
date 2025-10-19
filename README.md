## School Performance and Socioeconomic Predictors



\## Overview

This project analyzes how socioeconomic factors relate to school-level academic performance across the United States.  

Using data from the \*\*EdGap\*\* and \*\*Common Core of Data (CCD)\*\* datasets, we estimate how socioeconomic status (SES)—proxied by the percentage of students receiving free or reduced-price lunch—predicts average ACT scores.



\## Data Sources

\- \*\*EdGap\_data.xlsx:\*\* Contains socioeconomic indicators such as unemployment rate, adult education level, and median household income at the county level.  

\- \*\*ccd\_sch\_029\_1617\_w\_1a\_11212017.xlsx:\*\* Common Core of Data file with school-level identifiers and characteristics.  

\- These datasets were merged on the unique `NCESSCH` school ID.



\## Methods

1\. Clean and merge the two datasets.  

2\. Create a `ses\_index` variable (negative of the percent free/reduced lunch so higher = wealthier).  

3\. Explore the data (EDA): histograms, scatterplots.  

4\. Fit OLS regression with robust (HC1) standard errors.  

5\. Run diagnostics (Q–Q plot, residuals vs. fitted, Cook’s D, VIF).  

6\. Conduct sensitivity checks:  

&nbsp;  - Add state fixed effects.  

&nbsp;  - Remove influential observations.  

7\. Export cleaned data and regression results for reproducibility.



\## Key Findings

\- \*\*SES coefficient:\*\* ≈ 8.30 (p < 0.001) — a 10 percentage-point increase in SES is associated with about +0.83 points in average ACT score.  

\- Adjusted R² ≈ 0.605 indicating that SES explains roughly 60 % of ACT variation across schools.  

\- Results remain positive and significant after state fixed effects and outlier removal.



\## Files

| File | Description |

|------|--------------|

| `School\_Performance.ipynb` | Main Jupyter notebook with data cleaning, EDA, modeling, diagnostics, and sensitivity checks. |

| `cleaned\_edgap\_ccd.csv` | Final cleaned dataset used in the analysis. |

| `regression\_coefficients.csv` | Exported regression table with coefficients and robust SEs. |

| `README.md` | This documentation file. |



\## How to Reproduce

1\. Open `School\_Performance.ipynb` in Jupyter or VS Code.  

2\. Ensure the following packages are installed:  

