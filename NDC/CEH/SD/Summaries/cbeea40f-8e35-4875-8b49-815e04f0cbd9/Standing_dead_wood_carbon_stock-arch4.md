# DATA HEADER information for Standing_dead_wood_carbon_stock.csv

## Overview
- Dataset records the carbon stock of standing dead wood.
- Programme: ESPA; Project: P4GES.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Key fields and definitions
- site_ID
  - Information: P4GES site code
  - Variable type: Text String
- Surface
  - Information: not specified in header
  - Variable type: not specified
- DBH
  - Information: diameter of dead wood trunk at 130 cm height
  - Variable type: Numeric
  - Unit: Centimeter
  - Field materials/resources: forester compass
- Diam_base
  - Information: diameter at 30 cm height
  - Variable type: Numeric
  - Unit: Centimeter
  - Field materials/resources: forester compass
- Diam_top
  - Information: estimated diameter at the top of the trunk
  - Variable type: Numeric
  - Unit: Centimeter
- Height
  - Information: height of the standing dead wood
  - Variable type: Numeric
  - Unit: Meter
  - Field materials/resources: vertex
- Volume
  - Information: volume calculated using V = (1/3) * π * H * (r1^2 + r2^2 + r1*r2)
  - Variable type: Numeric
  - Unit: cubic metre (m3)
  - H: total height; r1: base radius; r2: top radius
- Category
  - Information: classification of wood density
  - Variable type: Categorical
  - Unit: S (sound) / I (intermediate) / R (rotten)
  - Field materials/resources: not specified
- Density
  - Information: wood density
  - Variable type: Numeric
  - Unit: not explicitly stated
- Carbon_stock
  - Information: carbon stock of standing dead wood
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field materials/resources: not specified

## Calculation and measurement notes
- Volume is derived from trunk dimensions using a frustum-like formula with base and top radii.
- Height, diameters, and density measurements have specific units (cm, m) and may rely on field tools (e.g., forester compass).
- Some fields show placeholder or missing information in the header (e.g., Surface).

## Data governance, provenance, and access
- Provenance: ESPA/P4GES project data; associated DOI provided.
- Usage rights: acknowledge Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Metadata completeness: header includes definitions and units for several variables, but some fields (e.g., Surface) have unspecified information.

## Data quality, limitations, and considerations for use
- Notes indicate "means no data available" for missing values in certain fields.
- Data completeness may vary by site; units and measurement methods should be harmonized when integrating with other datasets.
- The unit for Carbon_stock (milligrams per hectare) appears unusual and should be verified against documentation before aggregation or comparison.

## Implications for Data Leaders
- Emphasize clear metadata standards (consistent units, field definitions, and measurement methods) to improve discoverability and interoperability.
- Track data provenance (project/DOI) and required acknowledgements to ensure proper use.
- Identify and address data gaps (e.g., surfaces, missing field resources) to support portfolio-wide data strategy and cross-team collaboration.
- Ensure data quality control around derived metrics (volume calculation) and unit consistency across datasets.