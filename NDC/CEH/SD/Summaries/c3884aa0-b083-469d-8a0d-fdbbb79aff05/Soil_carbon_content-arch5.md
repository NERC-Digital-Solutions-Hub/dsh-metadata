# DATA HEADER INFORMATION for Soil_carbon_content.csv

- Overview
  - Dataset contains soil organic carbon content, obtained by using the MIRS prediction model.
  - Reference to Manual_1_Classical_Survey.rtf page 17, section 4.4.
  - DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
  - Programme: ESPA; Project: P4GES.
  - Acknowledgement required: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

- Provenance and references
  - Data linked to P4GES sites; metadata includes site identifiers and sampling details.
  - Access to broader documentation via the cited manual and project pages.

- Data schema and fields
  - Site_id
    - Information: P4GES site code
    - Variable Type: Text String
    - Unit: .
  - SOC_subplot
    - Information: subplot where the sampling was done
    - Variable Type: Categorical
    - Unit: S1 / S2 / S3 / S4
  - SOC_sampling_depth
    - Information: depth of the sampled soil layer
    - Variable Type: Numeric
    - Unit: centimeter
  - SOC_content
    - Information: Carbon content of the sample (g/kg of soil) generated using the MIRS prediction model
    - Variable Type: Numeric
    - Unit: grammes per kilo (g.kg-1)

- Data use and governance notes for data stewards
  - Ensure metadata accuracy and consistency with the described fields and units.
  - Maintain provenance links to the MIRS model and the referenced manual.
  - Respect acknowledgment requirements for products derived from these data.
  - Verify dataset discovery through appropriate portals and ensure updates are reflected in metadata.