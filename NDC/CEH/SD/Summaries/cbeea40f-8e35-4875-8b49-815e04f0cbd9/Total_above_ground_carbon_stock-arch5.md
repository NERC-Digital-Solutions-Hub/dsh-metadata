# DATA HEADER INFORMATION for Total_above_ground_carbon_stock.csv

## Overview
- Data header describing carbon stock data for total above-ground biomass across sites and subplots.
- Components included: trees, saplings, understorey, standing dead wood, lying dead wood, and litter.
- Associated with ESPA Programme and P4GES Project.
- DOI provided for dataset access.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data model and fields
- Identifier and location
  - Site_ID: P4GES site code; Information = Site_ID is text string.
  - Subplot: Information = subplot where the sample was collected; Variable type = Categorical; Unit = S1/S2/S3/S4.
- Core data fields (carbon stocks, numeric)
  - tree_carbon_stock: carbon stock of trees >5 cm diameter; Variable type = Numeric; Unit = milligrams per hectare (Mg.ha-1).
  - saplings_carbon_stock: carbon stock of saplings (height >1.3 m and diameter <5 cm); Numeric; Mg.ha-1.
  - standing_dead_wood_carbon_stock: carbon stock of standing dead wood; Numeric; Mg.ha-1.
  - lying_dead_wood_carbon_stock: carbon stock of lying dead wood; Numeric; Mg.ha-1.
  - understorey_carbon_stock: carbon stock of herbaceous biomass and small trees <1.3 m; Numeric; Mg.ha-1.
  - litter_carbon_stock: carbon stock of litter and root mat; Numeric; Mg.ha-1.
- Notes on data completeness
  - Notes indicate that “means no data available” for missing entries.

## Provenance and usage terms
- Data source: ESPA Programme; Project P4GES.
- DOI provided for dataset identification and access.
- Usage attribution requirement: Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data quality and governance considerations
- Potential unit inconsistency: described as "milligrams per hectare" but labeled Mg.ha-1; verify and harmonize units across systems.
- Metadata completeness: ensure Site_ID, Subplot, and all six carbon stock fields are present for each record; handle missing data per the dataset notes.
- Interoperability: dataset spans multiple sites/subplots; ensure consistent categoricals (S1–S4) and consistent site coding for integration with other datasets.

## Practical implications for data stewards
- Validate and standardize units (confirm Mg.ha-1 vs mg/ha) before integration into central catalogs.
- Maintain attribution metadata (DOI, project/program names, acknowledgment phrasing).
- Capture missing data semantics and document any data imputation or exclusions.
- Ensure provenance trails include records of data creators, transformations, and quality checks.