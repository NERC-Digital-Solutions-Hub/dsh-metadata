# DATA HEADER INFORMATION for Description_of_soil_profile.csv

- Overview
  - Dataset records soil profile pit descriptions collected during field sessions.
  - Used within the ESPA Programme and P4GES project.
  - Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
  - Related documentation: Manual_1_Classical_Survey, page 13, section 2.3.3.2; DOI provided.

- Key fields and data types
  - Site_ID
    - Type: Text string
    - Information: P4GES site code
  - Horizon
    - Type: Text string
    - Information: Name of the soil horizon
  - depth_cm
    - Type: Numeric
    - Information: Depth of the soil horizon (cm)
    - Notes: 0–10 means surface to 10 cm; 22–53 means 23–53 cm
  - color
    - Type: Text string
    - Information: Soil layer color according to Munsell code
  - texture
    - Type: Categorical
    - Information: Field-estimated soil texture
    - Values: Clayey, Sandy, Sandy-Clayey, Silty-Clayey, Clay-sandy
  - structure
    - Type: Categorical
    - Information: Observed soil structure
  - root_importance
    - Type: Numeric
    - Information: Coverage percentage of roots observed in the soil layer
  - porosity
    - Type: Numeric
    - Information: Percentage of small porosity holes observed in the soil layer

- Units
  - depth_cm: centimeters (cm)
  - root_importance: percent (%)
  - porosity: percent (%)
  - Other fields: text or categorical; no units specified beyond indicates

- Data quality and missing data
  - Blank cells/NA = no data
  - Potential variability in field estimates (texture, horizon naming, structure)
  - Data may require cleaning, standardization, and integration with other datasets

- Documentation and references
  - See Manual_1_Classical_Survey (section 2.3.3.2) for definitions and methodology
  - DOI link provided for the dataset
  - Programme: ESPA; Project: P4GES

- Usage considerations for analysts
  - Useful for analyzing soil profiles by horizon and depth, informing models of soil properties
  - Requires careful handling of missing data and variable field estimations
  - Ensure proper attribution and acknowledgment in outputs
  - Facilitates data discovery and interoperability when datasets are annotated with metadata and linked to related documentation