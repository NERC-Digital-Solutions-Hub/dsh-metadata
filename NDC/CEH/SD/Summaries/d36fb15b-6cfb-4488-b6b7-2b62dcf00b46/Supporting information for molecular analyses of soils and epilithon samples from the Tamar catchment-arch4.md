# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Describes a suite of molecular analyses on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Combines environmental chemistry data with biodiversity data obtained from DNA sequencing.
- Data organized into multiple CSV files and accompanied by a protocol document.

## Data assets (files and purpose)
- Soil_env_data.csv
  - Metadata for soil samples: Soil_ID, sampling date, grid reference (1 km anonymization), depth, and soil chemistry variables.
  - Chemistry columns include: Dry, C-total, Loss on Ignition, N-total, pH, and concentrations of Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K.
- water_env_data.csv
  - Metadata for epilithon/water samples: Water_lab_ID (unique lab identifier), Water_sample_ID (cross-referenced to WP4 water chemistry dataset), Stone_ID (A/B/C), sampling date, river, catchment, NGR, Eastings, Northings.
- water_bacteria_seq.csv
  - Epilithon bacterial community data (OTU table) with rows as OTU IDs and columns cross-referencing Water_lab_ID.
- water_eukaryotes_seq.csv
  - Epilithon eukaryotic community data (OTU table) with OTU rows and sample cross-references.
- soil_bacteria_seq.csv
  - Soil bacterial community OTU table, cross-referenced by Soil_ID.
- soil_eukaryotes_seq.csv
  - Soil eukaryotic community OTU table, cross-referenced by Soil_ID.
- Protocol CEH Tellus SW.docx
  - Protocol document referenced for methodology.

## Data structure and cross-referencing
- Biodiversity datasets are presented as OTU tables:
  - Rows: OTU IDs
  - Columns: sample IDs cross-referenced to corresponding environmental data
- Cross-references:
  - Epilithon: water_bacteria_seq.csv and water_eukaryotes_seq.csv map to water_env_data.csv via Water_lab_ID.
  - Soil: soil_bacteria_seq.csv and soil_eukaryotes_seq.csv map to soil_env_data.csv via Soil_ID.
- Data linkage example: OTU tables connect to environmental data through the lab/sample identifiers (Water_lab_ID / Soil_ID) listed in the env data files.
- Spatial data are anonymized using 1 km grid references for soil sampling.

## Methods and data processing
- DNA extraction: MOBIO PowerSoil kit (96-well format) used for all soil and epilithon samples.
- Quality control: DNA purity and yield checked prior to sequencing.
- Sequencing: 454 pyrosequencing performed to assess bacterial and eukaryotic biodiversity within each sample.
- Data processing: sequences clustered into operational taxonomic units (OTUs); final data tables report the percentage of each OTU within each sample.

## Sampling and field details
- Epilithon (water) sampling:
  - Sites chosen to provide broad spatial coverage along the Wolf River through to the Tamar River.
  - Exact sampling sites determined in the field; GPS coordinates recorded with a Garmin GPS12.
  - At each location, three stones were sampled (Stone_ID designations A, B, C).
  - Samples kept cold and transported to the laboratory for analyses.
- Soil sampling:
  - Targeted a range of soils across the Tamar region representing diverse land uses.
  - Exact site locations determined in the field; approximately mapped for initial coverage and refined in the field.
  - Grid references limited to 1 km to maintain site anonymity.
  - Soils sampled and stored for laboratory analysis following the specified protocol.

## Data governance, quality, and gaps
- Data management emphasizes clear cross-referencing between environmental and biodiversity data to enable integrated analyses.
- Some methodological details are still pending:
  - Full methodological descriptions and units for soil chemistry procedures are awaited.
- Documentation references related datasets (e.g., WP4 water chemistry dataset) for additional context on water chemistry data.

## Contributors and provenance
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples from the Tamar catchment in winter 2013/2014

## Relevance for data leaders
- Demonstrates end-to-end data stewardship: multiple related datasets, cross-referenced identifiers, and documentation of lineage.
- Supports collaboratives and co-ownership by aligning environmental and biodiversity data through common keys (Water_lab_ID, Soil_ID).
- Highlights data discoverability and interoperability through explicit cross-references between environmental metadata and OTU tables.
- Shows practical data quality practices (DNA QA/QC, anonymization via grid references) while identifying gaps (need for complete soil chemistry methodology and units).
- Indicates potential for broader data integration with partner datasets (e.g., WP4) to enrich analyses across data networks.