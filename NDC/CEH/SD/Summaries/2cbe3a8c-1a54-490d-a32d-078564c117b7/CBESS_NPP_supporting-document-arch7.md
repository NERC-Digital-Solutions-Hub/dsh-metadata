# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) net primary productivity (NPP) on salt marsh sites at Morecambe Bay and Essex

- Overview
  - A CBESS dataset documenting net primary productivity (NPP) of salt marsh vegetation.
  - Focuses on end-of-2013 growing season measurements from six sites split between Essex (three sites) and Morecambe Bay (three sites).
  - NPP is derived from above-ground vegetation biomass collected within grazer-exclusion cages during summer 2013, scaled to a per-square-metre annual rate.
  - Staff: Hilary Ford.

- Study sites and locations
  - Essex
    - Abbotts Hall (AH): 51.7833°N, 0.8667°E
    - Fingringhoe Wick (FW): 51.8167°N, 0.9667°E
    - Tillingham Marshes (TM): 51.6833°N, 0.9333°E
  - Morecambe Bay
    - Cartmel Sands (CS): 54.1667°N, 3.0000°W
    - Warton Sands (WS): 54.1333°N, 2.8000°W
    - West Plain (WP): 54.1500°N, 2.9667°W
  - Saltmarsh sites were chosen to represent contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation, creek structure, and vegetation.

- Habitat and management context
  - Essex sites: hare-grazed; Abbotts Hall and Fingringhoe Wick heavily grazed by overwintering Brent geese.
  - Morecambe Bay sites: Cartmel Sands and Warton Sands heavily grazed by sheep (~4–5 ha^-1) with pink-footed geese grazing in winter.
  - West Plain site: lightly grazed (<2 sheep ha^-1).

- Data collection and timing
  - Field campaign: CBESS winter and summer 2013; measurements taken at the end of the 2013 growing season during the summer 2013 campaign.
  - Sampling unit: 50 cm x 25 cm above-ground vegetation inside grazer-exclusion cages; vegetation harvested and dried for biomass measurements.

- Variables and data processing
  - Primary variable: NPP (net primary productivity).
  - NPP calculation: dry vegetation mass scaled to kg m^-2 yr^-1 after drying at 60°C for 72 hours.
  - Data transformation: from kg dry weight per core area to kg DW m^-2 per year.
  - Data quality notes: missing data where grazing exclosures were lost; some data cannot be strictly classified as a single 'summer' variable since measurements span the whole growing season.
  - Related metadata: staff responsible, exact sampling methods, and context on grazing/exclosure integrity.

- Procedures and data coding (as described in dataset)
  - Calibration procedures: coded options (e.g., 1, 2, 3) for applicable datasets; where not applicable, indicated as None.
  - Statistical treatment: coded options (e.g., 1, 2, 3) describing how observations were treated statistically (some entries indicate no advanced statistics beyond scaling).
  - Data quality control: described as part of the dataset’s quality checks.
  - File formats: CSV (comma-separated values).
  - Dataset field structures: includes fields for Season, Location, Site, Habitat, Quadrat Number, Scale, NPP, and related descriptive headers; multiple field-description variants indicate how data are organized in the CSV.

- Data structure and access
  - Primary data format: CSV with columns for description, row number, season, location, site, habitat, quadrat number, scale, and NPP values (kg DW m^-2 yr^-1).
  - Spatial and categorical fields enable GIS-ready mapping:
    - Location and site identifiers allow spatial joins.
    - Habitat types (e.g., Saltmarsh, Mudflat) aid layer classification.
    - Quadrat numbers and scales support spatial aggregation (1 m, 1–10 m, 10–100 m, etc.).

- Relevance for GIS applications
  - Provides geolocated NPP data across multiple saltmarsh sites with differing soil types and grazing regimes, suitable for map-based analyses of productivity, habitat quality, and ecosystem service assessments.
  - Enables comparisons between clay-rich Essex and sand-dominated Morecambe Bay sites, as well as impacts of grazing intensity on productivity.
  - Supports integration with other CBESS environmental layers (inundation frequency, vegetation type, creek structure) to explore spatial patterns in ecosystem services.