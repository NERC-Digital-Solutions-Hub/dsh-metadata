# DATA HEADER information for Litter_layer_carbon_stock.csv

## Overview
- Describes the carbon stock of the litter on each site.
- Associated with ESPA programme and P4GES project.
- DOI provided for dataset access: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Acknowledgement requirement: Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Dataset context and provenance
- Programme: ESPA
- Project: P4GES
- Data source notes: Information and field labels indicate how samples were collected and recorded; site_ID serves as the P4GES site code.
- Manual reference: Please also see Manual 1_Classical_Survey.

## Attribute definitions (fields)
- site_ID
  - Information: P4GES site code
  - Variable Type: Text String
  - Unit: (not specified)
  - Field materials/resources: (not specified)
- Subplot
  - Information: Subplot where the sample was collected
  - Variable Type: Categorical
  - Unit: S1 / S2 / S3 / S4
  - Field materials/resources: botanist
- Area
  - Information: Area of the quadrat in which the samples were taken
  - Variable Type: Numeric
  - Unit: square metre (m^2)
  - Field materials/resources: botanist
- Litter_thickness
  - Information: Thickness of the litter layer measured before sampling in the field
  - Variable Type: Numeric
  - Unit: Centimeter (cm)
  - Field materials/resources: ruler
- Matt_root_thickness
  - Information: Thickness of the root matt layer measured before sampling in the field
  - Variable Type: Numeric
  - Unit: Centimeter (cm)
  - Field materials/resources: ruler
- Biomass
  - Information: Biomass stock of litter
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field materials/resources: (not specified)
- Stock_C
  - Information: Carbon stock of litter
  - Variable Type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
  - Field materials/resources: (not specified)

## Data usage and GIS considerations
- Use site_ID to join with spatial site polygons for map-based visualizations.
- Subplot, Area, Litter_thickness, and Matt_root_thickness can be displayed as attribute layers or summarized per site.
- Biomass and Stock_C units appear as mg/ha (Mg.ha-1); verify unit consistency and perform conversions if integrating with datasets using different units.
- The quadrat area (Area) indicates spatial extent within each site; consider this when aggregating to larger map units.
- Field materials/resources notes (e.g., botanist, ruler) provide context for data collection methods and potential metadata considerations.

## Data quality, limitations, and challenges
- Information on data standardization and cross-dataset compatibility is implied by the header but not fully detailed here.
- Data provenance indicates multiple data collection aspects (e.g., thickness measures, biomass, carbon stock) that may require careful integration when combining with other datasets.
- Acknowledgement and citation requirements should be followed for derived products.

## References, access, and credits
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Programme: ESPA
- Project: P4GES
- Manual reference: Manual 1_Classical_Survey
- Acknowledged contributor: Laboratoire des Radio Isotopes, Université d'Antananarivo