# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A suite of molecular analyses was conducted on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Objectives include assessing biodiversity (bacteria and eukaryotes) and enabling downstream analyses of environmental correlations and potential predictions.

## Datasets and contents
- Environmental data files:
  - soil_env_data.csv: soil chemistry and related metadata
  - water_env_data.csv: water chemistry and related metadata
- Biodiversity sequence data files:
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
- Protocol documentation:
  - Protocol CEH Tellus SW.docx
- Data processing approach: DNA was extracted, quality checked, and sequenced; sequences clustered into OTUs; data tables show OTU proportions per sample.

## Sampling and field methods
- Epilithon (water) sampling:
  - Spatial coverage across the Wold River to Tamar River; exact sites chosen in the field for accessibility.
  - GPS-assisted pinpointing; three stones sampled per location (designated A, B, C); samples kept cold for lab analyses.
- Soil sampling:
  - Targeted soils across the Tamar region representing varied land uses.
  - Exact site locations determined in the field; cores taken and kept cold for analysis.
  - Location data anonymized to 1 km grid references.

## Data structure and cross-referencing
- Water epilithon data (water_env_data.csv):
  - Water_lab_ID: unique laboratory identifier (cross-referenced with biodiversity data)
  - Water_sample_ID: cross-references the SAMPLE ID in the WP4 water chemistry dataset
  - Stone_ID: A, B, or C (three stones per site)
  - Sampling Date, River, Catchment, NGR, Eastings, Northings
- Soil data (soil_env_data.csv):
  - Soil_ID: unique laboratory identifier (cross-referenced with biodiversity data)
  - Sampling date, Grid reference (1 km, anonymized), depth of core
  - Chemical parameters: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K
- Biodiversity datasets:
  - Rows: OTU IDs
  - Columns: Samples (cross-referenced to environmental data via IDs)
  - Example mapping: OTU tables cross-reference with Water_lab_ID or Soil_ID from the corresponding environmental data files

## Biodiversity data specifics
- Epilithon (water) datasets:
  - water_bacteria_seq.csv (bacteria OTUs)
  - water_eukaryotes_seq.csv (eukaryote OTUs)
- Soil datasets:
  - soil_bacteria_seq.csv (bacteria OTUs)
  - soil_eukaryotes_seq.csv (eukaryote OTUs)
- Sequencing and processing:
  - DNA extracted with MOBIO Powersoil 96-well kit
  - Quality checked before 454 pyrosequencing
  - Sequences clustered into OTUs; OTU relative abundance shown per sample

## Data integration and interpretation
- Cross-referencing keys ensure integration between environmental chemistry data and biodiversity sequencing data.
- The dataset supports analyses of relationships between soil/water chemistry and microbial eukaryotic/bacterial communities.
- Anonymized spatial references enable broad-scale spatial analyses while protecting site confidentiality.

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: consolidated description of the dataset

## Documentation and versioning
- Version: 1.0
- Date: 24/03/14
- Author: R. Griffiths
- Related documents: Protocol CEH Tellus SW.docx; WP4 water chemistry dataset documentation (full soil chemistry methods pending)

## Notes on data limitations and usage
- Soil chemistry methods and units are awaiting full methodological descriptions.
- Grid references are deliberately anonymized to 1 km resolution.
- Data are organized to facilitate exploratory analyses, correlation testing, and potential predictive modeling linking environment and biodiversity.