# Countryside Survey

- A rolling, long-term monitoring program of the UK countryside’s natural resources, conducted since 1978 and now part of the UKCEH Countryside Survey (UKCEH-CS) with rolling survey cycles starting in 2019.
- Aims to detect gradual and subtle changes over time by comparing results across surveys using a standardized, ecosystem-scale approach that integrates soils, vegetation, habitats, and landscape features.

## Data collection design and rolling program

- Rolling program:
  - Repeats once every five years or 500 squares completed; designed to buffer against climate variability and maximize national coverage over time.
  - First cycle for rolling program started in 2019.
- Sampling framework:
  - 500 x 1km squares selected per five-year cycle, stratified by the Land Classification of Great Britain (ITE-based), to provide national and sub-national indicators.
  - Approximately 100 squares visited each year.
  - Exclusions: any square with >75% urban land or >90% sea (per LCM2007 and census data).
  - Priority: retain 256 squares from 1978 to preserve the longest time series; add additional squares first surveyed in 1990 to extend history.
- Multi-metric, ecosystem-focused design:
  - Measures across soils, vegetation, headwater streams, habitats, and landscape features using coordinated sampling in the same locations where possible.

## Methods and data quality

- Field data collection:
  - Conducted by trained survey teams following standard protocols ( Smart et al., 2020).
  - Intensive pre-survey training; ongoing supervision and quality control during surveys.
  - 10% of plots re-surveyed for quality assurance; independent validation of plot locations and habitat classifications since 1990.
- Data standards and classifications:
  - Habitat and land classifications aligned with ITE/Land Classification (Bunce et al., 2007) and JNCC biodiversity classifications (BAP Broad and Priority Habitats).
  - Species nomenclature following Stace (1997).
  - Documentation and methodologies referenced in multiple CEH and UK-SCAPE materials.
- Visuals and accessibility:
  - Figure showing distribution of 1km survey squares for 2020–2021 (confidentiality protected in maps).

## Data products and file details

- Vegetation data for 2020 and 2021:
  - Two CSV files:
    - UKCEHCS_VEGETATION_PLOTS_2020_21.csv (Plot Information)
      - Key columns: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, X/XX (plot area), PLOT_BH (BAP Broad Habitat), PLOT_PH (BAP Priority Habitat), COUNTRY, COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07, LC07_NUM, etc.
    - UKCEHCS_VEGETATION_PLOT_SPECIES_2020_21.csv (Species List)
      - Key columns: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, BRC_NUMBER (species identifier), nest levels and cover metrics (e.g., ZERO_COVER, FIRST_COVER, TOTAL_COVER), taxonomic reference (Stace).
  - Species nomenclature: Stace (1997); data organized with nesting and cover details per plot.
- Documentation and supporting information:
  - Field Handbook: UK-SCAPE Field Survey Field Handbook 2020 Vegetation Plots (Smart et al., 2020).
  - Related methodological and statistical references (e.g., Scott 2008; Norton et al. 2012) and dataset documentation for context and reproducibility.
- Data lineage and quality references:
  - Quality assurance and methodology described in Smart et al. (2020) and related Countryside Survey technical reports.
  - Re-survey and validation processes maintained since 1990 to ensure data reliability and consistent classification alignment.

## Governance, metadata, and use

- Data provenance and standards:
  - Longitudinal time series with historical continuity (from 1978 to present) enabling trend detection across GB and its constituent countries.
  - Metadata and classifications tied to established UK biodiversity and land classification frameworks (ITE Land Classification, JNCC habitat classifications).
- Accessibility and context:
  - Countryside Survey website provides project overview, methodological documents, and links to supporting materials; dataset specifics (plots and species lists) are released as structured CSV files with detailed field descriptions.
- Relevance for data leaders:
  - Demonstrates effective data system design: rolling, standardized data collection; robust QA and validation; clear metadata and taxonomic references; scalable to national and sub-national analyses.
  - Supports data co-ownership and cross-network collaboration through shared methodologies, harmonized classifications, and publicly documented processes.
  - Provides a rich, multi-scale, ecosystem-focused longitudinal dataset suitable for policy-relevant analyses and monitoring of natural capital and biodiversity indicators.