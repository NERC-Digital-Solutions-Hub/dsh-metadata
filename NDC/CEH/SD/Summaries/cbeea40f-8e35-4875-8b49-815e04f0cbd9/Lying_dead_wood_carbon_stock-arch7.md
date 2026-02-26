# DATA HEADER information for Lying_dead_wood_carbon_stock.csv

## Overview
- Describes biomass stock in the lying dead wood pool, including fallen trees sampled along transects per plot.
- Related to ESPA project P4GES; DOI provided for the dataset.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data fields, types and units
- Site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: .
- Density (Wood category density)
  - Category: Classification of wood density
  - Variable Type: Categorical
  - Unit: S = sound, I = intermediate, R = Rotten
  - Density values correspond to the wood category; 0 indicates absent dead wood
- Density (Numeric value)
  - Density: Corresponding density values for S, I, R
  - Variable Type: Numeric
  - Unit: Unitless
  - Field and materials_ressources: .
- Diameter
  - Information: Diameter of the dead wood trunk in the transect crossing area
  - Variable Type: Numeric
  - Unit: Centimeter (cm)
  - Field and materials_ressources: Forester compass
- Volume
  - Information: Estimated volume of the lying dead wood
  - Variable Type: Numeric
  - Unit: cubic metres (m3)
  - Field and materials_ressources: meter
  - Calculation: Based on Winrock International 2005
- Biomass
  - Information: Biomass stock of lying dead wood
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field and materials_ressources: .
- Stock_C
  - Information: Carbon stock of lying dead wood
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field and materials_ressources: .
Notes
- means no data

## Measurements and methods
- Volume is estimated using the method from Winrock International (2005).
- Data are collected along transects per plot, sampling fallen trees to characterize lying dead wood.

## Data quality and considerations
- Data may include missing values as indicated by notes (means no data).
- Some fields list resources as blank; ensure proper interpretation when integrating with GIS workflows.
- The biomass and carbon stock units appear as Mg.ha-1, but biomass field text states “milligrams per hectare,” which should be confirmed for consistency in downstream analyses.

## Provenance, references and credits
- Reference: Winrock International 2005. Impact of logging on carbon stocks of tropical forests: the republic of Congo case study. (URL provided)
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA; Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data

## How this relates to GIS workflows
- Site_ID serves as a key attribute for linking plots to geospatial records.
- Diameter, Volume, Biomass, and Stock_C provide spatially relevant attributes for map-based summaries of standing/lying dead wood and carbon stocks.
- Data can be integrated with transect geometries to produce spatial visualizations of dead wood carbon stocks and biomass at plot level.