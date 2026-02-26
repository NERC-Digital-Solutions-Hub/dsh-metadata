# DATA HEADER information for Understorey_carbon_stock.csv

## Overview
- The dataset records the carbon stock of the understorey herbaceous plant cluster.
- Derived from samples collected in 1 m x 1 m subplots as part of the ESPA programme (Project P4GES).
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- DOI provided for the data: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Data likely intended for GIS use and map-based analysis to quantify and display understorey carbon/biomass.

## Data fields and metadata
- Field: site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: none (represented as .)
- Field: Subplot
  - Information: subplot where the sample was collected
  - Variable type: Categorical
  - Unit: S1 / S2 / S3 / S4
- Field: Area
  - Information: Size of area sampled = 1m x 1m
  - Variable type: Numeric
  - Unit: square metre (m2)
- Field: Species
  - Information: Species observed in sample
  - Variable type: (not specified in the header)
  - Unit: (not specified in the header)
- Field: freshweight
  - Information: Total fresh weight
  - Variable type: Numeric
  - Unit: grams
- Field: freshweight_sample
  - Information: Fresh weight of subsample taken from the total understorey collected in the quadrat
  - Variable type: Numeric
  - Unit: grams
- Field: dry_weight_sample
  - Information: Dry weight of subsample taken from the total understorey collected in the quadrat after drying in laboratory
  - Variable type: Numeric
  - Unit: grams
- Field: Biomasse
  - Information: Biomass stock of understorey
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- Field: Stock_C
  - Information: Carbon stock of understorey
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

Notes:
- -, NA and blank cells mean no data available.

## Data provenance and references
- Programme: ESPA
- Project: P4GES
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required for outputs derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo

## Data quality and considerations
- Data include multiple fields with explicit units and some fields lacking defined variable types in the header (Species, possibly others).
- Missing data indicated by -, NA, or blank cells.
- Units are specific (e.g., Biomasse and Stock_C in Mg.ha-1) and should be standardized when integrating with other datasets.

## GIS usage considerations
- Use site_ID to join with location/shapefile attributes for spatial mapping of carbon stock and biomass.
- Subplot and Area define the spatial resolution (1 m x 1 m subplot; Area = 1 m2 per sample).
- Normalize or convert Biomasse and Stock_C values if needed to align with project-specific units.
- Handle missing data appropriately during analysis (e.g., imputation or masking).
- Ensure species and weight fields are consistently formatted for filtering or thematic mapping.