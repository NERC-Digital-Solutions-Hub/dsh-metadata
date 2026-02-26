# DATA HEADER INFORMATION for Soil_texture.csv

- Purpose and scope
  - This dataset records information on soil granulometric analysis and is linked to the ESPA Programme and P4GES project.
  - Acknowledgement is required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

- Provenance and references
  - DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
  - Programme: ESPA (http://www.espa.ac.uk/)
  - Project: P4GES (https://www.p4ges.org)
  - Related documentation: Manual_3_ Laboratory_works.rtf, page 2

- Data schema (fields and definitions)
  - site_ID
    - Information: P4GES site code
    - Variable Type: Text String
    - Unit: (none)
  - subplot
    - Information: Subplot where the sample was collected
    - Variable Type: Categorical
    - Unit: S1 / S2 / S3 / S4
  - soil_fraction
    - Information: Granulometric class of soil particles (clay, silt or sand)
    - Variable Type: Categorical
    - Unit: Clay / Silt / Sand
  - depth_cm
    - Information: Depth of the sample collection
    - Variable Type: Numeric
    - Unit: cm
  - percentage_value
    - Information: Percentage of the granulometric fraction
    - Variable Type: Numeric
    - Unit: % (percent)

- How to interpret the data
  - Each row corresponds to a specific site, subplot, depth, and soil_fraction, with the associated percentage_value representing the fraction of that granulometric class at that depth.

- Usage notes
  - Data is suitable for analyzing granulometric distributions across sites, subplots, and depths, and can be used to build summary tables or visualizations (e.g., bar charts, depth profiles) to enable exploration of soil texture.

- Related documentation
  - See Manual_3_ Laboratory_works.rtf (page 2) for additional context on data collection and definitions.