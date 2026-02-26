# Countryside Survey vegetation species, recorded from plots in 2020 and 2021

- Background and purpose
  - Countryside Survey is a long-running UK audit of natural resources, with a rolling monitoring program adopted in 2019 (UKCEH-CS) to allow comparisons over time and across space.
  - The project captures multiple measures (soil, vegetation, habitats, landscapes) to assess size, location, causes, and consequences of change in the countryside.
  - The 2020–2021 data continue the rolling program, focusing on soil and vegetation in 1 km squares, enabling national and sub-national indicators across GB.

- Design and rolling programme
  - Five-year cycle surveying 500 randomly selected 1 km squares, stratified by the Land Classification of Great Britain.
  - About 100 squares are visited each year; the sampling builds on the 1978 set (256 squares) and additional squares from 1990 to maximise a long time series.
  - Exclusions: squares with >75% urban land or >90% sea are removed from selection.

- Methods and data quality
  - Field data collected by trained surveyors using standardized protocols; comprehensive training and supervision to ensure consistency.
  - 10% of plots re-surveyed for quality assurance; QA has been conducted by the same assessor since 1990, enabling independent validation of plot locations and habitat classifications.
  - The design supports detection of year-to-year change and spatial variation while buffering against climate extremes.

- Data files and contents (2020–2021)
  - Two CSV files:
    - UKCEHCS_VEGETATION_PLOTS_2020_21.csv: Plot-level information
      - Key fields: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, X, XX, PLOT_BH (BAP Broad Habitat), PLOT_PH (BAP Priority Habitat), COUNTRY, COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07, LC07_NUM
    - UKCEHCS_VEGETATION_PLOT_SPECIES_2020_21.csv: Species list per plot
      - Key fields: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, BRC_NUMBER (species identifier), NEST_LEVEL, COVER metrics (e.g., ZERO_COVER, FIRST_COVER, TOTAL_COVER), with nomenclature following Stace (1997)
  - Data description notes
    - Nomenclature follows Stace (1997); plots include nested nest and cover information for vegetation diagnostics.
    - The dataset covers surveys conducted in 2020 and 2021 across England, Scotland, and Wales.
  - Spatial and ecological context
    - Environmental zones and land classifications accompany plot data to enable habitat and landscape-level analyses.
    - Descriptions align with ITE Land Classification and JNCC Broad/Priority Habitat frameworks.

- Practical context and references
  - The Countryside Survey design and methodology are documented in supporting literature and field handbooks (e.g., Smart et al. 2020; Scott 2008; Bunce et al. 2007; Jackson 2000; Maddock 2008; Stace 1997).
  - The 2020–2021 vegetation data support national and regional change assessments, policy-relevant stock and trend analyses, and monitoring of plant diversity as part of broader ecological monitoring.

- Notes on data access and limitations
  - The rolling program is designed to maximize site coverage and temporal depth, but data collection can be affected by scale, access, and standardisation challenges typical of large-scale national surveys.
  - Data are accompanied by metadata and methodological documentation to aid replicability and reuse in analyses and modelling.