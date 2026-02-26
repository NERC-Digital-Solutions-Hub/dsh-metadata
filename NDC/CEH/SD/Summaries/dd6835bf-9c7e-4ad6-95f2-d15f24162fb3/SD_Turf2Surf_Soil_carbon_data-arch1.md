This document is a supplement to the supporting documentation for data series detailed in: 'Turf2Surf_WP2_Supporting_documentation.rtf'

## Overview
- Describes soil carbon data for the Conwy catchment in North Wales (2013 and 2014) within the Turf2Surf project.
- Serves as supplementary information to the main data-series documentation.

## Data structure and key fields
- The dataset shares the first 9 columns with several related datasets:
  - Plant structural measurements (North Wales and Northwest England, 2013–2014)
  - Plant aboveground and belowground standing biomass (Conwy catchment, 2013–2014)
  - Plant physiological measurements (North Wales and Northwest England, 2013, 2014, 2016)
  - Plant aboveground and belowground standing biomass (Conwy catchment, 2013–2014)
  - Soil physical, chemical and biological measurements (Conwy catchment, 2013–2014)
- Column details:
  - A: Unique Site Number
  - B: Habitat
  - C: Detailed Habitat description
  - D: Site name
  - E: Ecosystem Component (plant, soil, or roots)
  - F: If Plant, species; otherwise NA
  - G: Plot number (1–4)
  - H: Replicate number
  - I: Soil depth interval (for Soil and Roots)
  - J: Soil carbon (kg C m^-2) at the given depth interval
- Missing values are indicated as NA (e.g., restricted depths, limited replicates, or data not collected).

## Specifics of the soil carbon dataset
- Focuses on soil carbon measurements (column J) at defined depth intervals.
- NA in column J denotes measurements not performed for a site or depth due to limited soil depth.

## Dataset size and coverage
- Total rows: 469 (including the header row).
- Temporal scope primarily 2013 and 2014 for soil carbon; other datasets mentioned include 2016 for plant physiology.

## Data integration and usage notes
- The first 9 columns enable linking soil carbon data with the related plant and soil datasets for cross-dataset analyses.
- Depth-related data and replicate information should be considered when aggregating or comparing measurements across sites.
- Data quality considerations include potential missing details such as administrative boundaries and varying depths across sites.