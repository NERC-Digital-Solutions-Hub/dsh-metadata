# Supporting documentation for the dataset ' Avian hatching failure and management interventions in published studies of wild and captive populations '

## Purpose and scope
- Describes the dataset on hatching failure, threat status, and management interventions for 244 bird species across 233 published studies.
- Dataset supports meta-analysis on mean hatching failure across threatened vs. non-threatened birds under different management.
- Data are free to reuse with acknowledgement; citation of the original analysis (Marshall et al. 2023) is appreciated.

## Data sources and collection strategy
- Three main sources:
  - Web of Science Core Collection search (16/02/2020) with English-language results excluding domesticated species.
  - Datasets from previous comparative analyses (list of specific studies as verification sources).
  - Additional publications encountered via Google Dataset Search and Google Scholar alerts (Jan 2019–Sep 2020).
- Records pooled, deduplicated, and screened for eligibility; pre-2004 studies not identified in prior analyses were excluded.

## Inclusion criteria
- Publication type: peer-reviewed journals or online theses/dissertations; excludes predatory sources.
- Accessibility: retrievable through publisher sites or institutional libraries.
- Study subjects: wild or captive birds, not domesticated poultry or intensively bred for pets.
- Methodology: no in-ovo injections or eggshell manipulations unless appropriate controls; excluded if core data rely on such interventions.
- Hatching failure definition: proportion of eggs not hatching relative to eggs present at end incubation, excluding predation, desertion, accidents, extreme weather, or unknowns.
- Data sufficiency: enough information to calculate hatching failure/success from text or supplements.
- Sample size: total eggs present or calculable; minimum n = 10.

## Data extraction and processing
- Extracted qualitative and quantitative data from text, figures, tables, or Supplements; used WebPlotDigitizer for data in figures when needed.
- When data were not directly available, consulted cited sources; recording of missing data as NA where unavailable.
- For multiple species/populations within a study, data were separated into individual population records.
- When mean sample sizes were missing, estimated using available clutch data or external sources (with ties to standard references when necessary).
- Notes potential biases due to misclassification of nest status (e.g., abandoned nests) or partial data reporting.

## Geographic information and threat classifications
- Geographic coordinates converted to Decimal Degrees via Google Maps; central points used for range data when needed.
- Threat status from IUCN: current global status preferred; regional statuses used when global not available; subspecies statuses mapped to parent species when appropriate.
- Only species recognized by BirdLife International and listed on IUCN Red List included; if subspecies lacked status, parent species status used.

## Population type and management interventions
- Population type classifications:
  - Captive: adults in captivity; eggs hatched/reared in captivity with potential interventions.
  - Wild: adults in the wild; no management interventions beyond monitoring.
  - Wild managed: wild populations with management (e.g., predator control, nestboxes, supplementary feeding, egg manipulations).
- Management interventions:
  - Many studies lacked explicit details; assumptions applied:
    - Captive populations assumed supplementary fed and not given artificial nests unless stated.
    - Non-captive populations assumed no management unless stated.
    - If any portion had an intervention but effects could not be separated, the intervention was presumed to apply to the whole population.

## Hatching failure proportion extraction and calculation
- Primary outcome: proportion of hatching failure across the population (end-incubation eggs that failed to hatch).
- 483 records analyzed; 59.2% contained directly reported sample sizes.
- When sample size was missing, estimated from nest/clutch data and mean clutch size; various external sources used to fill clutch size where needed.
- Caveats noted: variation in nest classification (e.g., eggs deemed abandoned/deserted) and reporting often limited to nests with at least one hatch; these practices can bias estimates.

## Terminology harmonization and definitions
- Identified multiple terminology usages:
  - 51 definitions of hatching success and 12 definitions of hatchability after homogenization.
- Definitions homogenized to consistent phrasing; hatching failure definitions inverted to align with hatching success usage for uniformity.

## Data structure and variables
- Table 1 provides detailed variable descriptions and units (not reproduced here).
- Key data fields include:
  - Publication and study identifiers, titles, journals, and sources.
  - Geographic coordinates (Latitude/Longitude), population type, incubation type, nestbox or supplementary feeding status.
  - Reported and calculated hatching failure/success metrics, sample sizes, and associated statistics (standard error, standard deviation).
  - Clutch size data from various sources (Birds of the World, New Zealand Birds Online), and computed totals for eggs and cases.
  - Coding for data provenance and usage of hatching terminology.

## Quality control and reproducibility
- Data collection conducted by A. F. Marshall; approximately 10% of records independently checked by P. Brekke.
- Outliers were identified and reviewed to ensure data integrity.

## Usage rights and citations
- Dataset is free to reuse with proper acknowledgment of the data resource DOI.
- The open-access publication Marshall et al. (2023) provides the main methodological basis and should be cited for analysis context.

## Limitations and caveats
- Potential misclassification of wild vs. wild-managed populations due to incomplete source verification.
- Some management interventions remain under-reported or undefined, leading to possible exclusions.
- Reliance on secondary sources and approximations for some clutch sizes may introduce estimation bias.
- Data are subject to limitations of the original studies, including variable definitions of hatching success/failure.

## References (selected)
- Marshall AF, Balloux F, Hemmings N, Brekke P. 2023. Systematic review of avian hatching failure and implications for conservation. Biological Reviews.
- Briskie & Mackintosh (2004); Morrow et al. (2002); Reding (2015); Spottiswoode & Møller (2004); Soler et al. (2012); etc. (full cited references available in the dataset documentation).