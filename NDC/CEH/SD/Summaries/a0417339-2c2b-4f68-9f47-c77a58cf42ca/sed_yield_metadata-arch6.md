# Dataset name Sediment yield measurements for fire-affected locations in the United Kingdom (2018-2019), Tenerife (2018-2019) and Australia (2019-2020)

## Overview
- A compiled dataset of sediment yield measurements from three fire-affected locations across the UK, Tenerife, and Australia.
- Supports monitoring of sediment transport during rain events using standardized erosion plots and silt fences.

## Data files and contents
- sed_yield_ma.csv — Madre del Agua (Tenerife, Spain)
- sed_yield_ts.csv — Thompson reservoir (Victoria, Australia)
- sed_yield_sw.csv — Higher Swineshaw reservoir (Manchester, UK)
- Each file contains calculated sediment yields per site, per plot, and per collection date (units: T/ha).

## Spatial and temporal coverage
- Where (site coordinates):
  - Madre del Agua (Tenerife): UTM 28N 28 R 343340 3119657
  - Thompson reservoir (Australia): UTM 55 H 441956 5822296
  - Higher Swineshaw reservoir (UK): UTM 30 U 566670 5927917
- When (date ranges):
  - Madre del Agua: 17/08/2018 – 14/11/2019
  - Thompson: 13/05/2019 – 14/01/2020
  - Swineshaw: 03/08/2018 – 30/10/2019

## Data structure and variables
- Features per record: plot id, treatment, date, sediment yield (sed_yield), collection date, site
- Unit: sediment yield is reported as tonnes per hectare (T/ha)
- Data completeness: full record across sites

## Experimental design and treatments
- Replication: 1 (six plots per treatment)
- Treatments by site:
  - Madre del Agua: Control; wood mulch (C); 1.5 T/ha pine needle mulch (n1); 5 T/ha pine needle mulch (n2); 8 T/ha wood chips mulch (w1); 12 T/ha wood chips mulch (w2)
  - Thompson: Low fire severity; Moderate fire severity; High fire severity
  - Swineshaw: High severity (HS); Extreme severity (ES)
- Periodicity: collection after rain events with precipitation depths > 10 mm

## Sampling and methodology
- Experimental setup: Six erosion plots (3x8 m²) with sediment fences per treatment
- Field workflow: Sediments weighed in the field; subsample analyzed for water content; sediments oven-dried at 105°C for 48 h and re-weighed
- Calculation: Sediment yields (T/ha) computed by dividing corrected sediment weights by plot area and collection date

## Observations
- Madre del Agua: 102 observations
- Thompson: 90 observations
- Swineshaw: 84 observations

## Data quality and completeness
- Completeness: Full record for all three sites
- Data provenance: Collected by Dr Jonay Neris Tome, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr, Dr Gary Sheridan
- Methodological alignment: Based on Robichaud et al. (2002) silt fence protocol; laboratory procedures consistent across sites

## Provenance and references
- Robichaud, P.R., Brown, R.E. 2002. Silt fences: An economical technique for measuring hillslope soil erosion. Gen. Tech. Rep. RMRS-GTR-94.
  - URL: https://www.fs.usda.gov/research/treesearch/4543
- Parsons, A., Robichaud, P.R., Lewis, S.A., Napper, C., Clark, J.T. 2010. Field guide for mapping postfire soil burn severity. Gen. Tech. Rep. RMRS-GTR-243.
  - URL: https://www.fs.usda.gov/research/treesearch/36236

## How to use and potential applications
- Data support use cases:
  - Compare sediment yields across sites with different burn severities and mulching treatments
  - Evaluate effectiveness of mulching and restoration treatments on reducing erosion
  - Integrate with rainfall and hydrological data to model event-based sediment transport
  - Create dashboards or self-serve data views for policymakers, researchers, or managers
- Data integration considerations:
  - Ensure consistent unit interpretation (T/ha)
  - Align temporal formats and date parsing across the three CSVs
  - Use coordinates in the provided UTM zones for spatial analyses or map visualizations
  - Maintain provenance by citing Robichaud (2002) and Parsons (2010) where applicable

## Cautions and limitations
- Data are event-driven and site-specific; cross-site extrapolation should consider site context (soil, vegetation, burn severity)
- Coordinate reference systems are provided as UTM coordinates; transformations may be needed for some GIS workflows
- Periodicity is defined as events with >10 mm rainfall; results are conditional on rainfall distribution and plot maintenance