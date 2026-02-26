# The data included in Pasture_2050.csv relates to an analysis of the impact changes in water availability will have on cropland availability in 2050.

## Aim
- Combine projections of changes in water scarcity with current pasture land extent to identify country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources and measures
- Global projections of:
  - Change in annual runoff (%), derived from five global climate models (GCMs) based on Arnell et al. (2011) methodology.
  - Water scarcity index (1–4; 1 = not water scarce, 4 = severely water scarce).
- Global pasture land area: obtained from earthstat.org (open access; up-to-date data).
- Global cropland maps: produced from a combination of satellite-derived data and national/state/country census data; gridded at 5 arcminute resolution (Monfreda et al., 2008; Ramankutty et al., 2008).

## Methods and workflow
- Study design: desk-based; overlay of spatial data to identify vulnerabilities.
- Spatial analysis: overlay pasture land with GCM-specific projections of water scarcity and annual run-off using ArcGIS.
- Vulnerability criteria: pasture land in areas where
  - annual run-off is declining, and
  - the watershed is water scarce in 2050.
- Metric calculation: for each country, compute the percentage of total pasture area that meets both criteria.

## Data calibration and units
- Calibration: none required; all data are from published sources.
- Runoff changes: percentage change relative to baseline (1960–1990) to 2050.
- Water scarcity: scaled 1–4.
- Croplands: reported in hectares.
- Country identifiers: aligned with FAOSTAT country names.

## Outputs and interpretation
- Primary output: Pasture_2050.csv, presenting the percentage of each country’s pasture area classified as vulnerable.
- Uncertainty: all country estimates are averaged across the five GCMs; standard deviation provided to reflect model spread.

## Quality control and governance
- Data provenance: datasets obtained directly from data owners to avoid altered versions.
- Reproducibility: clear documentation of data sources and modeling steps enables replication.

## Data structure and accessibility
- Country-level estimates aggregated across five GCMs.
- Includes standard deviation across models for each country.
- Names and geographic coverage correspond to FAOSTAT conventions.

## Key models and references
- GCMs used: CSIRO Mk3, HADGEM, INMCM4, IPSL CM5 (noted as IPSL_CM3 in references), and MRIOC CM3.
- Core references for underlying datasets:
  - Arnell et al. 2011; Gosling & Arnell 2016; Gosling et al. 2010
  - Monfreda et al. 2008; Ramankutty et al. 2008

## Relevance for monitoring frameworks
- Provides a measurable vulnerability metric linking water resources and pasture/cropland distributions at country scale.
- Demonstrates a reproducible workflow for combining multiple climate projections with land-use data to inform policy and decision-making.
- Highlights data governance considerations (data provenance, openness, metadata clarity) and barriers (data accessibility, harmonization across datasets, and model agreement).