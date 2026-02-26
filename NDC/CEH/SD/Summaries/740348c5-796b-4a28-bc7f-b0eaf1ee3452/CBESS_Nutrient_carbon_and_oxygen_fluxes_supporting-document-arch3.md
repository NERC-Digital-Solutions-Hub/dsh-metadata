# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) nutrient exchange fluxes between sediment cores and overlying site water

- Purpose and scope
  - Provides measurements of sediment-water nutrient and oxygen exchange fluxes to support monitoring of coastal environmental health, biodiversity, and ecosystem services.
  - Focuses on interactions at the sediment–water interface in estuarine/coastal habitats.

- Study design and locations
  - Locations:
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
  - Habitats and site characteristics:
    - Saltmarsh sites spanning contrasting soil types (clay in Essex; sandy soils in Morecambe Bay)
    - Mudflat sites with differing sediment textures (cohesive clays/mud/silt in Essex vs coarser sediments in Morecambe Bay)
    - Broad differences in inundation frequency, creek structure, and vegetation between regions
  - Temporal design: Field campaigns conducted in winter and summer 2013
  - Sampling design: Twelve sediment cores collected per site across quadrats; dataset metadata includes Quadrat Numbers 1–22, indicating a detailed quadrat-based schema

- Methods
  - Core collection and incubation:
    - 8 cm diameter sediment cores, with 10 cm headspace, placed in trays of locally collected seawater
    - Cores incubated under light and dark conditions to capture seasonal and diel effects
    - Incubations conducted with daylength-simulating lighting; temperatures and light levels varied by season
  - Measurements:
    - Oxygen flux: Dissolved oxygen measured via Winkler titration from water on top and headspace after incubations
    - Nutrients and carbon: NPOC, NOx, Ammonia, Nitrite, Nitrate, Phosphate, and Silicate measured from water samples using autoanalyzers
    - Chlorophyll: Chlorophyll a quantified in the top 5 mm of sediment cores (per unit dry mass)
  - Quality control and calibration:
    - Instruments calibrated with appropriate standards
    - Data checked and processed to ensure accuracy and comparability
  - Data handling during experiments:
    - Calculations performed to determine fluxes per unit area and time
    - Nitrate values derived from NOx and nitrite measurements
    - Flux sign convention: positive flux = from sediment to overlying water; negative flux = from water to sediment

- Flux calculations and units
  - Fluxes expressed as rate of change per unit area (μmol/m^2/hour)
  - For each core, both light and dark fluxes reported for oxygen and nutrient species
  - Data converted to consistent units across cores and sites

- Measured variables
  - Oxygen flux (light and dark)
  - NPOC flux (light and dark)
  - Nitrogen species: NOx flux, Nitrate flux, Nitrite flux, Ammonia flux (each in light and dark)
  - Phosphate flux (light and dark)
  - Silicate flux (light and dark)
  - Total NOx flux (as a combined measure)
  - Chlorophyll a flux in sediment (as an ancillary biological indicator)

- Data handling, formats, and metadata
  - Data formats:
    - Nutrient and carbon concentrations collected as .txt files
    - Calculations performed in Excel
    - Final dataset provided as a CSV file
  - Dataset structure and field descriptions:
    - Row Number (sorting key)
    - Season (Winter W, Summer S)
    - Location (Morecambe M, Essex E)
    - Site (e.g., CS, WS, WP; AH, FW, TM)
    - Habitat (Mudflat MF, Saltmarsh SM)
    - Quadrat Number (1–22)
    - Scale (A–D representing spatial scales)
    - Flux fields for each parameter under Light and Dark conditions (μmol/m^2/hour)
  - Data quality and transparency:
    - All measurements linked to clear procedures and calibration steps
    - No anomalous data points removed from flux calculations
    - NA values indicate missing measurements

- Data governance, openness, and provenance
  - Dataset includes detailed staff responsible for data collection and analysis
  - Comprehensive methodological description to enable reproducibility and integration into monitoring frameworks
  - Clear data lineage from field sampling through laboratory analysis to final CSV format

- Key considerations for monitoring frameworks
  - Spatial and habitat diversity captured (two regions, contrasting sediment types; saltmarsh and mudflat habitats)
  - Seasonal dimension included (winter and summer)
  - Robust QA, calibration, and standardized flux calculations enhance comparability across sites and time
  - Detailed metadata (locations, habitats, quadrats, scale, and variable definitions) supports integration into dashboards and policy evaluation
  - Data handling choices (including explicit no-filtering of outliers) provide a transparent view of variability and potential sensitivities in interpretation