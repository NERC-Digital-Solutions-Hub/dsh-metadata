# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- General description of a dataset comprising molecular analyses to assess bacterial and eukaryotic biodiversity in epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Focus on cross-referenced environmental data and corresponding biodiversity sequencing data.

## Data files included
- soil_env_data.csv
- soil_bacteria_seq.csv
- soil_eukaryotes_seq.csv
- water_env_data.csv
- water_bacteria_seq.csv
- water_eukaryotes_seq.csv
- Protocol CEH Tellus SW.docx

## Contributors
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Field methods

### Epilithon (water samples)
- Approximately 20 sampling locations selected to provide good spatial coverage from the Wold River to the Tamar River; exact sites determined in the field for accessibility and logistics.
- Location determined using a Garmin GPS12.
- Three stones taken at each location and epilithon collected from a defined area.
- Samples kept cold and transported to the laboratory for analyses.

### Soil samples
- Targeted a range of soils across the Tamar region representing various land uses.
- Approximate locations planned from maps for broad catchment coverage; exact sites determined in the field considering accessibility and logistics.
- Soil samples collected and kept cold; locations recorded with Garmin GPS12.

## Data structure and cross-referencing

### Epilithon water data
- water_env_data.csv
  - Water_lab_ID: unique laboratory identifier (cross-referenced with biodiversity data)
  - Water_sample_ID: cross-references the SAMPLE ID column of the WP4 water chemistry dataset (e.g., T1:20)
  - Stone_ID: A, B, or C to label each stone at a site
  - Sampling date; River; Catchment; NGR; Eastings; Northings

### Soil data
- soil_env_data.csv
  - Soil_ID: unique laboratory identifier (cross-referenced with biodiversity data)
  - Sampling date
  - Grid reference: 1 km resolution British National Grid Reference (anonymization)
  - Depth of core
  - Chemical measurements: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K

### Biodiversity sequencing datasets
- Epilithon bacteria: water_bacteria_seq.csv
- Epilithon eukaryotes: water_eukaryotes_seq.csv
- Soil bacteria: soil_bacteria_seq.csv
- Soil eukaryotes: soil_eukaryotes_seq.csv
- Data concept: DNA extracted using MOBIO Powersoil 96-well kit; quality checked; 454 pyrosequencing performed to assess bacterial and eukaryotic biodiversity.
- Data organization: after processing, sequences clustered into operational taxonomic units (OTUs). For each dataset:
  - Rows: OTU IDs
  - Columns: sample IDs cross-referenced to the corresponding environmental data (via the IDs below)

### Cross-referencing examples
- Epilithon bacteria: water_bacteria_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv
- Epilithon eukaryotes: water_eukaryotes_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv
- Soil bacteria: soil_bacteria_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv
- Soil eukaryotes: soil_eukaryotes_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv

## Sequencing and data processing
- Method: DNA extraction, 454 pyrosequencing
- Bioinformatics: sequences clustered into OTUs; abundances expressed as percentages of each OTU within each sample
- Output enables comparison of microbial and microeukaryotic community composition across water and soil samples in relation to measured environmental variables. 

## Additional notes
- Protocol CEH Tellus SW.docx included as part of the data package.
- Soil chemistry section indicates that full methodological descriptions and units are awaited at the time of documentation.