# Countryside Survey

## Overview
- Countryside Survey is a long-running UK study (since 1978) auditing natural resources to detect changes over time.
- The project uses a rolling program (adopted in 2019) to monitor soil and vegetation across roughly 500 1km squares on a five-year cycle.
- Starting in 2024, the survey adds plots along linear landscape features (boundary, roadside, streamside, hedgerow) and samples soil in these plots using standard adjacent-field methods.
- The aim is to enable spatially explicit, time-series indicators at national and subnational scales, supporting policy and planning analyses.

## Rolling programme and design
- The rolling cycle repeats every five years, visiting about 500 squares to balance site coverage and temporal monitoring.
- First cycle began in 2019; 2024 marks the start of the second cycle.
- Squares are randomly selected and stratified by the Land Classification of Great Britain (ITE land classes) to reflect landscape diversity.
- Approximately 100 squares are visited each year.
- Exclusions: squares with more than 75% urban land or more than 90% sea are removed from sampling.

## Sampling frame and geographic scope
- The sample comprises 500 one-kilometer squares across Great Britain (England, Scotland, Wales).
- The initial 256 squares from 1978 are retained for continuity of long-term records; additional squares were added based on earlier survey coverage (starting 1990) to extend the time series.
- The Land Classification framework ensures robust national and subnational estimates for soils, vegetation, habitats, and landscape features.

## Data collection and quality assurance
- Field surveys are performed by trained botanical surveyors following standardized protocols (field handbook and methodologies published by Smart et al., 2024).
- Teams receive intensive pre-survey training; supervision and monitoring are used to maintain data quality.
- 10% of plots are re-surveyed for quality assurance, with independent validation of plot locations and habitat classifications since 1990.
- An independent QA assessor provides consistent validation across survey years.

## Data products (2024 vegetation plots)
- Two main CSV files are available:
  - UKCEHCS_VEGETATION_PLOTS_2024.csv: Plot-level information including year, square ID, plot type, plot ID, land classification codes, environmental zones, country, county, habitat classifications, vegetation structure (trees, canopy/shrub height), and plot-specific measurements (e.g., boundary, roadside, streamside, hedgerow plot fields).
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2024.csv: Species list per plot with species identifiers, nest/cover details, percent cover totals, and notes on recording conventions.
- Example key fields (Vegetation Plots file):
  - YEAR, SQUARE_ID, PLOT_TYPE (B, H, R, S), PLOT_ID
  - LC07, LC07_NUM (ITE Land Classification)
  - ENV_ZONE_2007, EZ_DESC_07 (Environmental Zones)
  - COUNTRY, COUNTY
  - PLOT_BH, PLOT_PH (Broad/Priority Habitats)
  - TREES, TREES_DEAD, TREE_DISEASE
  - CANOPY_HT, SHRUB_HT
  - Plot-specific modular fields for boundary, hedgerow, roadside, streamside plots
- Example key fields (Species list file):
  - YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE
  - BRC_NUMBER, BRC_NAMES (species identifiers and names)
  - NEST_LEVEL, ZERO_COVER, FIRST_COVER, TOTAL_COVER (cover metrics)

## Relationship to classifications and datasets
- Links to ITE Land Classification (Bunce et al., 1996; 2007) for the stratified sampling framework.
- Uses Biodiversity Broad Habitat and Priority Habitat concepts (PLOT_BH, PLOT_PH; Jackson 2000; Maddock 2008).
- Methodology and field protocols align with Countryside Survey publications (Carey et al. 2008; Norton et al. 2012; Scott 2008; Smart et al. 2024).

## GIS relevance and usage
- Delivers spatially explicit, time-series data suitable for map-based visualization of vegetation, habitats, and landscape features at 1km square resolution.
- The 2024 dataset expands geographic coverage by including linear-feature plots and soil sampling within adjacent field plots, enabling richer spatial analyses of boundary hedgerow networks and hydrological features.
- Useful for policy briefing, landscape planning, biodiversity assessments, and monitoring change in soil and vegetation across GB.

## Access and references
- Field methods and data handling follow UKCEH Countryside Survey Field Handbook (2024–2029) and related methodological publications.
- Data products include detailed column definitions and relationships between the two CSV files; supplementary documentation provides further context on sampling design, environmental zones, and habitat classifications.