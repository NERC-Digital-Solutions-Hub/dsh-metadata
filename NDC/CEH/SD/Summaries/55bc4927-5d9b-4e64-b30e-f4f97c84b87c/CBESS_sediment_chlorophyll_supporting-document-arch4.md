# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment chlorophyll concentrations in saltmarsh and mudflat habitats

- Overview
  - Dataset measuring chlorophyll concentrations in surface sediments (top 2 mm) in saltmarsh and mudflat habitats.
  - Chlorophyll a, b, and c1+c2 concentrations reported in µg/g.
  - Winter and summer 2013 field campaign as part of CBESS; five replicates per quadrat.
  - Staff: Jack Maunder.

- Spatial and temporal scope
  - Locations: Essex and Morecambe Bay.
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
  - Habitat contrasts:
    - Saltmarsh: two soil types (clay in Essex; sandy in Morecambe Bay) with differing inundation and vegetation.
    - Mudflat: cohesive clays/mud/silt (Essex) vs coarse, mobile sediments (Morecambe Bay).
  - Time: Winter and Summer 2013; no repeat sampling planned.

- Variables and measurements
  - Primary variables:
    - Chlorophyll a (µg/g)
    - Chlorophyll b (µg/g)
    - Chlorophyll c1+c2 (µg/g)
  - Additional fields (dataset structure):
    - Season (Winter or Summer)
    - Location (Essex or Morecambe Bay)
    - Site (AH, FW, TM, CS, WS, WP)
    - Habitat (Mudflat or Saltmarsh)
    - Quadrat Number (1–22)
    - Scale (A–D; various spatial sub-sampling levels)
    - Chl a, Chl b, Chl c1+c2 values and standard deviations
    - StDev for each chlorophyll measure
  - Data formats and units:
    - CSV files
    - Standardized lab protocol outputs for concentrations and summary statistics

- Sampling design and laboratory methods
  - Sampling unit: surface sediment collected with a contact corer (top 2 mm).
  - Sample handling: flash-frozen with liquid nitrogen; stored below -80°C; dried in a freeze dryer.
  - Chlorophyll extraction: acetone solvent; spectrophotometric analysis (Cecil CE3021) at 630, 647, 664, 750 nm.
  - Calculation: chlorophyll concentrations derived from absorption readings using standard equations.
  - Spatial sampling: 22 one-meter quadrats per site randomly allocated; quadrats analyzed across four spatial scales; randomization implemented in R.
  - Calibration and quality checks: laboratory-scale calibration; spectrophotometer accuracy verified with standard chlorophyll solutions.
  - Data entry and verification: readings entered into spreadsheets; spectrophotometer software used to record absorption values.

- Data format, structure, and metadata
  - File formats: Comma-separated values (.csv).
  - Dataset field descriptions include codes for Season, Location, Site, Habitat, Quadrat Number, Scale, and chlorophyll measurements with associated standard deviations.
  - Metadata supports data discoverability through explicit site, habitat, and sampling scale designations; notes include occasional missing data (NA) where applicable.

- Data quality, processing, and governance
  - Data processing follows standardized CBESS field methodology; no complex statistical treatment applied beyond basic recording of wet/dry weights for water content (as part of some procedures).
  - Quality checks include calibration steps and verification against standard solutions; data is captured through instrument software and manually entered into spreadsheets.
  - Responsibility: dataset managed with defined staff (Jack Maunder) and alignment to CBESS field campaign practices.
  - Repeat sampling: not planned, limiting temporal expansion to the winter/summer 2013 window.

- Access, reuse, and practical considerations for Data Leaders
  - Clear, machine-readable CSV format with explicit field codes facilitates integration into wider data systems.
  - Comprehensive metadata included to support data discovery, comparability across sites, habitats, and seasons.
  - Suitable for cross-site comparisons of MPB-associated chlorophyll concentrations and sediment-type effects in coastal habitats.
  - Potential for integration with broader CBESS data on coastal biodiversity and ecosystem services, with attention to ensuring consistent metadata standards and documentation for end users.