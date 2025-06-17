# ClinicalTrial — SurvivalAnalysis: TreatmentGroupComparison

## 🎯 Objective

This repository contains a comprehensive survival analysis comparing Control vs. Treatment groups in a clinical trial setting, featuring:

✔ Kaplan-Meier survival curves with risk tables

✔ Log-Rank test for between-group comparisons

✔ Cox Proportional Hazards regression with Hazard Ratios

✔ Comprehensive model diagnostics and assumptions testing

The analysis determines treatment efficacy and quantifies survival differences with 95% confidence intervals.

---

## 🧰 Technologies

- **Language**: R  
- **Main Packages**:  
  - `survival` – Survival models and tests 
  - `survminer` – Publication-quality KM plots
  - `tidyverse` – Model tidying  
  - `gtsummary` – Data wrangling and visualization 
 - **Reporting Packages**:  
  - `gtsummary` – Clinical tables 
  - `flextable` – Custom table formatting
  - `officer` – MS Word integration
  - `rmarkdown` – Data report and presentation
  - **Model Diagnostics**:  
  - `cox.zph` – Proportional hazards testing
  - `rms` – Extended modeling

---

## 📊 Analysis Workflow

1. Data Preparation
2. Primary Analysis: Kaplan-Meier estimation with survfit()| Log-Rank test via survdiff() | Cox PH modeling with coxph()
3. Secondary Analysis: Subgroup analyses by stratification| Time-dependent covariates | Competing risks assessment
4. Output Generation: KM plots with 95% confidence bands | Forest plots for hazard ratios | Model diagnostics visualizations

---

## 📝 Example Output

![ClinicalTrialSurvivalAnalysisTreatmentGroupComparison](newplot.png)


### 📋 Table 1. Log-Rank Test Results

          N   |Observed |Expected| (O-E)²/E
Control 100      82      96.3       2.12
Treated 100      80      65.7       3.11

Chisq=5.5, p=0.02

### 📋 Table 2. Cox Model Summary

Parameter	|HR (95% CI)     |  p-value
Treatment	|1.46 (1.06-1.99)|	0.020

