# Countryside Survey

- A rolling nationwide monitoring program (UKCEH-Countryside Survey) that repeats a five-year cycle across 500 randomly selected 1km squares to track long-term changes in soils, vegetation, and related habitat features.
- The design prioritizes robust national and subnational indicators with long time series, enabling year-to-year and cross-cycle comparisons while buffering against extreme climate years.

## Survey Design and Rolling Programme

- Rolling program adopted in 2019; five-year cycles with ~500 squares total, ~100 visited per year.
- Squares are stratified by the Land Classification of Great Britain to ensure representative sampling across topography, geology, climate, and landscape attributes.
- Original 1978 squares (256) are retained for the longest time series; additional squares added from earlier surveys to maintain continuity.
- Exclusions: squares with >75% urban land or >90% sea are removed from the sample.
- Design supports an ecosystem-based approach by capturing multiple metrics (soil, vegetation, headwater streams, habitats) in a coordinated manner and at multiple scales where possible.

## Data Collection and Quality Assurance

- Data collected by trained botanical surveyors following standardized protocols (Smart et al., 2020) with rigorous field handbook criteria.
- Field teams receive intensive training; supervision during surveys; 10% of plots re-surveyed for quality assurance.
- Independent validation of plot locations and their broader habitat classification to ensure data accuracy and consistency across years (since 1990 QA is conducted by the same assessor).
- Data are prepared to enable re-use and self-service analysis for end users (e.g., dashboards, reports, charts) with guidance on interpretation.

## Data Files and Metadata (Vegetation Plots 2022-2023)

- Two CSV files comprise the dataset:
  - UKCEHCS_VEGETATION_PLOTS_2022_23.csv: Plot-level information (year, square ID, plot ID, plot type, area measurements, habitat classifications, country, county, environment zones, land classification, etc.).
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2022_23.csv: Species-level data for each plot (species name and identifier, nest information, cover percentages for multiple nest layers, total cover; nomenclature follows Stace, 1997).
- Example key fields:
  - Plot file: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, X/XX area, PLOT_BH, PLOT_PH, COUNTRY, COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07, LC07_NUM.
  - Species file: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, Species name, BRC_NAMES, NEST_LEVEL, ZERO_COVER, FIRST_COVER, TOTAL_COVER.
- Nomenclature and references underpinning data: species names follow Stace (1997); related methodologies and habitat classifications documented in Bunce et al., Jackson (2000), Maddock (2008), and UK-SCAPE field handbook (Smart et al., 2020).

## Nomenclature, Methodology, and References

- Field methods and field handbook: UK-SCAPE Field Survey Field Handbook 2020 (Vegetation Plots) and Smart et al. (2020).
- Habitat classification and land classification frameworks referenced (JNCC habitat classifications; ITE Land Classification of Great Britain 2007).
- Key policy and biodiversity references informing interpretation of land cover and habitats (UK Biodiversity Action Plan descriptions).
- Links to Countryside Survey website and data centre for project documentation and data access.

## Implications for Data Support

- Produces a long-running, standardized dataset suitable for trend analysis, policy-relevant reporting, and cross-year comparisons.
- QA processes and independent validation enhance trustworthiness and reproducibility for data consumers.
- Data come in analysis-ready formats with clear metadata and documented nomenclature, facilitating integration with other datasets and dashboards.
- The rolling design and stratified sampling support robust estimates at national and subnational scales, with transparency about methodology and data provenance.