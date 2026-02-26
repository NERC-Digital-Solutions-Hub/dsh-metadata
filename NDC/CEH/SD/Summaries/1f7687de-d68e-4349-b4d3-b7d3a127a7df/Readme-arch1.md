# EIDC Archive version

## Overview
- Archive to comply with additional NERC requirements; hosts analysis scripts and raw data supporting Terry et al. (2021) No pervasive relationship between species size and local abundance trends.
- Full background and methods available in the related Nat Ecol Evol paper; this document paraphrases the methods section.
- Core data and scripts are provided; full raw data sources are archived in external repositories (e.g., Zenodo, BioTIME).

## Data sources and assembly
- Primary data: BioTIME database of community time series (open component).
- Time-series assembly: classify studies as single-site or multi-site; multi-site studies are subdivided into assemblages using a global hexagonal grid of 96 km² cells.
- Inclusion criteria for assemblages: abundance or biomass data for at least 10 distinct species and data spanning at least 5 years between first and last record.

## Cleaning and taxonomic standardization
- Name cleaning: convert non-binomial labels (e.g., spA, unidentified) to binomials using Encyclopaedia of Life via taxize R package; manual checks by location and species distributions; exclude studies with code-only labels.
- Taxonomic standardization: match informative names to GBIF backbone; distinguish homonyms using dominant kingdom per study.
- Trait matching: genus-level identifications matched to genus-level size traits where species-level data were absent.
- Data substitution: if only higher-rank taxonomy (above genus) is available, trait matching is not attempted.

## Trait data and size measures
- Four trait databases used (not mixed together):
  - Amniotes: life history database for adult_body_mass_g.
  - Plants: TRY database for seed mass (log scale) and plant height; mean log(seedmass) and max height calculated; entries with high variability (sd > 1) excluded.
  - Fish: curated North Atlantic and Pacific shelf traits; maximum length used; multiple values averaged; units standardized to millimetres.
  - Marine species: WoRMS for additional size attributes; only adult body size measured; qualitative WoRMS body size categories converted to ordinal 1–4; non-adult data and ambiguous size mappings discarded.
- Data processing: amphibious steps to ensure consistent unit scales; qualitative sizes converted where needed.

## Abundance-change–trait correlation methodology
- Assemblage-trait filtering: include only assemblages with ≥40% trait data coverage, ≥5 species with trait data, and ≥80% of sampling years with ≥5 species.
- Transients: remove species present in fewer than half of the years within an assemblage.
- Data preparation: square-root transform species totals, then standardize to zero mean and unit variance.
- Slopes per species: fit ordinary least-squares regression of each species’ population time series against year; slopes (β) summarize abundance change over time.
- Handling edge cases: very small β values set to 0 to avoid spurious rankings; trailing/leading zeros trimmed to prevent artificial trends.
- Main metric: τ = Kendall’s rank correlation between species’ size-trait values and their βs within an assemblage.
- Missing trait values: exclude species lacking trait data from τ calculations.
- Aggregation: for studies with multiple assemblages, compute study-level τ as the simple mean of assemblage-level τ values.
- Alternative transformations tested:
  - Rank-based transformation: within each year, rank species by abundance/biomass; ties averaged; absent species assigned rank zero for that year.
  - Mean-divided transformation: population time series divided by its mean value.

## Transformations and sensitivity analyses
- Two alternative formulations (β-based vs. rank-based vs. mean-normalized) used to assess robustness of τ estimates across assemblages and traits.
- Study-level determinants of τ and τ2 explored via linear models to predict potential differences based on data richness, sampling span, coverage, spatial extent, latitude, and trait range.

## Study-level predictors of τ
- For each study, computed predictors including:
  - Mean total species richness per assemblage over time.
  - Mean trait-data completeness per assemblage.
  - Mean number of years of data per assemblage.
  - Mean time span (years from first to last observation).
  - Log10 of the number of assemblages (spatial extent).
  - Absolute latitude of study center.
  - Whether the study area is a protected area.
  - Study grain (grid cell size) and other metadata (e.g., latitude range of traits).

## Data structures and outputs
- Core outputs:
  - AllThree_All.csv: large table detailing species population trends across three representations (D19_slope, Elas_slope, etc.) grouped by trait value and STUDY_ID_CELL; includes significance, standard errors, observed counts, and trait correlations.
  - Study_Corr_Predictors.csv: study-level τ values and associated predictors used for the main figures.
- Trait linkage table:
  - bt_names_all_traits.csv: links BioTIME names to trait databases; includes canonical names, kingdom, common names, Aphia IDs, TRY references, and relevant trait columns (e.g., body length, seed mass, max height).
  - Core trait fields include TR_BodyLength_mm, TR_QualitativeBodySize, TR_Mean_LengthMax, TR_adult_body_mass_g, TR_Mean_SeedMass, TR_Max_Height, TRY_datasetIDs for seed mass and height.
- Data sources and reuse:
  - Core data sources (BioTIME, amniote life history, fish traits, WoRMS, TRY) are archived elsewhere; raw data usage is subject to source-specific data reuse licenses.
  - The repository contains the code and processed outputs to support reproducibility, not all raw data.

## Reproducibility, scripts, and licensing
- Analysis and processing scripts are provided within the repository (KnittedScripts) and HTML analyses detailing the steps.
  - 1) Generates assemblages from raw BioTIME data by grouping dispersed studies into grid cells.
  - 2) Cleans taxonomic names against GBIF backbone.
  - 3) Gathers trait data from multiple sources.
  - 4) Conducts the described analyses.
- Authorship: Chris Terry (Queen Mary University of London); some parts adapted from other authors as noted.
- Licensing: Raw data usage is bound by source licenses; users should consult source data requirements for reuse.

## Availability and references
- Archive hosted to meet NERC requirements; full background/methods in the Tara Terry et al. paper.
- Full raw data and code dependencies linked to external repositories (BioTIME, Zenodo, TRY, WoRMS).
- For background and methods, refer to No pervasive relationship between species size and local abundance trends (Terry et al., Nat Ecol Evol, 2022).