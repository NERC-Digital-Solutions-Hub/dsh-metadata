# Dataset name Sediment yield measurements for fire-affected locations in the United Kingdom (2018-2019), Tenerife (2018-2019) and Australia (2019-2020)

## Overview
- Purpose: Monitoring sediment transport during rain events in burned areas and reporting sediment yields per plot.
- Locations and periods:
  - Madre del Agua, Tenerife, Spain (2018-2019)
  - Thompson reservoir, Victoria, Australia (2019-2020)
  - Higher Swineshaw reservoir, Manchester, UK (2018)
- Output: Full records of sediment yields per site, plot, and collection date (in T/ha).

## Data files
- sed_yield_ma.csv: Madre del Agua (Tenerife)
- sed_yield_ts.csv: Thompson reservoir (Australia)
- sed_yield_sw.csv: Higher Swineshaw reservoir (UK)
- Features included: plot id, treatment, date, sediment yield (T/ha) per plot, collection date

## Geographic information
- Georeferencing details provided for each site:
  - Madre del Agua: UTM 28N 28R, 343340 3119657
  - Thompson reservoir: UTM 55H, 441956 5822296
  - Higher Swineshaw reservoir: UTM 30U, 566670 5927917
- Data are tied to erosion plots and silt fences installed in fire-affected catchments.

## Methodology
- Experimental design: Six erosion plots per treatment (each 3 x 8 m2) with silt fences, following Robichaud et al. 2002 protocol.
- Sediment measurement: In-field weighing of collected sediments; subsample to lab to determine water content (105 °C for 48 h); correct weights and compute sediment yield per plot per collection date as total corrected sediment weight divided by plot area (T/ha).
- Sampling period: After rain events with precipitation depths > 10 mm.
- Treatments:
  - Madre del Agua: Control; wood mulch (C); 1.5 t/ha pine needle mulch (n1); 5 t/ha pine needle mulch (n2); 8 t/ha wood chips mulch (w1); 12 t/ha wood chips mulch (w2)
  - Thompson: Low, Moderate, High fire severity
  - Swineshaw: High (HS) and Extreme (ES) fire severity (per Parsons et al., 2010)
- Replication: 6 plots per treatment

## Data quality and completeness
- Completeness: Full record across locations and treatments.
- Data provenance: Collected by Dr Jonay Neris Tome, Dr Carmen Sánchez-García, Dr Cristina Santín, Prof. Stefan Doerr, Dr Gary Sheridan.
- Standards and references: Methodology aligns with Robichaud & Brown (2002) silt fence protocol and Parsons et al. (2010) burn severity field guide.

## Usage and integration notes
- Data are provided as CSV files suitable for GIS and map-based visualizations.
- Items can be joined across files using plot_id, site, and collection date to create integrated spatial-temporal datasets.
- Clear methodological metadata and references support reproducibility and appropriate attribution.