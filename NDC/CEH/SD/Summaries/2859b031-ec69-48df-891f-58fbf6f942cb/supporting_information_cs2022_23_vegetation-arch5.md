# Countryside Survey vegetation species, recorded from plots in 2022 and 2023

## Overview
- Countryside Survey is a long-running national study of the UK's countryside, conducted at intervals since 1978, with a rolling monitoring program since 2019 (UKCEH-CS).
- The project uses a multi-metric, ecosystem-based design to measure soils, vegetation, streams, habitats, and landscape features.
- A rolling program repeats sampling across 500 randomly selected 1km squares over a five-year cycle (roughly 100 squares per year) to balance spatial coverage and temporal change detection.
- Squares are chosen via stratified sampling based on the Land Classification of Great Britain; exclusions apply for squares that are >75% urban or >90% sea.

## Data collection and design
- Data collected by trained field surveyors following standard protocols (Smart et al., 2020) with intensive pre-field training to ensure consistency.
- Field teams are supervised during surveys and are subjected to quality assurance checks; 10% of plots are re-surveyed by QA assessors.
- QA is conducted by the same assessor for each survey since 1990, enabling reliable assessment of detection rates and validation of plot locations and habitat classifications (JNCC broad and priority habitats).
- The 2019 onwards rolling program allows repeated sampling to detect spatial variation and temporal trends.

## Data files and structure
- Two CSV files constitute the dataset:
  - UKCEHCS_VEGETATION_PLOTS_2022_23.csv (Vegetation Plot Information)
    - Key columns include: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, PLOT_BH, PLOT_PH, COUNTRY, COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07, LC07_NUM, etc.
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2022_23.csv (Vegetation Plot Species List)
    - Key columns include: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, SPECIES_NAME, BRC_NAMES, NEST_LEVEL, ZERO_COVER, FIRST_COVER, TOTAL_COVER, etc.
- Species nomenclature follows Stace (1997): New flora of the British Isles.
- Plot metadata includes habitat classifications (BAP Broad Habitat, Priority Habitat) and Land Classification details (LC07 and LC07_NUM).

## Methods and quality assurance
- Fieldwork follows the UK-SCAPE/CS Field Survey Field Handbook (2020) with standardized plots and nest data handling for larger and smaller plots.
- A QA assessor validates a subset of plots (10%) and maintains consistency across surveys since 1990.
- Data are aligned with established classifications and taxonomies (e.g., LC07, BAP habitats, JNCC broad habitats) to support interoperability and comparability with historic data.

## Design rationale and coverage
- The original five-point per 1km square approach has evolved into a rolling program to maximize site visits and detect year-on-year changes while buffering against climate variability.
- The initial 1978 square set (256 squares) remains part of the rolling program due to their long time-series value; additional squares from earlier surveys (1990 cohort) are included to extend the time series.
- The nationwide sampling is stratified by Land Classification, with urban-sea exclusions applied to maintain a landscape-representative sample.

## Data governance and provenance
- Data are produced under the Countryside Survey program led by UKCEH, with documented sampling design, field methodologies, and QA procedures.
- Versioning and longitudinal integrity are supported by consistent QA practices and linkage to established habitat and land-classification frameworks.
- Documentation and references accompany the dataset to support auditability and reproducibility (e.g., Smart et al., 2020; Bunce et al., 2007; Scott, 2008).

## Use considerations and limitations
- Data are designed for national and subnational indicators of vegetation and habitat change; nomenclature and classifications follow standardized references.
- Users should be aware of potential data gaps or limitations inherent in field surveys (e.g., nested plot structures, detection limits) and the rolling design that emphasizes repeat sampling over fixed-interval snapshots.

## References and further reading
- Key sources include: Bunce et al. (1996, 2007) on Land Classification; Jackson (2000) on Biodiversity Broad Habitat classification; Maddock (2008) UK BAP habitat descriptions; Scott (2008) CS Technical Report; Smart et al. (2020) UK-SCAPE Field Survey Field Handbook; Stace (1997) New flora of the British Isles; and associated Countryside Survey project documentation.