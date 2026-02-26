# Details of data structure to ' HF_NH3.csv '

## Overview
- Supplement to supporting CINAg experiments documentation.
- NH3 emissions dataset from a 2016 grassland fertiliser trial at Henfaes Research Station (Bangor University).
- 7 columns, 476 rows.
- Measurements taken daily over 3 weeks following three fertiliser applications (wind tunnel measurements on plots 3 and 14 limited data; some sensor failures documented).
- Data supports assessment of NH3 fluxes under different fertiliser types and application rates.

## Dataset Structure and Columns
- Time_Start: Start date/time of the sampling period.
- Time_End: End date/time of the sampling period.
- N_app: Fertiliser application identifier (1, 2, or 3). 1st & 2nd applications at 90 kg ha-1; 3rd at 60 kg ha-1.
- Plot: Plot identifier (1–16); each plot is 2 × 4 m.
- Block: Blocking factor (1–4) from randomized block design.
- Treatment: Fertiliser type
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (agrotain)
- Emission_rate_kghad: NH3 emission rate from the plot for one day, in kg NH3-N ha-1 d-1.

## Data Quality and Processing Notes
- Wind tunnel data gaps:
  - Plot 3 contributed data for the 1st and 2nd fertiliser applications.
  - Plot 14 contributed data for the 3rd fertiliser application.
  - Anemometer values from these failed measurements were removed and replaced with the mean of surrounding wind tunnels.
- Detection limit:
  - 0.1 mg NH4-N L-1 used as the limit of detection.
- Data cleaning:
  - Negative NH3 flux values were replaced with 0.
  
## GIS-Relevant Considerations
- Spatial components:
  - Plot-level data (1–16) on a 2 × 4 m footprint; suitable for joining with plot-based GIS shapefiles.
  - Block design can support spatial analysis of variability across blocks.
- Temporal components:
  - Daily emission rates across three fertiliser applications over three weeks; enables time-enabled GIS visualization (time sliders/animators).
- Data integration:
  - Can be merged with spatial data for fertiliser type (AN/U/IU) and application event (N_app) to create map-based comparisons of NH3 emissions by treatment, plot, and time.

## Use Cases for GIS Specialists
- Create thematic maps of NH3 emission rates by plot and treatment over time.
- Visualize spatial patterns across blocks to assess field layout effects.
- Compare emissions across fertiliser types (AN, U, IU) and application events.
- Develop dashboards showing time-series per plot or per treatment, integrated with other environmental layers.

## Provenance and Scope
- Source: Grassland fertiliser trial conducted in 2016 at Henfaes Research Station (Bangor University).
- Sampling cadence: Daily during the 3-week period post-fertiliser application.
- Purpose: Enable analysis of NH3 emissions under different fertiliser regimes and measurement conditions.