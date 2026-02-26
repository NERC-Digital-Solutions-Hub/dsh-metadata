Loch Leven long-term monitoring programme data

Overview
- Describes the Loch Leven long-term monitoring dataset from Scotland, UK, part of the UK-SCAPE WP7 LEVEN project.
- Purpose: document data, sampling/analysis methods, data processing, and output formats to support consistent environmental health assessments and policy performance monitoring over time.
- Data origin: collected by Natural Environment Research Council (NERC) and UK Centre for Ecology & Hydrology; ongoing since 1968.

Monitoring regime and sites
- Sampling frequency: fortnightly; two main sampling sites visited per occasion.
- Primary sites: Reed Bower (RB) and Sluices / Outflow (L; also labeled Sl8 in some data).
- Additional reference: Harbour site codes (Site_H) used in several datasets; map provided for RB, L, and H.
- Accessibility constraints: boat availability, weather, ice can limit sampling; if boats unavailable, only Sluices may be sampled or neither site sampled.
- Site coordinates: Harbour, Reed Bower, and Sluices with corresponding UK National Grid coordinates.

Measurements, parameters and methods
- In situ measurements: conductivity, pH, temperature; Secchi depth measured at Reed Bower (water clarity).
- Water sampling: duplicate 2 L samples from each site for laboratory analyses.
- Collection specifics:
  - Reed Bower: integrated water column sample via weighted tube.
  - Sluices: bottle sampled 10 cm below surface.
- Analyses (lab): SRP, TP, TSP, soluble reactive silicate, total diatom silica, total phosphorus, and chlorophyll a (via filtered samples).
- Nutrient methods: SRP by Murphy & Riley (1962); TP via persulfate digestion per Wetzel & Likens (2000) with added acid step; TSP via similar approach on filtered samples.
- Physical & other data: weather observations at Reed Bower when possible; wind force linked to Beaufort scale with a provided lookup table.
- Data format: results stored for each determinand by site, including units and context.

Crustacean and zooplankton data
- Composition: densities (ind/L) of crustacean zooplankton taxa at Reed Bower and Sluices.
- Taxa include Daphnia hyalina, Eudiaptomus gracilis, Eudiaptomus nauplii, Cyclopodidae, Cyclops species, Bosmina longirostris, Leptodora kindti, Bythotrophes longimanus, Chydoridae, Polyphemus pediculus, among others.
- Sampling and preservation: at Reed Bower, 4 m net hauls (120 µm); at Sluices, 30 L surface water through a 120 µm net; preserved in 4% formaldehyde.
- Laboratory processing: subsampling and counting under a microscope; identification to species level when possible; counts converted to number per litre.
- Notes: zero indicates non-detection at the sampling resolution; NA indicates missing values.
- Taxon-specific references are provided for identification keys and methodologies.

Data processing and quality assurance
- Processing: an R-based import script cleans and structures data for database entry.
- Wind data: when a range (e.g., "4-5") is input, the first value is used.
- Probe replicate handling: replicates screened with Median Absolute Deviation (MAD) criteria; values outside MAD are discarded; pH values are transformed for calculation (10^pH, then log10 back).
- Calibration: inter-calibration between Hach HQ30d and HQ4300 models; dataset uses HQ30d column nomenclature for consistency; future datasets will separate HQ4300.
- Rounding: pH/DO in 2 decimals; conductivity and temperatures in 1 decimal.
- QA: automated and manual checks for data entry errors and out-of-range values; anomalies investigated and corrected as needed.

Data format and documentation
- Primary storage: a single CSV file containing all columns, with units, sites, and context in column headers.
- Missing data: represented as NA.
- Column structure: date, site, week of year, and numerous measured determinants (e.g., water level, cloud cover, wind, depth, Secchi, conductivity, temperature, DO, pH, TP, SRP, TSP, chlorophyll a, zooplankton densities, and related metadata).
- Column descriptions: Table 3 provides full descriptions of each column, including determinand, site, and units.

Format of outputs and references
- Outputs aimed at standard, shareable formats for long-term trend analysis and cross-study comparisons.
- References for measurement methods and related readings are provided (Golterman et al., Murphy & Riley, Wetzel & Likens) and expanded reading on Loch Leven research is noted.

Data usage and objectives for analysts monitoring the environment
- Enables consistent, time-series assessment of Loch Leven’s environmental health and policy performance.
- Supports data verification, quality assurance, and standardised reporting formats (maps, charts, reports) for transparency and scrutiny.
- The dataset is part of broader efforts to maximise dataset value and facilitate access to underlying data for broader analysis and integration with other environmental datasets.