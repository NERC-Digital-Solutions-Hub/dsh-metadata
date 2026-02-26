# Supporting documentation for the dataset ' Avian hatching failure and management interventions in published studies of wild and captive populations '

## Overview
- Presents the dataset capturing rates of hatching failure, threat status, and management interventions for 244 bird species across 233 published studies.
- Originally created to support a meta-analysis on how hatching failure varies between threatened and non-threatened species under different management regimes.
- Data are free to reuse with proper acknowledgement; a preferred citation is provided for the underlying analysis (Marshall et al. 2023).

## Collection and inclusion methods
- Three main sources used to compile records:
  - Web of Science Core Collection search (Feb 16, 2020) with terms related to hatching and excluding poultry/fish.
  - Datasets from prior comparative analyses; verification of original data sources when possible.
  - Additional publications encountered via Google Dataset Search and Google Scholar alerts (Jan 2019–Sept 2020).
- Screening and eligibility criteria:
  - Peer-reviewed articles or online theses/dissertations; excludes predatory publications.
  - Accessible via publisher or institutional libraries.
  - Wild or captive birds, not domesticated or intensively bred for commercial purposes.
  - No in-ovo injections or manipulation of eggshell components (except where control data are appropriate).
  - Hatching failure defined as the proportion of eggs present at incubation end that failed to hatch, excluding certain losses (predation, desertion, etc.) and requiring sufficient information to calculate rates.
  - Minimum sample size of 10 eggs.
- Data extraction approach:
  - Qualitative and quantitative extraction from text, figures, tables, and supplements; WebPlotDigitizer used for extracting data from figures when needed.
  - Where sources were incomplete or inaccessible, data were marked as NA.
  - When multiple populations were reported, records were split accordingly.
  - Calculations provided or derived when direct numbers were not reported (noting potential biases in certain study reporting practices).

## Geographic, taxonomic, and threat-status details
- Geographic coordinates:
  - Study locations converted to Decimal Degrees using Google Maps when possible; NA if coordinates unavailable.
  - For broad ranges, central points or species distribution references (IUCN Birds of the World) used to approximate.
- Threat status classifications:
  - Current global IUCN status used when available; local/regional statuses used if global not available.
  - Subspecies handled with regional lists; if subspecies status unavailable, the parent species’ status used.
  - Only BirdLife International data and IUCN Red List categories used for consistency.
- Population type classifications:
  - Captive: adults in captivity; eggs hatched/reared in captivity; includes additional interventions.
  - Wild: adults in the wild with no management interventions apart from monitoring.
  - Wild managed: wild adults with management interventions (e.g., predator control, nestboxes, supplementary feeding, egg manipulation).
  - Inconsistent reporting in some sources led to NA or assumed classifications in some cases; explicit notes document how classifications were inferred for legacy analyses.

## Management interventions and data assumptions
- Many studies lacked detailed reporting on specific interventions; several assumptions applied:
  - Captive populations assumed to be supplementary fed unless stated otherwise; no artificial nests unless reported.
  - Non-captive populations assumed to have no management interventions unless mentioned.
  - If any part of a population experienced an intervention and results couldn’t be separated, the intervention was assumed to apply to the whole population.

## Hatching failure data and definitions
- Primary metric: proportion of hatching failure across the population (eggs present at incubation end that failed to hatch, excluding specified losses).
- Data extraction outcomes:
  - 286 records had direct sample sizes extracted.
  - 125 records had sample sizes estimated from clutch data and mean clutch size.
  - Use of clutch size sources when study-provided data were missing (Birds of the World, NZ Birds Online, or Cooney et al. 2020) to estimate eggs.
- Definitions and terminology:
  - Recorded terminology for hatching-related outcomes (hatching success/failure, hatchability, etc.) was standardized.
  - After standardization, 51 distinct definitions of hatching success and 12 of hatchability remained across the dataset.

## Data structure and variables
- Table 1 (detailed in the original document) describes all dataset variables and units, including:
  - Publication details (year, title, journal), study identifiers, and data provenance.
  - Location data (latitude/longitude).
  - Biological and management metadata (population type, incubation type, nestboxes, supplementary feeding).
  - Sample sizes, eggs counted, hatching outcomes, and derived proportions.
  - Clutch size sources and various related statistics (e.g., mean clutch size, total eggs, nest/clutch counts).
  - Definitions and calculations used to derive hatching failure/success, and notes on data sources.
- Standardization fields:
  - Uses standardized definitions for hatching success/failure to enable cross-study comparisons.
  - Includes standardised definitions for hatchability and other related terms.

## Data quality control and limitations
- Quality control:
  - Data collection conducted by a single primary extractor with approximately 10% of records checked by a second reviewer.
  - Potential outliers identified and checked for errors.
- Limitations and caveats:
  - Potential misclassification of population type for legacy sources where original details were unclear.
  - Some studies may have categorized undamaged but unfertilized eggs as non-failed or abandoned, affecting hatch failure estimates.
  - Some nests/selections were excluded due to reporting practices (e.g., nests only reporting successful nests).
  - Geographical and taxonomic biases likely due to data availability and historical focus.
  - Variability in reporting terminology and measurement approaches across studies necessitated extensive standardization and careful interpretation.

## Relevance for monitoring frameworks
- Demonstrates the value of harmonizing definitions and metadata when aggregating environmental health indicators across multiple studies.
- Highlights governance considerations:
  - Need for transparent data provenance, accessibility, and clear sharing policies to facilitate reuse.
  - Importance of data quality assurance, metadata completeness, and documentation of transformations and estimations.
- Key methodological takeaways for monitoring authors:
  - Establish clear inclusion criteria and standardized outcome definitions before data collection.
  - Implement robust data extraction protocols, including methods to handle missing data and estimations.
  - Document population classifications and management interventions with explicit criteria to minimize misclassification.
  - Provide comprehensive data structure documentation (codings, variable definitions, units, and derivations) to enable reuse in policy evaluations.

## Citations and data usage
- Data are free to reuse with acknowledgement of the DOI; the preferred acknowledgment includes citing the data resource DOI and the original meta-analysis (Marshall AF et al. 2023, Biological Reviews).
- Complete reference list of contributing studies is provided, illustrating the breadth of sources synthesized in the dataset.