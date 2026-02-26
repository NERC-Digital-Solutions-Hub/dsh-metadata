# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Soil_carbon_data.csv

## Overview
- Supplement to the supporting documentation for data series described in Turf2Surf_WP2_Supporting_documentation.rtf.
- Focuses on soil carbon data in the Conwy catchment, North Wales, for 2013 and 2014.
- The dataset has 469 rows, including the header row, and provides a detailed data structure for site- and plot-level records.

## Shared data structure
- The first 9 columns are shared with several related Turf2Surf datasets, enabling cross-dataset comparison and integration.
- Related datasets (sharing the first 9 columns) include:
  - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in North Wales and Northwest England (2013, 2014 and 2016)
  - Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)
  - Soil physical, chemical and biological measurements in the Conwy catchment in North Wales (2013 and 2014)

## Column definitions (A–J)
- A Site Number: unique identifier for each site (as introduced in Table 1).
- B Habitat: broad habitat category of the site.
- C Habitat description: more detailed description of the habitat.
- D Site name: designated site name.
- E Ecosystem Component: indicates whether the data pertain to Plant, Soil, or Roots.
- F Species (if Plant): specific plant species; for soil or roots this field shows 'NA'.
- G Plot number: plot number (1 to 4).
- H Replicate number: replicate identifier used when photosynthesis measurements were not co-located with plots.
- I Soil depth interval: depth interval information for soil and roots components.
- J Soil carbon: kg carbon per square meter (kg C m-2) at the given depth interval.

## Missing values and data availability
- Missing values are indicated as 'NA' and can arise from:
  - Restricted soil depths or limited number of replicates (soil cores).
  - Measurements not performed for a site or at a depth.
  - Outliers or data quality constraints.
- Column J (Soil carbon) reflects the measured value where available; NA indicates data not collected for that combination of site/depth.

## Dataset size and format notes
- 469 rows in total, including the header row (i.e., 468 data rows).

## Documentation context
- The table and its accompanying notes are part of the Turf2Surf project’s data documentation, intended to support clear understanding and reuse by data users and other datasets within the Turf2Surf suite.