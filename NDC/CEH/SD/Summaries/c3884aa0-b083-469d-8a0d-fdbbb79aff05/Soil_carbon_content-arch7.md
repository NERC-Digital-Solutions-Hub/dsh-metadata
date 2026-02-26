# DATA HEADER INFORMATION for Soil_carbon_content.csv

## Overview
- Dataset of soil organic carbon content derived using the MIRS prediction model.
- Associated with ESPA programme and P4GES project.
- Acknowledgement requirement for products derived from these data.

## Dataset schema and key variables
- Site_id: P4GES site code (text).
- SOC_subplot: Subplot where sampling was performed (categorical); Unit: S1 / S2 / S3 / S4.
- SOC_sampling_depth: Depth of the sampled soil layer (numeric); Unit: centimeters.
- SOC_content: Carbon content of the sample (numeric); Unit: g/kg (grammes per kilo) of soil.

## Units and data types
- Site_id: Text String.
- SOC_subplot: Categorical; values S1, S2, S3, S4.
- SOC_sampling_depth: Numeric; unit = centimeter.
- SOC_content: Numeric; unit = g/kg.

## Provenance and references
- Data derived from MIRS prediction model.
- Related documentation: Manual_1_Classical_Survey.rtf, page 17, section 4.4.
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme: ESPA; Project: P4GES (links provided in the header).

## Usage guidance for GIS applications
- Use Site_id as the primary join key to align with other GIS layers.
- SOC_content is the mapped attribute representing soil organic carbon; color/size scales can be based on g/kg.
- SOC_subplot provides categorical sub-division for stratified mapping or symbol differentiation.
- SOC_sampling_depth can be used to create depth-based layers or filter analyses.
- Be mindful of model-derived nature of SOC_content; assess uncertainty if available and consult the referenced manual.

## Acknowledgements
- Acknowledgement of Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.