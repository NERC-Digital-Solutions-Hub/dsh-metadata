# Woodlands Survey soil data 1971-2001

## Overview
- Longitudinal ecological dataset from 103 broadleaved woodlands in Britain. Initial survey in 1971 recorded site- and plot-level data, with 16 plots per site sampled randomly. Re-surveyed in 2000–2003 (referred to as 2001) using the same methods to assess ecological change.
- Focus on soil pH and Soil Organic Matter (SOM), plus soil classifications (Major Soil Group, Soil Group, Soil Sub-group) and a wide set of site/plot descriptors.
- Analyses aimed to identify drivers of change, including atmospheric deposition of sulfur and nitrogen, climate, canopy changes, and woodland management.
- Key results published in Kirby et al. (2005) and Corney et al. (2004); the dataset’s field methods and analytic context are detailed in those works.

## Data structure and content
- Data organized by Site (code 1–103) and Plot (1–16 per site).
- Core numeric variables:
  - pH1971, pH2003 (soil pH in 1971 and in the 2000s)
  - SOM1971, SOM2003 (soil organic matter content in 1971 and in the 2000s)
  - QA repeats (repeat pH measurements and repeat SOM measurements on archived samples)
  - SOM1971_QArepeats (repeat SOM measurements)
  - MSG (Major Soil Group code), SG (Soil Group code), SSG (Soil Sub-group code)
- Categorical/text variables:
  - Major_Soil_Group, Soil_Group, Soil_subgroup (descriptions)
- Coding framework follows Avery (1973) soil classifications; numeric codes accompany textual descriptions.

## Survey design and methods
- Stratified sampling across the study area.
- Field methods aligned with Bunce & Shaw (1973) standardized survey methods.
- Field handbook and supporting documentation available to guide data collection.

## Provenance and related datasets
- Originators (1971): R.G.H. Bunce & M.W. Shaw, Woodland Ecology Section, Nature Conservancy – Merlewood.
- Data collection (2001–2003): Simon Smart, Helaina Black (CEH Lancaster); Kirby (English Nature); Phil Corney (University of Liverpool).
- Related datasets: Countryside Survey; Steele (1968) National Survey of Woodlands.
- References for context and methodology include Avery (1973), Corney et al. (2004), Haines-Young et al. (2003), Kirby et al. (2005).

## Access and usage notes
- Dataset described with a clear data structure and metadata; analytical context and field methods are detailed in the cited publications.
- DOI/link provided for the dataset; users should consult Kirby et al. (2005) and Corney et al. (2004) for results and methodological details.
- Designed for long-term ecological change analysis and cross-time comparisons, with explicit QA measures and standardized coding.

## Reuse and implications for data leadership
- Demonstrates robust, long-term data collection with consistent methods enabling strong change analysis across decades.
- Highlights the importance of rich metadata, standardized classifications (Avery soil taxonomy), QA/repeats, and clear data provenance to support discoverability and reuse.
- Suitable for integration with related datasets and cross-site synthesis to understand environmental drivers of woodland soil change.
- Supports data governance practices around data lineage, documentation, and stewardship across evolving research networks.