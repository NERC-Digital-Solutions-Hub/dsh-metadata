# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- A dataset describing molecular biodiversity analyses and associated environmental chemistry data from epilithon (water) and soil samples collected in the Tamar catchment during winter 2013/2014.
- Integrates environmental chemistry with high-throughput biodiversity data (bacteria and eukaryotes) across multiple sites and sample types.
- Aims to support environmental monitoring, data quality, and cross-referencing of biodiversity signals with environmental parameters.

## Data files and contents
- soil_env_data.csv
- soil_bacteria_seq.csv
- soil_eukaryotes_seq.csv
- water_env_data.csv
- water_bacteria_seq.csv
- water_eukaryotes_seq.csv
- Protocol CEH Tellus SW.docx
- All datasets are linked via sample identifiers (Soil_ID, Water_lab_ID) to enable cross-referencing.

## Field Sampling and methods
- Epilithon (water) sampling
  - Approximately chosen sites to cover the Wold River through to the Tamar River.
  - Exact sampling locations determined in the field with GPS; three stones per location (A, B, C) were sampled from defined areas.
  - Samples kept cold and processed in the laboratory.
- Soil sampling
  - Targeted soils across the Tamar region representing different land uses.
  - Exact sites decided in the field for good spatial coverage; GPS coordinates recorded.
  - Soil cores collected to a specified depth; samples kept cold for laboratory analysis.
- Location and dating references
  - Sampling dates and river/catchment context recorded; exact coordinates gathered via Garmin GPS12.
- Protocol reference
  - Protocol CEH Tellus SW.docx governs sampling and handling procedures.

## Data structure and cross-referencing
- Water environmental data (water_env_data.csv)
  - Key fields: Water_lab_ID (lab-specific ID), Water_sample_ID (cross-references sample names in WP4 water chemistry), Stone_ID (A, B, C), SAMPLING DATE, RIVER, CATCHMENT, NGR, EASTINGS, NORTHINGS.
- Soil environmental data (soil_env_data.csv)
  - Key fields: Soil_ID (lab-specific ID), Sampling date, Grid reference (1 km resolution), depth of core, plus a suite of soil chemistry measurements.
  - The dataset includes columns: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K.
- Biodiversity datasets (OTU-based)
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Data are derived from DNA extractions (MOBIO Powersoil 96-well kit) and 454 pyrosequencing.
  - Processed data are clustered into operational taxonomic units (OTUs); table rows represent OTUs and columns represent samples.
  - Each biodiversity table’s columns cross-reference with the corresponding environmental data (e.g., OTU abundance per sample linked to Water_lab_ID or Soil_ID in the environmental datasets).

## Data processing and linking
- DNA extraction and sequencing
  - DNA extracted from all soil and epilithon samples.
  - Quality checked for purity and yield before 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
- OTU processing
  - Sequences clustered into OTUs; abundance tables produced per sample.
- Cross-referencing scheme
  - Example mappings:
    - Epilithon bacteria: columns in water_bacteria_seq.csv link to water_env_data.csv via Water_lab_ID.
    - Epilithon eukaryotes: columns in water_eukaryotes_seq.csv link to water_env_data.csv via Water_lab_ID.
    - Soil bacteria: columns in soil_bacteria_seq.csv link to soil_env_data.csv via Soil_ID.
    - Soil eukaryotes: columns in soil_eukaryotes_seq.csv link to soil_env_data.csv via Soil_ID.
- Overall data organization supports integrated analyses, enabling analysis of biodiversity patterns alongside environmental chemistry and spatial context.

## Quality, management, and accessibility
- Data are organized for monitoring and scrutiny of environmental health and policy performance over time.
- Data capture follows standardized methods with explicit identifiers to ensure traceability and reproducibility.
- Data were planned and managed by a team across sampling, processing, and analysis, with clear attribution to contributors.
- Indicates stored datasets and preparation for availability in appropriate data portals (data management and sharing intent noted).

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Temporal scope and study area
- Winter 2013/2014
- Tamar catchment, with epilithon samples from the Wold River to the Tamar River and soil samples across the Tamar region
- 20 locations for epilithon sampling (three stones per location) and a range of soil sampling sites reflecting diverse land uses

## Key use case for analysts monitoring the environment
- Enables tracking of biodiversity signals (bacteria and eukaryotes) across time and space in relation to soil chemistry and water chemistry.
- Supports assessments of environmental health, potential impacts of land use changes, and policy performance through integrated OTU data and environmental parameters.
- Provides a framework for reproducible data integration, cross-referencing of biological and chemical datasets, and scalable monitoring over time.