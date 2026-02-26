# EIDC Archive version

## Overview
- Archive created to comply with additional NERC requirements to host data on the EIDC.
- Full archive of code and extra files is on Zenodo (link provided).
- Contains analysis scripts and raw data to support Terry et al. (2021) No pervasive relationship between species size and local abundance trends. Nat Ecol Evol 2022; consult the paper for background and methods.
- Text summarized from the methods section of the paper; focuses on data collection, cleaning, trait integration, and analysis workflow.

## Data sources and scope
- BioTIME database of community time series (open component) used as the primary data source.
- Data include fixed plots and broad surveys; studies categorized as single-site or multi-site.
- Assemblages generated from BioTIME records; multi-site studies split into hexagonal grid cells (96 km^2).
- Inclusion criteria: assemblages must have ≥10 distinct species and data spanning ≥5 years.
- Original data are not re-hosted here; core data sources documented and cited.

## Collection and generation methods
- Time-series assemblage construction:
  - Single-site studies treated as one assemblage; multi-site studies partitioned by grid cells.
- Taxonomic name cleaning:
  - Uninformative labels converted to binomials via Encyclopaedia of Life (via taxize); manual checks by location and species distribution.
  - Informative names standardized against GBIF backbone; genus-level identifications mapped to size trait values when possible.
  - Studies with only codes excluded.
- Trait data collection:
  - Four separate trait databases used (no mixing between databases).
  - Amniotes: adult_body_mass_g from life-history database.
  - Plants: seed dry mass and plant height from TRY; mean log(seedmass) and max height computed; incomplete when variability too high.
  - Fish: maximum length from a curated North Atlantic/Pacific dataset; averages taken when multiple values exist.
  - Marine species: size data from WoRMS; adults only; lengths converted to mm; qualitative sizes mapped to 1–4; non-adult data and multi-category conflicts discarded.
- Taxon matching and data integration:
  - Aphia IDs used forWoRMS integration; sizes standardized to numeric units; multiple data quality checks implemented.

## Abundance change–trait correlation (τ)
- Assemblage–trait filtering criteria:
  - At least 40% of species have trait data; at least 5 species observed in >80% of years.
  - Transient species removed (seen in ≤50% of years); studies with insufficient data removed.
  - When both abundance and biomass present, abundance data preferred; presence–absence only data excluded.
- Data processing and modeling:
  - Trajectories trimmed of leading/trailing zeros; square-root transform of totals; standardized to zero mean and unit variance.
  - For each species, a regression of abundance/biomass over year to obtain slope β.
  - Very small β values (< 10^-5) set to zero to avoid spurious trends.
  - τ = Kendall’s rank correlation between trait values and species’ β within each assemblage.
  - Missing trait data lead to exclusion from τ calculation.
  - Study-level τ = mean of assemblage-level τs within the study.
- Alternative approaches:
  - Ranking approach within each year (highest to lowest); zeros for absent species.
  - Scaling populations by their mean value.
- Determinants of τ (within each size trait):
  - Mean species richness, data completeness, number of years, time span, number of assemblages, study latitude, and trait range.
  - Linear models used to assess if these factors predict τ or τ2.

## Data delivery and structure
- Analysis powered by R; scripts located in the KnittedScripts folder.
- Core files and tables:
  - Trait linkage table: bt_names_all_traits.csv
    - Maps BioTIME-tidy names to canonical names, ranks, kingdoms, common names, Aphia IDs, TRY IDs, and trait references.
  - Core trait fields (examples):
    - Body length (mm), qualitative body size (1–4), mean maximum length (cm), adult body mass (g), seed mass (log mg), plant max height (m), etc.
  - Results tables:
    - AllThree_All.csv: detailed assemblage-level results across three analysis framings; includes species counts, slopes, p-values, standard errors, ranks, and trait values.
    - Study_Corr_Predictors.csv: study-level predictors for τ; includes LogCells, mean diversity, years, completeness, year range, protected area flag, grain, and absolute latitude.
- Data structure notes:
  - Core datasets archived separately (BioTIME, amniote traits, fish traits); raw TRY and WoRMS data are not re-hosted here.

## Authorship, reuse and licensing
- Original code authored by Chris Terry (QMUL); some parts adapted from others as noted.
- Much of the underlying data have usage restrictions; users should consult source data licenses and citation requirements.
- Raw data included for reproducibility; users should reference original sources when reusing.

## Reproducibility and access
- Analysis scripts and HTMLs provided to document analyses and methods.
- Archive hosted to meet external data hosting requirements; full data provenance and links provided (Zenodo, BioTIME references).
- Emphasis on data provenance, standardization, and metadata to support discoverability and reuse.