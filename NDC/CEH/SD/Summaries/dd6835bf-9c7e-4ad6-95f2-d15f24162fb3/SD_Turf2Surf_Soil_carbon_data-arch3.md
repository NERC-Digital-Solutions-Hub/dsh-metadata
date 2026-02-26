# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014)

## Overview
- Supplement to the supporting documentation for data series detailed in Turf2Surf_WP2_Supporting_documentation.rtf.
- Covers soil carbon data in the Conwy catchment, North Wales, for 2013 and 2014.
- The Turf2Surf_Soil_carbon_data.csv table has 469 rows (including the header) and shares the first 9 columns with several related datasets.

## Dataset structure and fields
- The first 9 columns are common across multiple datasets, including:
  - A: Site Number (unique identifier, as introduced in Table 1)
  - B: Habitat
  - C: Habitat description
  - D: Site name
  - E: Ecosystem Component (Plant, Soil, or Roots)
  - F: Plant species (if the component is Plant); 'NA' for soil or roots
  - G: Plot number (1 to 4)
  - H: Replicate number (used when measurements are not co-located with plots)
  - I: Soil depth interval (for soil and roots)
- Column J: Soil carbon (kg C m-2) at the specified depth interval.
- Missing values are shown as 'NA' when data are not available (e.g., restricted depths, limited replicates, or unperformed measurements).

## Data characteristics
- The dataset explicitly notes that NA indicates measurements not performed for a site or depth due to limited soil depth.
- Contains 469 rows, including the header row.
- Measurements pertain to soil carbon at depth intervals within the 2013–2014 period.

## Relationship to other datasets
- The datasets sharing the first 9 columns include:
  - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment (2013 and 2014)
  - Plant physiological measurements in North Wales and Northwest England (2013, 2014, 2016)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment (2013 and 2014)
  - Soil physical, chemical, and biological measurements in the Conwy catchment (2013 and 2014)
- This structure facilitates cross-dataset integration and comparative monitoring across ecosystems and time.

## Data quality and use for monitoring
- Metadata and dataset quality are important for reuse; missing metadata or limited depth information can hinder verification and comparability.
- The dataset is designed to support environmental health monitoring and policy evaluation by providing standardized site, habitat, depth, and component information, enabling clear reporting and dashboards.