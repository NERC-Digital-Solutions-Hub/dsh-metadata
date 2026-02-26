# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- A dataset combining environmental chemistry data (soil and water) with biodiversity profiles (bacteria and eukaryotes) from epilithon and soil samples.
- Collected in the Tamar catchment during winter 2013/2014.
- DNA extracted, sequenced (454 pyrosequencing), and sequences clustered into OTUs; results expressed as percentage composition per sample.

## Datasets and files
- Soil chemistry and metadata
  - soil_env_data.csv
  - Fields include Soil_ID, Sampling date, Grid reference (1 km resolution for anonymity), depth of core, and chemical measurements (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- Water (epilithon) chemistry and metadata
  - water_env_data.csv
  - Key fields: Water_lab_ID (link to biodiversity data), Water_sample_ID (links to WP4 dataset), Stone_ID (A/B/C), Sampling date, River, Catchment, NGR, Eastings, Northings.
- Biodiversity datasets (OTU tables)
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Structure: rows = OTU IDs; columns = sample IDs cross-referenced to the environmental data; values = percentage of each OTU in each sample.
- Cross-reference guidance
  - Example cross-links: water_env_data.csv Water_lab_ID ↔ water_bacteria_seq.csv; soil_env_data.csv Soil_ID ↔ soil_bacteria_seq.csv
- Protocols and methods
  - Protocol CEH Tellus SW.docx

## Sampling and laboratory methods
- Epilithon (water samples)
  - Approximately 20 sampling locations spanning the Wolf River to the Tamar River; exact sites chosen in the field for accessibility after initial mapping.
  - Three stones sampled per location; epilithon collected from a defined area; samples kept cold and taken to the lab for analyses.
- Soil samples
  - Range of soils from the Tamar region with varied land uses; exact sites determined in the field to provide broad spatial coverage.
  - Location anonymized to 1 km grid references; samples kept cold and transported to the lab for analyses.
- DNA and sequencing
  - DNA extracted from all soil and epilithon samples using MOBIO Powersoil 96-well kit.
  - Quality checked before submission for 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
  - Bioinformatic processing clustered sequences into OTUs; results presented as OTU percentages per sample.

## Data structure and cross-referencing
- Biodiversity data organization
  - Rows: OTU IDs for each dataset
  - Columns: sample IDs that cross-reference with the corresponding environmental data file
  - Example mappings provided in the dataset documentation (e.g., Epilithon bacteria: water_bacteria_seq.csv column 1 matches Water_lab_ID in water_env_data.csv)
- Cross-dataset linking
  - Water samples linked via Water_lab_ID and Water_sample_ID to water biodiversity data
  - Soil samples linked via Soil_ID to soil biodiversity data
  - Cross-referencing enables combined analyses of chemical environment and OTU distributions

## Data processing and interpretation
- Sequencing data were processed to produce OTU tables representing relative abundances of taxa within each sample.
- Environmental data include key chemical parameters for soils and context for water samples, enabling correlations between chemistry and biodiversity.
- Note: Soil chemistry methods were described as pending in accompanying documentation at the time of data compilation.

## Access, metadata, and contributors
- Data provenance
  - Collected and processed by a team including field sampling, data processing/mapping, laboratory analysis, and planning/management roles.
  - Contributors: Sample collection (Peter Scarlett, Gearóid Webb, Pete Nuttall); Data processing and mapping (Gearóid Webb); Laboratory analysis (Radim Sarlej, Bruce Thomson, Rob Griffiths); Planning and Management (François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths).
- Data availability
  - Data files listed above are part of the CEH Tellus SW project documentation for the Tamar catchment study.
  - Protocols referenced for methodological detail (Protocol CEH Tellus SW.docx).