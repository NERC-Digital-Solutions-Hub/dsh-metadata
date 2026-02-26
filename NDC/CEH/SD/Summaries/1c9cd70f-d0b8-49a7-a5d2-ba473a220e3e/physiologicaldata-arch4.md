# Metadata for physiology data

- Overview
  - Three datasets derived from threespine sticklebacks, combining physiology and behavior across geothermal and ambient populations.
  - Data collection methods include respirometry for metabolism, video tracking for sociability, and temperature preference chambers.
  - Populations originate from Icelandic sites and are linked to published studies (Pilakouta et al. 2020; 2023).

- Datasets
  - Data set 1: Metabolism.csv
    - Purpose: Whole-body metabolism measured as oxygen consumption (SMR) in a flow-through chamber over weeks.
    - Key variables:
      - AcclimTemp: acclimation temperature (C)
      - PopTemp: habitat type (Cold or Warm)
      - Pop: site code (Ashn, GTS, CSWY, Myv) with W/C suffix for temperature
      - PopPair: sympatric or allopatric population relationship
      - Mass: weight (g)
      - SMR: standard metabolic rate (mg O2/hr)

  - Data set 2: Sociability.csv
    - Purpose: Social behavior assessed via video tracking; focal fish distances to a shoal across geothermal vs ambient ecotypes.
    - Key variables:
      - populationpair: allopatric or sympatric
      - population: population name
      - HabitatTemp: origin habitat (Warm or Cold)
      - Temp: acclimation and trial temperature
      - ID: individual fish ID
      - trial: trial number (1 or 2)
      - sociability: mean distance from stimulus shoal (cm) during 30-minute trial

  - Data set 3: temperature preference.csv
    - Purpose: Temperature preference over 24 hours in a chamber; time spent in preferred temperature.
    - Key variables:
      - Test date: collection date
      - Population: sympatric or allopatric
      - Popn: population and habitat as in Data set 1
      - TempPref: time spent in preferred temperature (minutes)
      - LogTempPref: log-transformed time in preferred temperature
      - Mass: weight (g)
      - LogMass: log-transformed weight

- Data quality, metadata, and provenance
  - Data were checked for outliers (e.g., TempPref) with consistent data collection by a single observer for the temperature preference dataset.
  - Units are specified (e.g., AcclimTemp in °C; SMR in mg O2/hr; Mass in g).
  - Provenance linked to Pilakouta et al. (2020, 2023) with respective study details:
    - 2020 Functional Ecology: Multigenerational exposure to elevated temperatures and SMR
    - 2023 Ecology and Evolution: Geothermal stickleback populations and cooler water preference
    - 2023 Global Change Biology: Warmer environments and sociability

- Data governance and reuse considerations for Data Leaders
  - Discoverability: clearly named CSV files with explicit headers and defined population/habitat codes.
  - Standardization: harmonize population codes (e.g., Ashn, GTS, CSWY, Myv) and HabitatTemp conventions across datasets.
  - Documentation needs: provide metadata definitions, units, collection methods, and links to the Pilakouta studies for traceability.
  - Accessibility: ensure availability of data and metadata to stakeholders (policy colleagues, researchers) with appropriate provenance.
  - Potential collaboration: datasets support cross-study analyses on metabolism, behavior, and temperature preference relative to geothermal versus ambient environments.

- Potential uses for Data Leaders
  - Assess integration of metabolic, behavioral, and temperature preference data to inform broader data strategy on organismal responses to climate variables.
  - Drive data standardization and metadata practices across interdisciplinary ecological datasets.
  - Enable cross-network sharing with partner institutions by clarifying data scope, provenance, and quality controls.