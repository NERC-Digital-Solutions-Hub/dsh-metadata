# DATA HEADER INFORMATION for Soil_carbon_content.csv

## Overview
- Dataset contains soil organic carbon content (SOC) estimated using the MIRS prediction model.
- Supports environmental monitoring by providing standardized SOC data across sampling sites and subplots.
- Associated with ESPA programme and P4GES project; DOI provided.
- Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

## Data Source and Scope
- Source: P4GES monitoring sites; data processed with a Metho d using MIRS model.
- Related documentation: Manual_1_Classical_Survey.rtf, page 17, section 4.4.
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05

## Data Fields and Units
- Site_id
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: .
- SOC_subplot
  - Information: subplot where sampling was conducted
  - Variable Type: Categorical
  - Unit: S1 / S2 / S3 / S4
- SOC_sampling_depth
  - Information: depth of the sampled soil layer
  - Variable Type: Numeric
  - Unit: centimeter
- SOC_content
  - Information: Carbon content of the sample (g/kg of soil) generated using MIRS prediction model
  - Variable Type: Numeric
  - Unit: grammes per kilo (g.kg-1)

## Data Processing and Quality
- Data are generated via the MIRS prediction model and follow standardized data formats for comparability.
- Data handling aligns with ESPA/P4GES protocols; data quality is maintained through established sourcing and processing procedures.

## Data Accessibility and Use
- Datasets should be stored and uploaded to the appropriate data portals as part of routine monitoring outputs.
- Appropriate acknowledgments must be made when using products derived from these data.

## Application for Environmental Monitoring
- Enables consistent reporting of soil carbon status over time.
- Facilitates integration with other environmental datasets to enhance analysis beyond single-use datasets.
- Supports clear presentation formats (e.g., maps, charts) for policy and health assessments.