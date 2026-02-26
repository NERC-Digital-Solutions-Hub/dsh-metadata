# EIDC Archive version

- Purpose: This archive complies with additional NERC requirements to host data on the EIDC and points to a full background in the associated Nat Ecol Evol paper. It contains analysis scripts and raw data supporting Terry et al. (2021) No pervasive relationship between species size and local abundance trends. Consult the original paper for full background and methods.

## Overview of the dataset and aim for environmental monitoring

- Demonstrates environmental condition through assemblage time series and trait-based analyses.
- Uses standardized methods to enable comparison across studies and over time.
- Provides outputs in reusable formats (datasets, tables, scripts) for scrutiny of environmental health and policy performance.

## Collection and generation of assemblages

- Data source: BioTIME open component, including fixed plots and diverse surveys/transects.
- Assemblage construction:
  - Classify studies as single-site or multi-site based on coordinates.
  - Single-site studies treated as one assemblage; multi-site studies subdivided into 96 km² grid cells (96km2 cells).
  - Retain assemblages with data for at least 10 species and 5 years between first and last record.
- Time-series preparation focuses on abundance or biomass data (prefer abundance when both are available).

## Taxonomic name cleaning and standardization

- Replace uninformative labels (e.g., spA, unidentified) and convert common names to binomials using Encyclopaedia of Life via taxize, with manual checks.
- Standardize informative names against GBIF backbone (taxize).
- Distinguish homonyms by dominant kingdom per study.
- When only genus-level IDs are present, match to genus-level trait values; otherwise, exclude overly coarse identifications from trait matching.

## Trait data and size measures

- Data sources:
  - Amniotes: life history database (adult_body_mass_g).
  - Plants: TRY database (seed dry mass; plant height vegetative).
  - Fish: curated trait dataset (maximum length; FishBase-derived).
  - Marine species: WoRMS for size attributes (length in mm; qualitative sizes 1–4).
- Processing:
  - Map to accepted species names; use adult size values; convert units to millimeters where applicable.
  - For plants, calculate mean log(seedmass) and maximum height; exclude high-variability seed masses.
  - Exclude non-adult values and ambiguous size categories; discard inconsistent records.
- Trait matching:
  - Link species in BioTIME to trait data via AphiaID and other taxonomic identifiers.
  - Use wound-up trait values where multiple values exist; handle qualitative categories as numeric proxies.

## Abundance change–trait correlation (τ)

- Inclusion criteria per assemblage–trait pair:
  - At least 40% of species have trait data and at least 5 species present in ≥80% of yearly samples.
  - Exclude transient species (present in fewer than half of the year samples).
  - If a study provides both abundance and biomass, prefer abundance data.
  - Exclude studies with only presence–absence data.
- Data processing and modeling:
  - Remove leading/trailing zeros in time series; apply square-root transformation and standardize to zero mean and unit variance.
  - For each species in an assemblage, fit an ordinary least-squares regression of transformed abundance/biomass against year to obtain a slope (β).
  - Define τ as Kendall’s rank correlation between trait values and species-specific βs within each assemblage.
  - If multiple assemblages exist within a study, average assemblage τ values to obtain a study-level τ.
- Alternatives:
  - Ranking approach within each year (ties averaged; absent species get rank 0).
  - Time series scaled by the mean (division by mean) as an alternative transformation.

## Study-level determinants of τ

- For each study, compute:
  - Mean total species richness per assemblage over time.
  - Mean data completeness per assemblage.
  - Mean number of years of data.
  - Mean span of years with data.
  - Log10 number of assemblages (spatial extent).
  - Absolute latitude of study center.
  - Trait range within assemblages (log10(max) − log10(min)).
- Analysis: Linear models to assess whether these factors predict τ or τ2.

## Data structure, outputs, and access

- Analysis framework and outputs implemented in R; four main scripts described in the repository:
  - Assemble assemblages from raw BioTIME data by grid cells.
  - Clean species names against GBIF backbone.
  - Gather trait data from multiple sources.
  - Conduct the abundance–trait analyses described above.
- Key result tables:
  - AllThree_All.csv: Comprehensive results for each trait–study combination, including:
    - Tidy species name, D19 and Elas slopes (population trends), p-values, standard errors, observation counts, ranking metrics, trait values, and study-cell identifiers.
  - Study_Corr_Predictors.csv: Final τ values with predictors like number of cells, mean diversity, years of data, completeness, latitude, etc.
- Trait mapping:
  - bt_names_all_traits.csv links BioTIME names to trait databases, including canonical names, taxonomic rank, kingdom, common names, Aphia IDs, and TRY identifiers.
  - Core trait fields include body length, body mass, seed mass, plant height, and qualitative body size.
- Data provenance and licensing:
  - Core data come from external repositories (BioTIME, trait databases); licensing and data-use requirements apply; raw data are retained for reproducibility.
- Accessibility note:
  - Core data sources are not rehosted here; this archive provides reproducible scripts and processed outputs, with original sources cited.

## Authorship, reuse, and quality control

- Original code authored by Chris Terry (QMUL) with parts from other authors.
- Data ownership and reuse restrictions apply; users should consult original data sources for reuse requirements.
- Quality control implemented through filtering, cleaning, and standardization steps described in the methods.