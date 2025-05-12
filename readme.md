# COVID-19 Data Analysis with Our World In Data (OWID)

A data-driven exploration of the global COVID-19 pandemic, its impact across countries, and the correlation between various health, demographic, and economic factors.

This project performs an exploratory data analysis (EDA) on the COVID-19 dataset provided by [Our World In Data (OWID)](https://ourworldindata.org/covid-deaths). The dataset includes global COVID-19 metrics such as cases, deaths, testing, hospitalizations, vaccinations, and demographic indicators across countries and over time.

---

##  📦 Dataset Source

The data is sourced directly from OWID's compact CSV:


This file contains 496,820 rows and 61 columns (as of the time of analysis), covering multiple indicators per country and date.

---

## 🧰 Technologies Used

- Python 3.x
- Pandas
- Jupyter Notebook (or any Python script environment)

---

## 📊 Data Overview

- **Countries Covered**: Global (e.g., Afghanistan, United States, India, etc.)
- **Date Range**: From Jan 1, 2020 onwards
- **Indicators Included**:
  - **Epidemiological**: `total_cases`, `new_cases`, `total_deaths`, `new_deaths`, etc.
  - **Vaccination**: `total_vaccinations`, `people_vaccinated`, `booster_shots`, etc.
  - **Testing**: `total_tests`, `positive_rate`, `tests_per_case`, etc.
  - **Hospital Data**: `hosp_patients`, `icu_patients`, `hospital_beds_per_thousand`, etc.
  - **Demographics**: `population`, `median_age`, `population_density`, etc.
  - **Development Metrics**: `gdp_per_capita`, `extreme_poverty`, `human_development_index`, etc.

---

## 🔍 Initial Analysis Steps

1. **Load the Data**:
   ```python
   import pandas as pd
   url = "https://catalog.ourworldindata.org/garden/covid/latest/compact/compact.csv"
   df = pd.read_csv(url)

2. **Preview Data**:
   df.head()

3. **Inspect Structure and Missing Data:**
   df.info()
  df.describe()



**Key Observations:**
-> Many early entries (especially in 2020) contain NaN values due to reporting lags.
-> Some columns such as life_expectancy have entirely missing values and may require external supplementation or be excluded.
-> Indicators vary widely in data completeness across countries.
