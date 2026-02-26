# AquaticMicrofibreExposurestudies2015-2024 Supporting information

## Overview of the dataset
- What: A dataset extracted from published laboratory studies on microfibres (<5 mm) effects on aquatic organisms, covering traits such as development, fecundity, feeding, growth, hatching, health, and survival.
- Where: Collected from published literature worldwide.
- When: Data accessible as of 19/06/2024; covers studies from 2015 to 2024.
- How: Data extracted directly from manuscripts (MS), supplementary information (SI), and figures using a plot digitiser when needed.
- Why: Compiled for a meta-analysis comparing responses to non-petroleum vs. petroleum-based microfibres.
- Who: Data collection and dataset compilation conducted by Ben Parker.
- Completeness: Includes only eligible studies and responses per defined criteria; references of eligible studies listed.

## Collection and generation
- Search and identification: Topic search in Web of Science (published articles, all collections) using microfibre/microfiber/textile and effect; conducted 19/06/2024.
- Screening process: Three-stage approach
  - Stage 1: Title/abstract relevancy for biological responses to microfibre exposure.
  - Stage 2: Screening of citing/cited studies for relevancy.
  - Stage 3: Eligibility screening with detailed criteria.
- Eligibility criteria: 
  - Aquatic organisms
  - Controlled microfibre exposure (>1 µm and <5 mm) of a single polymer type (no mixtures)
  - Means with errors available for exposure and control
  - Data extractable from MS/SI or supplementary material
- Data extraction: All eligible responses for key traits; final timepoint/lifestage used for multi-timepoint data; only non-co-contaminant exposures included; positive responses prioritized (and some negative responses converted to positive where appropriate).
- Data included: All eligible responses with exposure combinations across starved/fed conditions, excluding co-contaminants; data for multiple traits, exposures, and life stages as reported.

## Quality control
- Stage 1 and Stage 2 screening used to filter studies by relevance to microfibre exposure effects.
- Stage 3 eligibility screening implemented to confirm suitability and data extractability.
- Data extraction criteria ensure standardized selection of mean and error measures suitable for meta-analysis.

## Data structure and units
- File: AquaticMicrofibreExposurestudies2015-2024.csv
- Key fields (examples):
  - ID, Study.no, Reference, Authors, Title, Year, FA.country, Species, Source
  - Environment, Taxonomic.grouping
  - Days.exposed, Days.cat
  - Microfibre category (MF.category), Fibre.material, Length.mm, Length.cat, Width.mm
  - Study.exposure, Study.exposure.units, Standard.exposure, S.cat, Standard.units
  - Time.series, Additional.variable
  - Response, Converted.measure, Response.units
  - C.N, C.mean, C.SD (control), E.N, E.mean, E.SD (experimental)
  - Data.source
  - Where the data were extracted from (MS/SI)
- Categories and coding:
  - Trait classifications: Development, Fecundity, Feeding, Growth, Hatching, Health, Survival
  - Exposure and unit handling: Standardised exposure values (log-scale categories from A to K representing 10^-3 to 10^7), units may be by mass (µg/L) or fibre number (fibres/L)
  - Time and environment: Days exposed, environmental context (Freshwater, Marine, Estuarine), organism taxonomic grouping
- Data extraction specifics:
  - Means and standard deviations drawn from manuscript text, figures, or SI
  - For time-series data, only the final timepoint/lifestage is included
  - Negative responses converted to positive when outcome deemed beneficial for meta-analysis

## Data provenance and access
- Data source: Extracted from published MS and SI, with references provided for each study.
- Study references: Includes a wide range of studies (e.g., Au et al. 2015; Blarer & Burkhardt-Holm 2016; Bour et al. 2022; Choi et al. 2021, 2022; Cole et al. 2020; Jemec et al. 2016; Jabeen et al. 2018; etc.).
- Data collection and stewardship: Conducted by Ben Parker; dataset compiles globally conducted laboratory studies.
- Availability date: 19/06/2024; dataset reflects studies up to 2024.

## Implications for data governance and stewardship
- Data quality and standardization:
  - Clear, structured schema with explicit trait categories, exposure units, and timepoint rules supports interoperability but requires consistent interpretation of coded fields.
  - Conversion of non-directly compatible responses (e.g., negative responses converted to positive) should be documented and versioned.
- Metadata and provenance:
  - Comprehensive provenance through MS/SI references; explicit notes on data extraction sources enhance traceability.
  - Detailed field descriptions and the inclusion of both raw (C./E./N./mean/SD) and data source annotations facilitate auditability.
- Completeness and scope:
  - Transparent eligibility criteria limit scope to single-polymer, non-co-contaminant exposures, which may affect generalizability.
  - Final timepoint extraction may omit potentially informative intermediate responses; users should consider this when interpreting meta-analytic results.
- Access, licensing, and updates:
  - Dataset notes the existence of update mechanisms and adherence to sharing limitations; stewardship should define versioning, update cadence, and licensing to enable reuse.
- Data management considerations for future work:
  - Implement robust data validation and consistency checks across all fields (e.g., unit standardization, timepoint labeling).
  - Maintain a data dictionary and changelog to accompany updates.
  - Ensure clear documentation of any transformations or conversions applied during extraction.