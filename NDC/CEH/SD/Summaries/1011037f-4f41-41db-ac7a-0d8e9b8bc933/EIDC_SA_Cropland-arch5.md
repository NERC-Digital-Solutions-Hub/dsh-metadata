# The data included in Croplands_2050.csv relates to an analysis of the impact changes in water availability will have on cropland availability in 2050.

## Overview
- Purpose: Combine projections of changes in water scarcity with current cropland extent to identify country-level vulnerabilities of cropland to water scarcity in 2050.
- Scope: Global assessment using multiple climate model projections and global cropland maps.

## Data sources and collection methods
- Hydrology projections: Global maps of change in annual runoff (%) and water scarcity (index 1–4) derived from five general circulation models (GCMs). Data provided by Prof. N. Arnell; methodology in Arnell et al. (2011).
- Cropland data: Global cropland area maps downloaded from earthstat.org, created from satellite data integrated with national/state/country census stats; data on a global 5 arc-minute grid. Details in Monfreda et al. (2008) and Ramankutty et al. (2008).
- Study nature: Desk-based; no fieldwork or laboratory instrumentation involved (PC only).

## Calibration and data processing
- Calibration: No calibration required; all data were previously published.
- Measurements:
  - Annual runoff change: percent change from baseline (1960–1990) to 2050.
  - Water scarcity: scale from 1 (not water scarce) to 4 (severely water scarce).
  - Cropland areas: provided on a per-hectare basis.
  
## Analytical methods
- Spatial overlay: Cropland maps overlaid with GCM-specific runoff projections and water scarcity maps using ArcGIS.
- Vulnerability criteria: Areas where cropland lies in (i) declining runoff and (ii) water-scarce watersheds.
- Result metric: For each country, the percentage of cropland that meets both criteria (designated as vulnerable) is computed.

## Data format, structure, and units
- Croplands_2050.csv: shows the percentage of total cropland in each country classified as vulnerable.
- Country naming: Matches FAOSTAT country names.
- Aggregation: Country-level estimates averaged across five GCMs; includes standard deviation.

## Quality control and provenance
- Provenance: Datasets were sourced directly from data owners to ensure no modified versions were used.
- Reproducibility: The analysis uses standardized global datasets and documented methods; results reflect aggregation across multiple models.

## Data structure and models
- Models used: Five GCMs—CSIRO_Mk3, HADGEM, INMCM4, IPSL_CM4, MRIOC_CM3.
- Data scope: Global, country-level summaries with accompanying variability (standard deviation) across GCMs.

## Additional information and references
- Key references for underlying data:
  - Arnell et al. 2011; Gosling & Arnell 2016; Gosling et al. 2010
  - Monfreda et al. 2008; Ramankutty et al. 2008
- Data context: Links to FAOSTAT for country naming and to Earthstat for cropland maps; datasets are primarily open-access sources.