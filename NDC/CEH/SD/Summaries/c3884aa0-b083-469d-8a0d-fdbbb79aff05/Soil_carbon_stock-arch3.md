# DATA HEADER INFORMATION for Soil_carbon_stock.csv

- Purpose and scope
  - Presents soil carbon stock importance and sensitivity to land management at two depths: 0-30 cm and 0-100 cm.
  - Carbon stocks are reported as equivalent mass (Me) or equivalent volume (Ve), calculated from carbon content produced by the MIRS prediction model.
  - Detailed calculations are documented in Manual_1_Classical_Survey.rtf, page 17, section 4.4.

- Provenance and governance
  - Programme: ESPA; Project: P4GES.
  - DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
  - Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.
  - Data sharing and transparency: metadata includes data provenance, variable types, and units; underlying data should be shared with appropriate governance and stewardship.

- Dataset schema and key variables
  - Site_id
    - Information: P4GES site code
    - Variable Type: Text String
    - Unit: .
  - Site_id, Variable Type
    - Information: Text String
    - Variable Type: Text String
    - Unit: .
  - SOC_subplot
    - Information: subplot where the sample was collected
    - Variable Type: Categorical
    - Unit: S1 / S2 / S3 / S4
  - SOC_Me_30
    - Information: soil carbon stock in equivalent mass at 30 cm depth
    - Variable Type: Numeric
    - Unit: Mg.ha-1
  - SOC_Me_100
    - Information: soil carbon stock in equivalent mass at 100 cm depth
    - Variable Type: Numeric
    - Unit: Mg.ha-1
  - SOC_Ve_30
    - Information: soil carbon stock in equivalent volume at 30 cm depth
    - Variable Type: Numeric
    - Unit: Mg.ha-1
  - SOC_Ve_100
    - Information: soil carbon stock in equivalent volume at 100 cm depth
    - Variable Type: Numeric
    - Unit: Mg.ha-1
  - field_material s_ressources
    - Information: (not specified in header; appears empty)
    - Note: Some metadata fields may be incomplete or placeholders.

- Usage considerations for monitoring frameworks
  - Data are depth-segmented (0-30 cm and 0-100 cm) and linked to a predictive model (MIRS), enabling assessment of carbon stock and response to land management.
  - Standardized coding for sites and subplots supports comparability and aggregation across sites.
  - Clear provenance and citation requirements aid in reproducibility and governance of monitoring outputs.

- Potential data quality and accessibility aspects
  - Metadata appears to be fairly detailed for core variables but some fields (e.g., field_material s_ressources) are not populated, indicating room for metadata completion.
  - Access is governed by project-specific authorship and acknowledgement requirements; ensure compliance when sharing or reusing data.