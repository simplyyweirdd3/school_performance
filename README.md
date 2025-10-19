# School Performance and Socioeconomic Predictors

## Project Overview
This project analyzes how socioeconomic conditions relate to school-level academic performance in the United States.  
We merge school-level data (Common Core of Data, CCD) with socioeconomic indicators (EdGap) and estimate the association between socioeconomic status (SES) and average ACT scores. Key finding: higher community SES (lower share of free/reduced lunch) is strongly associated with higher school-level ACT averages (baseline coefficient ≈ 8.30, adj. R² ≈ 0.605).

## Data
- **Common Core of Data (CCD)** — school-level data (Nonfiscal files). Source: National Center for Education Statistics (NCES). See data files & documentation. :contentReference[oaicite:1]{index=1}  
  Link: https://nces.ed.gov/ccd/ccddata.asp.  
- **EdGap** — socioeconomic and ACT/SAT mapping dataset used to derive SES variables and ACT averages. :contentReference[oaicite:2]{index=2}  
  Link: https://www.edgap.org/

<<<<<<< HEAD
Using data from the *EdGap* and *Common Core of Data (CCD)* datasets, we estimate how socioeconomic status (SES)-proxied by the percentage of students receiving free or reduced-price lunch predicts average ACT scores.
=======
**Local/additional files included in this repository**
- `EdGap_data.xlsx` (provided)  
- `ccd_sch_029_1617_w_1a_11212017.xlsx` (provided)  
- `Hospital_General_Information_Dataset.csv` (contextual dataset)  
- `2020-Census-Disclosure-Avoidance-System-Detailed-Summary-Metrics_Dataset.xlsx` (contextual dataset)

## Analysis 
Major steps and where to find the code:
1. **Data loading & cleaning** — `School_Performance.ipynb` (cells near the top): loads CCD and EdGap, normalizes column names, and converts NCESSCH to a common key.  
2. **Feature engineering** — create `ses_index` from percent free/reduced lunch (ses_index = - pct_free_lunch so higher = wealthier).  
3. **Exploratory Data Analysis (EDA)** — histogram of `avg_act`, scatterplot of `ses_index` vs `avg_act`. (See the EDA cells in the notebook).  
4. **Modeling** — OLS regression: `avg_act ~ ses_index` with HC1 robust SEs. See `School_Performance.ipynb` (Results section).  
5. **Diagnostics & robustness** — Q–Q plot, residuals vs fitted, Cook’s D, VIF; sensitivity checks: state fixed effects, exclusion of high Cook’s-D observations.  
6. **Exports** — `cleaned_edgap_ccd.csv` and `regression_coefficients.csv` were produced by the notebook for reproducibility.

## Results
- Baseline OLS: `ses_index` coefficient ≈ **8.2958** (robust SE ≈ 0.086, p < 0.001).  
- Adjusted R² ≈ **0.605** (the model explains ~60.5% of variation in school-level average ACT in the sample).  
- Sensitivity: coefficient remains positive and significant with state fixed effects and after excluding influential observations; magnitude changed modestly (≈ +3.4% when influential observations removed).

## Files in this repository
- `School_Performance.ipynb` — Jupyter notebook with full analysis, plots, and diagnostics.  
- `regression_coefficients.csv` — exported regression table.  
- `Communicate the Results - Ruman Sidhu.docx` — final written report (Communicate the Results).  
- `EdGap_data.xlsx`, `ccd_sch_029_1617_w_1a_11212017.xlsx` — original datasets used.  
- `Hospital_General_Information_Dataset.csv`, `2020-Census-Disclosure-Avoidance-System-...xlsx` — contextual datasets.  
- `requirements.txt` — software requirements.  
- `LICENSE` — licensing information.

## Author
Ruman Sidhu — Seattle University, DATA 5100 02 (Fall 2025)  
>>>>>>> d6114d9 (Updated README with final sections and links per rubric)


## License
This repository is shared under the MIT License. See `LICENSE` for details.

<<<<<<< HEAD
# Data Sources

*EdGap\_data.xlsx:* Contains socioeconomic indicators such as unemployment rate, adult education level, and median household income at the county level.  

*ccd\_sch\_029\_1617\_w\_1a\_11212017.xlsx:* Common Core of Data file with school-level identifiers and characteristics.  
These datasets were merged on the unique `NCESSCH` school ID.



## Methods

1 Clean and merge the two datasets.  

2 Create a *ses\_index* variable (negative of the percent free/reduced lunch so higher = wealthier).  

3 Explore the data (EDA): histograms, scatterplots.  

4 Fit OLS regression with robust (HC1) standard errors.  

5 Run diagnostics (Q–Q plot, residuals vs. fitted, Cook’s D, VIF).  

6 Conduct sensitivity checks:  

&nbsp;  - Add state fixed effects.  

&nbsp;  - Remove influential observations.  

7 Export cleaned data and regression results for reproducibility.



## Key Findings

*SES coefficient:* ≈ 8.30 (p < 0.001)- a 10 percentage-point increase in SES is associated with about +0.83 points in average ACT score.  

Adjusted R² ≈ 0.605 indicating that SES explains roughly 60 % of ACT variation across schools.  

Results remain positive and significant after state fixed effects and outlier removal.



## Files


 `School\_Performance.ipynb`  Main Jupyter notebook with data cleaning, EDA, modeling, diagnostics, and sensitivity checks. 

 `cleaned\_edgap\_ccd.csv`  Final cleaned dataset used in the analysis. 
 
 `regression\_coefficients.csv`  Exported regression table with coefficients and robust SEs. 

 `README.md` This documentation file.


 
=======
## Acknowledgments
Course DATA 5100 (Seattle University) for the assignment and initial data. EdGap and NCES for the data sources. Additional contextual data from CMS/CDC/US Census as noted in the notebook.
>>>>>>> d6114d9 (Updated README with final sections and links per rubric)

## How to reproduce
1. Clone the repository:  
   `git clone https://github.com/simplyyweirdd3/school_performance.git`  
2. Create a Python environment and install requirements:  
   ```bash
   python -m venv venv
   source venv/bin/activate   # or .\venv\Scripts\activate on Windows
   pip install -r requirements.txt
