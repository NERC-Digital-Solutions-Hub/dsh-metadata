# PhenotypeField.txt

- Overview
  - Document describes the phenotype data dictionary for tree measurements across multiple years, including identifiers, location, and year-specific budburst and growth metrics.
  - Core fields cover site/population identity, geographic coordinates, and tree-level identifiers (seedling, family, bush/tree references).
  - Yearly phenotype fields (2015–2020) capture growth, budburst timing, and stage-specific observations, with dedicated time-to-event fields and duration metrics.

- Key identifiers and location
  - Site and Population metadata: Site of Population, Population code, Family, Family code, and related fields describing lineage and maternal origin.
  - Spatial data: Latitude and Longitude (decimal degrees) representing population location.

- Core tree identifiers and sampling structure
  - ID fields: ID, PopCode (population code), Unique individual tree id.
  - Seedling and family structure: Seedling number within family, Block, Randomised (block design), and family relationships (e.g., "family code are from the same mother tree").

- Phenotype fields by measurement type
  - Height: Height measurements with units (cm), including yearly entries (e.g., I15 Height, I16 Height, I17 Height, etc.).
  - Growth and increments: Height increments between years (e.g., increment, increment (increase in height from year to year)).
  - Budburst stage timing: Stage-based measures with defined stages (Stage 4: scales open, Stage 5: budburst with white tipped needles, Stage 6: needles visible) and associated timing.
  - Time to reach stages: Numerous fields denoting time (in days) from first observation to reaching a given stage, labeled with year-specific prefixes (e.g., T4-15, T5-15, T6-15 for 2015; T4-16, T5-16, etc.).
  - Duration and progress: Time taken to reach stages, duration of shoot growth, and related durations (often framed as "Time taken to reach stage X" and "Duration" fields).
  - Observation timing: First observation at each site for each tree, observation timing relative to site, and days since first observation to reach specific stages.

- Yearly structure and naming conventions
  - 2015 fields: I15 Height, budburst timing to stage 4/5/6, year-specific increments, and time-to-stage fields (e.g., T4-15, T5-15, T6-15).
  - 2016 fields: I16 Height, stage timings, and time-to-stage metrics (e.g., T4-16, T5-16, T6-16).
  - 2017 fields: I17 Height, stage timings, and time-to-stage metrics (e.g., T4-17, T5-17, T6-17).
  - 2018 fields: I18 Height, changes from 2017, stage metrics (e.g., budburst and stage 4 open along length of shoot).
  - 2019 fields: I19 Height, year-to-year increments, and stage/timing fields (e.g., T4-19, T5-19, T6-19).
  - 2020 fields: I20 Height, increments, and stage progression timing (e.g., T4-20, T5-20, T6-20).

- Stage-specific details (example concepts)
  - Stage 4: Scales open along length of shoot; includes timing to reach this stage and duration measurements.
  - Stage 5: Budburst with white tipped needles; timing and related duration fields.
  - Stage 6: Budburst with green needles visible; timing and related duration fields.

- Data structure and data quality considerations
  - Many fields are year-specific, combining into a longitudinal dataset across 2015–2020.
  - Some fields are described with placeholders or incomplete text (e.g., "." entries), indicating potential missing values or non-applicable cases for certain years or trees.
  - Data are organized to enable cross-year analyses by tree and site, using a consistent identifier system (ID, PopCode, Unique tree id) and year-specific field naming.

- Genotype data (GenotypeField.txt)
  - SNP marker metadata is included with snpid and marker-related fields.
  - Unique individual tree id is used to join genotype information with phenotype data.

- Practical use and data support implications
  - The dataset supports building self-serve analytics (dashboards, pivot tables) that summarize height growth, budburst timing, and stage progression over time.
  - Facilitates cross-year analysis of growth trajectories and phenological responses at multiple sites.
  - Enables integration with genotype information for genotype-phenotype analyses.

- Caveats for users
  - Expect patchy data across years and sites; plan for data cleaning and alignment across year-specific fields.
  - Pay attention to year-coded field prefixes (I15, T4-15, etc.) to correctly aggregate longitudinal measurements.
  - Ensure proper joining of phenotype and genotype data using the Unique individual tree id.