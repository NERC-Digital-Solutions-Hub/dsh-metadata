# Countryside Survey

## Overview
- A long-running study auditing the natural resources of the UK's countryside, conducted since 1978, enabling comparisons across surveys to detect gradual changes.
- In 2019, moved to a rolling monitoring program (UKCEH-CS) designed to sample repeatedly on a five-year cycle across 500 randomly selected 1km squares, with 100 squares surveyed per year.
- The rolling design prioritizes long-term time series by starting from the 256 squares surveyed in 1978, then adding squares first surveyed in 1990 to extend the time series.
- Squares are stratified by the Land Classification of Great Britain and exclude squares with more than 75% urban land or more than 90% sea.

## Design and Methods
- Multi-metric, ecosystem-based approach: aims to collect and integrate soil, vegetation, rivers/headwaters, habitats, and landscape features across scales.
- In each 1km square, five plots are recorded, focusing on soils and vegetation.
- Data collected by trained field surveyors following standardized protocols; all fieldwork preceded by intensive training to ensure consistency.
- Quality assurance includes re-surveying 10% of plots by a QA assessor; consistent QA across surveys since 1990.
- Independent validation checks place locations and map plots to JNCC broad and priority habitat classifications.
- A map (Figure 1) shows 2019 1km square distribution at a coarse 10km scale to protect data confidentiality.

## Data and Files (2019 Vegetation)
- Two main data files:
  - UKCEHCS_VEGETATION_PLOTS_2019.csv: plot-level information
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2019.csv: species observed in each plot
- Vegetation Plot - Plot Information (selected columns):
  - YEAR, SQUARE_ID (1km square), PLOT_ID, PLOT_TYPE (plot type), PLOT_BH (Broad Habitat classification), PLOT_PH (Priority Habitat classification), COUNTRY (ENG/SCO/WAL), COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07_NUM (Land Classification 2007)
- Vegetation Plot - Species List (selected fields):
  - YEAR, SQUARE_ID, PLOT_ID, BRC_NUMBER (species identifier), BRC_NAMES (species name), NEST_LEVEL (nesting information for plots when relevant)
  - Species nomenclature follows Stace (1997)
  - Additional fields capture cover and related metrics (with coding for total cover and percentage cover)
- Species data are structured to support robust community analyses and cross-plot comparisons, with nest-level data included for larger plots where nests may occur.

## Scope and Aim for Analysts
- Purpose: to provide robust national and sub-national indicators of countryside vegetation and habitat change, enabling analysis of size, location, causes, and consequences of change.
- Rolling program enables year-on-year monitoring while maintaining long-term time series, supporting trend detection and policy-relevant insights.
- Data are designed to be interoperable with broader habitat classifications (e.g., JNCC) and linked to established land classifications and biodiversity frameworks.

## Practical Considerations and Challenges
- The rolling design buffers against climate-year extremes and maximizes site coverage across GB.
- Data collection relies on standardized field methods and ongoing QA to ensure comparability over time.
- Access to the full dataset requires attention to metadata (e.g., field handbook references Smart et al., 2019) and alignment with accompanying documentation.
- The collection emphasizes vegetation and soil measures within 1km squares, which may influence the granularity of local-scale inferences.

## References and Further Reading
- Key methodological and contextual references include work on the ITE Land Classification, Biodiversity Habitat classifications, UK Biodiversity Action Plan descriptors, and prior Countryside Survey reports (e.g., 2007 UK results, 2012 stock-change measures, and methodological statistics reports).
- Foundational field methods and data handling are documented in the UK-SCAPE Field Survey Field Handbook (2019) and related statistical reports (e.g., Scott 2008; Norton et al. 2012).