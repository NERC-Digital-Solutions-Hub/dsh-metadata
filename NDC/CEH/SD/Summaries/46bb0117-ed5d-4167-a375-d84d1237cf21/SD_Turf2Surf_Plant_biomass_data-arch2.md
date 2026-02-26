# This document is a supplement to the supporting documentation for data series detailed in: 'Turf2Surf_WP2_Supporting_documentation.rtf'

## Overview
- Describes the data structure for Plant aboveground and belowground standing biomass measurements in the Conwy catchment, North Wales (2013 and 2014) as detailed in Turf2Surf_Plant_biomass_data.csv.
- Part of a set of datasets that share a common 9-column structure to enable integrated environmental monitoring and cross-dataset analysis.

## Dataset scope and relationships
- Focus: Plant biomass measurements (aboveground and total root biomass) with associated metadata.
- Related datasets (sharing the first 9 columns): 
  - Plant structural measurements (North Wales and Northwest England, 2013–2014)
  - Plant biomass measurements (Conwy, 2013–2014)
  - Plant physiological measurements (North Wales, Northwest England, 2013, 2014, 2016)
  - Soil carbon data (Conwy, 2013–2014)
  - Soil physical, chemical and biological measurements (Conwy, 2013–2014)

## Data structure: common first 9 columns
- A Site Number (unique identifier)
- B Habitat
- C Habitat Description (more detail)
- D Site name
- E Ecosystem Component (plant, soil, or roots)
- F Species information (for Plant; NA for soil/roots)
- G Plot number (1–4)
- H Replicate number (used when measurements are tied to dominant species rather than exact plot locations)
- I Soil depth interval (for soil/roots)

## Data completeness and missing values
- Missing values are indicated as 'NA' (data not available) due to constraints like soil depth limits, limited replicates, or outliers.
- At site 7, only one measurement was taken, and no standard error was derived.

## Additional biomass-specific columns (4 extra columns)
- J: Unit = g dry mass m-2; Description = Average standing plant biomass
- K: Unit = g dry mass m-2; Description = Standard error of average standing plant biomass
- L: Unit = g dry mass m-2; Description = Average total root biomass for the topsoil 0–15 cm
- M: Unit = g dry mass m-2; Description = Standard error of average total root biomass for topsoil 0–15 cm

## Data quality and workflow notes
- The dataset is prepared with verification, quality assurance, cleaning, and transformation steps to produce standardised outputs (e.g., reports, maps, charts).
- Created datasets are intended for storage and upload to appropriate data portals to facilitate reuse and accessibility.

## Practical implications for environmental monitoring
- The standardised, cross-dataset structure supports consistent reporting of environmental health indicators and enables long-term trend analysis across multiple related datasets.
- The explicit metadata (plot/replicate details, habitat descriptions, and depth intervals) enhances traceability and comparability for monitoring and policy evaluation.
- Emphasis on making underlying data accessible aligns with aims to maximise dataset value through integration with other environmental data sources.