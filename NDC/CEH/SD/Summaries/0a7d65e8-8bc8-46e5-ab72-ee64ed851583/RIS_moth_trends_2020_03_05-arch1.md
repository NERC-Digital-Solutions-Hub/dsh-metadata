# Moth trends for Britain & Ireland from the Rothamsted Insect Survey light-trap network (1968 to 2016)

- A dataset of abundance trends for 432 moth species (mostly macro-moths) estimated from Rothamsted Insect Survey (RIS) light-trap data spanning 1968–2016. Trends are provided as year coefficients (Annual Growth Rate, AGR) and total percentage changes, with 95% and 90% confidence intervals.
- Two trend versions are included:
  - Britain & Ireland (BI): uses data from 1968–2016 across the full Britain & Ireland network.
  - Great Britain (GB): GB-only analyses using 1970–2016 data.
- Some species have restricted time ranges due to taxonomic or data issues (e.g., certain Eupithecia species); GB analyses cover 430 species, BI analyses 432.

- RIS light-trap network and data context:
  - RIS operates long-running networks sampling moths with suction-traps and light-traps; the light-trap network is designed to sample local fauna and has sampling radii typically well under 100 m.
  - The network currently comprises around 80 active traps across Britain & Ireland, with historical operation at more than 600 locations and about 100 traps active per year.
  - The dataset contains over 14 million individual moths identified across more than 1,500 species collected over the study period.
  - Data have supported numerous ecological studies (diversity, climate change responses, population trends, etc.) and underpin national trend assessments.

- Data used and species coverage:
  - Final analyses are based on 4,687,310 abundance counts across 766 species (541 traps on BI dataset, average around 95 traps per year).
  - Many species are macro-moths; a small number of easily identified micro-moths (Nomophila noctuella, Plutella xylostella, Udea ferrugalis) are included to maintain consistency.
  - Analyses are typically conducted at the species level; some taxa are grouped into aggregates when necessary due to taxonomic or identification issues (Table 1 in the document describes aggregates and component taxa).

- Time periods and species-specific nuances:
  - Although the standard periods are 1968–2016 (BI) and 1970–2016 (GB), a subset of species used shorter periods due to data issues (e.g., reduced early years for various taxa; examples include several Eupithecia and other genera listed in the document).
  - GB analyses exclude certain years for specific species (e.g., 1971–2016, 1975–2016, 1986–2016 in listed cases).

- Analytical method (Generalized Abundance Index, GAI):
  - Step 1: Generalized Additive Models estimate annual flight curves for each species and standardize them so the area under the curve equals one.
  - Step 2: Correct within-year recording gaps to produce site-specific abundance indices.
  - Step 3: Poisson regression with site (categorical) and year (continuous) to estimate year coefficients.
  - Metrics derived:
    - AGR: annual growth rate derived from the year coefficient (exponentiated and converted to a proportion; AGR = 0 indicates no annual change; >0 indicates growth; <0 indicates decline).
    - Total percentage change: derived from the AGR over the number of years in the time series.
  - Uncertainty quantified via bootstrapping (1,000 replicates) to provide 95% and 90% CIs for both indices and trends.
  - Reliability: GAi provides reliable results for 432 BI species and 430 GB species based on expert evaluation of underlying data and model outputs (indices, trends, and CIs).

- Dataset structure and content:
  - Data provided as a CSV with two result sets:
    - BI_ prefixed columns for Britain & Ireland analyses.
    - GB_ prefixed columns for Great Britain analyses.
  - Key fields include:
    - SPECIES_ID, SPECIES_NAME, COMMON_NAME, FAMILY
    - BI_N_YEARS, BI_FIRST_YEAR, BI_LAST_YEAR, BI_YR_COEF, BI_YR_COEF_LOW, BI_YR_COEF_UPP, BI_YR_COEF_90LOW, BI_YR_COEF_90UPP
    - BI_AGR, BI_AGR_LOW, BI_AGR_UPP, BI_AGR_90LOW, BI_AGR_90UPP
    - BI_PERC_CNG, BI_PERC_CNG_LOW, BI_PERC_CNG_UPP, BI_PERC_CNG_90LOW, BI_PERC_CNG_90UPP
    - GB_N_YEARS, GB_FIRST_YEAR, GB_LAST_YEAR, GB_YR_COEF, GB_YR_COEF_LOW, GB_YR_COEF_UPP
    - GB_AGR, GB_AGR_LOW, GB_AGR_UPP, GB_AGR_90LOW, GB_AGR_90UPP
    - GB_PERC_CNG, GB_PERC_CNG_LOW, GB_PERC_CNG_UPP, GB_PERC_CNG_90LOW, GB_PERC_CNG_90UPP
  - A supplementary names & taxonomic codes file (moth_names_codes_lookup.csv) maps SPECIES_ID to BRC, UKSI (via Agassiz et al. checklist), and Bradley & Fletcher IDs, helping crosswalk to external data sources.

- Supplementary resources:
  - Supplementary lookup file contains crosswalk data:
    - BRC_CONCEPT, BRC_SPECIES_NAME, ABH_NUMBER, ABH_NAME, BF_NUMBER corresponding to industry-standard taxonomic references (UKSI, Agassiz et al. checklist, etc.).

- Acknowledgements and references:
  - Funded by NERC and BBSRC under ASSIST and related programs; RIS is a National Capability funded by BBSRC.
  - The work builds on prior model development and extensive literature on moth monitoring, climate responses, and long-term biodiversity trends.
  - The document cites numerous foundational studies on moth trends, climate effects, and methodology.

- Applications and uses:
  - Enables analysis of long-term moth population changes, climate-related phenology shifts, and spatial-temporal trends across Britain & Ireland.
  - Suitable for correlation analyses with environmental variables, habitat changes, land-use metrics, and climate data.
  - Provides a robust, standardized dataset with explicit confidence intervals and clearly defined metrics for interpreting population trajectories over multi-decadal scales.

- Limitations and considerations:
  - Local sampling biases due to trap proximity to human activity and limited Ireland coverage.
  - The light-trap method primarily samples local fauna; attraction radii and trap characteristics influence species detectability.
  - Some species have restricted time series due to taxonomic or data issues; GB analyses cover slightly fewer species than BI.
  - Micro-moth representation is limited to a small set of consistently identified species; macro-moth focus dominates the analyses.