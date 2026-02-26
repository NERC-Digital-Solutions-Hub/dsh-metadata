# EIDC Archive version

## Aim and governance context
- Archive created to comply with additional NERC requirements for hosting data on the EIDC.
- Full archive of code and extra files available on Zenodo to support transparency and reproducibility (link provided).
- Paraphrased methods summarize Terry et al. (2021) work; background and methods available in the original paper.

## Data sources and assemblage construction
- Primary data source: BioTIME database of community time series (open component).
- Studies classified as single-site or multi-site; multi-site studies subdivided into assemblages using a global 96 km2 hex grid (dggridR).
- Inclusion criteria: assemblages must have abundance or biomass data for at least 10 species and span at least 5 years.

## Data cleaning and taxonomic standardization
- Uninformative labels (e.g., spA, unidentified) converted to binomials; common names converted using Encyclopaedia of Life via taxize; manual checks based on location and species distribution.
- Studies listing only codes excluded.
- Taxonomic names standardized against GBIF backbone (taxize); dominant kingdom used to resolve homonyms.
- Genus-level identifications mapped to genus-level size traits when possible; higher-rank identifications not mapped.

## Trait data and sources
- Four independent trait databases used (not mixed):
  - Amniotes: adult_body_mass_g (life history database).
  - Plants: TRY database for seed mass (log mg) and plant height; mean seed mass (log) and max height computed per species.
  - Fish: curated traits (maximum length; average if multiple values) from FishBase-derived dataset.
  - Marine species: WoRMS for length-based body size; qualitative sizes converted to numeric categories; adults only.
- IDs harmonized across sources (AphiaID, WoRMS IDs, GT references) and units standardized (mm for lengths).

## Abundance change–trait correlation analysis
- Inclusion criteria for assemblage–trait combinations: ≥40% of species have trait data; ≥5 species per assemblage; ≥80% of years have ≥5 species observed.
- Transient species excluded (seen in less than half of the year samples).
- Data filtering: studies with only presence–absence data excluded.
- Data transformations:
  - Population series square-root transformed, then standardized (mean 0, SD 1); trailing zeros trimmed.
  - Ordinary least-squares regression of abundance/biomass over year per species; slope β used to summarize abundance change.
  - Kendall’s τ computed as the correlation between trait values and βs within each assemblage.
- Handling of special cases:
  - Very small β values set to 0 to avoid spurious results.
  - If multiple assemblages per study, τ is averaged across assemblages.
- Alternative data transformations tested:
  - Relative ranks within each year (ties averaged; unobserved species given rank 0).
  - Time-series data divided by its mean value.
- Additional study-level predictors considered to explain τ and τ2 (richness, completeness, years, spatial extent, latitude, trait range).

## Data structure and outputs
- Core scripts (KnittedScripts folder) produce assemblages, clean names, gather trait data, and perform analyses.
- Trait data linkage file:
  - bt_names_all_traits.csv: maps BioTIME tidy names to GBIF canonical names, taxonomic rank, kingdom, common name, Aphia and TRY IDs, and primary trait fields.
  - Core trait fields include body length, qualitative body size, maximum length (fish), adult body mass, seed mass, maximum height.
- Results files:
  - AllThree_All.csv: large table of species trends across three abundance representations (Dornelas et al. 2019 methodology), with fields for slopes, p-values, standard errors, observed counts, rank metrics, trait values, and study-cell identifiers.
  - Study_Corr_Predictors.csv: final τ values per trait-study combination and predictor metadata (e.g., LogCells, mean richness, data completeness, years of data, protected-area status, study grain, latitude).

## Access, licensing, and reuse
- Original code authored by Chris Terry (Queen Mary University of London) with contributions from others; data use subject to providers’ reuse requirements.
- Raw data are not re-hosted here; primary sources should be cited when reusing data.
- The repository’s materials (code and analysis HTMLs) support reproducibility; raw trait data and core external databases are referenced rather than redistributed.

## Quality control and data stewardship considerations
- Systematic cleaning and standardization of taxonomy and traits to ensure consistency across assemblages.
- Clear documentation of data processing steps, transformations, and criteria to support governance, audit trails, and reproducibility.
- Explicit handling of data availability, coverage gaps, and potential embargoes, with transparent disclosure of data origins and licensing constraints.
- Data archiving strategy aligns with governance requirements by storing analyses and provenance on accessible platforms (Zenodo and EIDC-compliant hosting).