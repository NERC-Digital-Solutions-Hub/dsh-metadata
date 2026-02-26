# Introduction to the Countryside Survey Design and the rolling program

- Overview
  - Countryside Survey is a long-running audit of the UK's countryside, enabling comparisons over time to detect gradual changes in soils, vegetation, streams, habitats, and landscape features.
  - Since 2019, a rolling program (UKCEH-CS) repeats surveys on a five-year cycle across 500 randomly selected 1km squares to monitor year-on-year changes while buffering against climate variation.
  - The program aims to provide robust national and subnational indicators for GB and its constituent countries.

- Design and sampling framework
  - The rolling sample comprises 500 x 1km squares over five years, stratified by the ITE Merlewood Land Classification (Land Classification of Great Britain, 2007).
  - Approximately 100 squares are surveyed each year.
  - Exclusions: squares with more than 75% urban land or more than 90% sea (based on LCM2007 and Census data).
  - The design preserves a long-running core from 1978 (256 squares) to maintain the longest possible time series; additional squares first surveyed in 1990 are included to extend coverage.

- Data collection and quality assurance
  - Field surveys are conducted by trained botanical surveyors following standard protocols (Smart et al., 2020) and field handbooks.
  - Teams receive intensive training; surveys are supervised and later monitored to ensure consistency and data quality.
  - About 10% of plots are re-surveyed for quality assurance; QA has been conducted by the same assessor since 1990, enabling validation of detection rates, plot locations, and habitat classification.

- Data products and structure
  - Vegetation data are organized into two CSV files:
    - Vegetation plots: plot-level information including year, square ID, plot ID, plot type, location data, habitat classifications (BAP Broad Habitat and Priority Habitat), country, county, and land classifications (environmental zones, LC07 and LC07_NUM).
    - Species list: species recorded per plot with nest information, cover percentages for multiple nests, and total cover; species nomenclature follows Stace (1997).
  - Key coding and classifications include BAP broad and priority habitats (Maddock, 2008), and the Land Classification of GB 2007.
  - The dataset covers plots from 2022 and 2023, with structure designed to support national and subnational analyses of vegetation composition and habitat associations.

- Methodological foundations and references
  - Field methodologies and data standards are outlined in Smart et al. (2020) UK-SCAPE Field Survey Field Handbook (Vegetation Plots).
  - Core classifications rely on Bunce et al. (2007) for the ITE Land Classification of Great Britain, Jackson (2000) for Biodiversity Broad Habitat guidance, and Stace (1997) for plant nomenclature.
  - Supportive reports and analyses include Scott (2008) on statistical methods, Carey et al. (2008) UK results, Norton et al. (2012) on measuring countryside stock and change.

- Purpose and potential uses for analysts
  - Provides multi-metric, ecosystem-scale data enabling analysis of size, location, causes, and consequences of change across soils, vegetation, headwater streams, habitats, and landscape features.
  - Supports development of predictive insights and policy-relevant indicators at national and subnational scales.
  - Data are designed to be discoverable and usable, with metadata and documentation linked to the Countryside Survey portal and related publications.

- Access, provenance, and documentation
  - Data are collected under standardized protocols with documented quality assurance and validation processes.
  - Metadata and field handbooks underpin reproducibility; data provenance is tracked to ensure traceability across survey cycles.
  - Related documentation and datasets are linked via the Countryside Survey program and CEH resources.

- Notable limitations and considerations for analysis
  - Rolling design mitigates some climate-year noise but still requires careful treatment of temporal and spatial autocorrelation.
  - Long-running time series (starting from 1978) enable trend detection but may involve changes in methods over time; cross-cycle consistency is maintained through standardized protocols and QA.
  - Integrating with other datasets (e.g., administrative boundaries) may require harmonization given the use of multiple classifications (LC07, environmental zones, habitat classifications).