# Countryside Survey

## Overview and purpose
- Long-running audit of the UK countryside, conducted since 1978, designed to detect gradual changes over time by comparing results across surveys.
- UKCEH Countryside Survey (CS) adopted a rolling monitoring program in 2019 to repeat data collection every five years across 500 1km squares, enabling both spatial and temporal trend analysis.
- The design integrates multiple measures (soil, vegetation, habitats, landscape features) to support an ecosystem-based understanding of change at national and sub-national scales.

## Rolling program and sampling design
- Rolling program: 5-year cycle or 500 squares total; first cycle began in 2019.
- Sampling framework: 500 x 1km squares randomly selected, stratified by the Land Classification of Great Britain (ITE method).
- Sampling history: 1978 baseline of 256 squares retained for long time-series; additional squares added from earlier surveys (1990) to extend continuity.
- Annual fieldwork: 100 squares visited each year; squares excluded if >75% urban land or >90% sea.
- Objective: maximize site coverage and detect spatial variation and temporal trends cost-effectively.

## Data collection and quality assurance
- Field data collected by trained survey teams using standardized protocols (Smart et al., 2019 field handbook).
- Rigorous training, supervision, and ongoing quality control to ensure consistency across surveys.
- QA sampling: 10% of plots re-surveyed by an independent assessor; consistent validation of plot locations and habitat classifications (JNCC framework).
- Data linked to a robust spatial framework (1km squares) and to habitat classifications.

## Data products and file structure (vegetation data for 2019)
- Two CSV files produced for vegetation plots in 2019:
  - Vegetation Plot - Plot Information: metadata about plot location and type.
  - Vegetation Plot - Species List: species detected in each plot, with nesting information where applicable.
- Representative columns (examples):
  - Plot Information: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, PLOT_BH (Broad Habitat), PLOT_PH (Habitat Type), COUNTRY (ENG/SCO/WAL), COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07 (Land Classification), LC07_NUM.
  - Species List: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, BRC_NUMBER (species identifier), BRC_NAMES (species name), NEST_LEVEL, TOTAL_COVER, FIRST_COVER (percent), etc.
- Data standards and nomenclature:
  - Species nomenclature follows Stace (1997).
  - Habitat and land classifications follow ITE and JNCC frameworks referenced in the accompanying documentation.

## Geographic and data-structure context for GIS
- Spatial resolution: 1km squares with plots within each square; data designed for map-based visualization and analysis across GB.
- Spatial distribution visuals are used to protect confidentiality (e.g., 2019 distribution shown plotted at 10km for confidentiality).
- Rich attribute sets enable multi-layer GIS analyses, including:
  - Land Classification (LC07 and codes)
  - Environmental Zones (ENV_ZONE_2007)
  - Broad and Priority Habitat classifications (BAP)
  - Habitat descriptors and regional metadata (COUNTRY, COUNTY)
- Linking Plot and Species datasets allows map-based visualization of species distributions and plot-level environmental contexts.

## Methodological and data-use considerations
- Rolling design supports year-on-year monitoring but individual cycles focus on 5-year totals; temporal comparisons should align with the five-year cycle.
- The dataset emphasizes long-running time series for robust change detection, with attention to data quality and consistent field methodologies.
- Awareness of potential data gaps due to annual sampling distribution and square exclusions is important for GIS analyses.
- References and supporting materials provide methodological foundations (e.g., Smart et al., 2019; Bunce et al., 2007/1996; Jackson 2000; Stace 1997).

## References and further reading (illustrative)
- Smart et al., 2019: UK-SCAPE Field Survey Field Handbook (Vegetation Plots)
- Bunce et al., 2007: ITE Land Classification of Great Britain 2007
- Bunce et al., 1996; 1981: ITE Merlewood Land Classification groundwork
- Jackson, 2000; Maddock, 2008; Norton et al., 2012; Scott, 2008
- Carey et al., 2008; Scott, 2008: Countryside Survey outputs and methodologies
- Stace, 1997: New flora of the British Isles

## Practical takeaways for GIS specialists
- Use 1km square grid and plot-level attributes to create scalable, map-ready products showing habitat types, land classification, and environmental zones.
- Integrate plot-level species data with environmental classifications to model species-habitat relationships and track changes over successive survey cycles.
- Leverage the QA framework (10% re-survey data) to quantify uncertainty and reliability in spatial analyses.
- Plan for time-series analyses by aligning GIS workflows with the rolling five-year cycle and the available 2019 vegetation plot data coupled with the supporting metadata.