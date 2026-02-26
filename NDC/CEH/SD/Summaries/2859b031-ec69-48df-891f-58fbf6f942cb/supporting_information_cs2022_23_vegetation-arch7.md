# Countryside Survey vegetation species, recorded from plots in 2022 and 2023

- The Countryside Survey is a rolling, long-term program (since 2019) to monitor UK countryside; the 2022–2023 dataset focuses on vegetation plots within a rolling 1 km square framework to support ecosystem-scale analysis and map-based visualisations.
- Aims to detect temporal and spatial changes in soils, vegetation, habitats and landscape features by linking multiple metrics collected in the same locations.

## Design and rolling program

- Rolling five-year cycle: 500 x 1 km squares surveyed per cycle; approximately 100 squares visited each year.
- Squares are stratified by the Land Classification of Great Britain (ITE/Bunce et al., 2007) to ensure national and subnational indicators.
- Core long-time-series squares from 1978 (256 squares) remain in the rolling program; additional squares were added beginning with those first surveyed in 1990.
- Exclusions: any square with more than 75% urban land or more than 90% sea (per LCM2007 and census high-tide data) is excluded.
- First cycle dates from 2019; aims to maximise site coverage and detect year-on-year variation.

## Sampling and data collection

- Data collected by trained field surveyors following standard protocols (Smart et al., 2020); intensive pre-survey training to ensure consistency.
- Field teams include botanists; supervision and later monitoring by project staff to ensure data quality.
- 10% of plots re-surveyed for quality assurance; independent validation of plot locations and habitat classification (JNCC broad and priority habitats) maintained since 1990.
- Spatial distribution reference maps (e.g., 2022–2023) accompany the dataset.

## Data files and structure

- Two CSV data files for 2022–23:
  - UKCEHCS_VEGETATION_PLOTS_2022_23.csv
    - Plot-level information: YEAR, SQUARE_ID (1 km square ID), PLOT_ID, PLOT_TYPE, area descriptors (X, XX), PLOT_BH (BAP Broad Habitat), PLOT_PH (BAP Priority Habitat), COUNTRY (ENG/SCO/WAL), COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07 (Land Classification code), LC07_NUM.
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2022_23.csv
    - Species per plot: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, Species name, Species identifier (BRC_NAMES), Nest-related fields (first recorded, NEST_LEVEL), and cover metrics (ZERO_COVER, FIRST_COVER, TOTAL_COVER).
    - Notes: nest counts differ by plot size (larger plots 200 m2 may have 0–1 nests; 2 m x 2 m plots have 1 nest). Nomenclature follows Stace (1997).
- Plot-level fields include habitat and land-class identifiers; species-level fields include abundance by cover and nest information.

## Data quality, standards and interpretation

- Standardised field methods and field handbook guidance (Smart et al., 2020) underpin data consistency across surveys.
- Quality Assurance ongoing since 1990; independent validation supports reliability of plot locations and habitat assignments.
- Terminology and classifications align with established UK biodiversity and habitat frameworks (JNCC Broad/Priority Habitats, Land Classification).
- Data are designed for integration into map-based products; suitable for visualising spatial patterns of vegetation across GB at the 1 km square scale and for linking with habitat and land-class layers.

## Using the data for GIS and mapping

- Spatial granularity is at 1 km squares with plot-level vegetation data; suitable for national and subnational map products.
- Can be joined with environmental zones, land classification, and habitat classifications to produce thematic maps of vegetation structure, species richness, and habitat associations.
- Data from England, Scotland, and Wales; supports cross-border comparisons and policy-relevant indicators.
- Important to account for rolling, multi-year design when interpreting trends; some time-series context is provided by the long-running 1978–present framework.

## References and further reading

- Smart et al., 2020. UK-SCAPE Field Survey Field Handbook 2020 Vegetation Plots (UK CEH).
- Bunce et al., 2007. ITE Land Classification of Great Britain.
- Stace, C. 1997. New Flora of the British Isles.
- Additional methodology and background: Countryside Survey project documentation and related technical reports (e.g., Scott 2008; Norton et al. 2012).