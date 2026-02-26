# Soil nematode communities from peri urban watersheds

## Overview
- Study of soil nematode communities in the Peri urban watershed of Ningbo, China.
- Sampling across four time points: April 9–12, 2017; July 15–18, 2017; October 14–17, 2017; January 11–14, 2018.
- Two land uses at each site: farmland and forest.
- Aimed at generating comparable nematode community data for integration with wider Centralized Zonation Observatories (CZO) datasets.

## Experimental Design
- At each watershed site, 250 g of soil collected by randomly sampling five cores across the site.
- Samples stored at 4 °C before shipping to the UK; shipped under Scottish government import licence and stored in quarantine at 8 °C per biosecurity policy.
- Aims to capture land-use–toned variation and seasonal changes in nematode communities.

## Collection Methods and Laboratory Instrumentation
- Nematodes extracted from soil via density centrifugation (adapted from Hallmann and Viaene 2013).
  - 100 g soil per tube; shake with water; centrifuge at 1800 g; remove supernatant; add MgSO4 to final density 1.18; repeat centrifugation; sieve through 20 µm; rinse into tube; freeze-dry; resuspend in 2 ml sterile water.
  - DNA extracted using PureLink genomic DNA mini kit.
- Nematode community structure assessed using directed T-RFLP (from Donn et al. 2012).
  - PCR with Nem_SSU_F74 and FAM-labeled Nem_18S_R primers.
  - PCR conditions: 95 °C 3 min; 35 cycles (94 °C 30 s, 55 °C 30 s, 68 °C 1 min); final extension 68 °C 10 min.
  - Digestion with Ple I and BtscI restriction enzymes; specific buffers and temperatures; denaturation steps.
  - Digests diluted, mixed with formamide and LIZ 1200 marker; sequenced on ABI 3730 capillary sequencer.
  - T-RF peaks identified in GeneMapper; baseline fluorescence set at 50 fluorescence units.
  - For each sample, relative peak fluorescence calculated; peaks <1% of total fluorescence removed.
  - Data transformed with Hellinger transformation.

## Data Structure, Nature, and Units
- Data file: CZOperiurban_watershed_Nematodedata.csv
- Columns:
  - Sample_ID: CZO watershed sample ID (matches other CZO datasets).
  - Season: season of collection.
  - Peak_...: Hellinger-transformed relative fluorescence for each T-RF peak (e.g., Peak_54.86 corresponds to peak 54.86).

## Data Processing and Quality Notes
- Baseline fluorescence threshold (50 units) used during peak identification.
- Relative fluorescence data are Hellinger-transformed to prepare for downstream multivariate analyses.
- Filtering removes peaks contributing less than 1% of total fluorescence per sample.

## Metadata and Access Considerations
- Data are structured for compatibility with other CZO catchment data (shared Sample_ID convention).
- Methodological details ( primers, enzymes, PCR and digestion conditions) support reproducibility and cross-study comparisons.

## References
- Hallmann and Viaene (2013). Nematode extraction. EPPO Bulletin.
- Donn, Neilson, Griffiths, Daniell (2012). A novel molecular approach for rapid assessment of soil nematode assemblages. Methods in Ecology and Evolution.

## Relevance for Data Leaders
- Demonstrates a multi-site, multi-season data collection pipeline with standardized processing suitable for integration into broader data systems.
- Highlights data governance needs:
  - Robust metadata and clear data dictionary (e.g., peak naming conventions, transformation procedures, baseline thresholds).
  - Consistent data formats to enable discoverability and interoperability across CZO datasets.
  - Documentation of sampling, storage, and lab procedures to support data quality and reproducibility.
- Potential challenges to address:
  - Fragmentation of data across methods (T-RFLP, PCR conditions) and the need for harmonized metadata across projects.
  - Ensuring ongoing data updates, versioning, and community-driven data sharing to strengthen data assets and practice within the wider data ecosystem.