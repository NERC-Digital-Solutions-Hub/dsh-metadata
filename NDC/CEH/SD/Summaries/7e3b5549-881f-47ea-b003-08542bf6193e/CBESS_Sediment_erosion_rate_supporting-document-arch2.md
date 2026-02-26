# Coastal Biodiversity Ecosystem Service Sustainability (CBESS) the erosion rate of sediment cores from salt marsh sites at Morecambe Bay and Essex

- Purpose: A dataset measuring erosion rate of sediment cores from salt marsh sites in Essex and Morecambe Bay to support modelling of coastal environmental health and ecosystem service sustainability under different flow conditions.

- Lead/responsible site: Hilary Ford.

- Observational units: One large sediment core (16 cm diameter, 30 cm height) per 1 m x 1 m quadrat, including above-ground vegetation.

- Flow treatments: Erosion assessed as % mass loss per hour under three waterfall flow regimes—low, medium, and high.

- Monitoring period and windows:
  - General campaign: Winter and Summer 2013.
  - Essex winter samples: Additional sampling window 2–6 March 2013.

- Site locations and coordinates:
  - Essex:
    - Abbotts Hall (AH): 51.7833°N, 0.8667°E
    - Fingringhoe Wick (FW): 51.8167°N, 0.9667°E
    - Tillingham Marshes (TM): 51.6833°N, 0.9333°E
  - Morecambe Bay:
    - Cartmel Sands (CS): 54.1667°N, -3.0000°W
    - Warton Sands (WS): 54.1333°N, -2.8000°W
    - West Plain (WP): 54.1500°N, -2.9667°W

- Site context and contrasting conditions:
  - Essex: clay soils; hare-grazed sites; Abbotts Hall and Fingringhoe Wick heavily grazed by over-wintering Brent geese.
  - Morecambe Bay: sandy soils; intensive sheep grazing with pink-footed geese wintering; West Plain lightly grazed.

- Sampling and data collection method:
  - For each core, record above-ground vegetation cover.
  - Place core in recirculation flume (“waterfall force”) for 1.5 hours total (0.5 h at each of low, medium, high force).
  - Compute erosion rate from mass loss measured at 0, 5, 10, 15, and 30 minutes (converted to % mass loss per hour).

- Data structure and variables:
  - Core and quadrat metadata: Season (Winter W / Summer S); Location (Morecambe M / Essex E); Site (CS, WS, WP, AH, FW, TM); Habitat (Mudflat MF / Saltmarsh SM); Quadrat Number (1–22); Scale categories (A–D representing 1 m to >100 m ranges); L_%massloss (low flow %mass loss per hour); M_%massloss (medium flow %mass loss per hour); H_%massloss (high flow %mass loss per hour).
  - Data identifiers: Row Number (sorting index).

- Calibration and measurement specifics:
  - Stagnation pressures: Low 61 Pa, Medium 146 Pa, High 351 Pa.

- Data quality and processing notes:
  - Statistical treatment: None.
  - Data checks/QA: None documented.
  - File format: Excel workbook.
  - Data validity caveats:
    - Mass loss per hour >100 is considered valid.
    - Low-flow mass loss can be negative due to initial saturation with water.
    - High-flow cores were sometimes destroyed, reducing usable data at that level.
    - Medium-flow results are more reliable and recommended for overall model usage.
  - Duplicate entries exist for core observations (two entries labeled 1 and 2 with identical procedures).

- Data usage and purpose within monitoring:
  - Enables comparison of erosion rates across contrasting soil types, grazing regimes, and inundation contexts.
  - Supports standardized reporting formats and potential incorporation into larger environmental health assessments and policy performance monitoring.

- Data storage and portal preparation:
  - Intended for storage and upload to appropriate data portals; designed to be reusable beyond a single study (not single-use).