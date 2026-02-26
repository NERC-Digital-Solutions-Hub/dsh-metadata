# DATA HEADER INFORMATION for Total_above_ground_carbon_stock.csv

## Overview
- Summaries carbon stocks on each site and subplot for the total above-ground biomass pool.
- Components included: trees, saplings, understorey, standing dead wood, lying dead wood, and litter.

## Provenance and acknowledgement
- Programme: ESPA; Project: P4GES.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data structure
- Site_ID: P4GES site code; information type Text String.
- subplot: subplot where the sample was collected; information type Categorical; unit values S1, S2, S3, S4.
- Variables (carbon stock components) are numeric and represent carbon stock for each component.

## Field definitions

- tree_carbon_stock
  - Information: Carbon stock of trees > 5 cm in diameter.
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

- saplings_carbon_stock
  - Information: Carbon stock of trees >1.3 m tall and <5 cm diameter.
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

- standing_dead_wood_carbon_stock
  - Information: Carbon stock of standing dead wood.
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

- lying_dead_wood_carbon_stock
  - Information: Carbon stock of lying dead wood.
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

- understorey_carbon_stock
  - Information: Carbon stock of herbaceous biomass and small trees <1.3 m height.
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

- litter_carbon_stock
  - Information: Carbon stock of litter (leaf litter and root mat).
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

## Data quality and notes
- Notes indicate “means no data available” for missing entries; absence of a value implies no data for that site/subplot/component.

## Considerations for GIS application
- Data are at the subplot level within sites, suitable for map-based visualization of spatial carbon stock distribution.
- Ensure consistent unit interpretation (Mg.ha-1) despite the stated unit wording (note potential discrepancy with “milligrams per hectare” in metadata).
- Be mindful of missing data when joining with other datasets or aggregating by site or subplot.