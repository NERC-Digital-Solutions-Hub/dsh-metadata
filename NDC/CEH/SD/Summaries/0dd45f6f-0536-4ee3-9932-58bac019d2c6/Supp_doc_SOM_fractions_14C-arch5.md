# Radiocarbon dating of soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Overview
- Dataset of radiocarbon ages (percent modern, 14C) for soil samples from grasslands and mature Scots pine plantations across four clusters in Scotland.
- Focuses on the 0-5 cm mineral soil layer and includes bulk soil and these fractions: dissolved organic matter (DOM), free light fraction (FLF), occluded particulate organic matter (POM), and mineral-associated organic matter (SC).
- Samples collected in summer 2018; fractions analyzed by accelerator mass spectrometry in summer 2019 to determine mean residence times of carbon under contrasting vegetation.
- Comprises one CSV file: SOM_fractions_14C.csv with five columns.
- Total samples: 40 (2 vegetation types × 4 clusters × (4 fractions + 1 bulk)).
- Authors responsible for collection and interpretation; geographic coordinates provided for each site.

## Dataset contents
- File: SOM_fractions_14C.csv
- Columns:
  - sample_ID
  - vegetation
  - cluster
  - soil_fration
  - per_modern
- Vegetation: GR = grassland; OL = Scot pine plantation
- Cluster: 1 (Alyth), 2 (Limerigg), 3 (Peebles), 4 (Hawick)
- Soil fraction: bulk, DOM, FLF, POM, SC
- per_modern: radiocarbon age in percent modern

## Sampling and processing
- Three soil cores per site pooled; eight sites total (four grasslands and four Scot pine plantations), yielding 40 samples.
- Each site contributed across four soil fractions plus a bulk sample (4 fractions + 1 bulk).
- Soil fractions were prepared prior to analysis; radiocarbon ages determined via AMS in 2019.

## Geographic coverage
- Four clusters across Scotland with site-specific coordinates:
  - Cluster 1, Grassland: 56.633827, -3.2410629
  - Cluster 1, Scot pine plantation: 56.735279, -3.2706253
  - Cluster 2, Grassland: 55.896026, -3.8524698
  - Cluster 2, Scot pine plantation: 55.914748, -3.7977104
  - Cluster 3, Grassland: 55.646448, -3.1281129
  - Cluster 3, Scot pine plantation: 55.613873, -2.9536157
  - Cluster 4, Grassland: 55.366159, -3.0258238
  - Cluster 4, Scot pine plantation: 55.37448, -3.0053828

## Data provenance and authorship
- Field collection conducted in 2018; fractionation and AMS analysis completed in 2019.
- Authors responsible for data collection and interpretation.

## Data governance and stewardship notes
- Metadata and clarity:
  - Column naming includes a likely typographical error in the header (soil_fration should be soil_fraction); ensure consistent naming in any downstream usage.
  - Clear definitions of categories (vegetation, cluster, soil fraction) are provided, with explicit label codes.
- Data quality and interoperability:
  - Units: per_modern expressed as percent modern 14C; depth defined as 0-5 cm mineral soil layer.
  - Fraction definitions (bulk, DOM, FLF, POM, SC) are specified.
- Access, licensing, and metadata:
  - Dataset consists of a single CSV; consider accompanying metadata describing methods, QC steps, license, and usage rights to facilitate reuse.
- maintenance and updates:
  - If future timepoints or additional sites are added, maintain the existing sample_id schema and fraction definitions to ensure comparability.
- reuse considerations:
  - Small sample size per site and pooling of cores may influence variability interpretation; users should account for this in analyses.