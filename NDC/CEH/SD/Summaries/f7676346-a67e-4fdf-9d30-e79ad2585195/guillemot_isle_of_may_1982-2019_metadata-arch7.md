# Guillemot_Isle_of_May_1982-2019_metadata

## Overview
- Metadata schema for a Guillemot Isle of May dataset spanning 1982–2019 intended for GIS-based data products and map-based visualizations.
- Covers population metrics, environmental context, chick and adult biology, feeding and diet, and survival indicators within a defined geographic area.

## Spatial and Temporal Scope
- Time range: 1982 to 2019
- Geographic area: Isle of May, bounded by 56°-57°N and 1°-3°W
- Likely organized by year (and possibly site) to support spatial-temporal mapping

## Key Variable Themes

- Population and trends
  - Year
  - Pairs
  - Pairst-1 (breeding pairs in year t-1)
  - PopGR (rate of change in breeding numbers between years)

- Environmental context
  - SST (Sea Surface Temperature in February–March for year t)
  - SSTt-1 (SST for year t-1)

- Reproduction and chick success
  - N_hatched (number of chicks hatched)
  - N_fledged (number of chicks fledged)
  - Fled_success (proportion of hatched chicks that fledged)
  - Fled_Age (mean age at fledging in days)

- Chick biology and growth
  - Chick_Mass_N (number of chicks weighed)
  - Chick_Mass_x (mean mass of weighed chicks)
  - Chick_M_SEM (standard error of mean chick mass)
  - Chick_growth_index (mean mass at fledging divided by mean age)
  - Chick_lineargrowth (growth rate in g/mm for chicks with wing lengths 25–59 mm)

- Parental behavior and care
  - 2_adults_present (proportion of chicks with two adults present)
  - 2_adults_SE (SE for two-adult presence)
  - NoAdult_present (proportion with no adult present)
  - Parental_effort (index of parental effort)
  - PESE (SE of parental effort)
  - Time_togther (time adults spent together after a chick was fed)

- Feeding and diet
  - FeedsD_1 (number of fish fed to a chick per day)
  - Fish_samples (number of fish identified)
  - PropDiet_SE (SE of proportion of chick diet by mass)
  - PropDiet_Clup (proportion by mass from Clupeidae)
  - PropDiet_others (proportion from other species)
  - SE_length (mean length of a sandeel)
  - Clup_length (mean length of a Clupeidae)
  - SE_energy (mean energy value of a sandeel)
  - Clup_energy (mean energy value of a Clupeidae)

- Adult survival and mass
  - AdSurvival (mean adult survival from year t to t+1)
  - AdS_LowCI/AdS_UpCI (lower/upper 95% confidence intervals for adult survival)
  - Ad_M_N (number of breeding adults weighed)
  - Ad_Mass_x (mean mass of weighed breeding adults)
  - Ad_M_SEM (SE of mean mass for breeding adults)

## Data Characteristics and GIS Utility
- Built to enable map-based presentation of spatial features and temporal trends
- Includes uncertainty metrics (SE, CI) for informed spatial analyses
- Variables combine counts, proportions, and continuous measurements suitable for thematic mapping and relationship exploration
- Data may be sourced from multiple datasets; alignment of resolutions and standardization may be required for integrated maps

## Practical GIS Applications
- Visualize annual breeding population trends by year with geographic context
- Correlate Sea Surface Temperature (SST) context with reproductive outcomes and chick growth
- Map spatial patterns of parental care and presence (two adults vs single)
- Analyze diet composition and energy intake in relation to chick growth and survival
- Integrate with auxiliary spatial layers (bathymetry, prey distribution, sea conditions) for predictive mapping

## Data Quality, Gaps, and Challenges
- Data held in multiple locations; potential inconsistencies in data standards
- Missing values or variable resolutions across years or sites
- Requires cleaning and transformation to align temporal and spatial resolutions
- Uncertainty fields (SEs, CIs) must be incorporated carefully in GIS analyses

## Implementation Notes for GIS Specialists
- Expect a year-centric dataset with a defined bounding box; confirm spatial attribution per year/site
- Pay attention to units and naming conventions (e.g., mass in grams, age in days)
- Plan for integrating uncertainty so that map symbology can reflect confidence (e.g., error bars, choropleth with uncertainty layers)
- Consider creating derived layers (e.g., SST vs. N_hatched trends, AdSurvival spatially across years) to enhance interpretability in map dashboards