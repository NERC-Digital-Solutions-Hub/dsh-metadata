# AquaticMicrofibreExposurestudies2015-2024 Supporting information

- The dataset collects trait-level responses of aquatic organisms to microfibre exposure from published laboratory studies (microfibres < 5 mm).
- Geographic scope: studies from around the world; data compiled up to 19 June 2024 (2015–2024 studies).
- Purpose: meta-analysis to compare biological responses to non-petroleum vs petroleum-based microfibres.
- Compiler: Ben Parker.
- Completeness: only studies that meet predefined eligibility criteria (Collection/generation) are included.

## What’s included in the dataset

- Traits covered: Development, Fecundity, Feeding, Growth, Hatching, Health, Survival.
- Response direction: only “positive” responses (increase deemed good) are included; some negative responses converted to positive to be included.
- Exposure scope: all eligible responses across starved/fed conditions and various parameters, excluding co-contaminants.
- Timepoints: for multi-timepoint data, only the final timepoint/lifestage is included.
- Data extraction sources: mean and standard deviation extracted from manuscripts, supplementary information, or figures using a plot digitiser.
- Dataset file: AquaticMicrofibreExposurestudies2015-2024 (CSV) with detailed metadata per response.

## Collection and screening process

- Search strategy: Web of Science topic search using "microfibre" OR "microfiber" OR "textile" AND "effect" (articles, 2015–2024).
- Screening stages:
  - Stage 1: relevance based on whether the study measures biological response to microfibre exposure.
  - Stage 2: forward and backward screening of citing/cited studies for relevance.
  - Stage 3: eligibility screening with strict criteria.
- Eligibility criteria:
  - Aquatic organisms used.
  - Controlled microfibre exposure (single polymer type, >1 µm and <5 mm, no mixtures).
  - Means with errors available for both exposure and control, extractable data.
- Data extraction scope: all eligible responses across key traits, with consistent exposure/response extraction and metadata.

## Data structure and units

- Core CSV: AquaticMicrofibreExposurestudies2015-2024 with the following types of fields:
  - Study.no, Reference, Authors, Title, Year
  - FA.country (country of first author)
  - Species, Source (where the organism was sourced)
  - Environment (Freshwater, Marine, Estuarine, etc.)
  - Assigned taxonomic grouping
  - Days.exposed, Days.cat (exposure duration categories)
  - Microfibre category (Non-petroleum vs petroleum-based)
  - Fibre.material, Length.mm, Length.cat, Width.mm
  - Study.exposure, Study.exposure.units, Standard.exposure, S.cat, Standard.units
  - Time.series, Additional.variable
  - Response (trait category: Development, Fecundity, etc.)
  - Converted.measure, Response.units
  - C.N, C.mean, C.SD (control counts/means/SD)
  - E.N, E.mean, E.SD (experimental counts/means/SD)
  - Data.source (source of data extraction: MS, SI, or figure)
- Trait categories (C.N, C.mean, C.SD) correspond to Development, Fecundity, Feeding, Growth, Hatching, Health, Survival.
- Standardised exposure and units are annotated (by mass or fibre number, e.g., 10^-3 to 10^7 scale).

## Quality control

- Screening and eligibility were applied in three stages to reduce duplicates and ensure relevance and extractability.
- Criteria ensured exposure was to a single polymer and that data could be reliably extracted (means with errors for both control and exposure).
- Data extracted directly from manuscripts, supplementary information, or digitised figures to maximise coverage of eligible studies.

## Study references (examples)

- Au, S.Y., Bruce, T.F., Bridges, W.C., Klaine, S.J., 2015
- Blarer, P., Burkhardt-Holm, P., 2016
- Bour, A., Leoni, D., Sundh, H., Carney Almroth, B., 2022
- Bunge, A., Lugert, V., McClure, M., et al., 2022
- Cheng, H., Feng, Y., et al., 2021
- Cheng, S., Jessica, Yoshikawa, K., Cross, J.S., 2024
- Choi, J.S., Kim, K., Hong, S.H., et al., 2021
- Choi, J.S., Kim, K., Park, K., et al., 2022
- Cole, M., Liddle, C., Consolandi, G., et al., 2020
- Coppock, R.L., Galloway, T.S., Cole, M., et al., 2019
- Cui, R., Kwak, J. Il, An, Y.J., 2022
- DiBona, E., Haley, C., et al., 2022
- Hu, L., Chernick, M., et al., 2020
- Jabeen, K., Li, B., Chen, Q., et al., 2018
- Jemec, A., Horvat, P., et al., 2016
- Jiang, Y., Li, Q., et al., 2023
- (and additional references spanning 2015–2024)

## How to use the dataset

- Designed for meta-analytic comparisons between non-petroleum and petroleum-based microfibres across multiple aquatic species and traits.
- Each row corresponds to a single study–response observation with associated exposure and outcome data, enabling cross-study synthesis and modeling.
- Limitations to consider:
  - Only single-polymer exposures; co-contaminants are excluded.
  - Final-timepoint data; dynamic temporal patterns beyond the final measure are not captured.
  - Data derived from text, supplementary materials, or digitised figures; potential digitising error may affect some values.
  - Data availability depends on reporting in MS/SI/figures; not all potentially relevant studies may be represented.