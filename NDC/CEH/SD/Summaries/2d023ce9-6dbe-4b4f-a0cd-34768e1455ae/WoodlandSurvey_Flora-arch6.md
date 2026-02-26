# Woodlands Survey flora data 1971-2001

## Overview
- A long-term flora dataset from 103 broadleaved woodlands in Britain, with detailed plot-level data collected in 1971 and re-surveyed in 2000, 2002, and 2003 using identical field methods.
- Aims to analyze ecological change over time and identify principal drivers (e.g., atmospheric deposition of S and N, climate, canopy changes, woodland management).
- Data and methods are designed to support analyses of long-term woodland vegetation change and to facilitate cross-site comparisons and driver identification.

## Survey design and methods
- Stratified sampling across the study area.
- Field methods follow Bunce & Shaw (1973) standardized survey methods; field handbook provided.
- 103 sites with 16 plots per site (2x2 m nested plots), with ecological information collected at canopy and ground flora levels, plus soil pH, soil organic matter, habitat management, and other descriptors.
- Re-surveys conducted in 2000, 2002, and 2003 using the same procedures; the 2000–2003 data are referred to as the 2001 survey in some contexts.
- Foundational publications for methods and analyses:
  - Kirby et al. (2005) Measuring Long Term Ecological Change in British woodlands (1971-2001)
  - Corney et al. (2004) and related works on spatial factors and drivers

## Data structure and fields
- Site: numeric code (1–103); Plot: numeric (1–16); BRC_number: numeric species code (per Biological Record Centre list); BRC_names: text (scientific species name).
- Amalgams: numeric grouping field; Amalgam_names: text (names of grouped taxa where species are hard to separate or inconsistently recorded, e.g., Viola riviniana/reichenbachiana).
- NEST: numeric; COV: numeric (percentage cover for whole plot; 0.5 = <1% cover; -1 indicates bare ground/litter/wood/rock/total bryophyte/water); Null values for woody species (recorded as counts/DBH).
- Yr fields: YR (survey year: 1971, 2000, 2002, 2003) and Yr_2 (code: 1971 or 2000/2002/2003).
- Bryo/Woody: text flags indicating bryophyte or woody life forms.
- Field_sheet: text reference to the original data sheet (e.g., Ground flora plot data).
- Data amalgamation note: in the 2000s, bare ground/litter/water/rock/mud were merged into a single category due to recording inconsistencies; multiple records may exist for the same code within a plot.

## Temporal coverage
- Baseline data: 1971 (103 sites, 16 plots per site).
- Re-surveys: 2000, 2002, 2003 (collectively referred to as 2001 in some analyses).
- Year and year-code fields enable longitudinal analyses across multiple survey waves.

## Data quality, harmonization, and caveats
- Inconsistent recording across time led to the creation of amalgamated taxa groups to improve comparability.
- Some fields (e.g., NEST, density/cover metrics) may have inconsistencies in historical entries; the dataset includes notes on how these were captured and interpreted.
- The amalgamations and coding conventions (e.g., 0.5 = <1% cover; -1 for certain presence/absence categories) must be considered when combining with other datasets or performing quantitative analyses.

## Access, linkage, and usage notes
- Field methods and supporting documentation (field handbook) accompany the dataset to enable proper interpretation and reuse.
- Related datasets and context provided in key publications:
  - Countryside Survey (related datasets)
  - Steele (1968) National Survey of Woodlands
  - Corney et al. (2004) on spatial drivers
  - Kirby et al. (2005) measuring long-term ecological change (core analysis)
- Ideal for:
  - Assessing long-term ecological change in British woodlands
  - Modeling drivers of change by linking vegetation data with external datasets (deposition, climate, canopy structure, management)
  - Creating dashboards or self-serve analytics to compare sites, plots, or taxa over time

## References
- Avery, B. W. (1973). Soil Classification in the Soil Survey of England and Wales. Journal of Soil Science.
- Corney, P.M., et al. (2004). The effect of landscapescale environmental drivers on the vegetation composition of British woodlands. Biological Conservation.
- Haines-Young, R.H., et al. (2003). Changing landscapes, habitats and vegetation diversity across Great Britain. Journal of Environmental Management.
- Kirby, K.J., et al. (2005). Measuring Long Term Ecological Change in British woodlands (1971-2001): A re-survey and analysis of change based on the 103 sites in the Bunce 1971 woodland survey. English Nature Research Reports.