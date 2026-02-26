# EIDC Archive version

## Overview
- Archive to comply with additional NERC requirements to host data on the EIDC.
- Full archive of code and extra files is on Zenodo (link provided).
- Text is paraphrased from the methods of Terry et al. (2021) and related background (Nat Ecol Evol 2022).

## Data collection and assembly
- Source: open component of the BioTIME database of community time series.
- Distinguish studies as single-site (combined assemblage) or multi-site (partitioned into 96 km2 grid cells via a global hex grid).
- Inclusion criteria: assemblages with abundance or biomass data for at least 10 distinct species and a time span of at least 5 years.
- Time series assembled to enable cross-study comparisons of species trends.

## Data cleaning and taxonomic standardization
- Uninformative labels (e.g., spA, unidentified) converted to binomials using the Encyclopaedia of Life via taxize, with manual checks.
- Informative names standardized against GBIF backbone; dominant kingdom used to resolve homonyms.
- Genus-only identifications matched to genus-level trait values; higher-rank-only identifications were not matched to traits.

## Trait data integration
- Four trait databases used (no mixing across databases):
  - Amniotes: adult_body_mass_g from life history database.
  - Plants: TRY database — seed dry mass (trait 26) and plant height vegetative (trait 3106); mean log(seed mass) and max height per accepted species name; exclude where trait SD > 1.
  - Fish: Beukhof et al. trait collection (FishBase-based) — maximum length; average when multiple values.
  - Marine species: WoRMS for size traits; use Aphia IDs to fetch attributes; convert lengths to mm; include only adults; qualitative sizes coded as 1–4; discard non-adult or ambiguous values.
- Trait matching uses Aphia IDs and GBIF/taxonomic backbones to ensure consistency.

## Abundance change–trait correlation
- Filtering criteria: assemblage–trait combination requires ≥40% and ≥5 of species have trait data; ≥80% of years contain data for ≥5 species.
- Transient species removed by requiring presence in more than half of year samples.
- If data yield is too small after filtering, the study is excluded.
- Data processing: square-root transform species totals, standardize to mean 0 and SD 1.
- Primary model: ordinary least-squares regression of each species’ time series against year; slope (β) represents directional change.
- Main response variable τ: Kendall’s rank correlation between trait values and species βs within an assemblage.
- Missing trait values cause exclusion from τ calculation.
- If a study has multiple assemblages, τ at the study level is the arithmetic mean of assemblage τs.
- Alternative transformations tested:
  - Within-year relative ranks of species by abundance/biomass (zero ranks for absent species).
  - Time series divided by its mean value.
  
## Study-level determinants
- Calculated per study (across assemblages): 
  - Mean total species richness, mean data completeness, mean number of years, mean span of years,
  - Log10 of number of assemblages (spatial extent),
  - Absolute latitude of study center,
  - Trait range within assemblage (log10(max) − log10(min)).
- Linear models used to assess whether these factors predict τ or the alternative τ2.

## Analysis and outputs
- Implemented in R; analysis scripts are in KnittedScripts.
- Outputs include:
  - AllThree_All.csv: comprehensive assemblage-level results across three ways of measuring population trends, with columns for species, trait, study-cell, and various trend metrics (e.g., D19_slope, Elas_slope, p-values, ranks, etc.).
  - Study_Corr_Predictors.csv: study-level τ values and predictor variables (e.g., number of cells, years, completeness, latitude, etc.).

## Data structure and key files
- Trait Tables (bt_names_all_traits.csv): maps BioTIME names to canonical taxonomic names, IDs (Aphia), and trait sources; includes core traits such as body length, qualitative body size, seed mass, and plant height.
- Core traits include: TR_BodyLength_mm, TR_QualitativeBodySize, TR_Mean_LengthMax, TR_adult_body_mass_g, TR_Mean_SeedMass, TR_Max_Height, TRY_datasetIDs_SeedMass, TRY_datasetIDs_Height.
- AllThree_All.csv: contains main population trend metrics (Dornelas et al. 2019 framework) and related statistics for each assemblage-trait combination:
  - TidyBTName, D19_slope, D19_pvalue, D19_StdErr, Elas_slope, Elas_pvalue, Elas_StdErr,
  - N_times_observed, N_used, Slope, MeanRank, MeanAbsRankChange, trait_value, RelTraitRank, trait, STUDY_ID_CELL.
- Study_Corr_Predictors.csv: study-level predictors and final τ values:
  - STUDY_ID, Trait, LogCells, Mean_Sp_div, Mean_N_Years, Mean_Completeness, Mean_YearRange, PROTECTED_AREA, GRAIN_SQ_KM_Log, Abs_Lat.

## Data sources, quality, governance and licensing
- Core data (BioTIME, amniote life history, fish trait databases, WoRMS, TRY) are external and not re-hosted here; data reuse requires citing original sources per their licenses.
- Raw data included for reproducibility; users should consult original sources for data rights.
- Data collection and cleaning involved quality control steps across sources; metadata and dataset provenance are maintained.
- Authorship: original code by Chris Terry; other contributions noted; licensing and data-use restrictions apply per source databases.

## Access, reproducibility and references
- Archival repository intended to support reproducibility of the Terry et al. analyses (2021/2022).
- Full archive and code are available via Zenodo; primary analyses and background methods are described in the document and accompanying HTML scripts.