# Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)

- Purpose for GIS: Provides a structured dataset suitable for map-based integration and visualization of biomass across sites in the Conwy catchment (North Wales) for 2013 and 2014, enabling spatial comparison and overlay with other soil and plant measurements.

- Scope and datasets
  - Primary dataset: Plant aboveground and belowground standing biomass measurements in the Conwy catchment (2013–2014), detailed in Turf2Surf_Plant_biomass_data.csv.
  - This dataset shares its first 9 columns with four related datasets:
    - Plant structural measurements in North Wales and Northwest England (2013–2014)
    - Plant physiological measurements in North Wales and Northwest England (2013, 2014, 2016)
    - Soil carbon data in the Conwy catchment (2013–2014)
    - Soil physical, chemical and biological measurements in the Conwy catchment (2013–2014)

- Data structure (first 9 columns common across datasets)
  - Column A: Site Number (unique identifier)
  - Column B: Habitat
  - Column C: Detailed Habitat Description
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: If Plant, the specific plant species; otherwise NA
  - Column G: Plot number (1–4)
  - Column H: Replicate number (used when measurements are not co-located with plots)
  - Column I: Soil depth interval for soil and roots

- Additional columns and measurements (specific to biomass dataset)
  - The dataset includes 4 additional columns beyond the first 9 (total 13 columns across all related data for this subject)
  - Column J: Unit = g dry mass m-2; Description = Average standing plant biomass
  - Column K: Unit = g dry mass m-2; Description = Standard error of average standing plant biomass
  - Column L: Unit = g dry mass m-2; Description = Average total root biomass for the topsoil 0–15 cm
  - Column M: Unit = g dry mass m-2; Description = Standard error of average total root biomass for topsoil 0–15 cm

- Data quality and handling
  - Missing values indicated as NA (not available)
  - NA also used where measurements were not performed for a site
  - Site 7 has only one measurement and no standard error

- Practical GIS considerations
  - Ensure consistent linking through the Site Number (A) when joining with other datasets
  - Account for plot and replicate fields (G, H) to distinguish spatial subplots or measurement locations
  - Use Column I (soil depth interval) to differentiate biomass data by depth where applicable
  - Handle NA values during analysis and visualization (e.g., gaps in biomass or root data)
  - When integrating with other layers (soil properties, plant physiology, structural measurements), maintain uniform coordinate reference systems and site-level identifiers for accurate spatial joins

- Notes
  - The dataset is part of the Turf2Surf project and serves as a data structure supplement to the WP2 supporting documentation, enabling consistent GIS-enabled exploration of plant biomass across sites in North Wales and adjacent regions (2013–2014).