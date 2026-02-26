# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- General description: A suite of molecular analyses on epilithon (water) and soil samples from the Tamar catchment, collected winter 2013/2014.
- Scope: Biodiversity profiling (bacteria and eukaryotes) via DNA sequencing; accompanying environmental chemistry data.
- Data files: Includes environmental data files (soil_env_data.csv, water_env_data.csv) and biodiversity sequence data (water_bacteria_seq.csv, water_eukaryotes_seq.csv, soil_bacteria_seq.csv, soil_eukaryotes_seq.csv) plus a protocol document (Protocol CEH Tellus SW.docx).

## Data components and architecture
- Environmental datasets
  - Epilithon water data: water_env_data.csv
  - Soil data: soil_env_data.csv
  - Key fields include unique lab identifiers (Water_lab_ID, Soil_ID), cross-references to biodiversity data, sample IDs, sampling dates, and location details (RIVER, CATCHMENT, NGR, Eastings, Northings). For soil, Grid reference is limited to 1km for site anonymity.
- Biodiversity datasets
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Structure: OTU-based tables with rows as OTU IDs and columns cross-referencing sample IDs to environmental data.
- Cross-referencing scheme
  - Example mappings: water_bacteria_seq.csv column 1 corresponds to Water_lab_ID in water_env_data.csv; soil_bacteria_seq.csv column 1 corresponds to Soil_ID in soil_env_data.csv.
- Methods and sequencing
  - DNA extraction: MOBIO Powersoil kit (96-well format)
  - Sequencing: 454 pyrosequencing to assess bacterial and eukaryotic biodiversity
  - Data processing: reads clustered into OTUs; resulting tables show relative abundance of OTUs per sample
- Protocols and documentation
  - Primary protocol: Protocol CEH Tellus SW.docx
  - Metadata fields and data structure documented within the environmental data files; full methodological descriptions and units for soil chemistry were awaited at the time.

## Sampling, field work, and data processing
- Field sampling design
  - Epilithon (water) sampling: 20 locations with approximate site locations selected for broad spatial coverage; exact sites chosen in the field for accessibility; three stones sampled at each location (A, B, C) and processed in the lab.
  - Soil sampling: Targeted soils across the Tamar region to capture a range of land uses; exact sites determined in the field with practical considerations; samples processed in the lab.
  - Location determination: GPS (Garmin GPS12) used to obtain precise coordinates; sites recorded and samples kept cold until lab analyses.
- Laboratory work
  - DNA extraction and quality checks performed before sequencing
  - Sequencing platform: 454 pyrosequencing
  - Post-sequencing: bioinformatic processing to cluster sequences into OTUs; data provided as OTU tables per sample
- Data linkage
  - Environmental data (sampling date, location, and identifiers) linked to biodiversity OTU data via sample IDs (Water_lab_ID, Soil_ID)

## Metadata, quality, and gaps
- Metadata visibility
  - Key metadata elements exist in the environmental data files (dates, locations, sampling IDs, cross-references)
- Quality and standardization
  - DNA quality checks conducted prior to sequencing
  - Soil chemistry procedures and units not fully described in the document; notes indicate that full methodological descriptions and units were awaited
  - Grid reference anonymization (1km) to protect site locations
- Data lineage and provenance
  - Contributors listed by role (sample collection, data processing/mapping, laboratory analysis, planning/management)
  - Version 1.0 dated 24/03/14; authorship by R. Griffiths
  - Reference to a protocol document and the WP4 dataset for additional context on water chemistry data

## Access, governance, and implications for data leaders
- Data governance
  - Clear mapping between environmental data and biodiversity sequence data via IDs
  - Cross-dataset linkage supports integrated analyses across environmental chemistry and biodiversity
- Community and collaboration
  - Indicates coordination with wider data workflows (e.g., WP4) and the potential for reuse within broader Tellus/CEH data ecosystems
- Practical implications for data strategy
  - Importance of complete methodological metadata (especially units and methods for soil chemistry) to enable reuse and comparability
  - Need for explicit data standards around IDs, cross-referencing keys, and documentation to improve discoverability and interoperability
  - Anonymization considerations (1km grid references) balance data utility with site privacy

## Takeaways for Data Leaders
- This dataset exemplifies integrating environmental metadata with biodiversity OTU data through stable identifiers, enabling multi-faceted analyses across chemistry and biology.
- Key actions to consider for data strategy
  - Ensure comprehensive metadata: provide full methodological descriptions, units, and QA steps for all measured variables (especially soil chemistry).
  - Strengthen data standards: formalize ID schemes and cross-reference mappings to improve discoverability and interoperability with related datasets (e.g., WP4).
  - Improve discoverability and lineage: document data provenance, processing steps, and any data transformations, including OTU clustering parameters.
  - Maintain data governance: uphold anonymization practices while offering sufficient spatial context for analyses; ensure versioning and updates over time.
  - Foster collaboration: align with wider data communities and protocols to support co-ownership and reuse of data products across networks.