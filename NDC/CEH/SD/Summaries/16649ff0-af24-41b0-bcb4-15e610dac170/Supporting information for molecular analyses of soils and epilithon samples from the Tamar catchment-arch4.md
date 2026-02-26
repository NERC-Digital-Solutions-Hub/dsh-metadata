# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

- Overview
  - A dataset comprising molecular analyses of epilithon (water) and soil samples from the Tamar catchment, collected in winter 2013/2014.
  - Focuses on biodiversity assessment via DNA sequencing (bacteria and eukaryotes) across environmental samples.

- Data assets (files)
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
  - Metadata and cross-reference structure: datasets include unique lab identifiers for cross-linking with biodiversity data.

- Data collection and field methods
  - Epilithon (water) sampling: 20 locations along a transect from the Wolf/Tamar area; three stones sampled per location; GPS-derived exact site locations; samples kept cold and brought to laboratory for analysis.
  - Soil sampling: range of soils from Tamar region with various land uses; approximate site locations from maps with field-identified exact sites; three cores per sampling event; samples kept cold and transported to lab.
  - Site anonymity: exact locations recorded as grid references (1 km resolution) to protect site confidentiality.

- Laboratory methods and data types
  - DNA extraction: MOBIO Powersoil 96-well kit; quality and yield checked prior to sequencing.
  - Sequencing: 454 pyrosequencing to assess bacterial and eukaryotic biodiversity; data clustered into OTUs (operational taxonomic units).
  - Data outputs per dataset: OTU tables with rows as OTU IDs and columns cross-referencing sample metadata.
  - Cross-referencing example: OTU data columns link to the corresponding environmental data via lab/sample IDs (e.g., Water_lab_ID matches water_env_data.csv; Soil_ID matches soil_env_data.csv).

- Biodiversity datasets and cross-referencing
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Cross-links: each OTU table row references sample metadata; sample IDs tie the biodiversity data back to environmental chemistry and sampling details in the respective env_data CSVs.

- Environmental data and content
  - Epilithon water chemistry cross-reference: water_env_data.csv includes Water_lab_ID, Water_sample_ID, Stone_ID (A/B/C), sampling date, river, catchment, grid references (NGR), Eastings/Northings.
  - Soil chemistry: soil_env_data.csv includes Soil_ID, sampling date, grid reference (1 km resolution), depth of core, followed by chemistry variables (Dry, C-total, Loss on Ignition, N-total, pH, various metals and nutrients).

- Data quality, standards, and metadata
  - Metadata fields defined for sampling and chemistry data; some methodological details and units pending in full descriptions.
  - Data quality checks performed on DNA (purity/yield) prior to sequencing; sequencing and OTU clustering described at a high level.
  - Documentation references additional WP4 water chemistry data for proximity context; full methodological standardization and units may be pending.

- Data governance and stewardship considerations
  - Multiple data silos (soil vs. water; chemistry vs. sequencing) require careful cross-referencing via IDs.
  - Anonymization via 1 km grid references supports privacy while enabling spatial analyses.
  - Protocol document (Protocol CEH Tellus SW.docx) underpins methodological transparency; ongoing need for complete methodological descriptions and units.

- Contributors and responsibilities
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
  - Overall scope: General description indicates a coordinated effort across field collection, lab analysis, and data integration.

- Implications for data leaders
  - Demonstrates the importance of cross-linking diverse data types (environmental chemistry and biodiversity sequencing) through consistent identifiers.
  - Highlights challenges in data standardization, metadata completeness, and ensuring discoverability across datasets.
  - Illustrates governance needs for documentation, versioning, and collaboration across partners and data communities.
  - Provides a model for anonymized spatial data handling while enabling robust, multi-dimensional analyses across ecosystems.