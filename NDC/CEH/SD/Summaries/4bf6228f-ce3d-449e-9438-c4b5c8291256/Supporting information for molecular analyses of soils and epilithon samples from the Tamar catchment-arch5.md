# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A dataset suite describing molecular analyses of epilithon (water) and soil samples collected from the Tamar catchment in winter 2013/2014.
- Samples include environmental chemistry data and biodiversity data (bacteria and eukaryotes) derived from DNA sequencing.
- Field sampling focused on spatial coverage, with site locations recorded and anonymized to a 1 km grid reference where appropriate.
- Data are organized to enable cross-referencing between environmental metadata and biodiversity results, with a clear lineage from sample collection to OTU tables.

## Data files and structure
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Biodiversity datasets are stored as OTU tables:
  - Rows: OTU IDs
  - Columns: samples cross-referenced to their respective environmental data files
  - Example cross-references:
    - Epilithon bacteria: water_bacteria_seq.csv <-> water_env_data.csv via Water_lab_ID
    - Epilithon eukaryotes: water_eukaryotes_seq.csv <-> water_env_data.csv via Water_lab_ID
    - Soil bacteria: soil_bacteria_seq.csv <-> soil_env_data.csv via Soil_ID
    - Soil eukaryotes: soil_eukaryotes_seq.csv <-> soil_env_data.csv via Soil_ID

## Data collection and methods
- General description: Suite of molecular analyses on epilithon and soil samples from the Tamar catchment (winter 2013/2014).
- Field methods:
  - Epilithon (water): Sampling sites chosen for broad spatial coverage along the Wolf–Tamar transect; exact sites determined in the field; samples collected from three stones per location; samples kept cold and transported to the lab.
  - Soil: Targeted soils across the Tamar region representing varying land uses; sites chosen for spatial coverage; exact locations determined in the field; samples collected following specified protocols.
  - Exact locations determined using a Garmin GPS12; storage and handling described (cold chain prior to laboratory analyses).
- Protocol reference: Protocol CEH Tellus SW.docx

## Metadata and data column details
- Water environmental data (water_env_data.csv):
  - Water_lab_ID: unique lab identifier for cross-referencing
  - Water_sample_ID: cross-references with sample names in WP4 water chemistry dataset
  - Stone_ID: A, B, C (three stones per location)
  - Sampling date, River, Catchment
  - NGR, Eastings, Northings
- Soil environmental data (soil_env_data.csv):
  - Soil_ID: unique lab identifier for cross-referencing
  - Sampling date
  - Grid reference: 1 km resolution (to anonymize exact sites)
  - Depth of core
  - Chemistry data columns: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K
  - Note: Analyses conducted at CEH Lancaster chemistry facility; full methodological descriptions and units pending
- Biodiversity data (OTU tables):
  - Data derived from MOBIO Powersoil 96-well DNA extraction
  - DNA quality-checked prior to 454 pyrosequencing
  - Sequences clustered into OTUs; data display percentage of each OTU within each sample
  - Data organization ensures cross-links to environmental data via the sample IDs described above

## Data provenance, governance, and sharing considerations
- Version control: Version 1.0, date 24/03/14; description and author noted (R. Griffiths)
- Contributors and roles:
  - Sample collection, data processing/mapping, laboratory analysis, planning/management
  - General description summarizes the study and collaborative effort
- Data provenance:
  - Clear linkage between field sampling, lab processing, sequencing, and downstream OTU analysis
  - Reference to a protocol document (Protocol CEH Tellus SW.docx) and to WP4 water chemistry documentation for further data details
- Location privacy and data access:
  - Site locations anonymized to 1 km grid references where applicable
  - Cross-dataset references enable integrated discovery without exposing precise site coordinates in raw data
- Considerations for data stewardship:
  - Ensure consistent use of IDs (Water_lab_ID, Water_sample_ID, Stone_ID, Soil_ID) across datasets
  - Maintain linkage between environmental metadata and biodiversity results (OTU tables)
  - Document methodological details and units for soil chemistry data when available
  - Plan for updates or new releases with clear versioning and data provenance notes

## Practical implications for data users and stewards
- The dataset provides a comprehensive, cross-referenced framework to study relationships between environmental chemistry and microbial/diversity composition in both epilithon and soil environments.
- Data stewards should maintain and communicate the cross-referencing scheme, ensure consistent ID usage, and document any methodological updates (especially for soil chemistry procedures and units).
- When integrating with WP4 or other datasets, users can leverage the explicit cross-links (IDs and sample references) to assemble a multi-domain view of the Tamar catchment samples.