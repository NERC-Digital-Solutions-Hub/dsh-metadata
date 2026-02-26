# Version control: 1.0, date = 24/03/14. 1.0, description = created. 1.0, author = R.Griffiths

## Overview
- A dataset documenting a suite of molecular biodiversity analyses (epilithon in water and soil samples) from the Tamar catchment collected in winter 2013/2014.
- Includes both environmental chemistry data and sequencing-based biodiversity data across multiple taxonomic groups.

## Data assets and structure
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Biodiversity datasets (DNA-based):
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
- Data organization:
  - Rows in sequencing datasets are OTU IDs; columns correspond to samples.
  - Cross-referenced via IDs to environmental data files (see cross-referencing below).

## Data collection and processing
- Field sampling
  - Epilithon (water): 20 locations along a transect from Wold River to Tamar River; three stones per location; exact sites chosen in the field; GPS coordinates recorded; samples kept cold and transported to lab.
  - Soil: range of soils with varying land uses; approximate locations from maps; exact sites determined in field; samples collected per protocol; GPS coordinates recorded.
- Laboratory and sequencing
  - DNA extraction: MOBIO Powersoil 96-well kit.
  - Quality checks: DNA purity and yield assessed prior to sequencing.
  - Sequencing: 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
  - Data processing: sequences clustered into operational taxonomic units (OTUs); results expressed as the percentage of each OTU within each sample.

## Metadata and cross-referencing
- Cross-referencing keys
  - Water data: Water_lab_ID (unique lab identifier) cross-references biodiversity data; Water_sample_ID links to WP4 water chemistry dataset sample names.
  - Epilithon/biodiversity links: water_bacteria_seq.csv and water_eukaryotes_seq.csv use Water_lab_ID to map to water_env_data.csv.
  - Soil biodiversity links: soil_bacteria_seq.csv and soil_eukaryotes_seq.csv use Soil_ID to map to soil_env_data.csv.
- Sample identifiers and location data
  - Epilithon: Stone_ID (A, B, C per site), SAMPLING DATE, RIVER, CATCHMENT, NGR, Eastings, Northings.
  - Soils: Soil_ID, Sampling date, Grid reference (1 km, anonymized), depth of core, followed by soil chemistry measurements.
- Protocols and documentation
  - Field sampling and analysis guided by Protocol CEH Tellus SW.docx.
  - Full methodological descriptions for soil chemistry procedures are awaited.

## Data quality, standards, and provenance
- Provenance
  - Contributors include field collection teams, data processing/mapping, laboratory analysis, and project planning/management.
  - Version 1.0 metadata captured (date, author, description).
- Quality assurance
  - DNA quality checks prior to sequencing; OTU-level abundance data generated.
  - Soil chemistry data include a defined set of chemical properties (Dry mass, C-total, Loss on Ignition, N-total, pH, and multiple elements).
- Anonymization and data governance
  - Soil site coordinates are masked to 1 km grid references to protect site anonymity.
  - Data integrity relies on explicit cross-referencing IDs across environmental and biodiversity datasets.

## Access, governance, and provenance
- Clear documentation of data lineage and responsibilities:
  - Sample collection: listed contributors.
  - Data processing and mapping: listed contributors.
  - Laboratory analysis: listed contributors.
  - Planning and management: listed contributors.
- Data lifecycle considerations
  - Environmental context (water and soil) linked to biodiversity data via standardized IDs.
  - Documentation supports reuse and integration with wider datasets or networks.

## Use and impact for data leadership
- Enables integrated analyses of biodiversity with environmental context (water and soil chemistry) in the Tamar catchment.
- Supports cross-dataset linkage (OTU data to environmental metadata) for ecosystem-level insights.
- Provides a governance and documentation framework (IDs, cross-links, anonymization, QC steps) that can inform data stewardship practices in similar projects.

## Key challenges and considerations for data leadership
- Discoverability and integration
  - Multiple files and cross-references require careful data discovery and mapping to enable end-to-end analyses.
- Metadata completeness
  - Some methodological details (full soil chemistry procedures) are pending; ensure complete metadata for reuse.
- Data scope and audience
  - Dataset serves potentially diverse user groups (ecologists, policy colleagues, data scientists); consider co-ownership and clear user-friendly documentation.
- Privacy and anonymity
  - Anonymization via 1 km grid references may limit site-specific analyses; balance between data utility and privacy.