# Soil profile descriptions from narrow diameter cores in UK saltmarshes collected between 2018 and 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Data resource describes soil profiles from 474 narrow-diameter cores collected across UK saltmarshes between 2018 and 2021
- Purpose aligned with analysing soil properties for carbon storage in intertidal environments
- Observations include geospatial coordinates (decimal degrees, WGS84) outlining UK extent and site distribution to capture diverse saltmarsh habitats

## Data Coverage and Location
- Geographic extent: United Kingdom; observation coordinates provided as decimal latitude/longitude (WGS84)
- Site selection intended to represent a diverse range of UK saltmarsh habitats and coastal regions
- Bounding coordinates referenced: 60.973491, -8.019200; 60.973491, 2.176113; 49.844006, -8.019200; 49.844006, 2.176113

## Variables and Observations
- Core_ID: unique identifier for each soil core
- Location: saltmarsh name (descriptor for the observation site)
- Depth_interval_cm: numeric upper and lower depth horizons for soil transitions
- Soil_description: description of soil using the Troels-Smith classification (1955)

## Data Collection and Quality Assurance
- Core details: 474 narrow-diameter cores (30 mm) described in field/lab contexts
- Observations described using Troels-Smith classification; depth transitions recorded
- Quality control: two experts independently described each core; independent descriptions merged to form the final dataset
- Calibration procedures: not specified (NA)

## Data Format and Access
- File format: CSV
- Data resource: C_SIDE_narrow_core_soil_description.csv
- Columns (as described in the dataset):
  - Core_ID: Text
  - Location: Saltmarsh name (Text)
  - Depth_interval_cm: Number (upper and lower depth horizons)
  - Soil_description: Troels-Smith classification (Text)

## Project Context and Related Metadata
- Data resource description and association with the C-SIDE project emphasize soil profiles for carbon storage analyses
- Troels-Smith (1955) referenced for soil classification methodology

## Limitations and Considerations for Analysts
- Local-scale data coverage may limit broad generalizations without supplementary datasets
- Potential data accessibility considerations if integrating with other systems (e.g., coordination with other site-level datasets)
- The core descriptions rely on expert interpretation (Troels-Smith classification), which may introduce subjectivity
- Calibration details are not provided in the summary; users should verify any required methodological specifics

## References
- Troels-Smith, J., 1955. Characterization of unconsolidated sediments. Reitzels Forlag.