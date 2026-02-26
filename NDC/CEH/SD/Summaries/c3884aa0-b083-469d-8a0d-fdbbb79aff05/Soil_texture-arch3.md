# DATA HEADER INFORMATION for Soil_texture.csv

- Overview
  - Records information on soil granulometric analysis.
  - Related project context: ESPA Programme and P4GES project.
  - Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

- Dataset context and provenance
  - Site code: site_ID identifies the P4GES site.
  - Subplot: Indicates the specific subplot where the sample was collected (S1, S2, S3, S4).
  - Intended use: Supports monitoring and evaluation of soil texture-related environmental health indicators.

- Data schema (variables)
  - site_ID
    - Information: P4GES site code
    - Variable Type: Text String
    - Unit: None
  - subplot
    - Information: Subplot where the sample was collected
    - Variable Type: Categorical
    - Unit: S1 / S2 / S3 / S4
  - soil_fraction
    - Information: Granulometric class of soil particles (clay, silt or sand)
    - Variable Type: Categorical
    - Unit: Clay / Silt / Sand
    - Description: Granulometric means relating to the distribution or measurement of grain sizes in soil deposits
  - depth_cm
    - Information: Depth of the sample collection
    - Variable Type: Numeric
    - Unit: cm
  - percentage_value
    - Information: Percentage of the granulometric fraction
    - Variable Type: Numeric
    - Unit: % (percentage)

- Data governance and metadata
  - DOI: Provided (https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05)
  - Data origin and acknowledgements: ESPA; P4GES; Laboratoire des Radio Isotopes, Université d'Antananarivo
  - Usage note: Acknowledgement required for products derived from these data; implies formal data provenance and potential sharing considerations.