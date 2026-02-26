# DATA HEADER information for Standing_dead_wood_carbon_stock.csv

## Overview
- The dataset records the carbon stock of standing dead wood (standing dead trees).
- Linked to Programme ESPA and Project P4GES, with a DOI provided for the data product.
- Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Key fields and definitions
- site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: not applicable
  - Field materials/resources: not specified
- Surface
  - Information: unspecified
  - Variable type: unspecified
  - Unit: not applicable
  - Field materials/resources: not specified
- DBH
  - Information: diameter of dead wood trunk at 130 centimetre height
  - Variable type: Numeric
  - Unit: Centimeter
  - Field materials/resources: forester compass
- Diam_base
  - Information: diameter of dead wood trunk at 30 cm height
  - Variable type: Numeric
  - Unit: centimeter
  - Field materials/resources: forester compass
- Diam_top
  - Information: estimated diameter of the top diameter of the dead wood trunk
  - Variable type: Numeric
  - Unit: centimeter
  - Field materials/resources: not specified
- Height
  - Information: height of the standing dead wood
  - Variable type: Numeric
  - Unit: Meter
  - Field materials/resources: vertex
- Volume
  - Information: volume calculated using the formula: volume = 1/3 * π * H * (r1^2 + r2^2 + r1*r2); H = total height; r1 = diameter at base; r2 = diameter at top
  - Variable type: Numeric
  - Unit: cubic metre (m^3)
  - Field materials/resources: not specified
- Category
  - Information: Classification of the wood density
  - Variable type: Categorical
  - Unit: S: sound / I: intermediate / R: rotten
  - Field materials/resources: not specified
- Density
  - Information: not specified
  - Variable type: Numeric
  - Unit: not specified
  - Field materials/resources: not specified
- Carbon_stock
  - Information: Carbon stock of standing dead wood
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field materials/resources: not specified

## Metadata, provenance, and governance
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA
  - Programme URL: http://www.espa.ac.uk/
- Project: P4GES
  - Project URL: https://www.p4ges.org
- Publication/derivation acknowledgements: Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Measurement context and data quality notes
- Field methods indicated by field materials/resources:
  - DBH, Diam_base: forester compass
  - Height: vertex
- Volume formula explicitly provided, linking H, base/top diameters to volume
- Notes mention: "Notes - means no data available" indicating a missing data flag or indicator within the dataset

## Data stewardship and lifecycle considerations
- Data reception and integration:
  - Data is received with defined field descriptions and is uploaded to portals and catalogues as part of data holdings
- Quality assurance and transformation:
  - Data steadying involves ensuring metric consistency (units), dimensional consistency (base/top diameters, height), and correct application of the volume formula
- Metadata and discoverability:
  - Clear field-level metadata, unit definitions, and measurement methods aid discoverability and reuse
- Sharing and governance:
  - Acknowledgement requirements should be enforced for derived products
  - Versioning and updates to the dataset should be handled while preserving provenance
- Potential data governance considerations:
  - Ensure compatibility across systems and formats when integrating with other datasets
  - Manage missing data indicators and communicate data availability to users

## Practical considerations for Data Stewards
- Verify completeness of field metadata (especially Density and Carbon_stock units/definitions)
- Confirm unit consistency across all records (e.g., ensure all lengths in centimeters, heights in meters)
- Maintain provenance information (DOI, programme/project links, acknowledgement requirements)
- Establish clear data update pipelines to handle updates and embargoes if present
- Document any non-interoperable field measurements or bespoke equipment notes (e.g., vertex, forester compass) to aid future data users