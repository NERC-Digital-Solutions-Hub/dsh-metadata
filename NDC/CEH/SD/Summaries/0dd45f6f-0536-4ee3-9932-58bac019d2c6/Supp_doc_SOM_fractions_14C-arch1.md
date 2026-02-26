# Radiocarbon dating of soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

- Purpose and scope
  - Dataset aims to determine mean residence time of carbon in different soil organic matter fractions under contrasting vegetation (grasslands vs mature Scot Pine plantations) established on former grassland across Scotland.
  - Sampling conducted in four clusters across Scotland (Scottish Central Lowlands and Southern Uplands) as true geographical replicates.

- Data content
  - One CSV file: SOM_fractions_14C.csv
  - Five columns: sample_ID, vegetation, cluster, soil_fraction, per_modern
  - Vegetation codes: GR = grassland, OL = Scot Pine plantation
  - Cluster codes: 1 = Alyth, 2 = Limerigg, 3 = Peebles, 4 = Hawick
  - Soil fractions: bulk (initial nonfractionated), DOM (dissolved organic matter), FLF (free light fraction), POM (occluded particulate organic matter), SC (mineral-associated organic matter, silt+clay)
  - per_modern: radiocarbon age expressed as percent modern 14C

- Sampling design and replication
  - Four clusters with two vegetation types per cluster: grassland and mature Scot Pine plantation on former grassland
  - Three soil cores per site, pooled prior to analyses
  - Fractionation into four soil fractions plus bulk soil, yielding 40 samples analyzed (2 vegetation types × 4 clusters × (4 fractions + 1 bulk soil))
  - Each combination is represented across the four clusters for both vegetation types

- Methods and processing
  - Field collection: summer 2018
  - Sample processing: drying, fractionation
  - Analysis: accelerator mass spectrometry (AMS) in summer 2019
  - Authors responsible for data collection and interpretation

- Location and spatial coverage
  - Eight site types (4 clusters × 2 vegetation types) with precise coordinates provided:
    - Cluster 1, Grassland: 56.633827, -3.2410629
    - Cluster 1, Scot pine: 56.735279, -3.2706253
    - Cluster 2, Grassland: 55.896026, -3.8524698
    - Cluster 2, Scot pine: 55.914748, -3.7977104
    - Cluster 3, Grassland: 55.646448, -3.1281129
    - Cluster 3, Scot pine: 55.613873, -2.9536157
    - Cluster 4, Grassland: 55.366159, -3.0258238
    - Cluster 4, Scot pine: 55.37448, -3.0053828

- Data quality, provenance and access
  - Dataset is clearly labeled with column definitions and unit of measurement (percent modern 14C)
  - Data creators responsible for collection and interpretation
  - Single, clearly defined CSV file facilitates reuse and integration with other datasets
  - Depth coverage limited to 0–5 cm mineral soil layer for samples

- Potential analyses for analysts
  - Compare mean residence times across vegetation types (GR vs OL) and across soil fractions (bulk, DOM, FLF, POM, SC)
  - Assess how carbon age varies with cluster (geographical variation) and soil fraction
  - Develop or test models of carbon turnover under grassland-to-forest conversion
  - Integrate with other site data to scale findings or to inform land management and carbon sequestration assessments

- Considerations and limitations
  - Depth restricted to 0–5 cm; may not reflect deeper soil dynamics
  - Temporal snapshot (one sampling event per site)
  - Radiocarbon ages expressed as percent modern 14C, requiring calibration to convert to calendar years
  - Sample size per category is modest (40 total samples across fractions and vegetation types)
  - Spatial coverage limited to four Scottish clusters; extrapolation to broader scales should be cautious

- Data use recommendations
  - Use per_modern values with appropriate calibration for year estimates
  - Leverage the clearly defined sample metadata (vegetation, cluster, soil_fraction) for stratified analyses
  - Combine with site coordinates for spatial analyses or mapping of carbon turnover patterns across Scotland