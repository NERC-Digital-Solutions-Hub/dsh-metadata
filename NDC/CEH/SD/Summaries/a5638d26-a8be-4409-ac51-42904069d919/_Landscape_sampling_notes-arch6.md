# Summary Experimental Design/Sampling Regime

- Study scope and sites
  - Multiple fields (Little Langton LL, Hutton Wandesley HW, Overton OV, Whenby WH) with varied land uses: organic arable (A1), conventional arable, organic ley (B1/B2), etc.
  - Transects: one transect per site; for some pairs (WH/HW) transects located in appropriate paired fields; LL transects placed on opposite sides of hedges.
  - Transects started from hedge with good condition; extended perpendicularly into fields up to 64 meters.

- Sampling regime and timing
  - Sampling dates range from 12–26 May 2016 (various sites: LL A1, LL A2, LL B1, LL B2, HW A1, HW B, OV7, WHA, WHB).
  - Each transect included multiple sampling points along the distance from hedge to field interior.

- Field notes and conditions
  - Site notes include ploughed fields with seedling growth, dry/compact soils, margins varying from wide to narrow, hedges with drains, manure spreading, and recent rainfall influences.
  - Some hedges and margins used for manure spreading; other margins show signs of cattle grazing or herbicide application.

- Collection methods (Earthworm sampling)
  - Soil pits (18 x 18 x 15 cm) dug along transects at hedge, margin, and at 2, 4, 8, 16, 32, 64 meters.
  - Mustard solution used to stimulate earthworms; collected worms preserved in ethanol and identified with Sims and Gerard field key.
  - Each pit area recorded along with the presence/absence and counts/biomass of earthworms.

- Measurements and data collected in the field
  - Physical and soil measurements at each pit:
    - Soil moisture: three readings at 5 cm and 10 cm depths using ML3 ThetaProbe (mV)
    - Soil temperature: at 5 cm and 10 cm depths
    - Soil bulk density: at 5 cm and 15 cm depths using bulk density rings (118 cm3)
  - Depth coding:
    - Mustard sample indicated by P; Topsoil indicated by S
  - Spatial coding:
    - Distance from hedge in metres; Hedge (H) samples taken below hedge; Margin (M) samples taken from field margins

- Data types and units
  - Earthworm data: number of earthworms; biomass in grams
  - Distance: metres from hedge
  - Depth indicators and sample types as above

- Data file structure and contents
  - Earthworm data files (30 columns): 
    - Examples: HWA1_EW_landscape.csv, HWB_EW_landscape.csv, LLA1_EW_landscape.csv, LLA2_EW_landscape.csv, LLB1_EW_landscape.csv, LLBS_EW_landscape.csv, OV7_EW_landscape.csv, WHA_EW_landscape.csv, WHB_EW_landscape.csv
    - Columns include: Date, Field, Transect, Distance, Depth, Sample type, plus species-specific columns
  - Species and coding
    - Codes and species names for endogeic, epigeic, and anecic earthworms (e.g., Allolobophora chlorotica, Eisenia fetida, Lumbricus terrestris, etc.)
    - Some codes represent damaged or immature stages (END-dm, EPI-im, etc.)
    - Sample type: A = abundance/count; B = biomass (grams)
    - Blank cells indicate no data available
  - Landscape2016_soil_data.csv
    - 14 columns: Date, field name, code, distance_m, hedge/margin indicator, moisture readings (5 cm and 10 cm at three replicates a, b, c), soil temperature (5 cm, 10 cm), soil bulk density (5 cm, 15 cm)
    - Includes multiple replicates per measurement (a, b, c)

- Additional context and classifications
  - Earthworm functional groups defined:
    - Endogeic: soil-living, horizontal burrows
    - Epigeic: litter-living
    - Anecic: soil-living, deep vertical burrows
  - References for identification: Sims & Gerard (1999)

- Data quality and notes
  - Some samples contain blank cells where data were not collected or not available
  - The dataset captures both worm counts and biomass, along with associated soil properties and spatial position relative to hedges

- Potential data products and uses
  - Analyze hedgerow effects on earthworm abundance/biomass across distances from hedge
  - Compare organic vs conventional practices and hedge margin conditions
  - Link earthworm communities to soil moisture, temperature, and bulk density profiles
  - Create self-serve dashboards or reports for soil fauna and soil property relationships across fields and dates

- References
  - Sims & Gerard (1999) for earthworm identification and classification