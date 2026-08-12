# ED Pressure & Prescribing Analysis

Time series analysis (ARIMA, SARIMA, ARIMAX) looking at whether community prescribing patterns in Ireland relate to Emergency Department trolley pressure.

## Requirements
- Python 3.9–3.11
- pip

## How to Run (use the following commands in terminal)
```bash

python -m venv venv
venv\bin\activate
pip install -r requirements.txt

```

Run the notebooks in order: `data_cleaning` → `exploratory_analysis` → `correlation_lag_analysis` → `time_series_modelling`.

## Notebooks
- `data_cleaning.ipynb` — loads and cleans the raw prescribing/trolley data, merges into one dataset
- `exploratory_analysis.ipynb` — initial plots, seasonality, and correlations
- `correlation_lag_analysis.ipynb` — tests prescribing variables against ED pressure across different time lags
- `time_series_modelling.ipynb` — ARIMA/SARIMA/ARIMAX models, comparisons, and diagnostics


## Overview
Uses monthly HSE prescribing data (PCRS) and INMO Trolley Watch figures to test whether specific prescribing classes are associated with ED trolley pressure, at various time lags. Baseline ARIMA/SARIMA models are compared, then extended with prescribing variables (ARIMAX) and checked against held-out data.

## Data
- Prescribing: HSE PCRS / eHealth Open Data Portal
- ED trolley figures: INMO Trolley Watch

## Limitations
Monthly data only — no finer resolution available. See thesis for full discussion.
