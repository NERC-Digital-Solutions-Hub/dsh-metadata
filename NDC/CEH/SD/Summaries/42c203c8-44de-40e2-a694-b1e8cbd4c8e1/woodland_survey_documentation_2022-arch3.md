# Bunce Woodland Survey of Great Britain 2020-2022

## Overview
- A repeat survey of broadleaved woodlands across Great Britain conducted from 2020 to 2022.
- Involved 97 woodland sites, sampled with 16 randomly placed 200 m² plots per site.
- Measures ecological information at the site level and within plots, enabling analysis of ecological change since earlier surveys (1971, 2000, 2002/2003).

## What was Collected
- Plant species data:
  - Canopy and ground flora composition; vascular plants, bryophytes, and lichens.
  - Ground cover categories including bare ground, litter, rock, and total bryophytes.
- Soil data:
  - pH (fresh and air-dried) and Loss on ignition (LOI) as a proxy for soil organic matter.
- Habitat and management descriptors:
  - Habitat categories, slope, aspect, site descriptions, and management details.
- Tree data:
  - Diameter at breast height (DBH), tree type (tree, sapling, shrub), and multi-stem indicators.
- Plot and nest level metadata:
  - Plot numbers, nest identifiers, and data sheet references for traceability.

## Data Structure and Files
- WOODLANDS_SURVEY_SITES_2022.csv: Approximate site locations (site number, name, OSGB coordinates).
- WOODLANDS_SURVEY_SITE_INFORMATION_2022.csv: Descriptions for sites and plots, including slope, aspect, habitat descriptions, and survey dates.
- WOODLANDS_SURVEY_TREE_DATA_2022.csv: Tree-level data per plot (DBH, species, tree type, multi-stem status, etc).
- WOODLANDS_SURVEY_GROUND_FLORA_2022.csv: Ground flora data by plot (species codes, cover estimates, growth form, etc).
- WOODLANDS_SURVEY_SOIL_DATA_2022.csv: Plot soil results (pH, LOI, sample metadata, notes).
- Data are organized by SITE_NO, PLOT_NO, and other descriptors; some sites from earlier surveys were not accessible in 2020-2022.

## Methods and Standardization
- Stratified sampling across the entire area, following Bunce & Shaw (1973) standardized survey methods.
- Field handbook: National Woodland Survey & Native Pine Survey Field Handbook (Smart & Wood, 2021).
- Consistent data collection across decades to enable long-term trend analyses.

## Temporal Context and Repeats
- This 2020-2022 survey repeats methods used in:
  - 1971 Bunce survey (103 sites)
  - 2000-2003 surveys (referred to as 2001)
- Aims to assess ecological change since the 2000-2002 survey and to support long-term monitoring of British woodlands.

## Data Quality, Metadata and Governance
- Metadata and data provenance are explicit: originators are S.M. Smart, C.M. Wood, F.M. Seaton (UKCEH Lancaster); field surveyors and soil analysts are documented.
- Quality control notes exist in the soil data (SAMPLE_NOTES, MISSING_CODE) to aid data integrity.
- Standardization across sites and plots supports reliable comparative analyses over time.
- Related datasets and historical baselines are identified for integrated long-term studies.

## Access, Limitations and Use
- Some sites were not granted access in 2020-2022 (noted in the site list).
- Data are intended to support analyses of ecological change and inform woodland health monitoring policies.
- Datasets are designed for release and reuse, with explicit references to data sources and field methods to facilitate replication and governance.

## Related Datasets and References
- Bunce, R.G.H. & Shaw, M.W. (1973): Standardized Procedure for Ecological Survey.
- Smart, S.M. & Wood, C.M. (2021): Field Handbook for National Woodland Survey & Native Pine Survey.
- Stace, C. (1997): Flora references for nomenclature.
- Related datasets: Bunce 1971, Countryside Survey, Scottish Pinewood Survey, and additional historical surveys, enabling cross-temporal analyses.

## Implications for Monitoring Frameworks
- Demonstrates a robust, long-term, standardized monitoring framework suitable for policy scrutiny and decision-making.
- Highlights the importance of accessible metadata, open sharing, and clear data governance to overcome barriers identified in monitoring work (data gaps, access issues, siloed data, and metadata inadequacies).
- Provides a comprehensive, multi-layered data model (site, plot, trees, ground flora, soil) that supports diverse environmental health indicators and trend analysis over multiple decades.