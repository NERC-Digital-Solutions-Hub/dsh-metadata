# DATA HEADER information for Lying_dead_wood_carbon_stock.csv

## Purpose and scope
- Describes biomass stock in the lying dead wood pool, including fallen trees sampled along transects within each plot.

## Provenance and references
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA
- Project: P4GES
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo)
- References: Winrock International 2005. Impact of logging on carbon stocks of tropical forests: the republic of Congo case study. https://www.winrock.org/wp-content/uploads/2016/03/WI-USAID-Logging-Carbon-CongoField-Report-2005.pdf

## Data structure and key fields
- Site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: .
  - Field and materials_resources: .
- Category
  - Information: Classification of the wood density
  - Variable Type: Categorical
  - Unit: S: sound / I: intermediate / R: Rotten
  - Field and materials_resources: .
- Density
  - Information: corresponding density values for the wood category (S, I, R); 0 indicates absent dead wood
  - Variable Type: Numeric
  - Unit: Unitless
  - Field and materials_resources: .
- Diameter
  - Information: Diameter of the dead wood trunk in the transect crossing area
  - Variable Type: Numeric
  - Unit: Centimeter (cm)
  - Field and materials_resources: forester compass
- Volume
  - Information: Estimated volume of the lying dead wood (Winrock International 2005)
  - Variable Type: Numeric
  - Unit: cubic metres (m3)
  - Field and materials_resources: meter
- Biomass
  - Information: Biomass stock of lying dead wood
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field and materials_resources: .
- Stock_C
  - Information: Carbon stock of lying dead wood
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field and materials_resources: 

## Data quality, semantics and notes
- Notes: means no data

## Governance, sharing and attribution considerations
- Data provenance and method: Volume is estimated using the Winrock International (2005) approach; field measurements use a forester’s compass for diameter.
- Sharing/attribution: Acknowledge the data source and the supporting project (P4GES/ESPA); ensure proper citation via the provided DOI.
- Metadata alignment: Ensure consistent interpretation of units (Mg.ha-1 vs mg.ha-1) and the categorical density categories (S, I, R); clarify any discrepancies in the metadata catalog.

## Limitations and considerations for data stewards
- Potential unit confusion between biomass and carbon stock (mg.ha-1 vs Mg.ha-1); verify and harmonize units in the data catalogue.
- Missing data indicated by “Notes: means no data”; handle accordingly in analyses and data discovery.
- Data may involve different field methods and inventory protocols; ensure metadata documents the measurement approaches and any deviations.

## References
- Winrock International 2005. Impact of logging on carbon stocks of tropical forests: the republic of Congo case study. https://www.winrock.org/wp-content/uploads/2016/03/WI-USAID-Logging-Carbon-CongoField-Report-2005.pdf