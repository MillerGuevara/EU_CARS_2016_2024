# Automotive Sector Econometric Analysis Dataset

This repository contains a curated dataset for econometric analysis of the automotive sector in the Euro area. The data is sourced from **Eurostat**, the statistical office of the European Union.

## 📊 Dataset Overview

The dataset combines key monthly and quarterly indicators related to car demand, production, prices, credit conditions, and overall economic activity for the **Euro area (EA20)**.

| Variable Name | Eurostat Code | Frequency | Description |
| :--- | :--- | :--- | :--- |
| `PASSENGER_CAR_REGISTRATIONS` | `CAR.M.I9.N.CREG.PC0000.4Z1.N.PN` | Monthly | New registrations of passenger cars. |
| `MOTOR_VEHICLE_PROD_INDEX_2021` | `sts_inpr_m` | Monthly | Production index for motor vehicles, trailers, and semi-trailers (2021=100). |
| `HICP_MOTOR_CARS` | `ICP.M.D0.N.071100.4.INX` | Monthly | Harmonised Index of Consumer Prices for Motor Cars. |
| `INTEREST_RATE_HOUSEHOLD_CONSUMPTION` | `MIR.M.U2.B.A2B.A.R.A.2250.EUR.N` | Monthly | Interest rate for household consumption loans. |
| `GDP` | `namq_10_gdp` | Quarterly | Gross Domestic Product (Chain-linked volumes, reference year 2010). |

## 🌍 Geographic Coverage
The data covers the **Euro area with 20 member countries (EA20)**. This aggregate includes all EU countries that have adopted the euro as their currency. The specific country composition is consistent with Eurostat's definition for the `EA20` aggregate during the data period.

## 🛠️ Data Transformation & Structure
For econometric analysis, the monthly series have been **aggregated to a quarterly frequency** to match the GDP data.
- **Flow variables** (e.g., `PASSENGER_CAR_REGISTRATIONS`) were summed.
- **Rate and index variables** (e.g., `HICP_MOTOR_CARS`, `INTEREST_RATE`) were averaged.

The final analysis-ready dataset is structured with one row per quarter.
