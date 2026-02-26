# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

- Overview
  - A dataset and related metadata from molecular biodiversity analyses of epilithon (water) and soil samples collected in the Tamar catchment during winter 2013/2014.
  - Aims to enable GIS-based visualization and spatial analysis of microbial and eukaryotic communities alongside environmental chemistry data.

- Data files and structure
  - Environmental data files:
    - soil_env_data.csv
    - water_env_data.csv
  - Biodiversity (sequence) data files:
    - soil_bacteria_seq.csv
    - soil_eukaryotes_seq.csv
    - water_bacteria_seq.csv
    - water_eukaryotes_seq.csv
  - Protocol and documentation:
    - Protocol CEH Tellus SW.docx
  - Cross-referencing and identifiers:
    - Water_lab_ID links to biodiversity data (via water_env_data.csv)
    - Water_sample_ID corresponds to sample names in WP4 water chemistry dataset
    - Stone_ID identifies each of three stones at sampling locations (A, B, C)
    - Soil_ID cross-references soil biodiversity data with soil_env_data.csv
  - Data presentation:
    - OTU tables: rows = OTU IDs; columns = samples (linked to environmental data via IDs)
    - Example linkage: water_bacteria_seq.csv <-> water_env_data.csv via Water_lab_ID; soil_bacteria_seq.csv <-> soil_env_data.csv via Soil_ID

- Field methods and sampling design
  - Epilithon (water) sampling:
    - Sites chosen for broad spatial coverage from the Wolf River to the Tamar River; exact sites variably determined in the field.
    - GPS-based site localization using Garmin GPS12; three stones per location (A, B, C) with epilithon collected from a defined area.
    - Samples kept cold and transported to the laboratory for analyses.
  - Soil sampling:
    - Targeted soils across the Tamar catchment representing different land uses.
    - Exact sites selected in the field; GPS12 used for localization.
    - Soils collected and kept cold prior to laboratory analyses.
  - Spatial references provided:
    - NGR (1 km resolution to maintain site anonymity)
    - Eastings, Northings
    - Grid reference for soils

- Data content and processing
  - Molecular workflow:
    - DNA extracted from all soil and epilithon samples using the MOBIO Powersoil 96-well kit.
    - DNA quality checked before 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
    - Bioinformatic processing yields operational taxonomic units (OTUs); sequencing results expressed as percentage composition of OTUs per sample.
  - Data structure:
    - For each dataset, rows = OTU IDs; columns = sample IDs (aligned with the environmental data via the cross-referenced IDs).
  - Cross-dataset linkage:
    - OTU abundance data can be joined to corresponding environmental measurements using the IDs in the associated env_data.csv files (e.g., Water_lab_ID or Soil_ID).

- Contributors and provenance
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
  - General project description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014
  - Version: 1.0; date: 24/03/14; author: R. Griffiths

- GIS relevance and use considerations
  - Spatial data types available: coordinate-based locations (Eastings/Northings), 1 km grid references, and site identifiers (NGR).
  - Enables mapping of biodiversity metrics (OTU abundance per sample) alongside environmental chemistry variables (soil and water) at corresponding sites.
  - Cross-referencing IDs permit integrating sequencing data with environmental layers for spatial analyses and visualization.
  - Anonymization via 1 km grid resolution may limit precise site-level disclosure in maps.

- Limitations and data quality notes
  - Data are from winter 2013/2014; methodological details and units for soil chemistry are pending in fuller methodological descriptions.
  - Data volume may be large and complex due to multi-dataset integration and varying resolutions.
  - Consistency of data standards across datasets may require harmonization prior to GIS integration.
  - Accurate linking depends on correct interpretation of cross-reference identifiers (e.g., Water_lab_ID, Soil_ID) across files.

- How to use in GIS workflows
  - Import environmental CSVs as attribute layers and join on the appropriate IDs to OTU abundance datasets.
  - Create spatial layers for sampling sites using Eastings/Northings or Grid References; preserve anonymity with 1 km grid references where required.
  - Visualize spatial patterns of microbial and eukaryotic communities and relate them to soil and water chemistry across the Tamar catchment.
  - Use the Protocol CEH Tellus SW as accompanying metadata for methodological context and reproducibility.