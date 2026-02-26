# Loch Leven long-term monitoring dataset

- Overview
  - Data originate from a long-term monitoring programme of Loch Leven, a lowland lake in Scotland, initiated in 1968 and ongoing.
  - Collected and processed by NERC and CEH staff; project linked to UK-SCAPE WP7 LEVEN.
  - Document describes data nature, sampling/analysis methods, data processing, and output format. Includes both physicochemical and biological (crustacean/zooplankton) data.

- Sampling regime and Sites
  - Fortnightly sampling with two main sites: Reed Bower (RB) and Sluices (L/Sl8).
  - RB is boat-accessible; Sluices can be sampled by boat or shore/outflow.
  - Data sometimes missing due to resource, weather, or ice; in some cases only Sluices sampled, or neither site.
  - Site codes and coordinates provided (Harbour H, Reed Bower RB, Sluices L/Sl8) with UK National Grid references.

- Measurements, measurement locations, and analysis
  - In situ measurements: conductivity, pH, temperature; Secchi depth measured at Reed Bower.
  - Water samples collected at each site for laboratory analysis of SRP, TP, TSP, soluble silicate, total diatom silica, chlorophyll a, and related parameters.
  - Sampling methods:
    - Duplicate 2 L water samples per site; vertical integrated sampling at Reed Bower; surface-limited sampling at Sluices.
    - Filtration and storage protocols described for each analyte; standard chemical methods referenced (Murphy & Riley for phosphate, Wetzel & Likens for TP, etc.).
  - Weather observations (cloud cover, wind direction, wind force) recorded at Reed Bower when possible; Beaufort scale used with detailed wind-force table.

- Data processing
  - An import script in R processes data before database entry; includes:
    - Wind force handling for ranges (e.g., "4-5" uses first value).
    - Probe replicate values: uses Median Absolute Deviation to retain plausible values; converts pH values for calculation, then back-transforms; rounds resulting values (pH/DO to 2 decimals; conductivity and temperatures to 1 decimal).
  - Quality Assurance (QA)
    - Automated and manual checks for data entry errors and out-of-range values; unusual values investigated and corrected as needed.

- Data format and storage
  - Stored as a single CSV file with columns describing determinand, site conditions, lake chemistry, and crustacean/zooplankton counts.
  - Missing data coded as NA.
  - Column naming convention includes determinand, site, and units; core reference is Table 3 (detailed column descriptions).

- Column descriptions and core dataset content
  - Variables span:
    - Date, Week of Year, climate indicators (cloud cover, wind direction, wind force).
    - Site-specific measurements: water depth, Secchi depth, conductivity, temperature, dissolved oxygen (mg/L and %), pH, pH/temperature measurements.
    - Nutrients and chlorophyll: TP, SRP, TSP, chlorophyll a (with replicates).
    - Crustacean zooplankton densities for numerous taxa (per litre), with site-specific rows (RB and L).
  - Replicate handling: many analytes have replicate columns (e.g., TP_rep1/rep2; SRP_rep1/rep2; chla_rep1/rep2; zooplankton replicates per site).
  - Column descriptions are provided in detail to facilitate interpretation and reuse.

- Crustacean & Zooplankton data
  - Densities reported as ind/L for a suite of taxa (e.g., Daphnia hyalina, Eudiaptomus gracilis, Cyclopodidae, Cyclops species, Bosmina longirostris, Leptodora kindti, Bythotrephes longimanus, Chydoridae, Polyphemus pediculus).
  - Sampling methods differ by site (RB: 4 m net haul; L: 30 L of surface water through 120 µm net) and samples preserved in formaldehyde.
  - Sub-sampling and counting conducted under microscopy; counts converted to ind/L using species-specific factors; preserved samples archived.
  - Taxonomic identification performed when possible; some identifications limited by preservation stage.

- References and supplementary information
  - Method references for chemical analyses and nutrient methods (e.g., Golterman et al., Murphy & Riley, Wetzel & Likens).
  - Additional resources and monitoring reports related to Loch Leven provided for context and further reading.

- Relevance for data governance and stewardship
  - Comprehensive metadata and methodological detail support data discoverability, reproducibility, and reuse.
  - Clearly defined data formats (CSV) and replicates, with explicit QA processes and update pathways.
  - Documentation addresses common data stewardship challenges: standardization across long timeframes, multiple systems/formats, and handling of incomplete or missing data.
  - The dataset is designed to be updated within a governed framework, with explicit provenance (institutions involved, sampling regimes, and analytical methods).