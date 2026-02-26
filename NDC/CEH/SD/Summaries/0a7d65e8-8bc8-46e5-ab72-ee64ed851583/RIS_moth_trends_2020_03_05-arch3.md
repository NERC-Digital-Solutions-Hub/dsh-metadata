# Moth trends for Britain & Ireland from the Rothamsted Insect Survey light-trap network (1968 to 2016)

## Overview
- Presents abundance trends for 432 moth species (mostly macro-moths) using Rothamsted Insect Survey (RIS) light-trap data from 1968–2016.
- Trends shown as: year coefficients from a Generalized Abundance Index (GAI) model, Annual Growth Rate (AGR), and total percentage change over the time series.
- Provides 95% and 90% confidence intervals for each trend metric.
- Two data sets are released: Britain & Ireland (BI; 1968–2016) and Great Britain (GB; 1970–2016); both use the same method but differ in data scope.

## Rothamsted Insect Survey light-trap network
- RIS operates two long-running trap networks (light-traps for moths; suction-traps for aphids); the light-trap network is ~80 active traps currently, with a long history (>600 locations sampled over time).
- Traps are designed to sample local moth communities; they have an opaque lid and operate from dusk to dawn with a fixed 200W bulb; estimated local attraction radii are 60–100 m.
- Trap sites are distributed across England, Scotland, Wales, Channel Islands (better coverage) with Ireland being more limited.
- Data volume: over 14 million moths across >1,500 species collected historically; the RIS data underpin numerous ecological studies and national trend assessments.

## Data used and time coverage
- Dataset comprises 4,687,310 abundance counts across 766 species (1968–2016; 541 traps on average ~95 traps/year) in BI analysis; most are macro-moths; a small number of well-identified micro-moths included.
- For GB analyses, 430 species are analyzed (out of 766 in BI).
- Some species have non-standard time periods due to taxonomic or data issues (e.g., Eupithecia spp.; several others listed with restricted years).
- Supplementary taxa aggregates were used where needed due to identification issues.

## Analytical method (GAI)
- Uses Generalized Abundance Index (GAI) to handle seasonal patterns and within-year recording gaps.
  - Step 1: Generalized Additive Model to estimate annual flight curves per species, standardized to unit area.
  - Step 2: Use standardized curves to estimate site-specific annual abundance indices.
  - Step 3: Poisson regression with site (categorical) and year (continuous) to derive year coefficients (trend).
- Trend metrics:
  - Year coefficient (from Poisson glm) as a measure of temporal trend.
  - Annual Growth Rate (AGR): exp(year coefficient) − 1 (interpretation: >0 indicates growth, <0 decline).
  - Total percentage change across the study period, computed from AGR.
- Uncertainty
  - Annual and trend confidence intervals via bootstrapping (1,000 replicates); both 95% and 90% intervals reported.
- Reliability
  - GAi-derived trends considered reliable for 432 BI species and 430 GB species after expert review of data quality and index/trend estimates.

## Description of the dataset and fields
- Data file format: comma-separated values (CSV).
- Two linked result sets:
  - BI analyses: data from all sites in Britain & Ireland, 1968–2016.
  - GB analyses: data from GB sites, 1970–2016.
- Key column groups (prefix BI_ for BI analyses; GB_ for GB analyses):
  - SPECIES_ID, SPECIES_NAME, COMMON_NAME, FAMILY
  - BI_N_YEARS, BI_FIRST_YEAR, BI_LAST_YEAR, BI_YR_COEF, BI_YR_COEF_LOW, BI_YR_COEF_UPP, BI_YR_COEF_90LOW, BI_YR_COEF_90UPP
  - BI_AGR, BI_AGR_LOW, BI_AGR_UPP, BI_AGR_90LOW, BI_AGR_90UPP
  - BI_PERC_CNG, BI_PERC_CNG_LOW, BI_PERC_CNG_UPP, BI_PERC_CNG_90LOW, BI_PERC_CNG_90UPP
  - GB_N_YEARS, GB_FIRST_YEAR, GB_LAST_YEAR, GB_YR_COEF, GB_YR_COEF_LOW, GB_YR_COEF_UPP, GB_YR_COEF_90LOW, GB_YR_COEF_90UPP
  - GB_AGR, GB_AGR_LOW, GB_AGR_UPP, GB_AGR_90LOW, GB_AGR_90UPP
  - GB_PERC_CNG, GB_PERC_CNG_LOW, GB_PERC_CNG_UPP, GB_PERC_CNG_90LOW, GB_PERC_CNG_90UPP
- Supplementary names & taxonomic codes file (moth_names_codes_lookup.csv) available to map Taxa to external taxonomic references (BRC, UKSI, Agassiz checklist, Bradley & Fletcher IDs). Columns include SPECIES_ID, BRC_CONCEPT, BRC_SPECIES_NAME, ABH_NUMBER, ABH_NAME, BF_NUMBER.

## Data quality, limitations, and governance
- Data quality considerations:
  - Some species have limited data windows or required taxonomic revisions, affecting the start/end years.
  - Identification inconsistencies necessitated restricting analyses for certain taxa (e.g., many Eupithecia spp.).
  - Within-year gaps and changes in trap turnover over time were addressed via the GAI standardization.
- Limitations related to monitoring design:
  - Light-trap sampling tends to reflect local fauna and is influenced by moth activity, weather, and moon phase; not all species or regions may be equally represented.
  - Trap placement near power sources and human maintenance areas can introduce biases due to proximity to anthropogenic influences.
- Data sharing and metadata:
  - The dataset provides extensive metadata through the BI/GB fields and the supplementary taxonomy lookup; but users should review the methodological notes (GAI approach, bootstrapping) when interpreting trends.
- Data governance:
  - Outputs include clearly defined metrics with uncertainty estimates; data are shared with underlying data gaps noted, and the methodology is described to support reproducibility.

## Access, usage, and applicability for monitoring frameworks
- The dataset offers concrete, policy-relevant trend measures (yearly trend coefficient, AGR, total change) with confidence intervals, suitable for monitoring environmental health indicators over multi-decadal scales.
- Two parallel analyses (BI and GB) enable regional and national comparisons, as well as assessment of data consistency over time.
- The documentation includes sufficient methodological detail to reproduce the analyses or adapt the approach to other seasonal invertebrate time-series datasets.
- Users should consider local sampling designs, potential biases of light-trap methods, and taxonomic limitations when applying these trends to broader biodiversity assessments.

## Acknowledgements and references
- Funded by Natural Environment Research Council (NERC) and BBSRC; RIS National Capability funded by BBSRC; development linked to UK-SCAPE program and related initiatives.
- References cover foundational work on the GAI method, long-term moth trends, climate and biodiversity studies, and the Rothamsted Insect Survey's contributions to ecological research.