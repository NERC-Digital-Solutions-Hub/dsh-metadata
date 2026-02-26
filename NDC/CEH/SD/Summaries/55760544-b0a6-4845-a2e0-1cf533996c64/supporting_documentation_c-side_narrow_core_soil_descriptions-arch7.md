# Data resource description for C_SIDE_narrow_core_soil_description.csv

- Project and funding
  - Project: Carbon Storage in Intertidal Environments (C-SIDE)
  - Funded by: Natural Environment Research Council (NERC) NE/R010846/1

- Dataset scope
  - Soil profiles described from narrow-diameter cores (30 mm) collected from UK saltmarshes
  - 474 sampling sites across UK saltmarshes
  - Data collection period: 2018–2021
  - Core descriptions use Troels-Smith classification; depth transitions recorded

- Spatial coverage
  - UK saltmarsh locations; study extent described as a set of site locations with decimal coordinates (WGS84)
  - Bounding extents provided: 
    - 60.973491, -8.019200
    - 60.973491, 2.176113
    - 49.844006, -8.019200
    - 49.844006, 2.176113
  - Per-record coordinates are not included in the CSV; site locations are described at the study level (to enable map-based representation when joined with external site coordinates)

- Data content and structure
  - Data resource: C_SIDE_narrow_core_soil_description.csv
  - Fields (per core/record):
    - Core_ID: Text (core identification)
    - Location: Text (saltmarsh name)
    - Depth_interval_cm: Number (upper and lower depth horizons of soil transitions)
    - Soil_description: Text (description following Troels-Smith classification)
  - Observational details
    - 474 soil core profiles described
    - Observations conducted by two experts independently; descriptions merged for final output
  - Calibration and statistics
    - Calibration: not applicable
    - Statistical treatment: not applicable
    - Data checking: two independent expert descriptions followed by consolidation

- Data format and access
  - File format: CSV
  - Additional notes: NA indicates no data in cells

- GIS usage notes
  - Suitable for map-based visualization of soil descriptions across UK saltmarshes
  - Depth_interval_cm provides depth-resolved soil information for each core
  - Soil_description (Troels-Smith) offers a categorical attribute for classification-based symbolization
  - To map at a per-core level, join the CSV to a site-level point dataset containing coordinates (WGS84); per-core coordinates are not included in the CSV itself
  - Useful for comparative analyses across sites and integration into carbon storage and habitat models

- References
  - Troels-Smith, J. (1955). Characterization of unconsolidated sediments. Reitzels Forlag