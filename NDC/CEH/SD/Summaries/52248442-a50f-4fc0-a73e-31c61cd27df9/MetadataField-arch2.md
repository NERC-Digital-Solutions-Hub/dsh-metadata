# PhenotypeField.txt

- Overview
  - A comprehensive, standardized schema for environmental/phenotypic monitoring of trees across multiple sites and years (example years referenced include 2015–2020). Captures spatial metadata, population/family structure, and detailed phenotypic observations such as height and budburst-related metrics.
  - Includes both year-specific measurements and stage-based phenology descriptors, plus observation timing and first-collection metadata.

- Core data categories
  - Identification and population metadata
    - Site, Population code (PopCode), Population code, Family, Family code (from), Seedling number within family, Block, and unique tree identifiers (ID, Unique individual tree id).
  - Location and spatial reference
    - Latitude (decimal degrees), Longitude (decimal degrees).
  - Experimental design and sampling structure
    - Observational structure such as Randomised or Block design indicators, and related fields describing how trees are organized and sampled within trials.
  - Phenotypic measurements by year
    - Height measurements (in cm) across multiple years, with corresponding year-labels (e.g., I15, I16, I17, etc.), and year-specific increments (growth from year to year).
    - Time-to-event and phenology fields for budburst and related stages (e.g., Stage 4, Stage 5, Stage 6) across years.
  - Growth and budburst metrics
    - Height trajectories, increments between years, stage-specific descriptors (e.g., budburst with scales opening, tipped needles visible, green needles visible).
    - Stage-specific timing records (days to reach a given stage, time taken from first observation to reach stage), including day-count fields such as T4-18, T5-18, T6-18, etc.
  - Phenology descriptors and stage definitions
    - Detailed textual descriptors for each stage (e.g., "scales open along length of shoot," "budburst: time," "tipped needles visible," "green needles visible"), with corresponding numeric indicators (1–35-scale-style fields) and site-by-site observations.
  - Observational timing and first observations
    - First observation at each site for each tree, and year-specific timing indicators (e.g., "first observation at" fields).
  - Data provenance and quality notes
    - Descriptive field-level notes and units (e.g., decimal degrees for coordinates, cm for height, days for time-based metrics).

- Yearly and stage-specific snapshots (examples)
  - Height and increments: I15, I16, I17, I18, I19, I20 (height observations); corresponding increment fields (increase in height from year to year).
  - Budburst timing and stages: T4-16 through T6-19 and similar, representing time taken to reach stages 4–6; stage-specific narratives such as “scales open along length of shoot,” “tip needles visible,” and “green needles visible.”
  - Time-to-reach-stage metrics: Days to reach budburst stages for 2015–2020 cohorts, including first observation timing and days elapsed since first observation.
  - Stage descriptors and measurements across sites/trees: Stage 4-18 to Stage 6-19 series with parallel textual descriptors and numeric codings.

- Genotype data linkage
  - GenotypeField.txt
    - SNP marker identifiers (snpid), with a column for the unique tree identifier (NA for some fields), enabling linkage between phenotypic observations and genotype data (e.g., BE7_6_C_YA and other markers).

- Data quality and access considerations for analysts
  - The schema is designed for verification, quality assurance, cleaning, and transformation from established data sources.
  - Outputs are intended to be presented in standardized formats (e.g., reports, maps, charts) and stored/uploaded to appropriate data portals to support ongoing monitoring and policy evaluation.
  - A core objective is to increase the value of datasets by enabling integration with other relevant data and by ensuring underlying data remain accessible for reuse.

- Relevance to environmental monitoring aims
  - Enables consistent time-series assessment of environmental health indicators (growth, phenology, and phenology-driven responses) across multiple populations and sites.
  - Facilitates scrutiny of environmental health and policy performance over time by providing standardized, comparable metrics across years and locations.