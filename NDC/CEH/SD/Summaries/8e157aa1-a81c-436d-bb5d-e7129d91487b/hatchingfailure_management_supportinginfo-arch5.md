# Supporting documentation for the dataset ' Avian hatching failure and management interventions in published studies of wild and captive populations '.

## Overview
- A dataset compiling hatching failure rates, threat status, and management interventions for 244 bird species across 233 published studies.
- Designed to support a meta-analysis on mean hatching failure rates by threat status and management level.
- Data are free to reuse with acknowledgement of the associated DOI; primary citation preferred: Marshall AF et al. 2023.

## Dataset scope and purpose
- Captures rates of hatching failure, threat status, and management interventions.
- Aims to quantify how hatching failure varies with threat status and management intensity across wild and captive populations.

## Collection sources and inclusion criteria
- Sources:
  - Web of Science Core Collection search conducted 16/02/2020.
  - Datasets from previous comparative analyses and their sources.
  - February 2020 Google Dataset Search results and Google Scholar alerts (Jan 2019–Sept 2020).
- Inclusion criteria:
  - Peer-reviewed articles or online theses/dissertations; excludes predatory journals.
  - Accessible via publisher site or institutional libraries.
  - Studies on wild or captive birds (not domesticated poultry/gamebirds or intensively bred for pets).
  - No in-ovo injections or direct egg manipulation unless relevant to controls.
  - Clear definition of hatching failure and sufficient data to calculate rates.
  - Minimum sample size of 10 eggs; data must allow calculation of hatching failure/success.

## Data extraction and provenance
- Data extracted from text, tables, figures, and supplementary materials; when needed, WebPlotDigitizer used to recover figure data.
- For missing details, attempted to trace original data sources; if unavailable, recorded as NA.
- When multiple species/populations reported, separated into individual population records.
- Where mean hatch rates were not directly reported, calculated from available data or estimated from related figures/tables.
- Data quality: extraction performed by A. F. M. with ~10% of records cross-checked by P. B.

## Geographic coordinates and threat status
- Geographic data:
  - GPS coordinates converted to decimal degrees via Google Maps; central point used for multi-site ranges.
  - If location unavailable, marked NA unless species distribution allowed approximate localization (verified with IUCN/BirdLife sources).
- Threat status:
  - Used current IUCN status when available; otherwise regional/national lists.
  - If subspecies lack status, parent species status used.
  - For subspecies later elevated to species, current IUCN category used.
  - Only species recognized by BirdLife International and listed on IUCN Red List included.

## Population type and management interventions
- Population type classifications (per study):
  - Captive: adults in captivity with eggs hatched/reared in captivity.
  - Wild: adults in wild with no management interventions beyond monitoring.
  - Wild managed: wild populations with management interventions (e.g., predator control, nestboxes, supplemental feeding, egg manipulations).
- Challenges:
  - Some records lack explicit management details; misclassification risk acknowledged.
  - Original sources re-checked where possible; some records labeled NA if unverifiable.
- Management interventions:
  - Many studies lack explicit details; assumptions used:
    - Captive populations assumed to be supplementary fed unless stated otherwise.
    - Non-captive populations assumed to have no management interventions unless stated.
    - If any part of a population experienced an intervention and results couldn’t be separated, the intervention assumed for the whole population.

## Hatching failure calculation and data handling
- Primary metric: proportion of hatching failure (eggs present at end of incubation that failed to hatch, excluding losses due to predation, desertion, accidents, weather, or unknown factors).
- Sample size handling:
  - Direct sample size available for 286 of 483 records.
  - When missing, approximate sample size using species-specific clutch metrics from various sources or study-derived values.
- Data caveats:
  - Some nests labeled as abandoned/deserted or cases where only nests with at least one hatch were reported can bias calculations.
  - Mean clutch size used from external sources if not reported, with parent species values used for subspecies lacking data.
- Terminology and standardization:
  - Changeable terminology across studies (hatching success, hatching failure, hatchability, etc.) standardized to consistent definitions.
  - Definitions homogenized; hatching success/failure terms inverted so that analyses consistently reflect hatching success when appropriate.
  - Resulting dataset contains numerous definitions (51 for hatching success, 12 for hatchability) before standardization.

## Data structure and variables
- Table 1 outlines dataset variables and units (e.g., publication year, study name, title, journal, geographic coordinates, population type, incubation type, nestbox/supplementary feeding indicators, sample sizes, hatching failure proportions, and related statistics).
- Multiple effect sizes per source allowed; includes fields for various clutch sizes and calculated egg counts.
- Variables capture data provenance (Original.Source_Publication.Year, Uses.Hatching.Success_Failure, etc.), geography (Latitude/Longitude), and methodological details (Incubation type, Nestboxes.Burrows.Sites, Supplementary.Feeding).

## Quality control and governance
- Single primary extractor with 10% of studies cross-checked for consistency.
- Outliers identified and investigated for potential errors.
- Data structure supports traceability from source to calculated effect sizes, enabling auditability and reproducibility.

## Limitations and caveats
- Potential misclassification of population type due to incomplete reporting.
- Incomplete or ambiguous reporting of management interventions in some studies leads to broad assumptions.
- Data extracted from figures/databases may carry estimation biases (e.g., via digitization or indirect calculations).
- Some records rely on older sources and proxies for clutch size or sample size, introducing variability.

## Usage, attribution, and rights
- Data are free to reuse with acknowledgment of the DOI; best practice to cite the main analysis (Marshall et al. 2023, Biological Reviews) for contextual interpretation.
- Dataset supports meta-analyses on hatching failure across threat categories and management regimes, with robust provenance and standardized definitions to facilitate cross-study synthesis.