# DATA HEADER information for Lying_dead_wood_carbon_stock.csv

## Overview
- Describes the biomass stock in the lying dead wood pool, including fallen trees sampled along a transect line for each plot.
- Supports environmental monitoring efforts under ESPA (Programme) and P4GES (Project).
- Acknowledges the need to cite Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Includes a DOI for the dataset and references to related documentation (Manual 1_Classical_Survey).

## Dataset scope and context
- Data header provides the structure, variables, and units used for lying dead wood carbon stock estimations.
- Used within environmental monitoring workflows to standardize reporting of dead wood density, volume, biomass, and carbon stock across plots.

## Variables and measurements
- Site_ID: P4GES site code; text string identifying the sampling location.
- Category: Wood density category; Categorical (S: sound, I: intermediate, R: Rotten).
- Density: Associated density values for wood category; Numeric; Unitless; 0 indicates absence of dead wood.
- Diameter: Diameter of the dead wood trunk along the transect; Numeric; Unit: centimeters (cm).
- Volume: Estimated volume of lying dead wood; Numeric; Unit: cubic metres (m3); estimated using methods from Winrock International 2005.
- Biomass: Biomass stock of lying dead wood; Numeric; Unit: milligrams per hectare (Mg.ha-1).
- Stock_C: Carbon stock of lying dead wood; Numeric; Unit: milligrams per hectare (Mg.ha-1).
- Notes: Indicates missing data with a value of "means no data" where applicable.

## Data quality and handling
- Data header outlines required data fields, their types, and units, enabling standard quality assurance and transformation.
- Missing data is explicitly acknowledged via the “Notes” entry (means no data).

## Methodology and references
- Volume estimation method attributed to Winrock International 2005 (Impact of logging on carbon stocks of tropical forests: Republic of Congo case study).
- Reference provided via DOI/link: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9

## Data access and provenance
- Programme: ESPA (Environmental Science for a Practical, sustainable environment) and Project: P4GES.
- Data products require acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo for derived outputs.
- Data and related outputs should be stored and uploaded to appropriate data portals as part of standard monitoring workflows.

## Related documentation
- Manual 1_Classical_Survey referenced for additional context on survey methods and data collection protocols.

## Key challenges and opportunities for analysts
- Challenge: Increase the value of lieing dead wood datasets by integrating with other relevant datasets to avoid single-use outputs.
- Challenge: Improve accessibility of underlying data used to generate final outputs, enabling broader reuse and validation.
- Opportunity: Align data with standardized formats to support cross-plot and temporal comparisons for monitoring environmental health and policy performance.