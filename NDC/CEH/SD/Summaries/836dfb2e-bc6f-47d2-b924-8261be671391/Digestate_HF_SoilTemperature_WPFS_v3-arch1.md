# Digestate_HF_SoilTemperature_WFPS_v1.csv

## Overview
- Data from the digestate wheat trial 2017 conducted at Henfaes Research Center, Bangor University.
- Contains soil temperature and water-filled pore space (WFPS) measurements at 2.5 cm depth.
- Observations span ten plots: 5, 6, 8, 10, 15, 18, 24, 28, 29, 30.
- Total records: 87,980 rows.

## Data structure
- 4 columns and 87,980 rows.
- Columns (with explanation and units):
  - Time: Date and time of day.
  - Plot: Plot numbers (5, 6, 8, 10, 15, 18, 24, 28, 29, 30).
  - Soil_temperature_degrees_celcius: Soil temperature at 2.5 cm depth (degrees Celsius).
  - WFPS_percent: Water-filled pore space at 2.5 cm depth (percent).

## Variables and units
- Time: Date and time stamp.
- Plot: Categorical/Numeric identifier for the plot.
- Soil_temperature_degrees_celcius: Temperature at 2.5 cm depth, in °C.
- WFPS_percent: Water-filled pore space at 2.5 cm depth, in percent.

## Scope and context
- Focused, fixed-depth measurements (2.5 cm) across 10 plots within a single trial year (2017).
- Data supplement to the supporting documentation for CINAg experiments.

## Potential analyses and uses for analysts
- Correlation and regression analyses between soil temperature and WFPS over time.
- Time-series analyses of temperature and moisture within each plot; cross-plot comparisons.
- Multiplot or mixed-effects modeling to assess plot-level variation and treatment effects implied by the digestate trial.
- Data cleaning and quality checks: validate time parsing, handle missing values, and ensure plotting IDs align with the listed plots.

## Provenance and accessibility notes
- Supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Dataset is labeled as v1; ensure alignment with the accompanying documentation for metadata and methodological details.