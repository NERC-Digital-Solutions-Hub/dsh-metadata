# FADOE_pollution.csv

## Overview
- Air pollutant concentrations measured in eight Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Experimental design comprises four treatments (Diesel exhaust D, ozone O3, diesel exhaust + ozone D+O3, and control CON) with two rings per treatment.
- Data intended to monitor environmental conditions and treatment effects over time.

## Experimental Design and Data Collection
- Ring setup: eight rings, each with 8 m diameter, centered data collection.
- Treatments: D, O3, D+O3, CON; two rings per treatment.
- Sampling cadence: measurements taken sequentially every 60 seconds.
- Pollutants measured at ring centers: NO, NO2, NOx, and O3 (ppb).
- Instruments: automated switching system feeding Thermo Scientific Model 49i for O3 and Model 42C for NOx; measurements are continuous and time-stamped.

## Pollutants, Measurements, and Columns
- NO (NO column Q), NO2 (NO2 column R), NOx (NOx column S), O3 (Ozone column P).
- Units: parts per billion (ppb).
- Data captured alongside pollutant concentrations.

## Temporal, Spatial, and Environmental Context
- Time data: Year (Column A), Date (Column B), Time (Column C) to log sampling events.
- Wind data: wind speed and direction from four surrounding positions:
  - South (ws1/wd1; Columns F/K)
  - West (ws2/wd2; Columns G/L)
  - North (ws3/wd3; Columns H/M)
  - East (ws4/wd4; Columns I/N)
- Field location: center of a wheat field with coordinates specified for 2018 (lat 51.482853, lon -0.897749) and 2019 (lat 51.482374, lon -0.895855).

## Data Structure and Management
- Data stored in a CSV file named FADOE_pollution.csv.
- Design supports standardised outputs (reports, maps, charts) and data quality practices (verification, QA, cleaning, transformation).
- Data can be stored and uploaded to appropriate data portals for broader accessibility.

## Relevance to Environmental Monitoring Analysts
- Provides a controlled, replicable dataset to assess environmental health and policy-relevant outcomes across treatments.
- Enables integration with additional context data (e.g., wind) to interpret dispersion and exposure.
- Illustrates data-standardization practices and the potential for cross-study comparability.