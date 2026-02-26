# Radiocarbon dating of soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Overview
- Dataset of radiocarbon ages (percent modern, 14C) for soil samples from grasslands and mature Scot Pine plantations across four clusters in Scotland.
- Samples collected in summer 2018; radiocarbon analysis conducted in summer 2019.
- Aims to determine mean residence time of carbon in different soil fractions under contrasting vegetation.
- Includes bulk soil and four soil fractions for each site, totaling 40 analyzed samples.

## Data File and Structure
- File: SOM_fractions_14C.csv
- Columns (five total):
  - sample_ID
  - vegetation (values: GR for grassland, OL for Scot pine plantation)
  - cluster (values: 1, 2, 3, 4)
  - soil_fration (note the misspelling in the dataset; refers to soil fraction)
  - per_modern (radiocarbon age in percent modern 14C)

## Fractions
- bulk: initial, non-fractionated soil
- DOM: dissolved organic matter
- FLF: free light fraction (free particulate organic matter)
- POM: occluded particulate organic matter
- SC: silt+clay, i.e., mineral-associated organic matter

## Sampling Design and Spatial Coverage
- Study design: true geographical replicates with grassland and mature Scot Pine forests planted on former grassland.
- Four clusters across Scotland:
  - Cluster 1: Alyth area
  - Cluster 2: Limerigg area
  - Cluster 3: Peebles area
  - Cluster 4: Hawick area
- Within each cluster, samples from both vegetation types (grassland and Scot pine plantation) were collected.
- 3 soil cores per site were collected and pooled, resulting in 8 site-context samples (2 vegetation types × 4 clusters) that were then fractionated into 5 groups (4 fractions + bulk), yielding 40 analyzed samples (8 sites × 5 fractions).

## Spatial and Temporal Details
- Locations provided as latitude/longitude for each site:
  - Cluster 1 Grassland: 56.633827, -3.2410629
  - Cluster 1 Scot pine: 56.735279, -3.2706253
  - Cluster 2 Grassland: 55.896026, -3.8524698
  - Cluster 2 Scot pine: 55.914748, -3.7977104
  - Cluster 3 Grassland: 55.646448, -3.1281129
  - Cluster 3 Scot pine: 55.613873, -2.9536157
  - Cluster 4 Grassland: 55.366159, -3.0258238
  - Cluster 4 Scot pine: 55.37448, -3.0053828
- Temporal context:
  - Field sampling: summer 2018
  - Fractionation and radiocarbon analysis: summer 2019

## Data Quality and Provenance
- The dataset is authored by the researchers responsible for collection and interpretation.
- Data suitable for GIS-based visualization of radiocarbon ages by vegetation type, cluster, and soil fraction.
- Note: column label contains a misspelling (soil_fration) which should be verified when integrating into GIS workflows.