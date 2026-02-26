# WildCrickets06A_EarlyLatencyVsSenescence Description of content

- Overview
  - Dataset describes singing activity per cricket sample and per individual male.
  - Classifies mating latency as high or low (EarlyLatency) relative to the population median.
  - Focuses on the relationship between early mating latency and senescence indicators via singing data.

- Data elements and coding
  - Latency: Coded as High (H) or Low (L).
  - EarlyLatency: Label indicating whether latency to mate is above or below the population median.
  - Year: Year when the cricket was alive (temporal context for the record).
  - ID: Individual identification (unique identifier for each cricket).
  - Temp: Ambient temperature at the time of sampling (degrees Celsius).
  - Age: Age at sampling (in days).
  - Sings: Binary indicator of singing behavior during sampling (1 = singing, 0 = not singing).

- Scope and context
  - Data captures per-sample and per-individual mating latency and singing activity, with environmental context (temperature) and demographic context (age).
  - Aims to support analyses of how latency to mating relates to senescence, modulated by temperature and age.

- Data quality and governance considerations
  - Metadata should clearly define variable formats, units, and permissible values (e.g., Latency/H; Temp in °C; Age in days; Sings as 0/1).
  - Document measurement methods for latency classification (how the population median was calculated, timing of measurements).
  - Ensure clear provenance: who collected the data, sampling dates, and any data transformations (especially for the EarlyLatency designation).
  - Identify and describe any missing data and handling procedures.
  - Maintain consistent identifiers (ID) across samples and individuals to avoid duplication.

- Sharing, access, and stewardship
  - Store in a dataset repository with a stable schema and versioning to track updates.
  - Provide a data dictionary and method notes alongside the dataset for discoverability and reuse.
  - Consider data retention and update processes if new samples or revised classifications are added.
  - If applicable, note any embargo periods or restrictions related to the dataset.

- Use cases and potential analyses
  - Examine associations between EarlyLatency (latency to mate) and indicators of senescence via singing behavior.
  - Explore how temperature (Temp) and age influence singing activity (Sings) and latency classification (Latency).
  - Facilitate cross-study comparisons by standardizing variable definitions and units.