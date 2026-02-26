# DATA HEADER information for Standing_dead_wood_carbon_stock.csv

## Overview
- Records the carbon stock of standing dead trees.
- Associated with ESPA Programme and P4GES project; DOI provided.
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
- Indicates data quality and provenance notes to guide usage.

## Data provenance and access
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA; Project: P4GES
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data schema (fields and definitions)
- site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: none
  - Field materials / resources: .
- DBH
  - Information: diameter of dead wood trunk at 130 cm height
  - Variable type: Numeric
  - Unit: Centimeter
  - Field materials / resources: forester compass
- Diam_base
  - Information: diameter of dead wood trunk at 30 cm height
  - Variable type: Numeric
  - Unit: centimeter
  - Field materials / resources: forester compass
- Diam_top
  - Information: estimated diameter of the top diameter of the dead wood trunk
  - Variable type: Numeric
  - Unit: centimeter
  - Field materials / resources: .
- Height
  - Information: height of the standing dead wood
  - Variable type: Numeric
  - Unit: Meter
  - Field materials / resources: vertex
- Volume
  - Information: volume calculated using the formula Volume = (1/3) * π * H * (r1^2 + r2^2 + r1*r2)
  - Variable type: Numeric
  - Unit: cubic metre (m3)
  - Field materials / resources: .
- Category
  - Information: Classification of the wood density
  - Variable type: Categorical
  - Unit: S (sound) / I (intermediate) / R (rotten)
  - Field materials / resources: .
- Density
  - Information: Density
  - Variable type: Numeric
  - Unit: (not specified)
  - Field materials / resources: .
- Carbon_stock
  - Information: Carbon stock of standing dead wood
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field materials / resources: .

## Data usage and interpretation notes
- Volume is derived from height and diameters using the provided formula; r1 corresponds to base diameter, r2 to top diameter.
- Wood-density category uses codes S, I, R to indicate quality/condition.
- Carbon stock is expressed per hectare; ensure alignment with spatial units when mapping.
- Missing data is indicated by explanatory notes in the dataset (Notes: means no data available).

## GIS-specific considerations
- Site-level keys (site_ID) enable joins to spatial layers for map-based visualization of standing dead wood carbon stock.
- Ensure consistent units across fields when performing analyses or aggregations (e.g., volumes in m3, carbon stock in Mg.ha-1).
- Data may be stored across multiple sources; verify provenance and attribution per the DOI and project information.

## Summary of constraints and best practices
- Attribute fields vary in data type (numeric, text, categorical); handle accordingly in GIS workflows.
- Validate that units are correctly interpreted (especially Volume and Carbon_stock) during integration.
- Respect attribution requirements for any products derived from these data.