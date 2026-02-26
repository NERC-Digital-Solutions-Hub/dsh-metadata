# Supporting documentation for the dataset ' Avian hatching failure and management interventions in published studies of wild and captive populations '

## Overview
- A compiled dataset covering 244 bird species across 233 published studies.
- Focuses on hatching failure rates, threat status, and management interventions.
- Intended for meta-analytic assessment of how hatching failure differs between threatened and non-threatened species under different management levels.
- Free to reuse with acknowledgment; primary citation: Marshall AF et al. 2023, Biological Reviews.

## Data content and purpose
- Primary aim: analyze mean hatching failure rates for threatened vs non-threatened birds under varying management regimes.
- Data sources and scope mirror the Marshall et al. 2023 open-access publication and its supplementary materials.

## Collection and inclusion methods
- Studies gathered from:
  - Web of Science Core Collection search (Feb 16, 2020): English-language results excluding poultry/fish-related topics.
  - Datasets from prior comparative analyses; verification of eligibility and extraction of additional information.
  - Additional publications found via Google Dataset Search and Google Scholar alerts (Feb 2019–Sept 2020).
- Inclusion criteria:
  - Peer-reviewed articles or online theses/dissertations; excluding predatory journals.
  - Accessible via publisher/institutional libraries.
  - Wild or captive birds; not domesticated poultry/gamebirds or intensively bred for pets.
  - No in-ovo injections or eggshell/egg component manipulation; control data allowed if applicable.
  - Clear definition of hatching failure with sufficient information to compute rates (per end-of-incubation eggs).
  - Minimum sample size of 10 eggs.
- Records screened to remove duplicates; pre-2004 studies included only if captured by prior analyses.

## Data extraction and processing
- Data extracted from text, figures, tables, and supplementary materials.
- When data appeared only in figures, WebPlotDigitizer used to extract values.
- If original sources unavailable or unclear, mark as NA.
- Data for multiple species/populations separated into individual records.
- When mean hatching rates were not directly reported, estimated from available data (e.g., number of hatched/unhatched and clutch sizes).
- Cautions noted regarding possible misclassifications due to nest abandonment, partial nest data, or inconsistencies in reporting.

## Geographic breakdown and location data
- Study site GPS coordinates converted to Decimal Degrees using Google Maps.
- If only a site location was provided, coordinates derived accordingly; NA assigned when unavailable.
- In limited-distribution cases, species range data from IUCN Red List and Birds of the World used to approximate location.

## Threat status classifications
- Threat status recorded at both current IUCN Red List and the status at the time of the study; global status preferred when available.
- Regional/national lists used when global status unavailable.
- For subspecies, regional statuses used; if subspecies later treated as full species, current IUCN status applied.
- Only species recognized by BirdLife International and listed on IUCN Red List used.

## Population type and management classifications
- Population type (captive, wild, wild managed) determined by the overall management of adults and eggs.
  - Captive: adults in captivity with eggs hatched/reared in captivity; may include artificial insemination/incubation.
  - Wild: adults in the wild with no management interventions (aside from monitoring).
  - Wild managed: wild adults with management interventions (e.g., predator control, nestboxes, supplemental feeding, egg manipulations).
- Classifications for some historical sources were NA if verification was not possible; several sources were re-classified based on context or standard definitions.
- Management interventions: many studies lacked detailed reporting; where possible, interventions like nestboxes or supplementary feeding were recorded. Assumptions used:
  - Captive populations: assumed supplementary fed unless stated otherwise; not given artificial nests unless specified.
  - Non-captive populations: assumed no management unless stated.
  - If any part of a population received an intervention but data could not be separated by subpopulation, the intervention was attributed to the whole population.

## Hatching failure proportion extraction and calculation
- Primary metric: proportion of hatching failure across the population (eggs present at incubation end that failed to hatch, excluding predation, desertion, accidents, extreme weather, or unknown factors).
- Sample size handling:
  - 286 of 483 records (59.2%) had directly available sample sizes.
  - 125 records (25.9%) had sample size estimated as (number of successful nests) × (mean clutch size).
  - 60 records used mean clutch size from external sources; 10 records used NZBO; 2 records used Birds of the World.
- Subspecies without clutch size data used parent species data when necessary.
- Potential biases acknowledged regarding nest abandonment classification and nests with only successful nests reported.

## Hatching terminology and standardization
- Documented usage of terms: hatching success, hatching failure, hatchability, and other variants.
- Definitions homogenized to align on a consistent concept of hatching success; alternate terms recoded accordingly.
- Result: 51 distinct definitions of hatching success and 12 definitions of hatchability across the dataset.

## Nature and units of recorded values
- Details and units described in Table 1 of the data documentation (not reproduced here).
- Variables cover publication data, study identifiers, taxonomic and geographic information, incubation type, nest/egg interventions, clutch counts, egg counts, success/failure cases, proportions, and definition metadata.

## Data structure, quality control, and documentation
- Data structure includes extensive variables such as publication year, study name, title, journal, data source notes, location coordinates, population type, incubation, nest provisions, feeding, clutch size sources, sample sizes, and calculated proportions.
- Quality control: data collection conducted by a single extractor (A.F.M.) with ~10% of records cross-checked by another author (P.B.); outliers examined.
- Data were adapted from the Marshall et al. (2023) open-access framework and supplemented with original data extraction procedures.

## Access, usage, and references
- Data are free to reuse with acknowledgment; primary citation recommended for analyses of the dataset (Marshall AF et al. 2023; Biol Rev).
- References listed include foundational studies on hatching failure, hatchability, and related ecological and evolutionary factors, as well as methods (e.g., WebPlotDigitizer) used for data extraction.

## Practical implications for analysts
- Enables cross-study analyses of hatching failure relative to threat status and management interventions across wild and captive populations.
- Allows stratification by population type (captive, wild, wild managed), incubation context, and presence/absence of nestboxes or supplementary feeding.
- Useful for meta-analytic modeling of predictors of hatching failure and for assessing conservation implications across species and regions.
- Requires consideration of dataset limitations (variable reporting, potential misclassification, imputed sample sizes, and diverse definitions of hatching metrics).