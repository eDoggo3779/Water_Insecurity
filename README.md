# Intersectionality in Plumbing Insecurity: Educational Attainment and Ethnic Composition Are Stronger Predictors When Considered Independently
**Author:** Atharva Naik

## Overview
This project analyzes the extent to which plumbing insecurity across U.S. counties is associated with **educational attainment** and **ethnic composition**, and whether an **interaction** between these variables improves predictive modeling. Using ACS data (via NHGIS) and generalized additive models (GAMs), the study finds that education and ethnicity contribute **independently**, while their interaction does **not** meaningfully enhance predictive performance.

## Data
Data were obtained from the American Community Survey through NHGIS:
- **B01003** — Total Population  
- **B03003** — Hispanic or Latino Origin  
- **B15003** — Educational Attainment (25+)  
- **B25049** — Tenure by Plumbing Facilities  

All analyses are performed at the **county level**.

## Methods
A series of GAM models were constructed:
- Baseline model with nonlinear smooth terms  
- Models adding education × ethnicity interaction  
- Ablation comparisons using R², RMSE, AIC, and GCV  
- Partial Dependence Plots (PDPs) and Effective Degrees of Freedom (EDoF) used to assess feature influence and model complexity  

## Key Findings
- Interaction terms show **minimal improvement** across all metrics (|ΔR²| < 0.02; |ΔRMSE| < 0.001).  
- PDPs indicate that **individual** variables exert stronger effects than their joint interaction.  
- EDoF values for interaction terms (0–2) are far lower than those for individual smooth terms (4–7), suggesting weaker or inconsistent interaction patterns.  
- Conclusion: **Education and ethnicity are more informative when modeled independently.**


## Code, Data Access, & Presentation
- Code: https://github.com/eDoggo3779/Water_Insecurity  
- NHGIS Data: https://www.nhgis.org/
- Oral Presentation: https://www.youtube.com/watch?v=AgllHcr-gtA

## Acknowledgments
Thanks to The Coding School, Kayvan Jalali, and Dr. Tara Flaugher for technical and research guidance.
