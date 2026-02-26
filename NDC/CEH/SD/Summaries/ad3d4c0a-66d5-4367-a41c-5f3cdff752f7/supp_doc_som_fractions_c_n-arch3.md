# Carbon and nitrogen stocks in soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Overview
- A dataset detailing soil carbon (C) and nitrogen (N) stocks in 0-5 cm and 5-20 cm mineral soil layers, across grasslands and Scots Pine plantations established on former grasslands.
- Aims to assess how total quantities and forms of C and N change following afforestation and land-use conversion, using soil organic matter (SOM) fractions.

## What is included
- Measurements of C and N stocks in kg/m^2 for:
  - Dissolved organic matter (DOM)
  - Free particulate organic matter (fPOM)
  - Occluded particulate organic matter (oPOM)
  - Mineral-associated organic matter (MAOM)
- Fractions expressed for both carbon and nitrogen (e.g., q_DOM_C_m2, q_DOM_N_m2, etc.).
- Soil layers: 0-5 cm and 5-20 cm.
- Contextual soil properties: pH, texture (sand, clay, silt), bulk density (BD), and rock content.
- Study design: four clusters across Scotland with true geographical replication, including grassland and Scots pine plantations planted on former grasslands.
- Sampling event: single sampling in summer 2018.
- Total samples: 32 soil cores (three cores per site pooled prior to analysis).
- Data file: SOM_fractions_C_N.csv with 5 main descriptive columns plus ten measured variables per fraction.

## Sampling design and locations
- Clusters and composition:
  - Cluster 1 (Alyth): Grassland and Scots pine plantation
  - Cluster 2 (Limerigg): Grassland and Scots pine plantation
  - Cluster 3 (Peebles): Grassland and Scots pine plantation
  - Cluster 4 (Hawick): Grassland and Scots pine plantation
- Within-cluster arrangement: grassland and Scots pine plantation on former grasslands, sampled at different ages (young, middle-aged, old) to represent chronosequences.
- Coordinates provided for each site (grassland vs. Scots pine within each cluster).

## Data structure and variable details
- CSV file: SOM_fractions_C_N.csv
- Columns:
  - cluster: 1 = Alyth, 2 = Limerigg, 3 = Peebles, 4 = Hawick
  - veg: vegetation type category (GR = grassland; YO = young Scots pine; MI = middle-aged Scots pine; OL = old Scots pine)
  - LUT: land-use type (Grassland or Scots pine forest)
  - depth: soil layer (0-5 cm or 5-20 cm)
  - plant_year: year pines were planted on former grassland
  - age: age of Scots pines at sampling (2018)
  - pH: soil pH
  - sand, clay, silt: texture percentages
  - BD: bulk density (g/cm^3)
  - rock: percentage rock content
  - q_DOM_C_m2, q_DOM_N_m2: C and N in dissolved organic matter per m^2
  - q_fPOM_C_m2, q_fPOM_N_m2: C and N in free particulate organic matter per m^2
  - q_oPOM_C_m2, q_oPOM_N_m2: C and N in occluded particulate organic matter per m^2
  - q_MAOM_C_m2, q_MAOM_N_m2: C and N in mineral-associated organic matter per m^2

## Data quality, provenance, and governance
- Authorship: the study authors are responsible for collection and interpretation of the data.
- Metadata and provenance: accompanying details (column definitions and units) are provided within the data file description.
- Data sharing and openness: dataset is structured for public use (CSV) but general monitoring considerations apply, including the need for clear metadata and consistent data governance.
- Potential barriers relevant to monitoring frameworks:
  - Ensuring metadata completeness and dataset discoverability
  - Harmonizing units and fraction definitions with other datasets
  - Facilitating timely data updates and integration with wider soil-monitoring systems

## Relevance for monitoring frameworks and policy evaluation
- Provides a baseline, site- and chronosequence-specific view of how C and N stocks, and their SOM fractions, respond to grassland-to-forest conversion.
- The fraction-level data (DOM, fPOM, oPOM, MAOM) offer insights into mechanisms of carbon stabilization and turnover under afforestation.
- Includes additional soil properties (pH, texture, BD, rock content) that can help contextualize C and N dynamics and support modeling efforts within monitoring programs.
- Chronosequence design supports assessment of short- to mid-term changes across age classes of Scots pine plantations.

## Limitations and considerations for use
- Temporal scope: single sampling event (no direct temporal trend within sites).
- Replication: 32 primary samples may limit statistical power for broader generalizations beyond the four Scottish clusters.
- Scope: results are specific to former grassland-to-Scots pine conversion contexts in four Scottish clusters and may not generalize to other regions or forest types without caution.
- Data interoperability: ensure alignment of fraction definitions and units when integrating with other monitoring datasets.

## Access and dataset details
- File: SOM_fractions_C_N.csv
- Location-specific sampling coordinates are provided for each cluster and land-use type, enabling spatial analyses and spatial harmonization in monitoring frameworks.