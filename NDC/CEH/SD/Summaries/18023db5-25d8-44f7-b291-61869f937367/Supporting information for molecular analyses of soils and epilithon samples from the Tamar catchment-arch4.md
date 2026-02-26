# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- Version control and provenance: Version 1.0, dated 24/03/14; description: created; author: R. Griffiths.

## Overview
- A dataset comprising molecular analyses of epilithon (water) and soil samples collected from the Tamar catchment in winter 2013/2014.
- Includes chemical environment data, biodiversity sequencing data (bacteria and eukaryotes), and metadata necessary to link datasets.

## Data assets and files
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Field methods and sampling design
- Epilithon (water samples):
  - Location planning aimed for good spatial coverage from the Wolf River through the Tamar River; exact sites determined in the field for accessibility and logistics.
  - Sites geolocated with a Garmin GPS12.
  - At each location, three stones were sampled (labeled A, B, C) and epilithon collected from a defined area.
  - Samples kept cold and transported to the laboratory for analyses.
- Soil samples:
  - Targeted a range of soils across the Tamar region representing different land uses.
  - Approximate locations determined from maps; exact sites chosen in the field based on accessibility and logistics.
  - Soil samples geolocated with a Garmin GPS12; samples kept cold and transported to the laboratory.
  - Grid references for soil samples are anonymized to 1 km resolution.

## Data structure and metadata

- Water epilithon data (water_env_data.csv):
  - Water_lab_ID: unique lab identifier for cross-referencing with biodiversity data.
  - Water_sample_ID: cross-references the SAMPLE ID column of the WP4 water chemistry dataset.
  - Stone_ID: labels each of the three stones at each location (A, B, C).
  - Sampling date, river, catchment, NGR, Eastings, Northings.

- Soil environment data (soil_env_data.csv):
  - Soil_ID: unique lab identifier for cross-referencing with biodiversity data.
  - Sampling date: date cores were taken.
  - Grid reference: 1 km resolution British National Grid reference (restricted to 1 km for site anonymity).
  - Depth of core: depth range from the soil surface.
  - Chemistry/metadata columns: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K.
  - Analyses performed at CEH Lancaster chemistry facility; full methodological details pending.

## Biodiversity datasets and data linking

- Epilithon bacteria (water_bacteria_seq.csv)
- Epilithon eukaryotes (water_eukaryotes_seq.csv)
- Soil bacteria (soil_bacteria_seq.csv)
- Soil eukaryotes (soil_eukaryotes_seq.csv)

- Data generation and format:
  - DNA extracted from all soil and epilithon samples using MOBIO Powersoil 96-well kit.
  - DNA quality-checked before submission for 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
  - After bioinformatic processing, sequences clustered into Operational Taxonomic Units (OTUs).
  - Each data table presents the percentage of each OTU within each sample.

- Cross-referencing scheme:
  - Rows: OTU IDs for the respective dataset.
  - Columns: OTU abundance per sample, cross-referenced to environmental data via sample IDs.
  - Examples of cross-links:
    - Epilithon bacteria: water_bacteria_seq.csv rows linked to water_env_data.csv via Water_lab_ID.
    - Epilithon eukaryotes: water_eukaryotes_seq.csv linked via Water_lab_ID to water_env_data.csv.
    - Soil bacteria: soil_bacteria_seq.csv linked to soil_env_data.csv via Soil_ID.
    - Soil eukaryotes: soil_eukaryotes_seq.csv linked to soil_env_data.csv via Soil_ID.

- Referenced documentation:
  - Protocol CEH Tellus SW.docx
  - Water chemistry cross-references with WP4 dataset for detailed chemistry metadata (Water_sample_ID cross-references to WP4 data).

## Data processing workflow
- Laboratory and sequencing:
  - DNA extraction → quality check → 454 pyrosequencing.
- Bioinformatics:
  - Sequence processing → OTU clustering → creation of OTU abundance matrices.
- Data integration:
  - OTU tables linked to corresponding environmental data via sample IDs (Water_lab_ID or Soil_ID).

## Governance, accessibility, and reuse notes
- Data assets are structured to enable cross-disciplinary reuse (chemistry, biodiversity, spatial analyses) through consistent ID-based linking.
- Spatial data are anonymized to 1 km grid references for soil samples.
- Protocol documentation and cross-referencing schemata are provided to support reproducibility and data discovery.