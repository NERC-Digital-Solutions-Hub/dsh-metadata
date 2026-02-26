# EIDC Archive version

## Overview
- Archive to comply with additional NERC requirements to host data on the EIDC.
- Full archive of code and extra files is hosted on Zenodo: https://zenodo.org/doi/10.5281/zenodo.4745553
- Supports Terry et al. (2021) No pervasive relationship between species size and local abundance trends. Nat Ecol Evol 6, 140–144 (2022); consult for full background and methods.
- Paraphrased methods provided; original data sources and methods are the basis for reproducibility.

## Data generation and collection
- Generating assemblage time series:
  - Pulled studies from the open BioTIME database of community time series.
  - Classified studies as ‘single-site’ or ‘multi-site’ based on coordinates.
  - Multi-site studies partitioned into assemblages within a global 96 km² hex grid (dggridR).
  - Retained assemblages with abundance or biomass data for at least 10 distinct species and a time span of at least 5 years.

- Cleaning names:
  - Convert records not identified to species level to binomials where possible.
  - Identify and convert uninformative labels (e.g., spA, unidentified, larvae) using Encyclopaedia of Life via taxize R package; manual checks by location and distribution.
  - Standardize informative names against GBIF backbone; resolve homonyms by dominant kingdom.
  - When only genus-level IDs exist, match to genus-level size traits; if only higher-rank taxonomy, traits are not matched.

- Trait data:
  - Four separate trait databases used; no cross-database data mixing.
  - Amniotes: adult_body_mass_g from life history database.
  - Plants: TRY data for seed dry mass (trait 26) and plant height (trait 3106); means of log(seedmass) and maximum height; exclude if SD of log(seedmass) > 1.
  - Fish: curated trait dataset (Beukhof et al., leveraging FishBase); maximum length, averaged if multiple values.
  - Marine species: WoRMS for Aphia IDs and attributes; body size in mm; only adult measurements; discard non-adult values and implausible ranges; qualitative sizes (1–4) retained when applicable.
  - For non-adult data or conflicting size categories, entries are discarded.

- Abundance change–trait correlation:
  - Assemblage–trait pairs require ≥40% of species with trait data and >80% of years with at least 5 species observed.
  - Exclude transitory species (present in >50% of year samples considered).
  - If data reduced to <1% of original cells, drop the study.
  - Prefer abundance data when both abundance and biomass exist; presence–absence-only data are not used.
  - Time series adjustments: trailing/leading zeros trimmed; apply square-root transformation and standardize to mean 0, sd 1.
  - Fit ordinary least-squares regression of species time series against year for each species; slopes (β) summarize temporal change.
  - τ (Kendall’s rank correlation) computed between trait values and βs within each assemblage; exclude species with missing trait values.
  - When a study has multiple assemblages, τ values are averaged to the study level.
  - Two alternative transformations tested: (1) within-year relative ranks of species by abundance/biomass (ties averaged; absent species get rank 0); (2) dividing each time series by its mean.
  - Study-level determinants of τ (and τ2) computed per study using metrics: mean richness, mean trait data completeness, mean number of years, mean time span, log10(number of assemblages), absolute latitude, and trait range; linear models assess predictive power.

- Analysis environment:
  - All analyses performed in R; scripts are included in the KnittedScripts folder.

## Data outputs and files
- Original data sources and core databases (BioTIME, amniote life history traits, the fish trait database, TRY, WoRMS) are archived elsewhere; not re-hosted here. Raw data included mainly for reproducibility; users should cite original sources.

- Data structure and scripts:
  - HTMLs detailing analyses accompany the repository.
  - Four main scripts:
    - Generate assemblages from raw BioTIME data
    - Clean species names against GBIF backbone
    - Gather trait data from diverse sources
    - Conduct analyses described in the paper

- Trait Tables:
  - bt_names_all_traits.csv: links tidied BioTIME names to trait records.
  - Key columns include TidyBTName, canonicalName, rank, kingdom, common_name, AphiaID, Aphia_sci, TRY_AccSpeciesName, TRY_datasetIDs for seed mass and height, etc.
  - Core traits used:
    - TR_BodyLength_mm, TR_QualitativeBodySize, TR_Mean_LengthMax
    - TR_adult_body_mass_g
    - TR_Mean_SeedMass
    - TR_Max_Height
    - TRY_datasetIDs_SeedMass, TRY_datasetIDs_Height

- Results Tables:
  - AllThree_All.csv: comprehensive table of species population trends across three representations; columns include:
    - TidyBTName, D19_slope, D19_pvalue, D19_StdErr
    - Elas_slope, Elas_pvalue, Elas_StdErr
    - N_times_observed, N_used, Slope, MeanRank, MeanAbsRankChange
    - trait_value, RelTraitRank, trait, STUDY_ID_CELL
  - Study_Corr_Predictors.csv: final τ values per trait-study combination with predictors such as:
    - STUDY_ID, Trait, LogCells, Mean_Sp_div, Mean_N_Years, Mean_Completeness, Mean_YearRange
    - PROTECTED_AREA, GRAIN_SQ_KM_Log, Abs_Lat

## Authorship, reuse, and licensing
- Original code by Chris Terry (Queen Mary University of London); some components adapted from others as noted.
- Much of the underlying data are subject to usage restrictions; users should cite original data sources when reusing.
- Raw data are included to support reproducibility; consult original sources for data reuse terms.

## Quality control and reproducibility
- Multi-step cleaning and filtering applied to source databases.
- Analyses are implemented in R; accompanying scripts and HTML documentation provide reproduction pathways.