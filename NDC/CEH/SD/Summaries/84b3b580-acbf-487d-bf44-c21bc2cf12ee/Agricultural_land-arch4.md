# The data included in Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv and Wheat_2050.csv relates to an analysis of the impact changes in water availability will have on the suitability of land used in the production of these commodities in 2050.

## Aim
- Combine projections of changes in water scarcity with current land-use extents for selected commodities to identify country-level vulnerabilities of pasture land to water scarcity in 2050.

## Data sources and collection
- Global maps of change in annual runoff (%) and water scarcity (1–4 scale) derived from projections of five GCMs, provided by Prof. N. Arnell (University of Reading).
- Global maps of current pasture land area downloaded from earthstat.org (open access).
- Global cropland maps created from a mix of satellite-derived data and national/state/country census statistics, expressed on a global 5 arcminute grid.
- Key references for data sources: Arnell et al. 2011; Monfreda et al. 2008; Ramankutty et al. 2008.

## Experimental design / Analytical approach
- Desk-based study using ArcGIS to overlay land-use maps with hydrological projections.
- Vulnerable land defined where:
  - pasture land lies in areas with declining annual runoff, and
  - the watershed is water-scarce in 2050.
- Outcome per country: percentage of land for each commodity meeting both criteria, classified as vulnerable.

## Calibration and data processing
- All data are previously published; no new calibration performed.
- Annual runoff change: percentage change from baseline (1960–1990) to 2050.
- Water scarcity: scaled from 1 (not water scarce) to 4 (severely water scarce).
- Agricultural land areas expressed on a hectare (ha) basis.

## Data structure and values
- Files Maize_2050.csv, Fruit_2050.csv, Pulses_2050.csv, Rice_2050.csv, Vegetables_2050.csv, Wheat_2050.csv contain:
  - Percentage of total country land area for each commodity classified as vulnerable.
- Country names aligned with FAOSTAT formatting.
- Data are country-level estimates averaged across 5 GCMs, with accompanying standard deviation.

## Analysis tools and workflow
- GIS platform: ArcGIS used for spatial overlays (land use and hydrological projections).
- Output: country-level vulnerability percentages with uncertainty (standard deviation).

## Quality control and provenance
- Datasets sourced directly from data owners to prevent use of modified versions.
- Provenance maintained to support reproducibility and discoverability.

## Additional information for interpretation
- GCMs used in the analysis: CSIRO_Mk3, HADGEM, INMCM4, IPSL_CM5_MR, and MRIOC_CM3.
- The study provides a framework for assessing how climate-induced water scarcity could affect land suitability for key commodities by 2050, with results suited for cross-country comparison and policy planning.