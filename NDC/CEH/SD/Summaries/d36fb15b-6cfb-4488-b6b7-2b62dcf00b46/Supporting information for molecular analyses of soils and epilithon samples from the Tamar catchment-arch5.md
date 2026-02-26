# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Suite of molecular analyses conducted on epilithon (water-associated) and soil samples from the Tamar catchment during winter 2013/2014.
- Aim aligned with assessing biodiversity (bacteria and eukaryotes) and linking to environmental data.

## Data files and structure
- Data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Biodiversity datasets:
  - OTU-based tables where rows are OTU IDs and columns reference samples.
  - Example cross-references:
    - Epilithon bacteria: water_bacteria_seq.csv corresponds to Water_lab_ID in water_env_data.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv corresponds to Water_lab_ID in water_env_data.csv
    - Soil bacteria: soil_bacteria_seq.csv corresponds to Soil_ID in soil_env_data.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv corresponds to Soil_ID in soil_env_data.csv

## Sampling methods and geographic data
- Field sampling approach:
  - Epilithon (water samples): 20 locations sampled along a river transect; three stones per location; exact site positions determined in the field using a Garmin GPS12; samples kept cold en route to the lab.
  - Soil samples: Targeted soils across the Tamar region with diverse land uses; exact sites determined in the field; samples collected following defined protocol; positions recorded with GPS.
- Geographic data:
  - Locations anonymized to a 1 km resolution grid reference.
  - Epilithon data include: Water_lab_ID, Water_sample_ID, Stone_ID (A, B, C), Sampling date, River, Catchment, NGR, Eastings, Northings.
  - Soil data include: Soil_ID, Sampling date, Grid reference (1 km), depth of core, and soil chemistry measurements.

## Biodiversity data and processing
- DNA extraction and sequencing:
  - DNA extracted from all soil and epilithon samples using MOBIO Powersoil 96-well kit.
  - Quality checks performed for purity and yield.
  - Sequencing performed using 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
- Data processing:
  - Sequences processed and clustered into operational taxonomic units (OTUs).
  - Data tables display the percentage representation of each OTU within each sample.
- Data linkage:
  - OTU data linked to corresponding environmental data via cross-reference IDs (Water_lab_ID, Water_sample_ID, Soil_ID).

## Cross-referencing and data linkage
- Cross-references between biodiversity data and environmental data:
  - Water datasets: Water_lab_ID in water_env_data.csv matches OTU tables in water_bacteria_seq.csv and water_eukaryotes_seq.csv.
  - Soil datasets: Soil_ID in soil_env_data.csv matches OTU tables in soil_bacteria_seq.csv and soil_eukaryotes_seq.csv.
- Example mapping notes:
  - Epilithon bacteria: water_bacteria_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv.
  - Epilithon eukaryotes: water_eukaryotes_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv.
  - Soil bacteria: soil_bacteria_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv.
  - Soil eukaryotes: soil_eukaryotes_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv.

## Data governance, provenance, and usage notes
- Versioning and stewardship:
  - Version 1.0, dated 24/03/2014; authors include sample collection, data processing/mapping, laboratory analysis, and planning/management contributors.
  - Documentation exists (Protocol CEH Tellus SW.docx) and field method descriptions.
- Data anonymization and access:
  - Site locations anonymized at 1 km resolution to protect site privacy.
  - Cross-referenced IDs used to connect datasets while preserving anonymity.
- Methodological notes and gaps:
  - Soil data column descriptions (chemistry measurements) and units are provided, with full methodological descriptions for soil procedures awaiting completion.
  - WP4 water chemistry documentation referenced for supplementary context.
- Quality and reuse considerations:
  - QA steps include DNA quality checks and OTU clustering; data are structured to enable integrated analyses across biodiversity and environmental datasets.
  - Users should ensure alignment of IDs across files and consult the Protocol and WP4 documentation for detailed methods and units.

## Contributors
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- Project description: General description of a suite of molecular analyses in epilithon and soil samples from the Tamar catchment (winter 2013/2014).