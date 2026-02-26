# Woodlands Survey tree diameter data 1971-2001

- Purpose and scope
  - Longitudinal dataset of broadleaved woodlands across Britain, with site-level ecological information and detailed plot-level data from 16 random plots per site (within 103 sites).
  - Data collected on species composition, soil characteristics, habitat management, and a wide range of plot and site descriptors; re-surveyed in 2000, 2002, and 2003 using identical methods.
  - Analyses aimed at identifying ecological change and its principal drivers (e.g., atmospheric deposition of S and N, climate, canopy change, woodland management); related publications provide methodological and analytical context.

- Survey design and methods
  - Stratified sampling across the survey area using Bunce & Shaw (1973) standardized methods; field handbook included.
  - 103 sites with 16 plots per site; data collected at both baseline (1971) and follow-up surveys (2000s) with the same field protocol.
  - Baseline and follow-up datasets used to assemble explanatory variables from survey data and external sources; related to ongoing assessments of spatial factors.

- Data structure and key variables
  - Site: numeric code (1-103); Plot: numeric (1-16).
  - BRC_number / BRC_names: species code and scientific name (Biological Record Centre list).
  - Amalgams / Amalgam_names: coded groupings for inconsistently recorded species (cross-specific taxa).
  - Status: Live or Dead; DBHclass: 5 cm DBH interval bands (codes 1-32 linking to ranges described in the dataset).
  - Count / Final_count: number of individuals per DBH class per plot (saplings/shrubs doubled due to counting schedule).
  - Yr: 1 = 1971, 2 = 2000s (survey year indicator); Woody: 'w' if woody species; Field_sheet: original data sheet reference.
  - DBH Range and DBH Class mappings provide the 5 cm interval framework across the dataset.

- Temporal coverage and related outputs
  - Baseline year: 1971.
  - Follow-up years: 2000s (surveys conducted in 2000, 2002, 2003; referred to as 2001 in some contexts).
  - Analytical outputs documented in Kirby et al. (2005) and Corney et al. (2004), focusing on drivers of change and spatial controls on woodland composition.

- Related datasets and origin
  - Related dataset: Countryside Survey.
  - Originators (1971): Bunce & Shaw; (2001-03): Simon Smart, Helaina Black, Keith Kirby, Phil Corney; CEH Lancaster; English Nature; University of Liverpool.
  - Supporting documentation and references provided for field methods and analytical context.

- Practical notes for data use and integration
  - Data are structured for self-service analysis (e.g., dashboards, pivot-like exploration) and cross-year comparisons.
  - Data quality considerations include possible patchy data, multiple formats across years, and the need to harmonize amalgamated taxa and live/dead status.
  - Users should consult the cited publications (Kirby et al. 2005; Corney et al. 2004) and the supporting documentation for methodological details and context on drivers of ecological change.

- References and provenance
  - Primary publications detailing methodology and findings: Kirby et al. 2005; Corney et al. 2004; supporting literature listed (e.g., Avery 1973; Haines-Young et al. 2003).
  - DOI and bibliographic details provided for access to the full methodological and analytical framework.