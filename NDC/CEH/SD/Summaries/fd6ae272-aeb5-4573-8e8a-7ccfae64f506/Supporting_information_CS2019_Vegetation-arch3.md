# Countryside Survey

- Background and aim
  - Long-running UK countryside audit (since 1978) to monitor natural resources and detect gradual changes over time.
  - Rolling program adopted in 2019 to enable periodic, comparable monitoring across multiple measures (soil, vegetation, streams, habitats, landscape features) and to withstand climate variability.
  - Designed for an ecosystem-based, multi-scale approach with data collected in the same locations where possible.

- Design and rolling program
  - Rolling five-year cycle surveying 500 x 1km squares, with 100 squares visited annually.
  - Sample selection stratified by the Land Classification of Great Britain; prioritizes squares with the longest time series by including the 1978 set and additions from 1990.
  - Exclusions: squares with >75% urban land or >90% sea.
  - Rationale: maximize site coverage, ensure robust national and sub-national indicators, and detect spatial and temporal changes cost-effectively.

- Methods and quality assurance
  - Data collected by trained field surveyors following standard protocols (Smart et al., 2019).
  - Intensive initial training; field teams supervised and later monitored to maintain data quality.
  - 10% of plots re-surveyed for quality assurance; QA conducted by the same assessor since 1990.
  - Independent validation of plot locations and habitat classification against JNCC broad and priority habitat classifications.

- Data products and structure (Vegetation data, 2019)
  - Two CSV files:
    - Vegetation Plot – Plot Information: includes YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, Broad Habitat (BAP), Priority Habitat, country (England, Scotland, Wales), county, environmental zone, land classification (LC07), and related codes.
    - Vegetation Plot – Species List: lists species recorded in each plot with species identifiers and names, nest level data, and cover metrics (e.g., FIRST_COVER, TOTAL_COVER).
  - Species nomenclature follows Stace (1997); documentation references include Smart et al. (2019) field handbook.
  - Large plots contain multiple nests; field data include various ecological metrics and classifications.

- Metadata, documentation, and access
  - Detailed methodologies and field protocols documented in the UK-SCAPE Field Survey Field Handbook (2019) and related CEH documentation.
  - Data referenced and accessible via the Countryside Survey and UKCEH resources; extensive references to supporting methodological literature.

- Policy relevance and outputs
  - Measures stock and change in GB countryside; supports policy development and monitoring of biodiversity and landscape indicators.
  - Key outputs and methodological foundations cited in policy-relevant analyses (e.g., Norton et al., 2012; Carey et al., 2008; Scott, 2008).

- Key challenges and governance considerations for monitoring authors
  - Data gaps and gaps in metadata can hinder rapid verification and use.
  - Ensuring timely access and avoiding data silos through integrated, well-documented workflows.
  - Public sharing of underlying data balanced with governance and data-management standards.
  - Transformation of data into usable formats and clear communication of complex findings.
  - Ongoing data governance to maintain quality, openness, and up-to-date datasets.

- Datasets (summary)
  - UKCEHCS_VEGETATION_PLOTS_2019.csv: plot-level information (YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, habitat classifications, location, LC07, ENV_ZONE_2007, etc.).
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2019.csv: species records per plot (species identifier, species name, nest level, cover metrics, etc.).
  - Nomenclature and coding references provided in accompanying documentation and Smart et al. (2019).