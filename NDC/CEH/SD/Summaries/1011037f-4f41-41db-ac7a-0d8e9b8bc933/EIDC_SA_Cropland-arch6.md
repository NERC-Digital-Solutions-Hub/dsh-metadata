# Croplands_2050.csv

## Aim
- Combine projections of changes in water scarcity with current cropland extent to identify potential country-level vulnerabilities of cropland to water scarcity in 2050.

## Data sources and collection
- Water scarcity and runoff changes: global maps of change in annual runoff (%) and water scarcity (scale 1–4) derived from projections of five general circulation models (GCMs), provided by Prof. N. Arnell (University of Reading). Methodology detailed in Arnell et al. (2011).
- Cropland extent: global cropland area maps downloaded from EarthStat (Monfreda et al., 2008; Ramankutty et al., 2008), based on satellite data plus census statistics, on a global 5 arc-minute grid.

## Data processing and analysis
- Desk-based study (no fieldwork).
- No data calibration; all data are from published sources.
- Runoff change: percentage change between baseline (1960–1990) and 2050.
- Water scarcity: categorical scale 1 (not water scarce) to 4 (severely water scarce).
- Cropland areas: provided in hectares.
- Spatial overlay in ArcGIS to identify vulnerable land: cropland located where runoff is declining and the watershed is water scarce.
- For each country, compute the percentage of cropland that meets both criteria (classified as vulnerable).

## Calibration, quality control, and uncertainty
- Calibration: not required; data were pre-published.
- Quality control: datasets sourced directly from data owners to avoid modified versions.
- Uncertainty: results are country-level averages across the five GCMs; standard deviation is provided for interpretation.

## Data structure and units
- Croplands_2050.csv contains the percentage (%) of a country’s total cropland classified as vulnerable.
- Country names align with FAOSTAT conventions.
- Values accompanied by standard deviation across the five GCM models.

## Models and data provenance
- GCMs used: CSIRO Mk3, HADGEM, INMCM4, IPSL_MR, MRIOC_CM3.
- References for underlying datasets:
  - Arnell et al. 2011
  - Gosling & Arnell 2016
  - Gosling et al. 2010
  - Monfreda et al. 2008
  - Ramankutty et al. 2008

## Notes and interpretation
- The figure mentioned (Figure 1) schematically represents the spatial overlays linking hydrological model outputs to cropland maps.
- Outputs are intended to support understanding of country-level vulnerability to water scarcity for planning and policy considerations, with explicit attention to model-based uncertainty (standard deviations across GCMs).