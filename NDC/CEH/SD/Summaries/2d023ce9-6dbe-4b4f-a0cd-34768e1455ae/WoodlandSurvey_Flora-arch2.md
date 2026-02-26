# Woodlands Survey flora data 1971-2001

## Overview
- Longitudinal vegetation dataset covering 103 broadleaved woodlands across Britain.
- Baseline data collected in 1971; re-surveyed in 2000, 2002, and 2003 (referred to as 2001) using identical methods.
- Field data include canopy and ground flora species, soil pH, soil organic matter, habitat management, and a range of plot- and site-level descriptors.
- Analyses aim to identify ecological changes over time and to estimate drivers of change (e.g., atmospheric deposition of S and N, climate, canopy changes, woodland management).
- Foundational publications document methods and drivers; dataset users should consult Kirby et al. (2005) and Corney et al. (2004) for results and interpretation.

## Data Coverage
- 103 sites stratified across Britain; 16 randomly placed 200 m² plots per site.
- Year coverage: 1971 (baseline) and 2000/2002/2003 (re-survey).
- Data collected at site level and plot level with standardized field methods.

## Field Methods and Sampling Design
- Stratified sampling across the survey area.
- Fieldwork conducted according to Bunce & Shaw's 1973 standardized survey methods.
- A field handbook was provided as supporting documentation.
- Data originally collected on multiple categories (ground flora, bryophytes, lichens, woody plants) and later consolidated for consistency.

## Data Structure and Key Variables
- Site: numeric code (1–103).
- Plot: numeric (1–16).
- BRC_number: numeric code for species (Biological Records Centre list).
- BRC_names: species names (scientific).
- Amalgams: numeric codes grouping certain species due to past recording inconsistencies (e.g., Viola riviniana/reichenbachiana).
- Amalgam_names: names for amalgam groups.
- NEST: numeric; inner 2x2 m plot nest estimate (not always consistently filled).
- COV: numeric; percentage cover for the whole plot; special codes for zeros or presence of bare ground.
- YR: survey year (1971, 2000, 2002, 2003).
- Yr_2: year code (1971 or 2000/2002/2003).
- Bryo/Woody: flags indicating bryophyte/lichen or woody species data.
- Field_sheet: field sheet where original data were recorded (e.g., Ground flora plot data).

## Temporal Dimension and Re-survey Details
- 1971 baseline with repeat visits in 2000, 2002, and 2003 (referred to as 2001 in some summaries).
- Aims to analyze long-term ecological change and link changes to explanatory variables gathered from survey data and external sources.

## Related Datasets and References
- Related dataset: Countryside Survey.
- Foundational references include:
  - Corney et al. (2004): landscape-scale drivers and vegetation composition.
  - Kirby et al. (2005): measuring long-term ecological change in British woodlands (1971–2001).
  - Haines-Young et al. (2003): landscape and vegetation diversity trends.
  - Avery (1973) and Steele (1968) as historical methodological/ contextual sources.

## Data Provenance and Access
- Originators (1971): R.G.H. Bunce & M.W. Shaw (Nature Conservancy, Merlewood).
- 2001–2003 contributors: Simon Smart, Helaina Black, Keith Kirby, Phil Corney (CEH, English Nature, University of Liverpool).
- Data structure and terminology reflect standardized field methods and later consolidation of records.
- Dataset notes acknowledge recording inconsistencies and amalgamation of categories to maintain comparability.

## Analytical and Monitoring Implications for Analysts
- Provides a standardized, long-term dataset suitable for monitoring environmental health and trends in woodland vegetation.
- Enables assessment of ecological change drivers by linking plant community data with atmospheric, climatic, and management variables.
- Outputs can be generated as maps, charts, and reports to illustrate changes over time and space.
- Data quality considerations include handling amalgamated categories and inconsistent nest/cover recordings; requires careful cleaning and documentation.
- Suitable for integrating with other environmental data sources to enhance value beyond single-use analyses.

## Challenges and Opportunities
- Challenge: augmenting the value of the dataset by combining with other relevant environmental data (avoiding single-use analyses).
- Challenge: enabling access to underlying data for reuse and verification by others.
- Opportunity: use as a baseline for longitudinal comparisons with other woodland surveys (e.g., Countryside Survey) to strengthen monitoring frameworks.