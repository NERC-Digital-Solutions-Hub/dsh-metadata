# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Suite of molecular analyses to assess bacterial and eukaryotic biodiversity in epilithon (water) and soils from the Tamar catchment, winter 2013/2014.
- Data types include environmental chemistry for soils and water, sampling metadata, and high-throughput sequencing results (OTU tables).

## Data files and structure
- Data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Key linking identifiers:
  - Water_lab_ID (cross-references with water_env_data.csv for epilithon datasets)
  - Soil_ID (cross-references with soil_env_data.csv for soil datasets)
- Biodiversity data format:
  - OTU tables: rows = OTU IDs; columns = samples; values = percentage of each OTU in the sample
  - Example cross-links provided between OTU tables and environmental data via the IDs
- Sequencing method: 454 pyrosequencing; OTUs clustered post-processing

## Sampling and field methods
- Epilithon (water samples):
  - Approximately 20 sampling sites chosen for broad spatial coverage from Wold River to Tamar River
  - Three stones sampled per site; epilithon collected from a defined area
  - Exact locations determined in the field with a Garmin GPS12; samples kept cold and transported to the lab
- Soils:
  - Range of soils from the Tamar region with diverse land uses
  - Exact sites determined in the field considering accessibility; 1 km grid reference anonymized
  - Soil cores collected and kept cold for laboratory analyses

## Data fields and chemistry
- Epilithon water data (water_env_data.csv) fields:
  - Water_lab_ID, Water_sample_ID, Stone_ID (A/B/C), Sampling date, River, Catchment, NGR, Eastings, Northings
- Soil data (soil_env_data.csv) fields:
  - Soil_ID, Sampling date, Grid reference (1 km, anonymized), depth of core
  - Chemical measurements: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K
- Note: soil chemistry methods described as ongoing with full methodological descriptions awaited

## Biodiversity sequencing data
- Datasets:
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
- Processing:
  - DNA extracted using MOBIO Powersoil 96-well kit
  - Quality checks performed; 454 pyrosequencing performed to profile biodiversity
  - Post-processing yields OTU tables; rows = OTU IDs; columns = samples; values = OTU percentages
- Cross-referencing with environmental data:
  - Epilithon bacteria: first column corresponds to Water_lab_ID in water_env_data.csv
  - Epilithon eukaryotes: first column corresponds to Water_lab_ID in water_env_data.csv
  - Soil bacteria: first column corresponds to Soil_ID in soil_env_data.csv
  - Soil eukaryotes: first column corresponds to Soil_ID in soil_env_data.csv

## Usage and potential outputs
- Integrate OTU data with environmental chemistry to explore drivers of biodiversity patterns
- Build self-serve dashboards or pivot tables to compare sites, years, or sample types
- Reference WP4 water chemistry dataset for additional metadata and context

## Contributors
- Field collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths

## Notes and considerations
- Spatial anonymization via 1 km grid references
- Methodological details for soil chemistry forthcoming
- Data integration requires careful matching of cross-reference IDs across datasets