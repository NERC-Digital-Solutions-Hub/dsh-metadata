# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Soil_carbon_data.csv

## Overview
- Supplement to the Turf2Surf WP2 supporting documentation describing the data structure of the soil carbon dataset for Conwy catchment, North Wales (2013–2014).
- The dataset is Turf2Surf_Soil_carbon_data.csv, consisting of 469 rows (including the header) and 10+ columns, with the first 9 columns shared with related datasets on plant and soil measurements.

## Dataset structure and fields
- Column A: Site Number (unique identifier for each site)
- Columns B–C: Habitat information and a more detailed Habitat description
- Column D: Site name
- Column E: Ecosystem Component (Plant, Soil, or Roots)
- Column F: If the component is Plant, species name; otherwise NA
- Columns G–H: Plot number (1–4) and Replicate number
- Column I: Soil depth interval for components 'Soil' and 'Roots'
- Column J: Soil carbon (kg C m⁻²) at the corresponding depth interval (NA if not measured)
- Notes:
  - NA indicates missing/unperformed data due to depth limits, limited replicates, or other constraints
  - The first 9 columns are shared across several datasets (Plant structural measurements, Plant biomass, Plant physiology, Soil physical/chemical/biological measurements) for cross-dataset GIS integration

## Data context and geographic scope
- Geographic scope: Conwy catchment, North Wales
- Timeframe: 2013 and 2014
- Part of the Turf2Surf data series; datasets are designed to be combined with related measurements (plant, biomass, physiology, and soil properties)

## Data quality and GIS usage notes
- Missing values are indicated with NA; users should account for incomplete measurements or depth gaps
- Depth interval information (Column I) is essential for depth-specific carbon mapping and may influence layer construction in GIS
- Replicates are provided where photosynthesis measurements were not co-located with plots, enabling more nuanced spatial representation
- Data are suitable for creating map layers of soil carbon by depth, site-level attributes, habitat type, and ecosystem component
- When integrating with other Turf2Surf datasets, ensure consistent interpretation of the shared first 9 columns

## Practical considerations for GIS Specialists
- 469 rows; manageable for typical GIS workflows but plan for depth-based stratification
- Use the shared 9-column schema to join soil carbon data with plant/soil datasets for enriched maps and analyses
- Consider 2D map representations by depth intervals or implement 3D visualization to reflect soil depth information
- Handle NA values during mapping (e.g., masking or interpolation where appropriate) and document data gaps

## Source and provenance
- Supplement to the Turf2Surf WP2 Supporting Documentation
- Data reference: Turf2Surf_Soil_carbon_data.csv

## Key takeaways
- The dataset provides site-level soil carbon measurements by depth for the Conwy catchment (2013–2014) using a consistent schema shared with related plant and soil datasets, enabling integrated GIS mapping and cross-dataset analyses.