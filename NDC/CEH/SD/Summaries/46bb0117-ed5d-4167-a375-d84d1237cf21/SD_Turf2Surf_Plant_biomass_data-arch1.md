# Details of data structure for the dataset Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Plant_biomass_data.csv

- Purpose and context
  - Supplement to the supporting documentation for Turf2Surf WP2 data series.
  - Describes the data structure for plant biomass measurements (aboveground and beneath) in the Conwy catchment, North Wales, for 2013 and 2014.

- Dataset scope and shared structure
  - The datasets share the first 9 columns, enabling cross-dataset comparisons and integration.
  - Related datasets include:
    - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
    - Plant aboveground and belowground standing biomass measurements in the Conwy catchment (2013 and 2014)
    - Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)
    - Soil carbon data in the Conwy catchment (2013 and 2014)
    - Soil physical, chemical and biological measurements in the Conwy catchment (2013 and 2014)

- Key columns and data description
  - Column A: Site Number (unique identifier)
  - Column B: Habitat
  - Column C: Habitat Description (more detail)
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: Plant species (for plant components); 'NA' for soil/roots
  - Columns G and H: Plot number (1–4) and Replicate number (for cases where measurements are based on the dominant species rather than the exact plot location)
  - Column I: Soil depth interval (for soil and roots)
  - Columns J–M (data fields with units and descriptions):
    - J: Unit = g dry mass m-2; Description = Average standing plant biomass
    - K: Unit = g dry mass m-2; Description = Standard error of average standing plant biomass
    - L: Unit = g dry mass m-2; Description = Average total root biomass for the topsoil 0-15 cm
    - M: Unit = g dry mass m-2; Description = Standard error of average total root biomass for topsoil 0-15 cm

- Data availability and limitations
  - Missing values indicated as 'NA' (data not available)
  - At site 7, only one measurement was carried out and no stand error could be derived

- Data specifics
  - The dataset comprises 4 additional columns beyond the first nine and 26 rows total
  - For plant components, F provides the plant species; for soil and roots, F shows 'NA'
  - Measurements are reported in grams of dry mass per square meter (g dry mass m-2)

- Source and usage notes
  - Data are described in detail in Turf2Surf_Plant_biomass_data.csv and linked documentation
  - This structure supports analyses of correlations between biomass and related variables across sites, as well as preparation for predictive modeling and cross-dataset comparisons