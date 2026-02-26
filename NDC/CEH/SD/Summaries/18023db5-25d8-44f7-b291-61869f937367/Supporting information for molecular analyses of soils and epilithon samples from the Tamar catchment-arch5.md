# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- General description: Suite of molecular analyses to assess biodiversity in epilithon (water-associated biofilm) and soils from the Tamar catchment during winter 2013/2014.
- Time/location: Winter 2013/2014; Tamar catchment (UK).
- Data scope: Environmental measurements (soil and epilithon) and biodiversity data (bacteria and eukaryotes) derived from DNA metabarcoding.

## Data files and contents
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx

- Environmental datasets:
  - Epilithon (water) dataset: water_env_data.csv
    - Water_lab_ID: unique lab identifier for cross-referencing with biodiversity data
    - Water_sample_ID: cross-references to WP4 water chemistry dataset sample names
    - Stone_ID: labels for the three stones sampled per location (A, B, C)
    - Sampling date, River, Catchment, NGR, Eastings, Northings

  - Soil dataset: soil_env_data.csv
    - Soil_ID: unique lab identifier for cross-referencing with biodiversity data
    - Sampling date: date cores were taken
    - Grid reference: 1 km resolution to anonymize sites
    - Depth of core
    - Soil chemistry data: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K

- Biodiversity datasets (OTU tables from metabarcoding):
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv

- Metadata and methods:
  - Protocol CEH Tellus SW.docx
  - DNA extraction: MOBIO Powersoil 96-well kit
  - Sequencing: 454 pyrosequencing for bacterial and eukaryotic biodiversity
  - Data processing: sequences clustered into operational taxonomic units (OTUs); data tables show OTU percentages per sample

## Data structure and cross-referencing
- OTU tables:
  - Rows: unique OTU IDs
  - Columns: sample-specific OTU percentages
  - Cross-referencing example:
    - Epilithon bacteria (water_bacteria_seq.csv) column 1 equals Water_lab_ID in water_env_data.csv
    - Epilithon eukaryotes (water_eukaryotes_seq.csv) column 1 equals Water_lab_ID in water_env_data.csv
    - Soil bacteria (soil_bacteria_seq.csv) column 1 equals Soil_ID in soil_env_data.csv
    - Soil eukaryotes (soil_eukaryotes_seq.csv) column 1 equals Soil_ID in soil_env_data.csv

## Data collection methods and governance
- Field sampling:
  - Epilithon: sampling sites chosen to cover spatial extent of the Wolf/Tamar transect; GPS (Garmin GPS12) used to determine exact sites; three stones per location; samples kept cold and transported to laboratory.
  - Soil: soils sampled across Tamar region to reflect land-use diversity; GPS-based site determination; field logistics considerations documented; samples kept cold for lab analyses.
- Data provenance:
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
  - General description: indicates study scope and dataset lineage
- Anonymization and data governance:
  - 1 km grid references used for soil location to protect site anonymity
  - Cross-referencing identifiers established for integration across environmental and biodiversity data

## Data quality, standards and interoperability
- Methods and QA:
  - DNA extraction and quality checks performed prior to sequencing
  - Sequencing data processed to OTUs; percentage composition per sample preserved
- Notes on methodology:
  - Full methodological descriptions for soil procedures are awaited
- Interoperability:
  - Clear cross-reference scheme between environmental and biodiversity datasets to enable integrated analyses

## Access, usage notes, and challenges
- Data linking:
  - Explicit cross-referencing rules facilitate combined analyses of chemical/physical soil data with microbial and eukaryotic biodiversity
- Potential challenges (as identified):
  - Incomplete understanding of user needs and priorities
  - Timely data return from contributors
  - Achieving standardization across data creators (especially metadata)
  - Handling multiple systems and formats, including challenging ones
  - Managing large datasets (e.g., OTU tables) and non-interoperable legacy formats
  - Dealing with outdated databases requiring bespoke solutions

## Contributors and roles (summary)
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths