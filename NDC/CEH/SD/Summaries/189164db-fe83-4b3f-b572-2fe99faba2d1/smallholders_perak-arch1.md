# Data on the locations of and temperatures (in deg C) recorded by dataloggers deployed in the soil during surveys at 24 oil palm smallholder farms in Perak, Malaysia, over approximately a 24-hour period.

- Scope
  - Soil temperature and logger locations across 24 oil palm smallholder farms in Perak, Malaysia.
  - Surveys conducted over roughly a 24-hour period between May and July 2022.
  - Includes three levels of smallholder collaboration with Wild Asia: WAGS-BIO, WAGS, and Independent farmers.
  - Four sampling locations per farm (T1–T4), spaced 20 m apart, totaling 96 sampling points.
  - Dataloggers buried at 5 cm depth; data collected in field campaigns by Wild Asia researchers; quality-checked by University of Cambridge.

- Data content and structure
  - Datalogger data
    - Variables track plantation, sampling point, and hourly soil/air temperature readings (TempHr1 through TempHr26).
    - Key fields: PlantationCode, SamplePoint, TempHr1–TempHr26, with units in °C.
    - Notes on data quality: NA used when a log was collected earlier than 26 hours or when data are missing.
  - Observational context
    - Observational data accompany soil measurements, adding species/biological context (butterflies, spiders, assassin bugs), weather, and microhabitat details.
  - Data handling
    - Data downloaded/checked for timing consistency, standardized for Cambridge analyses, and uploaded with metadata.

- Example variables ( Highlights)
  - PlantationCode, SamplePoint: Plot and logger location (T1–T4).
  - TempHr1–TempHr26: Air temperature readings at hourly intervals after logger deployment.
  - Weather conditions, date, and time fields to align environmental context with temperature data.

- Study design and locations
  - Four locations per plantation (T1–T4), 96 total sampling points across 24 farms.
  - Field campaigns conducted May–July 2022; data centrally quality-checked by Cambridge team.
  - Dataloggers wrapped in foil and buried in soil to minimize disturbance.

- Practical considerations for analysts
  - Temporal resolution is hourly for up to 26 hours post-deployment; late collections yield NA entries for corresponding hours.
  - Data are primarily environmental/physical (soil temperature), with ancillary observational data on flora/fauna and weather to support correlational analyses.
  - Three levels of smallholder collaboration introduce a quasi-experimental structure for assessing management impact on soil conditions.

- Potential analyses and questions
  - Correlations between plantation management type (WAGS-BIO, WAGS, Independent) and soil temperature profiles.
  - Temporal patterns in soil temperature across plots and their relation to canopy cover or vegetation attributes (if combined with other datasets).
  - Interaction of soil temperature with microhabitat variables collected in accompanying observational datasets (e.g., insect activity or plant cover).
  - Assessment of data gaps and scale alignment when linking with other Wild Asia datasets (e.g., vegetation, biodiversity, or social surveys).

- Data quality and provenance notes
  - Data consolidated and standardized at the University of Cambridge; timing and realism checks performed against field logs.
  - Metadata describe variable definitions, units, and data provenance to ensure reproducibility and discoverability.

- Caveats and limitations for interpretation
  - Focused on short-term (roughly 24-hour) temperature measurements; longer-term trends require integration with other time-series datasets.
  - Some hours and records may be NA due to early collection or missing data; interpret with appropriate imputation or exclusion.
  - Temperature data are auxiliary to broader biodiversity and management datasets; cross-dataset analyses require careful alignment of sampling threads (locations, dates, and plantation type).

- Related datasets and context (from the same project)
  - Observational biodiversity data (butterflies, spiders, assassin bugs) with weather and microhabitat context.
  - Data on set-up/collection times for sticky traps, dataloggers, and bait cards, plus mealworm counts.
  - Arthropod abundance data from sticky traps (taxa counts by order; removal data).
  - Vegetation, microclimatic, and soil condition data across 47 plantations (environmental mapping, soil chemistry and structure).
  - Plantation characteristics and management survey data (social/economic variables, attitudes toward nature, management motivations) across 49 plantations, with international comparators (Indonesia and Malaysia).

- Access and usage notes
  - Data are described with extensive metadata and field definitions; datasets are prepared for portal discovery and reuse.
  - Some fields use non-SI currencies (e.g., Malaysian ringgit, Indonesian rupiah) and self-reported information; appropriate normalization and auditing recommended for cross-site comparisons.
  - Cross-dataset analyses can illuminate interactions between management, soil conditions, and biodiversity, but require careful alignment of temporal and spatial keys (e.g., PlantationCode, SamplePoint, and date stamps).