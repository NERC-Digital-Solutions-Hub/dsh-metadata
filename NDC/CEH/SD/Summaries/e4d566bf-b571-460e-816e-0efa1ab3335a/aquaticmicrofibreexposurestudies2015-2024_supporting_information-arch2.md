# AquaticMicrofibreExposurestudies2015-2024 Supporting information

## Overview of the dataset
- A dataset comprising the CSV file 'AquaticMicrofibreExposurestudies2015-2024' derived from published laboratory studies on microfibre exposure (< 5 mm) and its effects on aquatic organisms.
- Scope: studies from 2015 to 2024, sourced from published literature worldwide.
- Purpose: support a meta-analysis comparing biological responses to non-petroleum versus petroleum-based microfibres.
- Collected and compiled by: Ben Parker.
- Completeness: includes only eligible studies and responses that meet defined criteria (see Collection/generation); references for eligible studies are provided.

## Collection/generation
- Source identification: Web of Science search (as of 19/06/2024) using topic strings related to microfibre/microfiber/textile effects; restricted to Article document type.
- Screening process: three-stage filtering (stage 1, stage 2 with forwards/backwards searches, stage 3 for thorough eligibility assessment).
- Eligibility criteria:
  - Aquatic organisms used.
  - Controlled microfibre exposure defined as single polymer type (>1 µm and <5 mm) with no mixtures.
  - Mean measures with errors available for both exposure and control.
  - Data extractable from manuscript (MS) and/or supplementary information (SI).
- Data extraction: responses collected for key traits (Development, Fecundity, Feeding, Growth, Hatching, Health, Survival); only final timepoint or life-stage data used; positive responses prioritized (negative responses converted to positive when appropriate).
- Exposures: across various conditions, including starved/fed, but excluding co-contaminants.
- Data sources: values extracted from manuscript text, figures (via plot digitiser), and SI where needed.
- End result: a comprehensive collection of eligible responses with associated metadata.

## Quality control
- Screening stage 1: title/abstract relevance to biological responses to microfibre exposure.
- Screening stage 2: screening of papers citing or cited by Stage 1 results for relevance.
- Screening stage 3: full eligibility screening; duplicates removed; inclusion based on predefined criteria.
- Outcome: ensures that only suitable, well-documented data are included in the dataset.

## Data structure and units
- Core dataset: 'AquaticMicrofibreExposurestudies2015-2024'
- Key fields (examples):
  - ID, Study.no, Reference, Authors, Title, Year
  - FA.country (country of first author’s affiliation)
  - Species, Source (where exposed species sourced)
  - Environment (Freshwater, Marine, Estuarine, etc.)
  - Assigned Taxonomic.grouping
  - Days.exposed, Days.cat
  - Microfibre category (MF.category): Petroleum-based vs other polymers
  - Length.mm, Length.cat, Width.mm
  - Study.exposure, Study.exposure.units, Standard.exposure, S.cat, Standard.units
  - Time.series, Additional.variable
  - Response, Converted.measure, Response.units
  - C.N, C.mean, C.SD (control)
  - E.N, E.mean, E.SD (experimental)
  - Data.source (MS or SI)
- Traits covered (classified responses):
  - Development, Fecundity, Feeding, Growth, Hatching, Health, Survival
- Purpose of units and conversions:
  - Exposures standardised to enable cross-study comparisons; some values converted to maintain consistent positive-response orientation.
  - Final timepoint/lifestage data used for multi-timepoint studies.

## Study references
- The dataset includes a broad set of studies (examples):
  - Au, S.Y., Bruce, T.F., Bridges, W.C., Klaine, S.J. (2015)
  - Blarer, P., Burkhardt-Holm, P. (2016)
  - Bour, A., Leoni, D., Sundh, H., Carney Almroth, B. (2022)
  - Bunge, A. et al. (2022)
  - Cheng, H. et al. (2021)
  - Cheng, S. et al. (2024)
  - Choi, J.S. et al. (2021, 2022)
  - Cole, M. et al. (2020)
  - Coppock, R.L. et al. (2019)
  - Cui, R. et al. (2022)
  - DiBona, E. et al. (2021, 2022)
  - Hu, L. et al. (2020)
  - Jabeen, K. et al. (2018)
  - Jemec, A. et al. (2016)
  - Jiang, Y. et al. (2023)
- A full list of study references is provided within the dataset.