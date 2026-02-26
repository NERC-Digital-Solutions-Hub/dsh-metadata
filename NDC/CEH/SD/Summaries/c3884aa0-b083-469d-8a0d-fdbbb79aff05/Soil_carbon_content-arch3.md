# DATA HEADER INFORMATION for Soil_carbon_content.csv

## Overview
- Contains soil organic carbon content measured using the MIRS prediction model.
- Part of ESPA (Programme) and P4GES (Project).
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo.

## Data fields and definitions
- Site_id
  - Information: P4GES site code
  - Variable Type: Text String
- SOC_subplot
  - Information: subplot where sampling was done
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

## Metadata, references, and provenance
- Related documentation: Manual_1_Classical_Survey.rtf, page 17, section 4.4
- DOI: https://doi.org/10.5285/c3884aa0-b083-469d-8a0d-fdbbb79aff05
- Programme/Project URLs: ESPA (http://www.espa.ac.uk/); P4GES (https://www.p4ges.org)

## Data quality and governance considerations
- Dataset created using a prediction model (MIRS); necessitates clear provenance and methodological transparency.
- Metadata completeness is essential to verify suitability for use; data sharing of underlying data is often required, which can be a barrier.
- Public sharing, data management standards, and acknowledgment requirements should be adhered to for governance and reproducibility.

## Relevance for monitoring frameworks
- Provides standardized, site- and depth-specific soil carbon measurements, enabling monitoring of soil health and carbon stocks across sites.
- Facilitates integration into dashboards, reports, and policy assessments, supporting evidence-based environmental decisions.