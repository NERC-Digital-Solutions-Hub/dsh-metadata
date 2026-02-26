# Soil carbon data in the Conwy catchment in North Wales (2013 and 2014)

## Context and purpose
- Supplement to the supporting documentation for data series described in Turf2Surf_WP2_Supporting_documentation.rtf.
- Describes the soil carbon data for the Conwy catchment in North Wales for 2013 and 2014, as detailed in Turf2Surf_Soil_carbon_data.csv.
- Part of a set of related Turf2Surf datasets; the first 9 columns are shared across these datasets to enable cross-dataset analysis.

## Dataset structure and key fields
- Shared structure: The first 9 columns are common with the following datasets:
  - Plant structural measurements (North Wales and Northwest England, 2013–2014)
  - Plant aboveground/belowground standing biomass (Conwy catchment, 2013–2014)
  - Plant physiological measurements (North Wales and Northwest England, 2013, 2014, 2016)
  - Soil physical, chemical and biological measurements (Conwy catchment, 2013–2014)
- Column A: Site Number (unique identifier as introduced in Table 1)
- Column B: Habitat
- Column C: Habitat description (more detailed)
- Column D: Site name
- Column E: Ecosystem Component (plant, soil, or roots)
- Column F: If the component is Plant, the specific plant species; otherwise NA for soil/roots
- Column G: Plot number (1–4)
- Column H: Replicate number (used when photosynthesis measurements were not co-located with plots)
- Column I: Soil depth interval (for Soil and Roots components)
- Column J: Soil carbon (kg C m^-2) at the given depth interval
- NA indicates data not available
- The dataset contains 469 rows, including the header row

## Data interpretation and scope
- Measurements cover soil carbon at specified depth intervals, with context on site, habitat, and plant/soil/roots components.
- Depth-specific data are captured where applicable; some cells may be NA due to limited soil depth, restricted replicates, or other constraints.
- Data are aligned with outcomes for 2013 and 2014 within the Conwy catchment, enabling temporal and spatial comparisons as part of environmental monitoring.

## Relevance to monitoring and the Analysts archetype
- Provides a structured, standardized dataset suitable for verification, quality assurance, cleaning, and transformation.
- Facilitates integration with other Turf2Surf datasets via the common first-9-column schema, enabling comprehensive assessments of environmental health and soil carbon dynamics.
- Supports presentation in reports, maps, and charts, and can be uploaded to appropriate data portals to enhance accessibility and reuse.

## Access and provenance notes
- Documented as a supplement to the Turf2Surf WP2 supporting documentation.
- Data described by Turf2Surf_Soil_carbon_data.csv, with the accompanying context in the cited supplementary document.