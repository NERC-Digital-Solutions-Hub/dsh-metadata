# Soil profile descriptions from narrow diameter cores in UK saltmarshes collected between 2018 and 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: Natural Environment Research Council (NERC), NE/R010846/1
- Dataset describes soil profiles from 474 narrow-diameter cores (30 mm) collected across UK saltmarshes between 2018 and 2021
- Data resource file: C_SIDE_narrow_core_soil_description.csv
- Purpose: document soil profiles to support cross-site comparisons and carbon storage research; enable discovery and reuse by others

## Dataset scope and content
- 474 sampling sites across UK saltmarshes
- Variables/fields included in the dataset:
  - Core_ID (text): unique core identifier
  - Location (text): saltmarsh name
  - Depth_interval_cm (number): upper and lower depth horizons of soil transitions
  - Soil_description (text): Troels-Smith classification of soil description
- Observation method: soil cores described using the Troels-Smith (1955) scheme; depth transitions recorded
- Quality control: observations described independently by two experts; descriptions combined to form the final output
- Format: CSV; file uses percent-compatible metadata conventions (e.g., NA indicating missing data where applicable)

## Spatial and temporal coverage
- Geographic extent: United Kingdom; coordinates provided (WGS84)
- Site locations chosen to represent UK saltmarsh environments and enable comparability across similar ecological regions
- Temporal window: data collection and description conducted during 2018–2021

## Data structure and metadata
- Core_ID: Text
- Location: Text (saltmarsh name)
- Depth_interval_cm: Number (upper and lower soil horizons)
- Soil_description: Text (Troels-Smith classification)
- Data quality notes: dual-describer approach; final output reflects combined assessments
- Calibration/statistical procedures: not applicable (NA where not used)

## Data collection and quality assurance
- Procedures: description of 474 narrow-diameter cores; Troels-Smith classification with depth transitions recorded
- Quality assurance: two independent expert descriptions per core; discrepancies reconciled to produce the final description
- Calibration and statistical analyses: not provided (NA)

## Data access, formats, and sharing
- File format: CSV (C_SIDE_narrow_core_soil_description.csv)
- Metadata fields documented above; coordinates in decimal degrees (WGS84)
- Access considerations: standard governance practices apply; ensure compliance with data sharing limitations and update mechanisms

## Provenance and references
- Troels-Smith, J., 1955. Characterization of unconsolidated sediments. Reitzels Forlag (classification basis for soil descriptions)
- Project context: C-SIDE, carbon storage research in intertidal environments; funded by NERC

## Data stewardship and governance considerations
- Ensure metadata completeness and accuracy (Core_ID, Location, Depth_interval_cm, Soil_description)
- Maintain interoperability by adhering to Troels-Smith classification and consistent depth interval documentation
- Respect data sharing limitations; establish clear update and versioning processes for future data additions or revisions
- Catalog and publish datasets to relevant portals; document data provenance and processing steps
- Monitor for incomplete user requirements and plan for additional data or metadata enhancements as needed

## Risks and mitigation
- Missing data fields (NA): document why data are missing and consider providing guidance for users on interpretation
- Interoperability: ensure consistent class definitions and naming across datasets
- Updates: implement a version-controlled update mechanism to incorporate new cores or re-descriptions without breaking existing references