# Moth trends for Britain & Ireland from the Rothamsted Insect Survey light-trap network (1968 to 2016)

- Purpose and scope
  - Provides abundance trends for 432 (predominantly macro-moth) species using the Rothamsted Insect Survey light-trap network data from 1968–2016 (and 1970–2016 for the GB subset).
  - Output metrics per species: model year coefficient ( AGR ), and total percentage change over the time series, each with 95% and 90% confidence intervals.
  - Two dataset versions: Britain & Ireland (BI) 1968–2016 and Great Britain only (GB) 1970–2016.

- Data sources and network context
  - Based on the Rothamsted Insect Survey light-trap network: around 80 active traps at any time, with a history of over 600 locations and ~100 traps per year.
  - Traps sample primarily local moth fauna with limited long-range attraction (local scale ~30–100 m depending on trap type), reflecting local population dynamics.
  - The RIS networks (light-trap and suction-trap) are among the longest standardised terrestrial insect time series.

- Data and species coverage
  - Total counts: 4,687,310 abundance counts across 766 species (mostly macro-moths) from Britain & Ireland traps (541 traps, average ~95/year).
  - 14 million individual moths identified across >1,500 species historically; data widely used in diverse ecological and climate-change research.
  - Micro-moths are largely excluded due to identification inconsistencies, with a small set of easily identified micro-moths included (e.g., Nomophila noctuella, Plutella xylostella, Udea ferrugalis).
  - Some species have non-standard time periods due to taxonomic or data issues (detailed in Table 2).

- Analytical method (GAI approach)
  - Generalized Abundance Index (GAI) methodology:
    - Step 1: Generalized Additive Model to estimate annual flight curves for each species and standardize so the area under the curve equals one.
    - Step 2: Correct for within-year recording gaps to produce site-specific annual abundance indices.
    - Step 3: Poisson regression with site (categorical) and year (continuous) to derive year coefficients (trend metrics).
  - Trends derived:
    - Year coefficient (basis for temporal trend)
    - Annual Growth Rate (AGR): exponentiated year coefficient minus 1 to express annual change
    - Total percentage change: derived from AGR over the number of years
  - Confidence intervals via bootstrapping (1,000 replicates) for both indices and trends (95% and 90% levels).
  - Reliability: assessed by expert review of underlying data, annual indices, and confidence intervals; robust for 432 species in BI (430 in GB).

- Dataset structure and fields
  - Delivered as comma-separated values (CSV).
  - Two result sets distinguished by column prefixes:
    - BI_ fields for Britain & Ireland analyses (1968–2016)
    - GB_ fields for Great Britain analyses (1970–2016)
  - Core columns (illustrative):
    - SPECIES_ID, SPECIES_NAME, COMMON_NAME, FAMILY
    - BI_N_YEARS, BI_FIRST_YEAR, BI_LAST_YEAR, BI_YR_COEF, BI_YR_COEF_LOW, BI_YR_COEF_UPP, BI_YR_COEF_90LOW, BI_YR_COEF_90UPP
    - BI_AGR, BI_AGR_LOW, BI_AGR_UPP, BI_AGR_90LOW, BI_AGR_90UPP
    - BI_PERC_CNG, BI_PERC_CNG_LOW, BI_PERC_CNG_UPP, BI_PERC_CNG_90LOW, BI_PERC_CNG_90UPP
    - GB_N_YEARS, GB_FIRST_YEAR, GB_LAST_YEAR, GB_YR_COEF, GB_YR_COEF_LOW, GB_YR_COEF_UPP, GB_YR_COEF_90LOW, GB_YR_COEF_90UPP
    - GB_AGR, GB_AGR_LOW, GB_AGR_UPP, GB_AGR_90LOW, GB_AGR_90UPP
    - GB_PERC_CNG, GB_PERC_CNG_LOW, GB_PERC_CNG_UPP, GB_PERC_CNG_90LOW, GB_PERC_CNG_90UPP
  - Supplementary data: moth_names_codes_lookup.csv linking SPECIES_ID to BRC codes, UKSI names, Agassiz et al. checklist IDs, Bradley & Fletcher IDs, etc.

- Supplementary and references
  - Supplementary lookup file (moth_names_codes_lookup.csv) enables cross-referencing with external taxonomic databases (BRC, UKSI, Agassiz et al., Bradley & Fletcher).
  - Acknowledgements: NERC and BBSRC funding; RIS core capability support.
  - Key references detail the GAI method, RIS data history, and related moth population trend studies.

- Practical considerations for data use (Data Support perspective)
  - Data quality and reliability: model-based trends with bootstrapped CIs; species-level reliability varies, with explicit expert validation.
  - Temporal and taxonomic caveats: some species have non-standard time ranges; macro-moths predominate due to identifiability constraints; GB subset uses different time window and trap scope.
  - Data integration opportunities: compatible with climate, habitat, and land-use datasets to explore drivers of moth population changes; can be used to build dashboards or reports enabling self-service access to species trends.
  - Potential data products: time-series trend metrics (AGR and total % change) per species, uncertainty ranges, and cross-collection comparisons (BI vs GB).

- End-user value proposition
  - Enables long-term biodiversity monitoring and assessment of insect population responses to environmental change.
  - Provides a transparent, replicable framework for generating and interpreting species-specific population trends across a standardized time series.