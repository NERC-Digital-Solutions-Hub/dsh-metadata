# DATA HEADER INFORMATION for Soil_texture.csv

## Overview
- The dataset records soil granulometric analysis data, linking sample fractions to their collection context (site, subplot, depth) and the measured proportion of each fraction.
- Associated with the ESPA programme and the P4GES project.
- Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.
- See Manual_3_ Laboratory_works.rtf page 2 for additional details.

## Data schema

- site_ID
  - Type: Text String
  - Information: P4GES site code identifying the sampling location
  - Unit: 

- subplot
  - Type: Categorical
  - Information: Subplot where the sample was collected
  - Unit: S1 / S2 / S3 / S4

- soil_fraction
  - Type: Categorical
  - Information: Granulometric class of soil particles
  - Unit: Clay / Silt / Sand
  - Note: Granulometric means relate to the distribution or measurement of grain sizes in soils

- depth_cm
  - Type: Numeric
  - Information: Depth of the sample collection
  - Unit: cm

- percentage_value
  - Type: Numeric
  - Information: Percentage of the granulometric fraction
  - Unit: %