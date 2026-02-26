# Summary Experimental Design/Sampling Regime

- Scope and datasets
  - Experimental regime across multiple farms/fields with hedges and field margins
  - Datasets cover earthworm sampling (counts and biomass) and associated soil properties
  - Files include per-site, per-transect, and per-distance measurements with detailed metadata

- Experimental design
  - Sites and landuses
    - LL (Little Langton): organic arable (A1) and organic ley (B1) and conventional arable (A2, B2)
    - HW (Hutton Wandesley): conventional ley (HWA1) and conventional arable (HWB)
    - OV (Overton): conventional arable (OV7)
    - WH (Whenby): organic ley (WHA) and organic arable (WHB)
  - Sampling structure
    - Number of transects: 1 per site
    - Hedge-associated sampling: transects run from hedge into field; distances from hedge recorded
    - Margins vs. field samples: Hedge (H) vs. Margin (M) designations
  - Temporal coverage
    - Sampling dates: May 12–26, 2016 (range across sites)

- Field collection methods and instrumentation
  - Transect layout
    - 90-degree transect from hedge into field; transects mid-field length when possible
    - Paired transects for WH/HW comparisons; opposite sides of hedge for OV/LL
  - Soil pit sampling
    - Pits: 18 x 18 x 15 cm, located at hedge, margin, and 2, 4, 8, 16, 32, 64 m along transect
    - Soil processed by hand-sorting; mustard solution used to extract earthworms
    - Earthworms preserved in ethanol and identified via Sims and Gerard key
  - Additional measurements at each pit
    - Soil moisture: three readings in millivolts (5 cm and 10 cm depths)
    - Soil temperature: measurements at 5 cm and 10 cm
    - Soil bulk density: 5 cm and 15 cm depths (oven-dry basis)
  - Data captured: earthworm abundance/biomass, distance, and depth context

- Data types and units
  - Earthworm data
    - Variables: number of earthworms, biomass (grams), distance from hedge (metres)
    - Depth/position indicators: Hedge (H) vs. Margin (M)
  - Soil and environmental data
    - Measurements: soil moisture (mV), soil temperature (°C), soil bulk density (g/cm³)

- Data structure and file organization
  - Earthworm data files (30 columns each)
    - HWA1_EW_landscape.csv, HWB_EW_landscape.csv, LLA1_EW_landscape.csv, LLA2_EW_landscape.csv, LLB1_EW_landscape.csv, LLBS_EW_landscape.csv, OV7_EW_landscape.csv, WHA_EW_landscape.csv, WHB_EW_landscape.csv
    - Common headers (examples): Date, Field, Transect, Distance, Depth, Sample type
    - Depth indicators: Mustard (P) vs. Topsoil (S)
    - Sample type: A = abundance/count, B = biomass (g)
    - Species columns coded with codes and species names (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.)
    - Taxonomic codes include endogeic, epigeic, and anecic groupings (with specific species mapping)
  - Landscape data for earthworms
    - Landscape2016_soil_data.csv
    - 14 columns: Date, field name, code, distance_m, moisture readings at 5 cm and 10 cm (three replicates each), soil temperatures at 5 cm and 10 cm, bulk densities at 5 cm and 15 cm
    - Variables named to indicate depth, replicate, and measurement type
  - Miscellaneous
    - Endogeic, Epigeic, and Anecic functional groups defined; species list provided with corresponding group codes

- Taxonomy and data coding
  - Species and functional group mappings included (e.g., Allolobophora chlorotica – endogeic; Eisenia fetida – epigeic)
  - Sample codes indicate lineage and grouping (e.g., END-dm for endogeic damaged, ANE-im for anecic immature)
  - Blank cells indicate no data for that observation

- Data quality, governance, and sharing considerations
  - Consistency and standardization across multiple sites and formats are essential
  - Metadata should capture site, hedge condition, transect orientation, date, and sampling depth to support traceability
  - Potential data challenges align with Data Steward concerns: incomplete user needs, timely data acquisition, standardization across systems, handling large datasets, and managing legacy formats
  - Reference for taxonomy: Sims & Gerard (1999)

- Notes and references
  - References: Earthworms by Sims & Gerard (1999)

- Governance implications for data stewards
  - Ensure comprehensive data dictionaries and metadata schemas accompany the datasets
  - Maintain consistent coding schemes for depths, sample types, and hedgerow/margin designations
  - Preserve raw vs. processed data versions and document any transformations
  - Plan for data sharing through appropriate portals and catalogues, with clear provenance and lineage
  - Address potential embargoes or access restrictions for site-specific data if applicable