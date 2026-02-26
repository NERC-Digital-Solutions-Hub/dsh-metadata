# Supporting documentation

## Overview
- Dataset containing model output from an agricultural land-use model at a 2 km grid resolution across Great Britain (GB) for 2000–2089.
- Four scenario combinations: standard climate change vs climate tipping point (AMOC collapse) and with vs without widespread irrigation.
- Focus: arable area by grid cell (hectares) under each scenario.

## Scenarios and Climate Assumptions
- Climate scenarios:
  - Standard climate change (SRES-A1B, ~3.5 K global climate sensitivity, HadRM3-PPE-UK)
  - Climate tipping point via AMOC collapse (simulated with HadGEM3; gradual 2030–2050 collapse)
- Irrigation:
  - Presence or absence of irrigation, implemented as a rainfall threshold equivalent to the optimal rainfall for GB arable farming.
- Climate data sources:
  - UKCP09 HadRM3-PPE-UK, daily data for 1950–2100, bias-corrected using 1960–1989 observations to align with historical data.
  - AMOC collapse scenario uses HadGEM3 with a present-day control and a perturbed run; seasonal means used for 50–80 years after perturbation to reflect steady-state conditions.

## Data Sources and Modeling Approach
- Modeling framework follows the Fezzi & Bateman approach (central to UK NEA and related studies).
- Inputs:
  - GB land-use data derived from the June Agricultural Census (GB 2 km grid, 1972–2010).
- Outputs are designed for consistency with environmental monitoring and policy evaluation over time.

## Data Structure and Files
- Four scenario-specific CSV files:
  - Ag_model_sc{scenario #}.csv
  - Scenario mapping:
    - 1: Climate tipping point = No; Irrigation = No
    - 2: Climate tipping point = No; Irrigation = Yes
    - 3: Climate tipping point = Yes; Irrigation = No
    - 4: Climate tipping point = Yes; Irrigation = Yes
- Each file contains:
  - Unique grid cell identifier
  - Total arable land area per grid cell (hectares; max 400 ha)
- Grid coordinates:
  - Ag_model_grid_2km.csv includes easting, northing (cell center) and min/max X/Y (cell corners) matched to grid cell IDs.

## Climate and Irrigation Details
- Climate input specifics:
  - Growing-season data (April–September) derived from 30-year means preceding each year’s projection.
  - Bias-correction applied to align model outputs with historical observations.
- Irrigation specification:
  - Implemented as a threshold rainfall condition corresponding to historically optimal arable rainfall in GB.

## Quality Control and Validation
- Methodology anchored in established practice from UK NEA and subsequent studies (Fezzi & Bateman; Bateman et al.; NEA follow-on).
- Data structure and inputs validated through peer-reviewed references and prior applications in regional environmental-economic assessments.
- Grid-scale outputs (2 km) enable detailed spatial monitoring and policy analysis.

## Uses, Access, and Practical Considerations
- Aligns with an Analyst’s aim to monitor environmental health and policy performance over time using standardized, transparent datasets.
- Facilitates combining with additional environmental or socioeconomic data to enhance dataset value beyond single-use applications.
- Underlying data accessibility supports broader data sharing and reproducibility for monitoring programmes.

## Limitations and caveats
- AMOC collapse is an idealized, linearly-weighted representation; real-world collapse dynamics may differ.
- Spatial resolution is fixed at 2 km (400 ha cells); some local heterogeneity may be smoothed.
- Irrigation is implemented via a simplified rainfall-threshold proxy, which may not capture all irrigation decision drivers.
- Climate projections rely on specific ensemble outputs (HadRM3-PPE-UK, UKCP09) and bias-correction approach; results should be interpreted within that methodological context.

## References
- Fezzi, C. et al. (2011, 2014, 2015)
- Bateman, I. et al. (2013, 2014)
- Jackson, L. et al. (2015)
- Jenkins, G. (2009)
- Mecking, J. et al. (2016)
- Nakicenovic, N. et al. (2000)
- NEA (2011)
- Safta, C. et al. (2015)
- UKCP09 (Met Office Hadley Centre) (2014)