# Moth trends for Britain & Ireland from the Rothamsted Insect Survey light-trap network (1968 to 2016)

## Overview
- Dataset of abundance trends for 432 moth species (mostly macro-moths) using Rothamsted Insect Survey (RIS) light-trap data from 1968–2016.
- Two trend versions provided:
  - Britain & Ireland (BI): 1968–2016
  - Great Britain (GB): 1970–2016
- Trends expressed as year coefficients from a generalized abundance index (GAI) model, annual growth rates (AGR), and total percentage changes, with 95% and 90% confidence intervals.

## Data provenance and scope
- Source: RIS light-trap network, one of the longest-standardised terrestrial insect time series (since 1964).
- Network characteristics:
  - ~80 active traps across Britain & Ireland (historically >600 locations; ~100 traps per year on average).
  - Traps sample locally due to design features (opaque lid, trap height, exposure).
  - Sampling biased toward areas near power and maintenance sites; Ireland coverage is comparatively limited.
- Data scope:
  - 4,687,310 abundance counts across 766 species (1968–2016 BI; GB subset 1970–2016).
  - Most species are macro-moths; a small number of easily identified micro-moths included (e.g., Nomophila noctuella, Plutella xylostella, Udea ferrugalis).
  - Analyses often at species level; some aggregates used due to taxonomic/identification issues.

## Analytical method
- Generalized Abundance Index (GAI) approach (Dennis et al. 2016):
  - Step 1: Generalized Additive Model to estimate annual flight curves per species; standardize so area under curve sums to one.
  - Step 2: correct for within-year recording gaps to produce site abundance indices.
  - Step 3: Poisson regression with site (categorical) and year (continuous) to estimate temporal trends from annual indices.
- Trend metrics:
  - Year coefficient from Poisson model (main trend measure).
  - Annual Growth Rate (AGR): derived from exponentiated year coefficient minus 1.
  - Total percentage change: derived from AGR over the number of years in the interval.
- Uncertainty:
  - Bootstrapping (1,000 replicates) to obtain 95% and 90% confidence intervals for AGR and total change.
- Reliability:
  - GAI-based trends considered reliable for 432 species (430 GB) after expert review of indices, trends, and confidence intervals.

## Description of dataset and structure
- File format: comma-separated values (CSV).
- Two linked result sets:
  - BI_ANALYSIS: Britain & Ireland data (1968–2016).
  - GB_ANALYSIS: Great Britain data (1970–2016).
- Column prefixes distinguish the two analyses:
  - BI_... fields for BI analysis.
  - GB_... fields for GB analysis.
- Core fields include:
  - SPECIES_ID, SPECIES_NAME, COMMON_NAME, FAMILY.
  - BI_N_YEARS, BI_FIRST_YEAR, BI_LAST_YEAR, BI_YR_COEF, BI_YR_COEF_LOW, BI_YR_COEF_UPP, BI_YR_COEF_90LOW, BI_YR_COEF_90UPP.
  - BI_AGR, BI_AGR_LOW, BI_AGR_UPP, BI_AGR_90LOW, BI_AGR_90UPP.
  - BI_PERC_CNG, BI_PERC_CNG_LOW, BI_PERC_CNG_UPP, BI_PERC_CNG_90LOW, BI_PERC_CNG_90UPP.
  - Corresponding GB_ fields: GB_N_YEARS, GB_FIRST_YEAR, GB_LAST_YEAR, GB_YR_COEF, GB_YR_COEF_LOW, GB_YR_COEF_UPP, GB_YR_COEF_90LOW, GB_YR_COEF_90UPP, GB_AGR, GB_AGR_LOW, GB_AGR_UPP, GB_AGR_90LOW, GB_AGR_90UPP, GB_PERC_CNG, GB_PERC_CNG_LOW, GB_PERC_CNG_UPP, GB_PERC_CNG_90LOW, GB_PERC_CNG_90UPP.
- Data coverage notes:
  - BI: 4,687,310 counts across 766 species (541 traps sampled on average ~95/year).
  - GB: same dataset subset for GB analysis (GB-specific time window and traps).
  - Some species had reduced time periods (e.g., Eupithecia spp. due to identification issues) (Table 2 in the document describes these exceptions).
- Supplementary taxonomy and crosswalk:
  - moth_names_codes_lookup.csv provides crosswalk to BRC, UKSI, Agassiz et al. checklist, Bradley & Fletcher IDs, helping match taxa to external data sources.

## Supplementary names & taxonomic codes
- Contents link species to external taxonomic references (BRC concepts and species names, ABH/Agassiz checklists, BF numbers).
- Columns include SPECIES_ID, BRC_CONCEPT, BRC_SPECIES_NAME, ABH_NUMBER, ABH_NAME, BF_NUMBER.

## Data quality, governance, and reuse considerations
- Data quality:
  - Trends subject to model-based corrections and bootstrapped uncertainty estimates.
  - Expert validation of the reliability of per-species trend results.
  - Some species excluded from trends due to data issues or inconsistent identifications; micro-moths largely excluded except a few consistently identified species.
- Data governance implications:
  - Clear provenance: long-running, standardised RIS time series with documented methodology.
  - Detailed metadata on data scope, time periods, trap network, and data processing steps.
  - Crosswalks provided to facilitate integration with external taxonomic repositories (BRC, UKSI, Agassiz et al., Bradley & Fletcher).
- Limitations for users:
  - Light-trap sampling bias toward local fauna; results represent relative abundance trends rather than absolute population sizes.
  - Ireland coverage is weaker; GB-only vs BI-wide differences require careful interpretation.
  - Some species/time periods vary due to taxonomic or data issues; aggregated taxa used when appropriate.
- Intended use:
  - Long-term population trend assessment for moths in Britain & Ireland.
  - Cross-study comparisons, taxonomy alignment, and integration with biodiversity indicators and climate-related analyses.

## Access, usage, and attribution
- Data organized for reproducibility, enabling replication of GAI-based trend calculations with the described method (GAI, GAMs, Poisson regression, bootstrapping).
- Accompanying taxonomy crosswalk enhances interoperability with external datasets and inventories.
- Acknowledgement of funding and contributing institutions is provided in the source documentation.

## Acknowledgements and references
- Funded by Natural Environment Research Council (NERC) and BBSRC under the ASSIST programme and related core capabilities.
- RIS operates as a National Capability; data usage supported by the associated program references and methodological literature (e.g., Dennis et al. 2016 for GAI).