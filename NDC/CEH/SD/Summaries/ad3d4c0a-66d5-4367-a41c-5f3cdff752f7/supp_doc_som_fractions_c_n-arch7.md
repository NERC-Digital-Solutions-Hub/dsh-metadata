# Carbon and nitrogen stocks in soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Overview
- Presents carbon (C) and nitrogen (N) stocks in soil organic matter fractions across grassland-to-Scots pine forest conversion in Scotland.
- Stocks are expressed as kilograms per square meter (kg/m²) for two depth intervals: 0–5 cm and 5–20 cm.
- Fractions analyzed: dissolved organic matter (DOM), free particulate organic matter (fPOM), occluded particulate organic matter (oPOM), mineral-associated organic matter (MAOM).
- Study scope: four clusters across Scotland (Scottish Central Lowlands and Southern Uplands), with grassland and Scots Pine plantations established on former grasslands.
- Aim: determine changes in total quantity and form (fraction distribution) of C and N stocks following afforestation.

## Data collection and sampling design
- Sampling occurred in summer 2018 using soil corers.
- Soils were split into 0–5 cm and 5–20 cm layers and fractionated into four organic matter fractions.
- Measurements also included soil pH, texture, bulk density, and rock content.
- Design features true geographical replication: grasslands and Scots Pine forests of three ages, planted on former grasslands, across four clusters.
- Each site contributed three soil cores that were pooled, yielding 32 samples in total (across all clusters and land uses).

## Data file and structure
- Dataset file: SOM_fractions_C_N.csv
- Key fields include:
  - cluster: origin cluster (1 Alyth, 2 Limerigg, 3 Peebles, 4 Hawick)
  - veg: vegetation origin (GR = grassland; YO = young; MI = middle-aged; OL = old Scots pine)
  - LUT: land-use type (Grassland or Scots pine forest)
  - depth: soil layer (0–5 cm or 5–20 cm)
  - plant_year: year Scots pines were planted on former grasslands
  - age: age of Scots pines at sampling (2018)
  - pH, sand, clay, silt, BD (bulk density, g/cm³), rock (percentage)
  - q_DOM_C_m2, q_DOM_N_m2, q_fPOM_C_m2, q_fPOM_N_m2, q_oPOM_C_m2, q_oPOM_N_m2, q_MAOM_C_m2, q_MAOM_N_m2
- Units: C and N stocks in kg/m²; fractions represent dissolved, free POM, occluded POM, and MAOM for each C and N.
- Data coverage by cluster/land-use and depth is explicitly linked to geographic coordinates.

## Spatial coverage and locations
- Locations provided as latitude/longitude coordinates for cluster and land-use combinations:
  - Cluster 1, Grassland: 56.633827, -3.2410629
  - Cluster 1, Scots pine: 56.735279, -3.2706253
  - Cluster 2, Grassland: 55.896026, -3.8524698
  - Cluster 2, Scots pine: 55.914748, -3.7977104
  - Cluster 3, Grassland: 55.646448, -3.1281129
  - Cluster 3, Scots pine: 55.613873, -2.9536157
  - Cluster 4, Grassland: 55.366159, -3.0258238
  - Cluster 4, Scots pine: 55.37448, -3.0053828
- The clusters represent four geographic replication sites within Scotland, located in the Scottish Central Lowlands and Southern Uplands.

## Intended use and analytical opportunities
- Enables GIS-based analysis of spatial patterns in C and N stocks by depth and by organic matter fraction.
- Facilitates comparison between grassland and Scots pine forest land uses and across forest ages.
- Supports visualization of stock distributions (by fraction and depth) and assessment of afforestation effects on soil carbon and nitrogen pools.
- Data can be integrated with additional soil properties (pH, texture, bulk density) for more comprehensive spatial modeling.

## Quality, provenance, and limitations
- Data collected and interpreted by the study authors.
- Single sampling period (summer 2018) with pooled cores per site; spatial replication at each cluster is limited to 32 total samples.
- Fractionation and measurement details are documented within the dataset; users should consider regional representativeness when generalizing beyond the study sites.
- The dataset provides explicit provenance (cluster-based origin and planting history), aiding reproducibility and GIS traceability.