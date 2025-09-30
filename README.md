# LPGA vs PGA Hot Hand Analysis

This repository contains the code and supporting files for analyzing **hot hand and cold hand effects** in men’s (PGA) and women’s (LPGA) professional golf.  
All data used in this project are derived from official **scorecard data**.

---

## Repository Structure
```
data/                  # Raw scorecard data (source files)
LICENSE                # License for this repository

lpga_vs_pga/
│
├── data/              # Cleaned and processed data created by the scripts
├── HMM.Rmd            # Hidden Markov Model analysis (hot vs. cold states)
├── logit_analysis.Rmd # Logistic regression with fixed effects
├── tables/            # Output tables from models
└── visualizations/    # Plots and figures generated from analyses
```
---

## Workflow

1. **Data Preparation**  
   - Raw scorecard data are stored in `data/`.  
   - Scripts inside `lpga_vs_pga/` clean and process the data, saving outputs into `lpga_vs_pga/data/`.

2. **Modeling Approaches**  
   - **Logistic Regression (`logit_analysis.Rmd`)**: Estimates hot and cold hand effects using fixed effects for players and tournament rounds.  
   - **Hidden Markov Models (`HMM.Rmd`)**: Identifies latent “hot” and “cold” states based on strokes gained.

3. **Outputs**  
   - **Tables** summarizing regression results are saved in `lpga_vs_pga/tables/`.  
   - **Visualizations** (e.g., density plots, state probabilities) are saved in `lpga_vs_pga/visualizations/`.

---

## Requirements

- R (≥ 4.2)
- Recommended packages:  
  `fixest`, `ggplot2`, `dplyr`, `HMM`, `knitr`, `rmarkdown`

---

## Reproducibility

To reproduce results:  

1. Place raw scorecard data in `data/`.  
2. Run `logit_analysis.Rmd` and/or `HMM.Rmd`.  
3. Outputs (tables, visualizations, cleaned datasets) will be saved to the appropriate subfolders.  

---
