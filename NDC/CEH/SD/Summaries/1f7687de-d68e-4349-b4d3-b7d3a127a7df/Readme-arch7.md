# EIDC Archive version

- Purpose and scope
  - Archive to comply with NERC requirements to host data on the EIDC.
  - Full archive of code and extra files is stored on Zenodo for Terry et al. (2021) and related Nat Ecol Evol 2022 paper; consult those sources for full background and methods.
  - Text is paraphrased from the paper’s methods; code and analyses are included to support reproducibility.

- Spatialization and assemblage generation (GIS-relevant)
  - Multi-site and single-site data are handled by identifying studies and partitioning multi-site studies into assemblages on a global hexagonal grid of 96 km2 cells (dggridR).
  - Assemblages retained if they have abundance or biomass data for at least 10 species and cover at least 5 years.
  - Spatially explicit outputs enable map-based visualization of assemblage dynamics over time.

- Data cleaning and standardization
  - Species names are standardized: uninformative labels converted to binomials; common names mapped via Encyclopaedia of Life (via taxize); GBIF backbone used for canonical names; dominant kingdom used to resolve homonyms.
  - Studies with codes or unresolvable identifications are excluded.
  - For higher-rank identifications (e.g., genus), trait values are matched when possible; otherwise excluded.

- Trait data and sources (size-related traits)
  - Amniotes: adult body mass (g) from life-history database.
  - Plants: seed dry mass and maximum vegetative height from TRY database; mean log(seedmass) and max height calculated per species.
  - Fish: maximum length from curated TraitCollection (FishNAtlanticNEPacificContShelf) and WoRMS; genus and species level where available.
  - Size data standardized and converted to millimetres where applicable; adults only; qualitative WoRMS body sizes retained as 1–4 categories.

- Abundance change–trait correlation (τ)
  - Assemblage–trait combinations require adequate data coverage (≥40% of species with trait data; ≥5 species per year; ≥80% of yearly samples meet this).
  - Trailing/leading zeros trimmed; per-species population series square-root transformed and standardized.
  - OLS regression of each species’ time series on year; slopes β summarized per assemblage.
  - τ is Kendall’s rank correlation between trait values and βs; zero or near-zero slopes are set to 0 to avoid spurious rankings.
  - Alternative transformations tested: (1) yearly relative ranks within year, (2) population series scaled by its mean.

- Study-level determinants of τ
  - Calculated per study: mean species richness, data completeness, number of years, time span, number of assemblages (log), absolute latitude, and trait range (log max − log min).
  - Linear models used to assess whether these factors predict τ or a related metric τ2.

- Analysis tools
  - All analyses performed in R.
  - KnittedScripts folder contains:
    - Assembly generation from raw BioTIME data
    - Taxonomic name cleaning against GBIF backbone
    - Trait-data gathering
    - The described analyses

- Data structure and outputs
  - Trait mapping table: bt_names_all_traits.csv
    - Links tidied BioTIME names to GBIF/Aphia/TRY sources
    - Includes taxonomic rank, kingdoms, common names, and various IDs
    - Core traits include body length (marine), qualitative body size, mean maximum length (fish), adult body mass, seed mass, max height, and references
  - Results tables:
    - AllThree_All.csv: comprehensive results per study and trait, including:
      - D19_slope, D19_pvalue, D19_StdErr (main population trend measure)
      - Elas_slope, Elas_pvalue, Elas_StdErr (alternative trend measure)
      - N_times_observed, N_used, Slopes, MeanRank, MeanAbsRankChange
      - trait_value, RelTraitRank, trait, STUDY_ID_CELL
    - Study_Corr_Predictors.csv: study-level τ values and predictors:
      - STYUD_ID, Trait, LogCells, Mean_Sp_div, Mean_N_Years, Mean_Completeness, Mean_YearRange
      - PROTECTED_AREA, GRAIN_SQ_KM_Log, Abs_Lat

- Core data sources and licensing
  - BioTIME database (community time series)
  - Amniote life history trait data
  - Fish trait collection and WoRMS for marine taxa
  - TRY plant traits database
  - Core data sources have usage requirements and citations; raw data in this repository is primarily for reproducibility.

- Quality control
  - Data cleaning, filtering, and standardization were applied to source databases to ensure appropriate, usable inputs for the analyses.
  - Documented data structure, scripts, and provenance to support reproducibility.

- Authorship and reuse
  - Original code by Chris Terry (QMUL) with contributions from others noted inline.
  - Data access often requires citation back to original compilations; consult source databases for reuse constraints.