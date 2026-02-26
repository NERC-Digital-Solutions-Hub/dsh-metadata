# Radiocarbon dating of soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Overview
- A dataset and provenance describing radiocarbon ages (percent modern) for soil organic matter in the top 0–5 cm across grassland and mature Scot Pine plantations, sampled across four Scottish clusters representing grassland-to-forest conversion.
- Aim: determine mean residence time of carbon in different soil fractions under contrasting vegetation.

## Data contents
- Single CSV: SOM_fractions_14C.csv
- Five columns:
  - sample_ID
  - vegetation (GR = grassland; OL = Scot pine plantation)
  - cluster (1 = Alyth, 2 = Limerigg, 3 = Peebles, 4 = Hawick)
  - soil_fraction (bulk, DOM, FLF, POM, SC)
  - per_modern (radiocarbon age in percent modern)
- Dataset scope: 40 samples analysed (2 vegetation types × 4 clusters × (4 fractions + 1 bulk soil) = 40)
- Note: minor variable naming in the source (soil_fration) but interpretation aligns with soil_fraction.

## Study design and sampling
- Sites: four clusters across Scotland (Central Lowlands and Southern Uplands), true geographical replicates.
- Sampling year and method:
  - Summer 2018: soil cores collected from 0–5 cm mineral soil layer.
  - Three cores per site pooled prior to analysis (resulting in 8 site-level samples).
  - Summer 2019: soil fractions analysed by accelerator mass spectrometry (AMS).
- Vegetation contrast: grassland (GR) vs mature Scot Pine plantations on former grassland (OL).

## Soil fractions analyzed
- Bulk: initial, non-fractionated soil
- DOM: dissolved organic matter
- FLF: free/light fraction (free particulate organic matter)
- POM: occluded particulate organic matter
- SC: mineral-associated organic matter (silt+clay)

## Locations and coordinates
- Cluster 1 (Alyth): Grassland (56.633827, -3.2410629); Scot pine (56.735279, -3.2706253)
- Cluster 2 (Limerigg): Grassland (55.896026, -3.8524698); Scot pine (55.914748, -3.7977104)
- Cluster 3 (Peebles): Grassland (55.646448, -3.1281129); Scot pine (55.613873, -2.9536157)
- Cluster 4 (Hawick): Grassland (55.366159, -3.0258238); Scot pine (55.374480, -3.0053828)

## Data usage and potential products
- Enables cross-vegetation comparison of carbon residence times across soil fractions and clusters.
- Suitable for creating dashboards or charts on per_modern by vegetation, cluster, and soil_fraction to explore carbon turnover patterns.
- Can be combined with site coordinates for spatial analyses or integrated into meta-analyses of soil carbon dynamics.

## Considerations and limitations
- Single sampling event per site; results reflect mean residence times at the time of sampling.
- Three cores per site pooled to a single sample per fraction; intra-site variability not explicitly provided.
- Data are specific to the 0–5 cm mineral soil layer and may not represent deeper horizons.