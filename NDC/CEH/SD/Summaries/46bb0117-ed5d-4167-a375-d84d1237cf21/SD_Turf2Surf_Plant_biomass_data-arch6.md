# This document is a supplement to the supporting documentation for data series detailed in: 'Turf2Surf_WP2_Supporting_documentation.rtf'

## Overview
- Supplementary details for plant aboveground and belowground biomass measurements in the Conwy catchment, North Wales (2013 and 2014), as described in Turf2Surf_Plant_biomass_data.csv.
- Several datasets share the first 9 columns, enabling cross-dataset comparison and integration.

## Dataset structure
- The Plant biomass dataset has 4 additional columns and 26 rows.
- The first 9 columns (shared across related datasets) are:
  - A: Site Number (unique identifier)
  - B: Habitat
  - C: Habitat Description
  - D: Site name
  - E: Ecosystem Component (plant, soil, or roots)
  - F: Plant species (if component is plant; otherwise NA)
  - G: Plot number (1–4)
  - H: Replicate number
  - I: Soil depth interval (for soil and roots)

## Additional columns and measurements
- J: Unit = g dry mass m-2; Description = Average standing plant biomass
- K: Unit = g dry mass m-2; Description = Standard error of average standing plant biomass
- L: Unit = g dry mass m-2; Description = Average total root biomass for the topsoil 0–15 cm
- M: Unit = g dry mass m-2; Description = Standard error of average total root biomass for the topsoil 0–15 cm

## Data quality and notes
- Missing values are indicated as NA (data not available)
- NA can reflect restricted depths, limited replicates, or outliers
- At site number 7, only one measurement was carried out and no stand error was derived