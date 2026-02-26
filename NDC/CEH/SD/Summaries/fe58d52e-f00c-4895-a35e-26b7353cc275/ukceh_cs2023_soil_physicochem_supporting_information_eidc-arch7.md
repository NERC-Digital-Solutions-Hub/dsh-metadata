# UKCEH Countryside Survey QA metadata and analysis report 2023 - EIDC Topsoil physico-chemical data 2023

## Overview
- A QA metadata and analysis report for topsoil physico-chemical data from the UK Countryside Survey (CS) rolling program.
- Focuses on topsoil (0–15 cm) metrics collected across GB during the rolling survey, with data stored and quality-checked for GIS use.
- Data linkage: squares (1-km x 1-km), plots within squares (X-Plots), year of survey, and co-located vegetation assessments.

## Design and Sampling Framework
- Rolling survey design: 500 squares sampled over a five-year cycle; 100 squares visited each year.
- Purpose: detect change over time and spatial variation in soil condition and function; buffer against climate year effects.
- Spatial units:
  - 1-km x 1-km squares (SQUARE) with unique IDs.
  - Within each square, up to five sampling locations (PLOT) for soils and vegetation.
- Selection and exclusions:
  - Squares chosen within Land Classification of GB strata (LC07).
  - Excluded if >75% urban land or >90% sea.
- COVID disruption (2020): partial year fieldwork; 50 England-only squares reselected and added.

## Sample Collection and Metrics
- Topsoil sampling:
  - Five randomly dispersed locations per square (where possible), using a 15 cm long core, co-located with vegetation plots.
  - Sample depth targeted as the top 0–15 cm; methods align with the Soils Manual.
- Data and storage:
  - Samples processed or stored at UKCEH sites; soils bank maintained.
- Measured and derived metrics (per sampling point and square):
  - pH in deionised water (PH).
  - Loss on ignition (LOI) and derived soil carbon: LOI, C_CONC_LOI (g C per kg soil), C_STOCK_LOI (t C per ha).
  - Soil organic matter categories (SOIL_GROUP) based on LOI.
  - Bulk density (BULK_DENSITY), moisture content (MOISTURE; MOISTURE_DRY).
  - Total nitrogen (N_PERCENT; N_STOCK).
  - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland.
  - Land Classification (LC07; LC07_NUM) and Environmental Zones (EZ_DESC_07).

## Data Quality Assurance
- Robust QA workflow developed to ensure high data standards; implemented with R scripts and guidance documents.
- Quality control for lab analyses:
  - pH: internal standards and duplicates; acceptance within ±2 SD of batch mean.
  - LOI: internal standards and calcite checks; repeat if deviation exceeds thresholds.
  - Olsen-P and total N: use of standards, blanks, duplicates, and calibration checks.
- Data processing and storage:
  - Data logged in laboratory system; processed and stored in the UKCEH Soil Bank.
  - Ongoing QA integrated into data workflows for rolling surveys.

## Data Structure and Accessibility
- Dataset characteristics:
  - Table 5: 18 columns, 597 rows.
  - -9999 denotes missing samples.
- Key fields:
  - SQUARE (text): 1-km square identifier.
  - PLOT (number): soil sampling location within square.
  - YEAR (number): year of soil sampling.
  - PH, LOI, C_CONC_LOI, C_STOCK_LOI, N_PERCENT, N_STOCK, PO4_OLSEN, BULK_DENSITY, MOISTURE, MOISTURE_DRY.
  - LOI, C_CONC_LOI, C_STOCK_LOI are derived from LOI measurements.
  - SOIL_GROUP: LOI-based soil carbon grouping.
  - LC07, LC07_NUM: ITE Land Classification (2007) details.
  - COUNTRY: GB country (ENG, SCO, WAL).
  - EZ_DESC_07: Countryside Survey Environmental Zone description.
- Data availability and linkage:
  - Linked to environmental classifications (LC07) and environmental zones (EZ_DESC_07) for GIS-enabled analyses.
  - Samples processed in UKCEH labs; data suitable for map-based visualization and change assessment.

## Geospatial Context and Applications for GIS
- Spatial framework ideal for map-based data products:
  - Visualize topsoil properties across GB by 1-km squares and within-square sampling points.
  - Enable analyses of spatial patterns in LOI, soil carbon stocks, nitrogen, phosphorus, and pH in relation to land classes and environmental zones.
- Temporal dimension:
  - Rolling five-year cycles allow mapping of change in soil indicators over time and identification of trends.
- Data integration:
  - Can be combined with vegetation data and other CS datasets for ecosystem-level analyses.

## Endnotes and References
- Methodologies and classifications draw on CS Soils Manual and related CS reports.
- Key references include Emmett et al., Bunce et al., Reynolds et al., and supporting CS documentation on environmental zones and land classification.