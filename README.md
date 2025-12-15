# Trip Distance and Duration Patterns in Austin’s Shared Micromobility System

## Overview
This repository contains the final report and supporting materials for a descriptive analysis of bicycle and scooter trips in Austin’s shared micromobility system. Using trip-level data from the Austin Open Data Portal, the study examines conditional differences in trip distance and trip duration between bicycles and scooters under comparable temporal and spatial conditions.

The analysis focuses on trips taken in calendar year 2019 to represent a typical pre-pandemic baseline year. All results are descriptive and associational rather than causal.

---

## Key Findings
- **Scooter trips are substantially shorter than bicycle trips in distance.**  
  After controlling for hour of day, day of week, and starting council district, scooter trips remain significantly shorter than bicycle trips, indicating that the two modes are used for systematically different trip lengths.

- **Once trip distance is controlled for, scooters and bicycles have nearly identical trip durations.**  
  Conditional on distance and contextual factors, expected trip durations for scooters and bicycles are almost the same, with differences that are statistically small and substantively negligible for a typical trip.

- **Observed mode differences primarily reflect usage patterns rather than travel-time efficiency.**  
  The results suggest that scooters and bicycles serve complementary roles within Austin’s micromobility system: scooters are typically used for shorter trips, while bicycles are used for longer trips, but neither mode exhibits a clear advantage in travel-time efficiency for a given distance.

---

## Repository Contents

### 📄 Main Report
**Trip Distance and Duration Patterns in Austin’s Shared Micromobility System.pdf**

- Describes research questions, data preprocessing, modeling strategy, results, and interpretation
- Uses log-linear regression models with controls for hour of day, day of week, and starting council district
- Includes model selection via Bayesian Information Criterion (BIC)
- Presents all figures and tables referenced in the text

---

### 📎 Appendix
**Appendix_Donghyun_Kim.pdf**

- Supplementary exploratory data analysis (EDA)
- Diagnostic plots for raw-scale and log-transformed models
- Robustness checks (Box–Cox transformation, weighted least squares, Huber regression)
- BIC comparisons, GVIF diagnostics, and partial residual plots
- Full model summaries and supporting figures referenced in the main report

All code outputs and extended diagnostics are intentionally placed in the appendix to comply with the course requirement that no computer code appear in the main report.

---

## Data Source
- **Austin Open Data Portal**
- Dataset: *Shared Micromobility Vehicle Trips*
- https://data.austintexas.gov
- Time period analyzed: January–December 2019

The original dataset contains trips from 2018–2022; analysis was restricted to 2019 to avoid COVID-19–related disruptions and to represent a typical baseline year of operations.

---

## Methods Summary
- **Unit of analysis:** Single completed trip  
- **Outcomes:** Trip distance (meters), trip duration (seconds)  
- **Primary exposure:** Vehicle type (bicycle vs. scooter)  
- **Controls:** Hour of day, day of week, starting council district  
- **Preprocessing:** Removal of missing values and extreme outliers (3 × IQR rule)  
- **Modeling:** Log-linear regression to address right skewness and heteroscedasticity  
- **Model selection:** Bayesian Information Criterion (BIC)

---

## Notes
- This project is **observational and descriptive**, not causal.
- Results summarize conditional usage and travel patterns rather than estimating causal effects of vehicle choice.
- All analyses were conducted in R; reproducibility materials and diagnostic outputs are documented in the appendix.

---

## Author
**Donghyun Kim**  
University of Michigan  
STATS 500 – Applied Statistics
