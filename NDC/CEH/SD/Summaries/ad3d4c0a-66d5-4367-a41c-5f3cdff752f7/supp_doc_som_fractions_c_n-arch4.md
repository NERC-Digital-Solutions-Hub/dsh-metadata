# Carbon and nitrogen stocks in soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Overview
- Quantifies carbon (C) and nitrogen (N) stocks in soil organic matter fractions across grassland-to-forest conversion chronosequences in Scotland.
- Data express stocks in kg per m2 for two soil depths: 0–5 cm and 5–20 cm.
- Focuses on grasslands and Scots Pine plantations planted on former grasslands, across four geographical clusters.
- One CSV dataset: SOM_fractions_C_N.csv, with detailed metadata and stock measurements by fraction.

## Data content and structure
- Stocks by fractions: dissolved organic matter (DOM), free particulate organic matter (fPOM), occluded particulate organic matter (oPOM), mineral-associated organic matter (MAOM) for both C and N.
  - Column names include q_DOM_C_m2, q_DOM_N_m2, q_fPOM_C_m2, q_fPOM_N_m2, q_oPOM_C_m2, q_oPOM_N_m2, q_MAOM_C_m2, q_MAOM_N_m2.
- Environmental and site metadata:
  - cluster (origin: 1 Alyth, 2 Limerigg, 3 Peebles, 4 Hawick)
  - veg (sampling source: GR grassland, YO young, MI mid-age, OL old Scots pine)
  - LUT (land use type: Grassland or Scots pine forest)
  - depth (soil layer: 0–5 cm or 5–20 cm)
  - plant_year (year pines were planted on former grasslands)
  - age (age of Scots pines at sampling in 2018)
  - pH, sand, clay, silt
  - BD (bulk density, g/cm3)
  - rock (percentage rock content)
- Dataset size and structure:
  - 32 samples in total (3 cores per site pooled)
  - Four clusters, grassland and Scots pine representations, across three age categories, sampled in 2018
- Geographic coordinates for sampling locations (lat/long) per cluster and land-use type

## Sampling and methods
- Sampling timeframe: Summer 2018
- Site selection: grasslands and Scots Pine forests planted on former grasslands across four clusters
- Core collection: three soil cores per site, pooled prior to analysis
- Depths: 0–5 cm and 5–20 cm
- Fractionation: soils fractionated into DOM, fPOM, oPOM, MAOM
- Additional measurements: soil pH, texture (sand, clay, silt), bulk density, and rock content
- Data authorship: authors responsible for collection and interpretation of the data

## Data format and metadata
- File: SOM_fractions_C_N.csv
- Key variables:
  - cluster, veg, LUT, depth, plant_year, age
  - pH, sand, clay, silt, BD, rock
  - q_DOM_C_m2, q_DOM_N_m2, q_fPOM_C_m2, q_fPOM_N_m2, q_oPOM_C_m2, q_oPOM_N_m2, q_MAOM_C_m2, q_MAOM_N_m2
- Cluster mapping:
  - 1 = Alyth, 2 = Limerigg, 3 = Peebles, 4 = Hawick
- Veg categories:
  - GR = grassland; YO = young; MI = middle-aged; OL = old Scots pine
- LUT values denote Grassland or Scots pine forest

## Spatial and temporal coverage
- Four spatial clusters across Scotland with specified coordinates
- Temporal scope: single sampling event in 2018 (no longitudinal sampling reported)

## Data quality, limitations, and considerations
- Strengths:
  - Comprehensive fractionation into major soil organic matter pools
  - Includes essential soil properties (pH, texture, bulk density, rock content) for context
  - Enables cross-site comparisons of C and N stocks by depth and fraction
- Limitations:
  - One-time sampling limits temporal trend analysis
  - 32 samples total may constrain broad generalizations across wider landscapes
  - Details on data standards or validation beyond the listed variables are not specified

## Data governance, access, and potential reuse
- Authorship: data collected and interpreted by the study authors
- Dataset governance: clearly defined columns, units, and cluster mappings to support reuse
- Potential reuse:
  - Soil carbon and nitrogen dynamics related to afforestation/restoration
  - Cross-site comparisons of organic matter fractions under grassland-to-forest transitions
  - Integration with other Scottish soil datasets for broader environmental analyses
- User alignment:
  - Structured for policy, research, and environmental management colleagues needing site-level and fraction-specific C and N data

## Relevance for Data Leaders
- Data asset clarity: single, well-documented CSV with explicit variable definitions and units
- Discoverability: descriptive file name and explicit column metadata, including cluster and location context
- Data quality considerations: includes key soil properties plus fractionated C/N stocks, though limited replication and a single sampling event
- Stewardship and governance: authorship and data interpretation responsibility indicated; suitable for future updates or linkage with broader networks
- Value for data strategy:
  - Demonstrates end-to-end data collection, fractionation, and multi-site synthesis
  - Supports co-ownership of data products across clusters and land-use types through consistent metadata
  - Provides a model for managing soil data assets that merge physical measurements with ecological transitions (grassland to forest) for broader use and policy discussions