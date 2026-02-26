# Turf2Surf_WP2_Supporting_documentation.rtf

## Overview
- Supplement to the supporting documentation for Turf2Surf data series, detailing the data structure for biomass and related measurements in the Conwy catchment (North Wales) for 2013 and 2014, with broader plant measurements (2013–2016) referenced elsewhere.
- Describes how datasets share core identifying columns and how biomass-related metrics are recorded and interpreted.

## Data structure and variables
- The following datasets share the first 9 columns:
  - Site Number (unique identifier)
  - Habitat
  - Habitat Description (more detail)
  - Site name
  - Ecosystem Component (plant, soil, or roots)
  - If the ecosystem component is Plant, the Plant species is provided; otherwise NA
  - Plot number (1–4)
  - Replicate number (used when photosynthesis measurements were based on a dominant species rather than direct co-location)
  - Soil depth interval (for soil and roots components)
- Missing values are indicated by NA (e.g., restricted depths, limited replicates, or outliers).

## Additional data columns (J–M)
- The dataset has 4 additional columns beyond the first 9:
  - J: Unit = g dry mass m-2; Description = Average standing plant biomass
  - K: Unit = g dry mass m-2; Description = Standard error of the average standing plant biomass
  - L: Unit = g dry mass m-2; Description = Average total root biomass for the topsoil 0–15 cm
  - M: Unit = g dry mass m-2; Description = Standard error of the average total root biomass for topsoil 0–15 cm
- NA indicates measurements not performed for that site.
- Note: At site number 7, only one measurement was carried out and no stand error was derived.

## Dataset scope and structure
- The dataset comprises 26 rows and 4 additional (J–M) columns beyond the initial 9 core columns.
- Related datasets (sharing the first 9 columns) include:
  - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment (2013 and 2014)
  - Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)
  - Soil carbon data in the Conwy catchment (2013 and 2014)
  - Soil physical, chemical and biological measurements in the Conwy catchment (2013 and 2014)

## Relevance for monitoring and governance
- Provides standardized biomass and root measurements essential for evaluating vegetation health, carbon stocks, and soil-biological status across sites.
- Highlights data quality and governance considerations:
  - Data completeness and gaps (NA values) and limited replicates at some sites
  - Metadata sufficiency (e.g., detailed habitat descriptions, growth stages)
  - Data sharing and openness requirements (underpinning access to underlying data)
  - Barriers from missing or inconsistent metadata, and the need for consistent data transformation and quality assurance processes
- Useful for informing policy decisions, monitoring environmental health, and identifying data gaps to target in future monitoring iterations.