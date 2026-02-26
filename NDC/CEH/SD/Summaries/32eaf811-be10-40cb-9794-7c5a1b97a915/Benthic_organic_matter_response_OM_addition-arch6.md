# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates how added organic matter (leaf litter) affects benthic organic matter (BOM) in Welsh upland rivers.
- Uses a before-after-control-impact (BACI) design with upstream reference and downstream experimental zones within each stream.
- Temporal framework: before period (T1) Nov 2012–Jan 2013 with no manipulation; after period (T2) Jan–Mar 2013 with leaf litter additions to the experimental zone.
- Leaf litter types: oak, birch, and alder; one tonne bags used to simulate natural senescence and abscission.
- Additional leaf litter (630 kg wet weight) added after two storm events to maintain supply.
- Data aim: quantify BOM stocks in response to controlled organic matter input.

## Experimental Design and Sampling Regime
- Each stream split into:
  - Upstream reference zone (control)
  - Downstream experimental zone (receives leaf litter)
- Independent sampling achieved by maintaining 20–50 m between zones.
- Sampling periods:
  - T1 (before): 61–65 days
  - T2 (after): 57–62 days
- Sampling framework includes five reaches per stream, with six random BOM samples per reach across five time points (January–May 2013).

## Data Collection and Laboratory Methods
- Field equipment: Surber net (area 0.1 m², 330 µm mesh, 10 cm depth).
- Sample handling: on-site preservation in 70% IMS; laboratory processing to separate macroinvertebrates and BOM.
- Laboratory processing: BOM dried to constant weight; portion cycles used to determine inorganic content via ash at 550°C for ash-free correction.
- Measurements reported as weights (grams) of BOM components.

## Data Structure and Variables
- Core data stored as flat CSV files with 10 columns:
  - site_code: sampling site identifier
  - landuse: basin land-use
  - region: stream basin
  - time: Before or After manipulation
  - month: sampling month
  - reach: Experimental or Control site
  - replicate: replicate code
  - surber_area: area of the Surber sampler in m²
  - cpom: coarse particulate organic matter (grams)
  - fpom: fine particulate organic matter (grams)
- Supporting site metadata file (DURESS_CU_site_description.csv) includes:
  - site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey campaign and catchment information

## Data Processing and Quantities
- BOM stocks weighted to the nearest 0.01 g.
- Units for BOM components are grams.
- Inorganic correction applied via ash-free conversion for subsets.

## Data Quality and Calibration
- Calibration steps and values: None specified.
- Quality control: None specified within the data description.
- Data interpretation should consider potential absence of formal QC/validation notes and ash-free corrections applied only to a subset.

## Supporting Documentation and Data Availability
- Main BOM data described with metadata fields and measurement procedures.
- Site descriptions provided as a separate CSV with geospatial identifiers and catchment information.
- Data structure designed to enable cross-site comparisons of BOM before/after manipulation and between reference and experimental zones.

## Potential Data Products and Uses (Data Support Perspective)
- Self-serve dashboards or pivot-table reports enabling:
  - Comparison of BOM (cpom and fpom) by time (Before vs After), reach (Experimental vs Control), and month.
  - Spatial visualization of BOM changes across sites using site metadata (coordinates, land-use, region).
  - Delta BOM calculations (After minus Before) by site and reach to assess litter addition effects.
- Data integration ideas:
  - Merge BOM data with site metadata for GIS-enabled mapping and regional trend analysis.
  - Link with environmental variables (e.g., storm events) to explore drivers of BOM changes.
- Data quality enhancements:
  - Document and apply a data quality flag framework (e.g., missing values, QC checks) given the current absence of formal QC notes.
  - Provide clear ash-free correction methodology for all samples or indicate the subset used for correction.