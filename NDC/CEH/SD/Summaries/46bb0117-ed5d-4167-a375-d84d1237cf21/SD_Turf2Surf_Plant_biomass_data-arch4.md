# Details of data structure for the dataset Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Plant_biomass_data.csv

## Overview
- Describes the data structure and metadata for Plant aboveground and belowground standing biomass measurements in the Conwy catchment, North Wales (2013–2014), as documented in Turf2Surf_Plant_biomass_data.csv.
- Part of a broader suite of related datasets that share a common 9-column schema.

## Data structure and fields
- Shared framework: The first 9 columns are common across multiple datasets, including:
  - Column A: Site Number (unique identifier)
  - Column B: Habitat
  - Column C: Habitat Description
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: If Component is Plant, the plant species; otherwise NA
  - Column G: Plot number (1–4)
  - Column H: Replicate number (used when photosynthesis measurements are not co-located with plots)
  - Column I: Soil depth interval (for soil and roots components)
- Additional data columns for this dataset (total 4 columns, making 26 rows):
  - J: Unit = g dry mass m-2; Description = Average standing plant biomass
  - K: Unit = g dry mass m-2; Description = Standard error of average standing plant biomass
  - L: Unit = g dry mass m-2; Description = Average total root biomass for topsoil 0–15 cm
  - M: Unit = g dry mass m-2; Description = Standard error of average total root biomass for topsoil 0–15 cm
- Data gaps and note: NA indicates data not available (e.g., restricted soil depths, limited replicates, or outliers). Site 7 has only one measurement with no stand error derived.

## Dataset relationships and context
- This dataset is a component of Turf2Surf_WP2 and related to other measurements (plant structural, plant physiological, soil carbon, and soil physical/chemical/biological data) collected in North Wales and Northwest England (2013–2016), sharing the same initial 9 columns for consistency.

## Data quality, gaps, and limitations
- Data availability varies by site; some fields are NA due to measurement restrictions.
- Site 7 lacks a stand error due to having only a single measurement.
- Potential variability due to differing depths (soil/roots) and replicates across sites, requiring careful handling during analysis.

## Access, reuse, and governance considerations
- Clear metadata for units and descriptions aids discoverability and correct interpretation.
- Aligns with broader data-sharing efforts within the Turf2Surf project and its supporting documentation.
- When reusing, verify data content/format against the related supporting documentation to ensure consistency across datasets.

## Notes for data leaders
- The standardized first-9-column structure facilitates cross-dataset integration and cross-site comparisons.
- Monitoring data availability and provenance is important to address gaps and plan targeted data collection or imputation strategies.
- Collaboration with the wider data community may help harmonize metadata standards (e.g., depth intervals, replicates) to reduce ambiguity and improve discoverability.