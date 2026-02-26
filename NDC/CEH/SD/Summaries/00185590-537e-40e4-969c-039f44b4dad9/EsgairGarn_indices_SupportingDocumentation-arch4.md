# Nant Esgair Garn catchment - 20 year derived statistics of rainfall, streamflow and acidity

## Overview
- A 20-year derived dataset of monthly statistics for rainfall, streamflow, and stream acidity (pH) linked to Nant Esgair Garn near Llyn Brianne, UK.
- Data were generated to understand long-term controls on aquatic biodiversity, using observations from 2013 and modelling to extend back to 1982–2013.

## Data lineage and provenance
- Observations collected at two stations in 2013 (15-minute resolution) to derive daily rainfall, streamflow, and pH.
- Daily data modelled to produce 20-year monthly Statistics via the CAPTAIN Toolbox (RIVC algorithm) and LSIM in Matlab.
- The dataset’s methodology and site details are documented in supporting materials; IP rights vetted by the Environmental Information Data Centre (EIDC).
- Key references: Jones and Chappell (2014) and Jones, Chappell & Tych (2014).

## Experimental setup and instrumentation
- Catchment: Nant Esgair Garn LI6, near Llyn Brianne, Powys, Wales; contributory catchment areas ~0.573–0.690 km².
- Instruments:
  - Streamflow: trapezoidal flume with a Sensortechnics pressure transmitter; data logged by Campbell Scientific CR1000.
  - pH: Hach Lange pH sensor with SC200 controller; data logged by Campbell Scientific CR1000.
- Ambient data sources:
  - Rainfall: historical records from Welsh Water/NRA/Environment Agency Wales; gaps filled using nearby raingauges.
  - Temperature: Felindre weather station; MI DAS MIDAS data (Met Office).

## Data processing and analytical methods
- Modelling approach:
  - Daily rainfall-to-streamflow and rainfall-to-pH models identified from 2013 observations using CAPTAIN’s RIVC algorithm; validated for 2013.
  - Identified models used to simulate daily values from 1982–2013, from which monthly statistics are derived.
- Tools and code:
  - Matlab (R2013) used for modelling and statistical calculations.
  - Included Matlab code for computing statistics (mean, percentiles, moving averages, pulses, growth season, rate of change, etc.).
- Variables and statistics:
  - A wide range of rainfall, temperature, NAO index, flow, and pH statistics calculated with various estimation periods (e.g., 365 days, 120 days) and percentile-based thresholds.
  - Growing season defined as mean temperature above 5°C; high/low pulses determined by 75th/25th percentile thresholds.
- Documentation:
  - Supporting documentation provides full lineage and processing steps; data are released with IPR vetting.

## Data structure and units
- Delivery as a single CSV file with 159 columns (columns 2–5 intentionally blank) and 32 rows.
- Rows correspond to statistics for the first day of each month from 1 April 1982 to 1 April 2013.
- Content includes, among others:
  - Mean rainfall, rainfall percentiles, and rainfall totals.
  - Temperature metrics (max/min/range/variation, growing season length, high/low temperature pulses).
  - NAO index (seasonal).
  - Streamflow and its distributional statistics (mean, percentiles, moving-average-based metrics, pulses, rise/drop rates, ranges, etc.).
  - pH statistics (mean, percentiles, moving-average metrics, ranges, coefficients of variation).
- Data quality:
  - Quality control involved identifying and replacing erroneous log values with NaN.
  - Data availability through Environmental Information Data Centre (EIDC).

## Reproducibility, provenance, and governance
- Provenance via explicit lineage from 2013 observations to 1982–2013 simulations; detailed in Supporting Documentation.
- Reproducibility supported by:
  - CAPTAIN Toolbox (RIVC) and Matlab LSIM modelling steps.
  - Publicly documented methods and DOIs for referenced tools and studies.
- Data rights:
  - Intellectual property rights vetted; dataset and methods are documented for reuse and verification.