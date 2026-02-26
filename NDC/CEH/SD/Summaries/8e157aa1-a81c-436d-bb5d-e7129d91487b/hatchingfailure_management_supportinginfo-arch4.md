# Supporting documentation for the dataset ' Avian hatching failure and management interventions in published studies of wild and captive populations '

## Overview
- A dataset documenting hatching failure rates, threat status, and management interventions for 244 bird species across 233 published studies.
- Purpose: support a meta-analysis of mean hatching failure under different management levels.
- Data are free to reuse with acknowledgement; best practice to cite the associated original analysis (Marshall AF et al. 2023).

## Data scope and coverage
- Includes wild and captive birds; excludes domesticated species bred for commercial purposes (e.g., poultry, gamebirds).
- Focus is on reported hatching failure/success and related variables; geographic coordinates are captured when available.

## Data sources and collection process
- Three main sources:
  - Web of Science Core Collection search (Feb 16, 2020) with hatching-related terms (excluding poultry/fish).
  - Datasets from prior comparative analyses and their data sources.
  - Publications found via Google Dataset Search and Google Scholar alerts (Feb 2019–Sept 2020).
- Records pooled, deduplicated, and screened for eligibility; pre-2004 studies excluded if not already captured by prior analyses.

## Inclusion criteria
- Peer-reviewed journals or theses/dissertations online; not predatory sources.
- Accessible via publisher or institutional libraries.
- Species non-domesticated; no in-ovo injections or eggshell manipulations (unless in control groups where appropriate).
- Clear definition of hatching failure as eggs not hatching relative to eggs present at incubation end, excluding predation/desertion/etc.
- Sufficient information to calculate hatching failure/success.
- Minimum total sample size of 10 eggs.

## Data extraction and harmonization
- Extracted qualitative and quantitative data from text, tables, figures, and supplementary materials; WebPlotDigitizer used for data in figures.
- Where data were incomplete, attempted to source original data; if unavailable, recorded as NA.
- When multiple populations or species appeared in one study, data were separated into independent population records.
- Absolute sample sizes estimated when not directly reported (with caveats about classifying abandoned/deserted eggs or nests with only successful nests).

## Geographic and threat data
- GPS coordinates converted to decimal degrees using Google Maps; when only site location was given, centroids were used where possible.
- Threat statuses captured in two ways:
  - Current global IUCN Red List classification (preferred when available).
  - Regional/national threat classifications when global data were unavailable.
- Taxa treated as species recognized by BirdLife International and listed on IUCN; subspecies’ status used from regional lists where applicable.

## Population types and management classifications
- Population type:
  - Captive: adults in captivity; eggs hatched/reared in captivity with possible additional interventions.
  - Wild: adults in the wild with no management interventions (except monitoring).
  - Wild managed: wild populations with management interventions (e.g., predator control, nestboxes, supplemental feeding, egg manipulations).
- Management interventions:
  - Many records lacked explicit details; authors made explicit or implicit assumptions:
    - Captive populations assumed to be supplementary fed unless stated otherwise.
    - Non-captive populations assumed no management unless stated.
    - If part of a population received an intervention but results could not be separated, the intervention was attributed to the whole population.

## Hatching failure measurement and terminology
- Primary metric: proportion of hatching failure across the population (eggs not hatched divided by eggs present at incubation end, excluding certain losses).
- Definitions and terminology were harmonized:
  - 51 distinct definitions of hatching success and 12 definitions of hatchability identified across sources; definitions were standardized for consistency.

## Data structure and variables
- Dataset includes multiple fields per record, such as:
  - Publication year, study name, title, journal, and notes.
  - Geographic coordinates (latitude/longitude) and location details.
  - Population classification (Wild, Wild managed, Captive).
  - Incubation type, nestbox/burrow availability, and supplementary feeding.
  - Clutch size data from various sources (Birds of the World, New Zealand Birds Online, etc.).
  - Sample sizes (eggs present, eggs hatched/unhatched) and derived fields (total eggs, cases, proportions).
  - Definitions used for hatching success/failure and any related calculations or estimations.
  - flags for whether the source used hatching success/failure or hatchability terms.

## Quality control
- Data extraction conducted by one author; approximately 10% of records checked by another author.
- Potential outliers identified and checked for errors.

## Limitations and considerations for data leadership
- Variable reporting detail led to incomplete or inferred classifications (e.g., population type, management interventions).
- Possible biases from data availability, inconsistent definitions across studies, and misclassification risks.
- Estimation steps (e.g., estimating sample size) introduce uncertainty; nest-specific reporting biases (e.g., only successful nests) may affect calculations.

## Reuse guidance and attribution
- Data are free to reuse with acknowledgment of the data resource and DOI.
- For analyses of the meta-analysis results, cite Marshall AF et al. 2023 (Systematic review of avian hatching failure and implications for conservation, Biological Reviews).