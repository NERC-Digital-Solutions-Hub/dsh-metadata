# Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014) as detailed in the table Turf2Surf_Plant_biomass_data.csv

- Purpose and context
  - Supplement to the supporting documentation for data series described in Turf2Surf_WP2_Supporting_documentation.rtf.
  - Details the data structure for the dataset of plant aboveground and belowground standing biomass measurements in the Conwy catchment, North Wales (2013 and 2014), as represented in Turf2Surf_Plant_biomass_data.csv.

- Shared structure with related datasets
  - The first 9 columns are common with the following datasets:
    - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
    - Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)
    - Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)
    - Soil carbon data in the Conwy catchment in North Wales (2013 and 2014)
    - Soil physical, chemical and biological measurements in the Conwy catchment in North Wales (2013 and 2014)

- Key columns and their meaning (A-I)
  - Column A: Site Number (unique identifier)
  - Column B: Habitat
  - Column C: Habitat Description (more detailed)
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: If Component is Plant, species details; otherwise NA
  - Columns G-H: Plot number and Replicate number (Plot 1–4; Replicates needed when measurements are not co-located with plots)
  - Column I: Soil depth interval for soil and roots components

- Data availability and handling of missing values
  - Missing values indicated as NA (data not available) due to restricted depths, limited replicates, or outliers.
  - The dataset includes 4 additional columns beyond the first 9 and contains 26 rows.
  - At site number 7, only one measurement was obtained and no standard error (stand) could be derived.

- Measurement specifics and units (J-M)
  - J: Unit = g dry mass m-2; Description = Average standing plant biomass
  - K: Unit = g dry mass m-2; Description = Standard error of average standing plant biomass
  - L: Unit = g dry mass m-2; Description = Average total root biomass for the topsoil 0–15 cm
  - M: Unit = g dry mass m-2; Description = Standard error of average total root biomass for topsoil 0–15 cm

- Data governance and quality notes
  - NA indicates measurements not performed for a site; guidance on data completeness and limitations is documented.
  - Emphasizes the need to respect data availability constraints, metadata consistency, and proper handling of exclusions or embargoed data when sharing or reusing the dataset.