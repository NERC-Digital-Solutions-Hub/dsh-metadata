# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Objective and Scope
- Conduct molecular biodiversity analyses on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Provide standardized datasets combining environmental chemistry, habitat context, and OTU-level biodiversity data to support environmental health monitoring and policy performance assessment.

## Datasets and File Catalog
- Environmental chemistry and metadata
  - soil_env_data.csv
  - water_env_data.csv
- Biodiversity sequence data (OTU tables)
  - soil_bacteria_seq.csv (soil bacteria OTUs)
  - soil_eukaryotes_seq.csv (soil eukaryotes OTUs)
  - water_bacteria_seq.csv (epilithon bacteria OTUs)
  - water_eukaryotes_seq.csv (epilithon eukaryotes OTUs)
- Protocols
  - Protocol CEH Tellus SW.docx

## Field Sampling Methodology
- Epilithon (water samples)
  - Approximately 20 sampling locations selected to achieve good spatial coverage from the Wolf River through to the Tamar River.
  - Exact site locations determined in the field; GPS (Garmin GPS12) used for coordinates.
  - Three stones sampled per location; epilithon scraped from a defined area; samples kept cold and processed in the lab.
- Soil samples
  - Range of soils targeted across the Tamar region to capture diverse land uses.
  - Exact sites determined in the field with accessibility and logistics in mind.
  - GPS-based coordinates recorded; soil sampling conducted under a defined protocol; samples kept cold and processed in the lab.
  - 1 km grid reference (BNG) used to anonymize site locations.

## Laboratory and Bioinformatics Methods
- DNA extraction and sequencing
  - DNA extracted from all soil and epilithon samples using MOBIO Powersoil 96-well kit.
  - DNA quality checked for purity and yield prior to sequencing.
  - Sequencing performed via 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
- Data processing
  - Sequencing reads clustered into operational taxonomic units (OTUs).
  - Data tables show the percentage of each OTU within each sample.
- Cross-referencing and data structure
  - Water epilithon data cross-referenced to environmental data via Water_lab_ID and Water_sample_ID.
  - Soil data cross-referenced to environmental data via Soil_ID.
  - Example mappings provided to align OTU tables with corresponding environmental datasets.

## Data Structures and Cross-References
- Epilithon bacteria: water_bacteria_seq.csv
  - Column 1 corresponds to Water_lab_ID in water_env_data.csv.
- Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Column 1 corresponds to Water_lab_ID in water_env_data.csv.
- Soil bacteria: soil_bacteria_seq.csv
  - Column 1 corresponds to Soil_ID in soil_env_data.csv.
- Soil eukaryotes: soil_eukaryotes_seq.csv
  - Column 1 corresponds to Soil_ID in soil_env_data.csv.
- Environmental datasets
  - water_env_data.csv provides sampling context (Water_lab_ID, Water_sample_ID linked to WP4 water chemistry data, Stone_ID A/B/C, date, river, catchment, coordinates).
  - soil_env_data.csv provides sampling date, 1 km grid reference, core depth, and soil chemistry measurements (Dry, C-total, Loss on Ignition, N-total, pH, and trace elements: Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).

## Data Quality, Standards, and Access
- Data were quality checked for purity/yield prior to sequencing; subsequent bioinformatic processing produced OTU-based outputs.
- Soil chemistry methodology and units are pending full methodological descriptions at the time of documentation; data are prepared for integration with other datasets and standardised reporting formats.
- Outputs are designed for storage and upload to appropriate data portals, promoting accessibility of both final outputs and underlying data.

## Provenance, Contributors, and Documentation
- Version control: 1.0, dated 24/03/14; description “created.”
- Contributors
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses applied to epilithon and soil samples from the Tamar catchment (winter 2013/2014).
- Field and protocol notes reference Protocol CEH Tellus SW.docx for standardized procedures.

## Notes for Analysts and Use Cases
- The integrated datasets enable monitoring environmental health over time by combining chemistry, habitat context, and microbial/eukaryotic biodiversity.
- Standardised cross-referencing between environmental data and biodiversity OTUs facilitates downstream analyses, mapping, and policy performance assessments.
- A key ongoing objective is increasing the utility of the datasets by integrating with additional data sources and ensuring broad access to underlying data used to generate final outputs.