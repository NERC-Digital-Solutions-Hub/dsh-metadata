# Moth trends for Britain & Ireland from the Rothamsted Insect Survey light-trap network (1968 to 2016)

- An environmental monitoring study delivering long-term trend data for moth abundances across Britain & Ireland.
- Provides trends for 432 moth species (mostly macro-moths) using data from the Rothamsted Insect Survey (RIS) light-trap network from 1968 to 2016.
- Trends are presented as Annual Growth Rates (AGR) based on a Generalized Abundance Index (GAI) model, plus total percentage change over the time series. Both 95% and 90% confidence intervals are provided.
- Two trend datasets are supplied:
  - BI: Britain & Ireland analysis using 1968–2016 data (541 traps, ~4.7 million counts across 766 species).
  - GB: Great Britain-only analysis using 1970–2016 data.
- Reliability: The GAI method yields robust results for 432 species (430 for GB) after expert vetting of data quality and model outputs.

- Rothamsted Insect Survey light-trap network
  - The RIS light-trap network is a long-running, standardized monitoring system for moths, using 200 W tungsten light traps operated year-round.
  - Traps sample locally (highly local area sampling; typical attraction radii well under 30 m; possibly 60–100 m for this light source) and require proximity to power/maintenance sites.
  - Historically operated at >600 locations; ~100 traps active per year; currently around 80 active traps across Britain & Ireland.
  - Data volume and scope: over 14 million individual moths identified from >1,500 species; this dataset underpins numerous ecological and climate-related studies.

- Data used and species coverage
  - 4,687,310 abundance counts across 766 species (1968–2016 for BI; GB subset typically 1970–2016) from all Britain & Ireland traps (541 sites; average ~95 traps/year).
  - Most analyses at the species level; a few groups are aggregated due to identification or taxonomic issues (Table 1 in the study documents these aggregates).
  - A small number of species have restricted time periods due to data or taxonomic issues (e.g., Eupithecia pug/related species).

- Analytical method (GAI approach)
  - Step 1: Use a Generalized Additive Model to estimate annual flight curves for each species and standardize so the area under the curve equals 1.
  - Step 2: Use standardized curves to correct for within-year recording gaps, producing site-specific abundance indices.
  - Temporal trend estimation: Poisson regression with site (categorical) and year (continuous) to obtain the year coefficient (trend). Derived metrics include:
    - AGR: exp(year coefficient) − 1; describes average annual change.
    - Total percentage change: calculated from AGR over the number of years studied.
  - Confidence intervals: bootstrapping (1,000 replicates) to provide 95% and 90% intervals for both indices and trends.

- Dataset structure and contents
  - Delivered as CSV with two result sets (BI and GB). Columns are prefixed with BI_ or GB_ to distinguish Britain & Ireland and GB analyses.
  - Key fields include:
    - SPECIES_ID, SPECIES_NAME, COMMON_NAME, FAMILY
    - BI_N_YEARS, BI_FIRST_YEAR, BI_LAST_YEAR, BI_YR_COEF, BI_YR_COEF_LOW, BI_YR_COEF_UPP, BI_YR_COEF_90LOW, BI_YR_COEF_90UPP
    - BI_AGR, BI_AGR_LOW, BI_AGR_UPP, BI_AGR_90LOW, BI_AGR_90UPP
    - BI_PERC_CNG, BI_PERC_CNG_LOW, BI_PERC_CNG_UPP, BI_PERC_CNG_90LOW, BI_PERC_CNG_90UPP
    - GB_N_YEARS, GB_FIRST_YEAR, GB_LAST_YEAR, GB_YR_COEF, GB_YR_COEF_LOW, GB_YR_COEF_UPP, GB_YR_COEF_90LOW, GB_YR_COEF_90UPP
    - GB_AGR, GB_AGR_LOW, GB_AGR_UPP, GB_AGR_90LOW, GB_AGR_90UPP
    - GB_PERC_CNG, GB_PERC_CNG_LOW, GB_PERC_CNG_UPP, GB_PERC_CNG_90LOW, GB_PERC_CNG_90UPP
  - A supplementary lookup file (moth_names_codes_lookup.csv) links SPECIES_ID to BRC, UKSI, ABH and BF taxonomic identifiers and names to facilitate cross-referencing with external databases.

- Supplementary resources and acknowledgments
  - Supplementary names and taxonomic codes help align dataset taxa with external nomenclatures (BRC, UKSI, Agassiz et al. 2013, Bradley & Fletcher IDs).
  - Research funded by NERC and BBSRC; RIS is a national capability supported by core grants.
  - The work builds on methodological developments (GAI, bootstrapping) and connects to a wide range of related ecological and climate-change literature.

- Practical implications for environmental analysts
  - Provides a standardized, long-term, cross-species indicator suite for monitoring environmental health and policy performance.
  - Enables assessment of climate and habitat change signals in lepidopteran communities over multi-decadal timescales.
  - Data are ready for integration with other environmental datasets and for informing biodiversity status, conservation priorities, and agricultural policy assessments.
  - The dual BI and GB datasets support both broad regional analyses and GB-specific insights, with explicit timeframes and quality considerations noted for each species. 
  - Key considerations: data reliability varies by species; some taxa require aggregates; time periods differ for a small number of species due to identification and data issues; access to underlying site-level indices and detailed metadata supports deeper auditing and reuse.