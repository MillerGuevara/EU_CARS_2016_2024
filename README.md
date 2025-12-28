# Econometric Analysis of the European Automobile Market (2016–2024)

## Overview

This repository contains the data, code, and final report for an econometrics project analyzing the European automobile market using quarterly time-series data from 2016Q1 to 2024Q4.

The objective of the project is to examine whether passenger car registrations and production activity are linked by a stable long-run relationship and how the market adjusts in the short run following major exogenous shocks, such as the COVID-19 pandemic and the introduction of stricter EU CO₂ emission standards.

The analysis is conducted using Python and follows standard time-series econometric methodology.

---

## Research Questions

The project addresses the following questions:

1. Do passenger car registrations and motor vehicle production activity exhibit a stable long-run relationship?
2. How quickly does the market adjust after short-run deviations from this long-run relationship?
3. What is the role of income, prices, and borrowing costs in explaining demand dynamics?
4. Did the COVID-19 pandemic and related restrictions cause significant short-run disruptions?
5. Is there evidence of a structural change in the market following the EU decarbonisation policy period?

---

## Data Description

- **Frequency:** Quarterly  
- **Sample period:** 2016Q1–2024Q4 (36 observations)  
- **Geographical coverage:** European aggregate (EA20 / EU aggregate, consistent across all series)

### Variables

- **Passenger car registrations**  
  Quarterly total (sum of monthly registrations). Used as a proxy for market demand.

- **Motor vehicle production index**  
  Quarterly average of the industrial production index for motor vehicles. Used as a proxy for production activity.

- **HICP motor cars index**  
  Quarterly average. Used as a proxy for car prices.

- **Real GDP (chain-linked volumes)**  
  Quarterly, seasonally adjusted. Used as a proxy for aggregate income.

- **Household consumption loan interest rate**  
  ECB MFI interest rate series. Used as a proxy for borrowing costs faced by households.

- **Policy regime dummy (post-2019)**  
  Indicates the period following the introduction of stricter EU CO₂ emission standards.

- **Pandemic/restrictions dummy**  
  Captures the period of COVID-19-related restrictions as defined in the dataset. This variable represents a regime period rather than a one-quarter shock.

All level variables (except interest rates) are transformed using natural logarithms.

---

## Methodology

The analysis follows a standard time-series econometric approach:

1. **Data cleaning and transformation**
   - Conversion to quarterly frequency
   - Log transformations for level variables

2. **Stationarity testing**
   - Augmented Dickey–Fuller (ADF) tests in levels and first differences

3. **Long-run relationship**
   - Estimation of a log-level regression
   - HAC (Newey–West) standard errors to account for autocorrelation

4. **Cointegration testing**
   - Engle–Granger residual-based test

5. **Short-run dynamics**
   - Error Correction Model (ECM) with lagged differences
   - Interpretation of the error-correction term as adjustment speed

6. **Structural change analysis**
   - Interaction terms to assess potential changes after the policy period

Diagnostic tests are reported, and HAC standard errors are used where residual autocorrelation is detected.

---
