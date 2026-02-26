# Summary Experimental Design/Sampling Regime

- Purpose and scope
  - Earthworm survey across multiple farms with hedges and field margins, conducted in May 2016.
  - Sites include LL (Little Langton) with organic arable (A1) and conventional arable (A2) plus organic ley (B1, B2); HW (Hutton Wandesley) with conventional ley and arable; OV (Overton) conventional arable; WH (Whenby) with organic ley and organic arable.
  - Data captured: earthworm abundance and biomass by species, along with soil properties; includes metadata on land use, transects, and distances from hedges.

- Experimental design and field methods
  - Transect method: one transect per site, laid perpendicular to hedge into the field; attempts to start from hedge where condition is good; paired transects used for comparisons (e.g., WH and HW).
  - Soil pit sampling: pits 18 x 18 x 15 cm along the transect at hedge, margin, and successive distances (2, 4, 8, 16, 32, 64 m).
  - Earthworm extraction and identification: Mustard solution for extraction; specimens preserved in ethanol; identified using Sims & Gerard field key; preserved specimens available for detailed lab work.
  - Additional measurements per pit: three soil moisture readings (mV) at 5 cm and 10 cm depths; soil temperature at 5 cm and 10 cm; soil bulk density at 5 cm and 15 cm; data collected in specified units.

- Data captured and structure
  - Earthworm data
    - Variables: date, field, transect, distance from hedge (H = hedge, M = margin), depth sample type (Mustard = P, Topsoil = S), sample type (A = abundance/count, B = biomass in grams).
    - Species list with codes and functional group classification (Endogeic, Epigeic, Anecic) and status (healthy, damaged, immature) where applicable.
    - A set of 9 to 20+ species names with corresponding codes (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.).
  - Soil and environmental data
    - Two dataset types:
      - Landscape2016_soil_data.csv with 14 columns: Date, field name, distance from hedge, moisture readings at 5 and 10 cm (three replicates each), soil temperature (5 cm and 10 cm), and bulk density at 5 cm and 15 cm.
      - Landscape earthworm dataset files (e.g., HWA1_EW_landscape.csv, HWB_EW_landscape.csv, LLA1_EW_landscape.csv, etc.) with 30 columns: Date, Field, Transect, Distance, Depth (Mustard or Topsoil), Sample type, followed by species-specific counts/biomass and a code/species mapping.
  - File naming and coverage
    - Files cover each site and land-use combination, with multiple LL files (A1, A2, B1, B2), HW, OV, WH datasets.
    - A comprehensive mapping of 30 columns per earthworm dataset and 14 columns for soil data provided.
  - Miscellaneous classification
    - Earthworm functional groups defined: Endogeic (soil-living), Epigeic (litter-living), Anecic (deep vertical burrows); includes data codes for damaged/immature individuals.

- Data quality, metadata, and notes
  - Data include notes on field conditions (e.g., ploughed field, dry soils, manured margins) and sampling day conditions (e.g., rain).
  - Blank cells indicate no data were collected for that observation.
  - Standardization notes: units include grams for biomass, meters for distance, and millivolts for soil moisture readings; species names and codes align with the Sims & Gerard classification.
  - Reference for methodology: Sims & Gerard (1999).

- Relevance for data governance and leadership
  - Provides a curated, site- and hedge-contextual dataset suitable for assessing hedgerow effects on earthworm communities and soil properties.
  - Organization-wide considerations: metadata richness supports discoverability, data lineage, and cross-site comparability; alignment with data standards recommended for broader data-sharing and partnership work.
  - Opportunities for data product development: integrated datasets combining species counts/biomass with soil conditions enable targeted analyses and community-of-practice collaboration.