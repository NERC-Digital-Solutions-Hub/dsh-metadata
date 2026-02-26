# Abstract and lineage Nant Esgair Garn catchment - 20 year derived statistics of rainfall, streamflow and acidity

## Overview
- A 20-year derived statistics dataset providing monthly statistics for rainfall, streamflow, and stream acidity (pH) for the Nant Esgair Garn catchment near Llyn Brianne, Wales.
- Observations for 2013 at 15-minute resolution underpin dynamic modelling; monthly statistics derived from daily models.
- Aimed at understanding controls on long-term aquatic biodiversity dynamics.

## Provenance and lineage
- Collected and maintained by Lancaster University; data lineage detailed in supporting documentation.
- Data and modelling rely on CAPTAIN Toolbox for Matlab; models identified with the RIVC algorithm and validated on 2013 data.
- All data released through the Environmental Information Data Centre (EIDC) and vetted for Intellectual Property Rights (IPR) by NERC EIDC.

## Experimental design and data collection
- Nant Esgair Garn catchment (LI6) near Llyn Brianne; contributory areas: 0.573 km2 (streamflow) and 0.690 km2 (pH downstream).
- Geological context: shales, mudstones, greywackes, grits; soils of Podzols and Histosols; catchment historically moorland and improved pasture.
- Water data collected in 2013 at 15-minute intervals; rainfall data spanning 1982-04-01 to 2013-04-01 with gaps filled from nearby gauges; NAO index sourced from public datasets.

## Data processing and modelling
- Daily rainfall, streamflow, and pH were modelled and interpolated to daily values; monthly statistics derived from these daily series.
- Modelling workflow:
  - Use CAPTAIN RIVC algorithm to identify model structures/parameters from 2013 observations.
  - Use LSIM in Matlab to simulate daily streamflow and daily pH for 1982-2013.
  - Derive monthly statistics from simulated daily data.
- Software: Matlab R2013; CAPTAIN Toolbox; code snippets provided for common statistics (mean, percentiles, moving averages, pulses, growth season, etc.).

## Variables and data structure
- Single CSV dataset with 159 statistical variables; columns 2–5 intentionally blank; 32 rows (one row per month from 1982-04-01 to 2013-04-01; first row header).
- Examples of statistics and estimation windows:
  - Rainfall, temperature, NAO index, and related metrics with estimation windows of 365 days, 120 days, and other derived periods before biological sampling dates.
  - Derived metrics include means, percentiles (10th, 95th), totals, ranges, coefficients of variation, growing season (threshold 5°C), durations/pulses of high/low conditions, and related flow and pH statistics.
  - Columns specify detailed timing and thresholds (e.g., 75th/25th percentile for high/low pulses, moving-average-based minima/maxima, and various pulse durations).
- Example variables cover: mean rainfall, rainfall percentiles, mean/percentile temperature measures, NAO, rainfall/flow/pH statistics at multiple lags, and derived growth and pulse metrics.

## Calibration and quality control
- Field data quality control: QA checks on CR1000 loggers; erroneous values replaced with NaN to handle outages or sensor issues.
- Calibration: salt-dilution checks for flume stage-discharge; SC200 pH controller recalibrations every 2–3 months; manual pH sensor recalibrations as needed.

## Data access, rights, and documentation
- Data released via the Environmental Information Data Centre online catalogue; IP rights vetted by NERC EIDC.
- Dataset format: CSV with 159 variables, 32 rows; comprehensive metadata detailing units, estimation periods, and data derivation.
- Documentation and site details referenced in the Supporting Documentation and associated publications.

## Reproducibility and contact
- Modelling and statistics generation are reproducible via the CAPTAIN Toolbox (Matlab) and provided code fragments.
- Primary contact: Dr Nick A. Chappell (Lancaster University); orcid: 0000-0001-6683-951X.