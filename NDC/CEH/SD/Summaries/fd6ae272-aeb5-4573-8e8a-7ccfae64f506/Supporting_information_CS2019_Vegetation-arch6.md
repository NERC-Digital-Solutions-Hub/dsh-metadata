# Countryside Survey

- A long-running national study of the UK countryside’s natural resources, conducted to compare results over time and detect gradual changes in soils, vegetation, streams, habitats, and landscape features.
- Rolling program introduced in 2019 to monitor ecosystem components across multiple scales with year-on-year and long-term comparability.

## Design and rolling program

- Rolling program repeats every five-year cycle or after 500 1km squares are surveyed; first cycle started in 2019.
- Sampling uses 500 randomly selected 1km squares per cycle, stratified by the Land Classification of Great Britain to ensure robust national and sub-national indicators.
- The 1978 set of 256 squares forms the backbone for the longest time series; additional squares from 1990 onward extend the history.
- Annual work includes visits to 100 squares to balance temporal and spatial coverage.
- Exclusions: squares with >75% urban land or >90% sea are excluded.

## Methods and data quality

- Data collection follows standard protocols (Smart et al., 2019) with trained field surveyors and intensive pre-survey training to ensure consistency.
- Surveys are supervised, with ongoing monitoring by project staff; 10% of plots are re-surveyed for quality assurance.
- QA processes provide independent validation of plot locations and their assignment to habitat classifications (JNCC broad and priority habitats).
- The design captures multiple metrics (soil, vegetation, habitats) to enable integrated, ecosystem-based analyses across scales.

## Outputs and data products

- Outputs include vegetation plot data and species lists suitable for analysis, dashboards, or self-serve exploration.
- Outputs support policy-relevant reporting and trend detection over time.

## Data files and structure (2019 vegetation data)

- Two CSV files comprise the 2019 vegetation data:
  - UKCEHCS_VEGETATION_PLOTS_2019.csv
    - Contains plot-level information: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, PLOT_BH, PLOT_PH, COUNTRY, COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07_NUM, and related habitat/land-class fields.
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2019.csv
    - Contains species-level data per plot: YEAR, SQUARE_ID, PLOT_ID, BRC_NUMBER, BRC_NAMES, NEST_LEVEL, and cover metrics (TOTAL_COVER, FIRST_COVER, etc.).
- Species nomenclature follows Stace (1997); data include nest information for larger plots and cover percentages.
- Data collection is tied to the field handbook (Smart et al., 2019) and includes plot-level and species-level detail for 2019.

## Context and references

- Supports long-term trend analysis and policy-oriented assessments of GB countryside stock and change (e.g., 2007 UK results and related publications).
- Key methodological and classification references include:
  - Countryside Survey design and methodology (Bunce et al.; Scott 2008; Bunce et al., 2007 Land Classification)
  - Field handbook (Smart et al., 2019)
  - Biodiversity classifications and habitat descriptions (Jackson 2000; Maddock 2008)
  - Related statistical and management reports (Carey et al., 2008; Norton et al., 2012; Scott 2008)
- Data are distributed with documentation and links via the Countryside Survey program, supporting robust, comparable national and sub-national indicators.