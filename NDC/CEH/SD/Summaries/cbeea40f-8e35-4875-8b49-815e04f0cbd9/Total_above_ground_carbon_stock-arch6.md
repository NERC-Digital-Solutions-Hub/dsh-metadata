# DATA HEADER INFORMATION for Total_above_ground_carbon_stock.csv

## Overview
- This header describes the dataset that summarizes above-ground biomass carbon stocks for each site and subplot.
- Carbon stock components included: trees (>5 cm diameter), saplings (>1.3 m height and <5 cm diameter), standing dead wood, lying dead wood, understorey (herbaceous biomass and small trees <1.3 m), and litter.
- Reference to related material: please also see Manual 1_Classical_Survey.

## Dataset schema
- Site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: (not specified beyond being a site identifier)
- Site_ID, Information
  - Variable type: Text String
- Site_ID, Unit
  - Unit: (not specified beyond being a site identifier)
- subplot
  - Information: subplot where the sample has been collected
  - Variable type: Categorical
  - Unit: S1 / S2 / S3 / S4

## Variables and units (carbon stock components)
- tree_carbon_stock
  - Information: Carbon stock of trees more than 5 centimetres (cm) in diameter
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- saplings_carbon_stock
  - Information: Carbon stock of trees with height >1.3 metres and diameter <5 cm
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- standing_dead_wood_carbon_stock
  - Information: Carbon stock of standing dead wood
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- lying_dead_wood_carbon_stock
  - Information: Carbon stock of lying dead wood
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- understorey_carbon_stock
  - Information: Carbon stock of herbaceous biomass and small trees <1.3 m
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- litter_carbon_stock
  - Information: Carbon stock of litter (leaf litter and root mat)
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)

## Data provenance and references
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA (http://www.espa.ac.uk/)
- Project: P4GES (https://www.p4ges.org)
- Acknowledgement: Required for products derived from these data to acknowledge Laboratoire des Radio Isotopes, Université d'Antananarivo
- Cross-reference: Manual 1_Classical_Survey

## Usage notes
- The header notes that a dash or similar indicator signifies no data available for a given field.
- Outputs may be used to create dashboards, reports, or self-serve data products to explore carbon stock by site and subplot.
- When using outputs, consider data completeness across sites/subplots and reference the provided manual for context on survey methods and data interpretation.