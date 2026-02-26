# This document is a supplement to the supporting documentation for data series detailed in: 'Turf2Surf_WP2_Supporting_documentation.rtf'

## Purpose and scope
- Supplements the data series documentation for soil carbon data in the Conwy catchment (North Wales) for 2013 and 2014.
- Indicates that the soil carbon dataset is described in Turf2Surf_Soil_carbon_data.csv and that several related datasets share the same initial structure.

## Data structure and key fields
- Shared structure: the first 9 columns are consistent across these datasets.
- Column A: Site Number (unique identifier for each site).
- Column B: Habitat.
- Column C: Habitat description.
- Column D: Site name.
- Column E: Ecosystem Component (plant, soil, or roots).
- Column F: Plant species (if Component is Plant); otherwise NA.
- Columns G and H: Plot number (1–4) and Replicate number (for non-coincident measurements based on dominant species).
- Column I: Soil depth interval (applicable to soil and roots components).
- Column J: Soil carbon (kg C m-2) at the specified depth interval (NA if not measured).
- The dataset Turf2Surf_Soil_carbon_data.csv contains 469 rows, including the header row.

## Data relationships and context
- The soil carbon dataset is one of several related datasets that share the same initial columns, including:
  - Plant structural measurements (North Wales and NW England, 2013–2014)
  - Plant biomass measurements (Conwy catchment, 2013–2014)
  - Plant physiological measurements (North Wales and NW England, 2013–2016)
  - Soil measurements (physical, chemical, biological) in the Conwy catchment (2013–2014)

## Data quality and missing data
- Missing values are represented as NA, indicating data not available due to constraints such as limited soil depth, restricted replicates, or outliers.
- NA appears in fields where data were not collected or not applicable (e.g., non-plant components in the Plant species column, depth intervals for some components).

## Implications for data leaders
- Discoverability and integration: identical first-9-column structure across datasets supports cross-dataset searches and integration.
- Metadata importance: consistent habitat descriptions, accurate species information, and clear depth interval definitions are crucial for usability.
- Data gaps and limitations: NA entries point to data gaps in depth coverage and measurements; plan for supplementation or careful handling in analyses.
- Provenance and documentation: this dataset is a supplement to Turf2Surf WP2 documentation; ensure traceability to the Turf2Surf project and maintain linkage to related data series.
- Governance needs: maintain metadata standards, coordinate updates across related datasets, and manage data sharing with appropriate disclosures of missing values and measurement limitations.

## Suggested actions for data management
- Harmonize and standardize habitat descriptions and plant species nomenclature across all related datasets.
- Document depth intervals clearly and consistently; flag any non-standard depth ranges.
- Establish data quality checks for NA entries, ensuring transparent reporting of data availability and limitations.
- Ensure robust metadata and cross-linking between Turf2Surf data files and supporting documentation.