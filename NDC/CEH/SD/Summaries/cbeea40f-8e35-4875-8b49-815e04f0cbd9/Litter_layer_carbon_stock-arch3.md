# DATA HEADER information for Litter_layer_carbon_stock.csv

## Overview
- Describes the carbon stock of the litter layer on each site.
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA; Project: P4GES
- Acknowledgement required for products derived from these data: Laboratoire des Radio Isotopes, Université d'Antananarivo

## Provenance and scope
- Part of the Litter_layer_carbon_stock.csv dataset; associated with ESPA (ESPA Programme) and P4GES project.
- Metadata and field definitions accompany the dataset to support reuse and interpretation.

## Dataset schema and key fields
- site_ID
  - Type: Text String
  - Information: P4GES site code
  - Unit: none
- Subplot
  - Type: Categorical
  - Information: subplot where the sample was collected
  - Unit: S1 / S2 / S3 / S4
  - Field resources: botanist
- Area
  - Type: Numeric
  - Information: Area of the quadrat in which the samples were taken
  - Unit: square metre (m^2)
  - Field resources: botanist
- Litter_thickness
  - Type: Numeric
  - Information: Thickness of the litter layer measured before sampling in the field
  - Unit: Centimeter (cm)
  - Field resources: ruler
- Matt_root_thickness
  - Type: Numeric
  - Information: Thickness of the root matt layer measured before sampling in the field
  - Unit: Centimeter (cm)
  - Field resources: ruler
- Biomass
  - Type: Numeric
  - Information: Biomass stock of litter
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field resources: (not specified)
- Stock_C
  - Type: Numeric
  - Information: Carbon stock of litter
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field resources: (not specified)

## Data quality and governance implications for monitoring frameworks
- Metadata richness: The header provides definitions, units, and data origins for key variables, aiding interpretation and cross-site comparability.
- Data standards and transformations: Some units and descriptions (e.g., Biomass unit phrasing) may require standardization for internal dashboards or dashboards across datasets.
- Data accessibility and provenance: Dataset is linked to a DOI and project context; acknowledgement requirements must be respected when disseminating results derived from the data.
- Data sharing and governance: Underlying data sharing practices are implied by project links and acknowledgments; ensure compliance with data governance norms and proper attribution when publishing outputs.
- Barriers to practical use: While metadata is present, users should verify metadata completeness for all fields and confirm any originator-specific metadata needed to fully verify data suitability for monitoring purposes.

## References and provenance notes
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA; Project: P4GES
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data

## Practical implications for monitoring frameworks
- Useful for assessing litter-layer carbon stock across sites with standardized measurements (Area, Litter_thickness, Matt_root_thickness, Biomass, Stock_C).
- Facilitates cross-site comparisons, trend analyses, and integration into broader environmental health monitoring dashboards, provided metadata consistency is maintained and data governance practices are followed.