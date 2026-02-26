# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A suite of molecular analyses conducted on epilithon (water-associated) and soil samples from the Tamar catchment during winter 2013/2014.
- Includes environmental chemistry data and biodiversity data derived from DNA sequencing of microbial and eukaryotic communities.
- Data designed to enable linking environmental variables with microbial/eukaryotic community composition via OTU profiling.

## Field sampling and data collection
- Epilithon (water samples): approximate sampling locations chosen to provide broad spatial coverage from the Wolf River through to the Tamar River; exact sites determined in the field. GPS used (Garmin GPS12). Three stones per location (20 locations) with epilithon collected from a defined area; samples kept cold and transported to the lab.
- Soil samples: targeted across the Tamar region to cover a range of land uses; exact sites determined in the field, with logistics considered; GPS used (Garmin GPS12). Samples kept cold and transported to the lab.
- Sampling documentation references: Protocol CEH Tellus SW.docx; water chemistry context linked to WP4 documentation for proximity to epilithon samples.

## Datasets and data structure
- Datasets (CSV files):
  - water_env_data.csv: metadata for epilithon water samples
  - water_bacteria_seq.csv: epilithon bacterial OTU data
  - water_eukaryotes_seq.csv: epilithon eukaryote OTU data
  - soil_env_data.csv: metadata for soil samples
  - soil_bacteria_seq.csv: soil bacterial OTU data
  - soil_eukaryotes_seq.csv: soil eukaryote OTU data
- Environmental data columns:
  - Water: Water_lab_ID (link to biodiversity data), Water_sample_ID (cross-references WP4 water chemistry sample names), Stone_ID (A/B/C), Sampling date, River, Catchment, NGR, Eastings, Northings.
  - Soil: Soil_ID, Sampling date, Grid reference (1 km resolution, anonymized), depth of core, and chemical measurements (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- Biodiversity data structure:
  - DNA extracted via MOBIO Powersoil kit; tested for purity/yield; processed with 454 pyrosequencing.
  - Sequences clustered into OTUs; data tables show the percentage of each OTU within each sample.
  - Rows correspond to OTU IDs; columns correspond to samples (linked to environmental data via IDs).
  - Cross-reference examples:
    - Epilithon bacteria: water_bacteria_seq.csv column 1 matches Water_lab_ID in water_env_data.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv column 1 matches Water_lab_ID in water_env_data.csv
    - Soil bacteria: soil_bacteria_seq.csv column 1 matches Soil_ID in soil_env_data.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv column 1 matches Soil_ID in soil_env_data.csv

## Data processing and biodiversity sequencing
- DNA extraction and sequencing workflow:
  - Extraction: MOBIO Powersoil 96-well kit.
  - Quality control: purity and yield assessed before sequencing.
  - Sequencing: 454 pyrosequencing to profile bacterial and eukaryotic biodiversity within each sample.
- Data processing:
  - Sequences clustered into OTUs.
  - OTU tables provide relative abundance per sample (percentage composition).

## Data provenance, contributors, and documentation
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall.
- Data processing and mapping: Gearóid Webb.
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths.
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths.
- Related documentation and references: Protocol CEH Tellus SW.docx; WP4 water chemistry documentation for proximate chemical data.