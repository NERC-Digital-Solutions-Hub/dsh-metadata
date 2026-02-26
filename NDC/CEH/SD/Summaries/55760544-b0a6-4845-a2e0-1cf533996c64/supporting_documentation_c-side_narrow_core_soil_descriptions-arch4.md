# Data resource description for C_SIDE_narrow_core_soil_description.csv

## Overview
- Dataset describing soil profiles from 474 narrow-diameter cores (30 mm) collected across UK saltmarshes (2018–2021).
- Project: Carbon Storage in Intertidal Environments (C-SIDE); funded by NERC (NE/R010846/1).
- Observations include site locations in decimal longitude/latitude (WGS84) and saltmarsh site names.
- Soil descriptions follow the Troels-Smith classification; depth intervals and transitions recorded.
- Data described and quality-checked by two independent expert observers; final output reconciled from dual descriptions.
- File format: CSV (C_SIDE_narrow_core_soil_description.csv).

## Data content and structure
- Core_ID: Text identifier for each soil core.
- Location: Text, saltmarsh name.
- Depth_interval_cm: Numeric, upper and lower depth horizons of soil transitions.
- Soil_description: Text, Troels-Smith classification description (1955).

## Methods and quality control
- Core description methodology: Descriptions based on Troels-Smith classification (Troels-Smith, 1955) for each 30 mm diameter core.
- Depth transitions recorded as depth_interval_cm.
- Calibration: Not available (NA).
- Data quality: Two experts independently described each core; results combined to form final dataset output.

## Geographic scope and sampling
- Geographic extent: United Kingdom saltmarshes.
- Site selection: Chosen from across the UK coastline to enable representative coverage of diverse saltmarsh habitats.
- Coordinates provided for observations (WGS84).

## Metadata and standards
- Key variables and formats:
  - Core_ID, Location (saltmarsh name) as text.
  - Depth_interval_cm as numeric.
  - Soil_description as text (Troels-Smith classification).
- Troels-Smith (1955) referenced for soil classification; dataset notes and field procedures align with standard soil description practices of the period.

## Data access and format
- Data resource: C_SIDE_narrow_core_soil_description.csv.
- Structure supports straightforward integration into data catalogs and analysis workflows.
- File-level and variable-level metadata accompany the data (as described above).

## References
- Troels-Smith, J., 1955. Characterization of unconsolidated sediments. Reitzels Forlag.

## Implications for data strategy and use
- Provides a standardized, comparable soil description dataset across multiple UK saltmarsh sites, aiding cross-site analyses of soil properties and carbon storage potential.
- Strengths:
  - Standardized classification (Troels-Smith) across many sites.
  - Independent quality control via dual expert descriptions.
  - Clear, machine-readable structure (CSV) with explicit metadata fields.
- Considerations for data leaders:
  - Ensure discoverability and linkage to corresponding location data (coordinates) within the broader data system.
  - Maintain metadata completeness (e.g., consider filling remaining NA fields where possible).
  - Facilitate reuse by aligning with common data standards and incorporating richer metadata (methods, QA notes) for future integration.
  - Be aware of potential subjectivity in soil classifications and document any contextual notes to aid interpretability.