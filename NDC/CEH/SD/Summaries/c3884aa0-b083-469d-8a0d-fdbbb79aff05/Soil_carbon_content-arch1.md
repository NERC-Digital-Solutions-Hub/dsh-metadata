# DATA HEADER INFORMATION for Soil_carbon_content.csv

## Overview
- Contains soil organic carbon content measured using the MIRS prediction model.
- Associated with ESPA programme and the P4GES project.
- DOI provided for data reference.
- Acknowledgement required for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Data schema (fields, types, units)
- Site_id
  - Type: Text String
  - Information: P4GES site code
  - Unit: .
- SOC_subplot
  - Type: Categorical
  - Information: Subplot where sampling was conducted
  - Unit: S1 / S2 / S3 / S4
- SOC_sampling_depth
  - Type: Numeric
  - Information: Depth of the sampled soil layer
  - Unit: centimeter
- SOC_content
  - Type: Numeric
  - Information: Carbon content of the sample generated using the MIRS prediction model
  - Unit: grammes per kilo (g.kg-1)