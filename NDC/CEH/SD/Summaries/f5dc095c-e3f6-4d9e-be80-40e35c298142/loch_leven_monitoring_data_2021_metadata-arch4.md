# Loch Leven long-term monitoring dataset

- Overview
  - Data from the Loch Leven long-term monitoring programme in Scotland, initiated in 1968 and ongoing.
  - Collected under project UK-SCAPE WP7 LEVEN; associated with NERC / UK Centre for Ecology & Hydrology.
  - Two primary sampling sites used for measurements: Reed Bower and Sluices (also Harbour data referenced for context).
  - Data include lake chemistry (conductivity, pH, temperature, Secchi depth, nutrients) and crustacean zooplankton densities (per litre) over time.
  - Fortnightly sampling regime with occasional gaps due to weather, ice, or resource constraints; sampling methods and site access described.

- Data types and content
  - Water chemistry measurements (in situ at most sites, with lab analyses for certain determinations):
    - Conductivity, pH, temperature
    - Secchi depth (water clarity)
    - Nutrients: soluble reactive phosphorus (SRP), total soluble phosphorus (TSP), total phosphorus (TP), chlorophyll a
  - Zooplankton data:
    - Densities (ind/L) of crustacean taxa across two sites (Reed Bower and Sluices), including multiple taxa (e.g., Daphnia hyalina, Eudiaptomus spp., Cyclopidae, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus, etc.)
    - Some taxa identified to species level; zero indicates non-detection within sampling/identification resolution; NA indicates missing values.
  - Site metadata and coordinates:
    - Site codes (Harbour, Reed Bower, Sluices) with UK National Grid coordinates; data columns describe measurement context and units.

- Sampling, measurement and analysis methods
  - In situ measurements for conductivity, pH, temperature; Secchi depth measured at Reed Bower.
  - Water samples collected as duplicates from each site; Reed Bower uses a vertical integrated sample, Sluices uses near-surface sample.
  - Laboratory analyses include filtered and unfiltered samples for phosphorus forms, silicate, diatom silica, chlorophyll a; standardized filtering and storage procedures.
  - Phosphorus analyses based on established methods (Murphy & Riley for SRP; Wetzel & Likens for TP/TSP with digestion); chlorophyll a analysis via filtration.
  - Weather observations (when possible) include cloud cover and wind; wind force mapped to Beaufort scale with descriptive table.

- Data processing and quality assurance
  - Import script in R handles data ingestion with sensible decisions (e.g., wind force values, replicate handling).
  - Probe replicate handling uses Median Absolute Deviation (MAD) to filter outliers; pH values are transformed for processing and back-transformed for final reporting.
  - Instrument continuity maintained across model changes (HQ30d to HQ4300) by keeping column structure consistent; new model values prepared for future datasets.
  - Automated and manual QA checks performed; anomalies investigated and corrected as appropriate.

- Data format and metadata
  - Stored as a single CSV file with columns detailing determinand, site conditions, lake chemistry, and zooplankton counts; missing values indicated as NA.
  - Table 3 (and accompanying documentation) provides detailed column-level metadata, including date, week of year, site, units, and descriptive details for each variable.

- Data provenance, references, and documentation
  - Data collection and processing described with references to standard methods and previous hydrological/limnological literature.
  - Core references include Golterman et al. (1978), Murphy & Riley (1962), Wetzel & Likens (2000).
  - Additional reading and project context provided through related Hydrobiologia outputs and Scottish Natural Heritage reports.

- Implications for data use and governance (Data Leaders perspective)
  - Rich, multi-decadal time series enabling trend analysis of water quality and zooplankton communities in Loch Leven.
  - Comprehensive metadata and standardized processing enhance discoverability, reuse, and cross-dataset integration.
  - Potential challenges include gaps due to sampling interruptions, changes in instrumentation, and the need to maintain consistent unit conventions and taxonomic resolution over time.
  - Clear provenance, methods, and QA processes support credible downstream analyses and integration with wider data communities.