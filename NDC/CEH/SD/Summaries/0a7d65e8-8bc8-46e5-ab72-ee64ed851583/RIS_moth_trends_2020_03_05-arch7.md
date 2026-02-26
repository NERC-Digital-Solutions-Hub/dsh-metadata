# Moth trends for Britain & Ireland from the Rothamsted Insect Survey light-trap network (1968 to 2016)

## Scope and purpose
- Provides abundance trends for 432 moth species (mostly macro-moths) using data from the Rothamsted Insect Survey (RIS) light-trap network (1968–2016).
- Trends are presented as year coefficients from a generalized abundance index (GAI) model, i.e., Annual Growth Rate (AGR), and total percentage changes over the time series.
- Includes 95% and 90% confidence intervals (CIs) for both trend metrics.
- Two datasets are provided:
  - BI: Britain & Ireland (1968–2016)
  - GB: Great Britain only (1970–2016)
- Methodology and datasets align with the GAI framework (Dennis et al. 2016).

## Data sources: Rothamsted Insect Survey light-trap network
- RIS operates long-running networks sampling aphids and moths; light-traps sample local moth fauna with a standardized design.
- Light-trap characteristics:
  - 200 W tungsten bulb, trap height 1.2 m, opaque lid to bias sampling to local area.
  - Attracts moths within an approximate radius of 60–100 m; sampling largely local rather than high-flying moths.
- Network status:
  - ~80 active traps across Britain & Ireland; historically >600 locations, ~100 traps active per year.
  - Traps spread across England, Scotland, Wales, Channel Islands; Ireland coverage is more limited.
- Data scope:
  - Over 14 million individual moths captured; >1,500 species represented.
  - Data widely used in climate change, biodiversity, and population-trend research.

## Dataset composition
- Counts and species coverage:
  - 4,687,310 abundance counts across 766 species (GB & BI analyses use 432–430 reliable species).
  - 541 traps used in BI analysis; average ~95 traps operating per year.
  - Mostly macro-moths; a small number of easily identified micro-moths (e.g., Nomophila noctuella, Plutella xylostella, Udea ferrugalis) included.
- Taxonomic and time-period notes:
  - Analyses primarily at the species level; some aggregates due to taxonomic or identification issues (examples listed in Table 1 of the source).
  - GB analyses sometimes use a reduced time period for certain taxa (e.g., 1970–2016 or 1971–2016), due to data quality or identification issues (see Table 2 in the source).

## Analytical approach
- Generalized Abundance Index (GAI) method:
  - Step 1: Generalized Additive Model (GAM) to estimate annual flight curves per species; curves are standardized so area under the curve equals one.
  - Step 2: Correct for within-year recording gaps to produce site-specific annual abundance indices.
  - Step 3: Poisson regression with site (categorical) and year (continuous) to obtain yearly coefficients.
- Trend metrics derived:
  - Year coefficient from Poisson model used as the temporal trend measure.
  - Annual Growth Rate (AGR): exp(year coefficient) − 1.
  - Total percentage change: calculated from AGR over the number of years in the period.
- Uncertainty:
  - Bootstrapping (1,000 replicates) to produce 95% and 90% CIs for AGR and total percentage change.
- Reliability:
  - The method yields reliable results for 432 species (430 GB) after expert data-quality assessment of indices, trends, and CIs.

## Dataset structure and fields
- File format: comma-separated values (CSV).
- Two result sets distinguished by prefix:
  - BI_…: Britain & Ireland analyses (1968–2016)
  - GB_…: Great Britain analyses (1970–2016)
- Key columns present (examples; BI and GB prefixes apply to corresponding sets):
  - SPECIES_ID, SPECIES_NAME, COMMON_NAME, FAMILY
  - BI_N_YEARS, BI_FIRST_YEAR, BI_LAST_YEAR, BI_YR_COEF, BI_YR_COEF_LOW, BI_YR_COEF_UPP
  - BI_YR_COEF_90LOW, BI_YR_COEF_90UPP
  - BI_AGR, BI_AGR_LOW, BI_AGR_UPP, BI_AGR_90LOW, BI_AGR_90UPP
  - BI_PERC_CNG, BI_PERC_CNG_LOW, BI_PERC_CNG_UPP, BI_PERC_CNG_90LOW, BI_PERC_CNG_90UPP
  - GB_N_YEARS, GB_FIRST_YEAR, GB_LAST_YEAR, GB_YR_COEF, GB_YR_COEF_LOW, GB_YR_COEF_UPP
  - GB_YR_COEF_90LOW, GB_YR_COEF_90UPP
  - GB_AGR, GB_AGR_LOW, GB_AGR_UPP, GB_AGR_90LOW, GB_AGR_90UPP
  - GB_PERC_CNG, GB_PERC_CNG_LOW, GB_PERC_CNG_UPP, GB_PERC_CNG_90LOW, GB_PERC_CNG_90UPP
- Supplementary names & taxonomic codes:
  - moth_names_codes_lookup.csv provides crosswalks to BRC, UKSI, Agassiz et al. checklist, Bradley & Fletcher IDs.
  - Columns include SPECIES_ID, BRC_CONCEPT, BRC_SPECIES_NAME, ABH_NUMBER, ABH_NAME, BF_NUMBER.

## GIS-ready usage and outputs
- Spatial mapping potential:
  - Create species- or aggregate-level trend maps across traps/sites using BI/GB site indices and year coefficients.
  - Map AGR and total percentage change to visualize directional trends (increasing vs decreasing populations) over time.
  - Combine with habitat, climate, or land-use layers to explore drivers of regional trends.
- Temporal analysis capabilities:
  - Time-series dashboards per species or per site to display annual indices, AGR, and confidence intervals.
  - Comparative analyses across Britain vs Great Britain by applying BI and GB datasets.
- Data integration considerations:
  - Use supplementary names lookup to align with other biodiversity data sources (UKSI, BRC, Agassiz checklist).
  - Be mindful of acknowledged data quality issues and species-specific time-period differences when aggregating.

## Data quality, limitations, and caveats
- Taxonomic and data issues:
  - Some species have time periods shortened or adjusted due to identification inconsistencies in early years.
  - A subset of taxa relies on aggregated species groups due to taxonomic complexities.
- Spatial coverage and sampling bias:
  - Ireland coverage is relatively limited; GB analyses rely on traps located near power/maintenance facilities, potentially influencing spatial representativeness.
  - Light-trap sampling tends to sample local moths rather than highly mobile, high-flying individuals.
- Methodological considerations:
  - RELIABILITY is based on expert assessment of underlying data and model outputs; some species may have less robust trends due to data gaps or sampling variance.
- Temporal scope:
  - BI analyses cover 1968–2016; GB analyses cover 1970–2016, with some species using non-standard periods.

## Access and supplementary resources
- Primary datasets available as CSV:
  - Moth trend data for Britain & Ireland (BI) and Great Britain (GB) analyses.
- Supplementary resources:
  - moth_names_codes_lookup.csv for cross-referencing species names and codes with external taxonomic databases (BRC, UKSI, Agassiz checklist, Bradley & Fletcher IDs).
- Acknowledgements and references provide context on funding, data provenance, and methodological foundations.