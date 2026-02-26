# Countryside Survey

- A long-running national study of the UK countryside, conducted since 1978, to track gradual environmental changes over time. Since 2019, it operates as a rolling monitoring program (UKCEH-CS) designed to detect year-to-year and longer-term spatial and temporal trends across soils, vegetation, headwater streams, habitats, and landscape features using a cohesive ecosystem-based approach.

- Aims and outputs
  - Capture multiple metrics and integrate them to answer questions about the size, location, causes, and consequences of change.
  - Produce robust indicators at national and sub-national scales to inform environmental health and policy performance.
  - Present results in clear formats and ensure datasets are stored and accessible for reuse and analysis.

- Design and rolling program
  - Rolling survey adopted to repeat approximately every five years or after surveying 500 squares, buffering results against climate variability and increasing site coverage.
  - First rolling cycle began in 2019.
  - Sampling uses 1km squares; a total of 500 squares are surveyed in each five-year cycle, with about 100 squares visited per year.
  - Squares are stratified by the Land Classification of Great Britain (ITE land classification) and exclude any square with more than 75% urban land or more than 90% sea (based on LCM2007 and census data).

- Sample selection and legacy
  - The 256 squares from 1978 remain part of the rolling program to provide the longest time-series data.
  - Additional squares are added from the next earliest survey years (1990) to broaden the time series and spatial coverage.
  - The sampling framework aims to deliver robust national and sub-national indicators for GB and its constituent countries.

- Data collection and quality assurance
  - Field data are collected by trained surveyors following standardized protocols (Smart et al., 2020) and field handbooks.
  - Teams receive intensive training to ensure consistent methodology and accurate recording across years.
  - Systematic quality assurance: around 10% of plots are re-surveyed by QA assessors; QA analyses have been conducted by the same assessor since 1990 to provide consistent validation of detection rates and plot localization within habitat classifications.
  - Surveys include supervision and ongoing monitoring by project staff to maintain high data quality and comparability across years.

- Outputs and visualization
  - Data are designed to support integrated analyses across soils, vegetation, habitats, and landscape features at multiple scales.
  - Outputs are typically presented as reports, maps, and charts, with ongoing emphasis on comparability across years to detect change.

- Datasets described ( vegetation plots for 2020–2021 )
  - Two CSV files comprise the vegetation data:
    - UKCEHCS_VEGETATION_PLOTS_2020_21.csv (Plot Information)
      - Key columns include: YEAR, SQUARE_ID (1km square), PLOT_ID, PLOT_TYPE, X/XX (plot area), PLOT_BH (BAP Broad Habitat), PLOT_PH (BAP Priority Habitat), COUNTRY (England/Scotland/Wales), COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07, LC07_NUM, and related land classification fields.
      - Captures information about plot location, plot type, location attributes, and environmental classifications.
    - UKCEHCS_VEGETATION_PLOT_SPECIES_2020_21.csv (Species List)
      - Includes YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, BRC_NUMBER (species identifier), nest-related fields (for nests in plots), cover metrics (ZERO_COVER, FIRST_COVER, TOTAL_COVER), and related species data.
      - Species nomenclature follows Stace, 1997 (New flora of the British Isles).
  - Data are collected following the UK-SCAPE/CS field survey handbook (2020) and are aligned with standard taxonomic references and habitat classifications (e.g., JNCC/broad habitat classifications; BAP habitat concepts).

- Reference framework and supporting documentation
  - Methodology and classifications draw on a broad set of sources, including:
    - Countryside Survey design, land classification (ITE), and habitat classifications.
    - UK-SCAPE Field Survey Field Handbook (2020) for vegetation plots.
    - Foundational studies and reports detailing the rolling program, statistical approaches, and historical context (e.g., Scott 2008; Carey et al. 2008; Norton et al. 2012; Jackson 2000; Maddock 2008; Stace 1997).
  - The dataset and methods are supported by a series of technical and reference documents that provide the rationale for sampling, QA procedures, and data interpretation.

- Visual and mapping notes
  - Visuals include distribution maps of 1km survey squares across Great Britain for 2020–2021, with data confidentiality considerations.
  - The design emphasizes spatial coverage and repeatability to enable detection of regional and national trends over time.