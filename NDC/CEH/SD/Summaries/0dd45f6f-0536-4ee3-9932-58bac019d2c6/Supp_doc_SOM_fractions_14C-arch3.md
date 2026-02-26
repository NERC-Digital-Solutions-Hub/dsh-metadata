# Radiocarbon dating of soil organic matter fractions along grassland-to-forest conversion chronosequences across Scotland

## Overview
- Study aims to determine the mean residence time of carbon in different soil organic matter fractions under contrasting vegetation (grassland vs mature Scot Pine plantations) across four clusters in Scotland.
- Focuses on the 0–5 cm mineral soil layer, using bulk soil and fractions including dissolved organic matter (DOM), free light fraction (FLF), occluded particulate organic matter (POM), and mineral-associated organic matter (SC).

## Dataset and Variables
- Data file: SOM_fractions_14C.csv
- Columns:
  - sample_ID
  - vegetation (GR = grassland; OL = Scot Pine plantation)
  - cluster (1 = Alyth, 2 = Limerigg, 3 = Peebles, 4 = Hawick)
  - soil_fration (types: bulk, DOM, FLF, POM, SC)
  - per_modern (radiocarbon age in percent modern)
- Note: The column name for soil fraction is listed as "soil_fration" (potential typo in the original data description).

## Study Design and Sampling
- Location and sampling:
  - Four clusters across Scotland: Central Lowlands and Southern Uplands
  - Two vegetation types at each cluster: grassland (GR) and mature Scot Pine plantation (OL)
  - Coordinates provided for each cluster-vegetation pair
- Sampling details:
  - Summer 2018: soil cores collected (3 cores per site) and pooled
  - 8 site types total (4 clusters × 2 vegetation types)
  - Each site fractionated into 4 fractions plus bulk soil, yielding 5 measurements per site
  - Total analysed samples: 40 (2 vegetation types × 4 clusters × (4 fractions + 1 bulk))
  - 2019: samples fractionated and analyzed by accelerator mass spectrometry (AMS)
- Dataset structure:
  - Each row corresponds to a sample from a given vegetation type, cluster, and soil fraction, with its radiocarbon age (percent modern)

## Data Management and Quality
- The authors collected, fractionated, and analyzed samples, ensuring traceability of vegetation type, cluster origin, soil fraction, and radiocarbon age.
- The provided metadata includes site-level context (vegetation, cluster) and fraction designation, but detailed metadata such as measurement uncertainties or calibration specifics are not described in the excerpt.

## Relevance for Monitoring Frameworks
- Demonstrates a structured approach to measuring soil carbon dynamics across land-use change (grassland to forest) with clear spatial replication (clusters) and soil fractions.
- Data framework supports monitoring of carbon turnover and storage in soils under different vegetation regimes, informing policy decisions and evaluations of land management impacts on environmental health.
- Emphasizes the need for standardized data components (sampling design, fraction definitions, and clear variable coding) to enable aggregation, comparison, and replication in monitoring programs.

## Limitations and Considerations
- Results are not provided in the excerpt; focus is on dataset and methodology.
- Sampling occurred at a single time point (summer 2018) with no temporal replication described.
- Limited geographic scope to four clusters within Scotland; broader generalization would require additional sites and times.
- Metadata completeness beyond the listed fields is not specified, which can affect data reuse and governance.

## Data Access and Structure
- File: SOM_fractions_14C.csv
- Contents include sample IDs, vegetation type, cluster origin, soil fraction category, and radiocarbon age (percent modern) for each sample.