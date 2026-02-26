# Countryside Survey

## Overview
- A long-running study/audit of the UK's countryside natural resources, conducted at regular intervals since 1978.
- Adopts a rolling program (from 2019) to monitor changes over time, enabling comparability with past surveys.
- Recent cycle focuses on soil and vegetation data; starting in 2024, additional linear landscape feature plots are included (boundary, roadside, streamside, hedgerow).
- UKCEH Countryside Survey (UKCEH-CS) rolling program visits ~500 1km squares on a five-year cycle to balance site coverage and year-to-year monitoring, detecting spatial and temporal change cost-effectively.

## Design and rolling program
- Multi-metric, ecosystem-based design: measures soil, vegetation, headwater streams, habitats, and landscape features; aims to answer questions about size, location, causes, and consequences of change.
- Rolling program steps:
  - 2019-2023: focus on soil and vegetation at five plots per 1km square.
  - 2024 onward: add plots for linear landscape features (1 boundary, 1 roadside, 1 streamside, 1 hedgerow; England hedgerows sampled for dominant species).
- Sample selection:
  - 500 x 1km squares randomly chosen for survey each cycle.
  - Stratified by the Land Classification of Great Britain (ITE method).
  - Approximately 100 squares visited annually.
  - Exclusions: any square with >75% urban land or >90% sea (per LCM2007 and census data).

## Data collection, quality, and methodologies
- Data collected by trained field surveyors following standard protocols (Smart et al., 2024), with intensive pre-survey training to ensure consistency.
- Field surveys supervised and then monitored by experienced project staff to maintain data quality.
- Quality assurance: 10% of plots re-surveyed by QA assessor; ongoing QA analysis conducted by the same assessor since 1990 for consistency and validation (including plot location and habitat classification alignment with JNCC).
- Confidentiality: distribution maps are anonymized to protect data confidentiality.

## Data products and data schema
- Two primary vegetation data files for 2024:
  - UKCEHCS_VEGETATION_PLOTS_2024.csv
    - Plot-level information: YEAR, SQUARE_ID, PLOT_TYPE (B boundary, H hedgerow, R roadside, S streamside), PLOT_ID, LC07/LC07_NUM (ITE Land Classification), ENV_ZONE_2007 (environmental zone), EZ_DESC_07, COUNTRY, COUNTY, and various plot attributes (e.g., TREES, TREES_DEAD, TREE_DISEASE, CANOPY_HT, SHRUB_HT, etc.).
    - Plot geometry and site descriptors (e.g., boundary/road/stream/hedgerow specifics).
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2024.csv
    - Species list per plot including BRC identifiers, species names, nesting records, nest level counts, percent cover per nest, total cover, and notes on total canopy vegetation.
    - Nomenclature aligned with Stace (1997).
- Data relationships:
  - Ties to the ITE Land Classification (Bunce et al., 1996; 2007) and Environmental/Zones (ENV_ZONE_2007).
  - Links to broader Countryside Survey documentation and methodologies (Field Handbook 2024-2029; supporting references: Jackson 2000; Maddock 2008; Norton et al. 2012; Scott 2008; Smart et al. 2024; etc.).
  - Referenced resources and datasets accessible via the Countryside Survey website and associated data chapters.

## Methods and quality assurance details
- Field methodologies documented in the UKCEH Countryside Survey Field Handbook (2024-2029) with standardized survey and data recording procedures.
- QA processes include:
  - 10% plot re-surveys by QA assessor on each survey cycle.
  - Independent validation of plot locations and their classification within JNCC habitat frameworks.
- Data provenance and traceability are maintained through consistent QA assessors since 1990, enabling robust assessment of detection variation across year and location.

## Practical notes for data users and data support considerations
- Data are designed to support self-serve data exploration via plot-level and species-level records across years, enabling trend analysis and policy-relevant insights.
- The rolling five-year cycle and standardized methodologies enhance comparability across cycles and with historical data.
- Users should account for:
  - The expansion in 2024 to include linear landscape feature plots, which adds new data types to the historical dataset.
  - The environment zones, land classifications, and plot-type codes when merging with other datasets.
  - Confidentiality constraints on spatial distribution maps.
- Core data access is via the Countryside Survey dataset, with complete metadata and field handbook references to ensure reproducibility and comparability across analyses.