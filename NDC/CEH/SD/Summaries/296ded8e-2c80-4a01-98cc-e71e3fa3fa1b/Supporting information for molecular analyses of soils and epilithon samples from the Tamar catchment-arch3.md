# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- Describes a suite of molecular biodiversity analyses performed on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Aims to assess bacterial and eukaryotic biodiversity using DNA sequencing and to relate biodiversity to environmental data.

## Datasets and files
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Biodiversity datasets are linked to environmental data via sample IDs.

## Field sampling and sites
- Epilithon (water) sampling:
  - Located to achieve broad spatial coverage from the Wolf River to the Tamar River.
  - Exact sampling sites chosen in the field for accessibility; GPS (Garmin GPS12) used to record locations.
  - At each location, three stones were sampled (A, B, C) and epilithon collected.
- Soil sampling:
  - Targeted a range of soils across the Tamar region to capture different land uses.
  - Exact site locations determined in the field; samples kept cold and transported to the lab.
  - Soil site coordinates limited to 1 km grid references to maintain anonymity.

## Data content and structure
- Water environmental data (water_env_data.csv):
  - Water_lab_ID: unique lab identifier (cross-reference with biodiversity data).
  - Water_sample_ID: cross-references the SAMPLE ID from WP4 water chemistry data.
  - Stone_ID: labels each stone at a site (A, B, C).
  - Sampling date, river, catchment, NGR, Eastings, Northings.
- Soil environmental data (soil_env_data.csv):
  - Soil_ID: unique lab identifier (cross-reference with biodiversity data).
  - Sampling date: date cores were taken.
  - Grid reference: 1 km British National Grid reference (anonymity of sites).
  - Depth of core; subsequent columns with soil chemistry data (Dry, C-total, Loss on Ignition, N-total, pH, and trace elements such as Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
  - Note: full methodological descriptions and units for soil chemistry procedures were still awaited at the time of documentation.
- Cross-referencing schema:
  - Epilithon bacteria: water_bacteria_seq.csv rows are OTUs; columns align with Water_lab_ID in water_env_data.csv.
  - Epilithon eukaryotes: water_eukaryotes_seq.csv similarly cross-referenced.
  - Soil bacteria: soil_bacteria_seq.csv cross-referenced to Soil_ID in soil_env_data.csv.
  - Soil eukaryotes: soil_eukaryotes_seq.csv cross-referenced similarly.

## Biodiversity analyses and processing
- DNA extraction: MOBIO Powersoil 96-well kit for all soil and epilithon samples.
- Quality checks: DNA purity and yield assessed before sequencing.
- Sequencing: 454 pyrosequencing used to assess bacterial and eukaryotic biodiversity per sample.
- Data processing: sequences clustered into operational taxonomic units (OTUs); datasets present OTU percentage composition per sample.
- Data organization:
  - Rows: OTU IDs.
  - Columns: Sample IDs (linked back to environmental data via the IDs described above).

## Metadata, linking, and handling
- Cross-referencing between biodiversity and environmental datasets via:
  - Water_lab_ID and Water_sample_ID linking epilithon data to water chemistry context (WP4 documentation).
  - Soil_ID linking soil biodiversity data to soil environmental data.
- Location data:
  - Epilithon: approximate site coverage mapped with exact site locations recorded in-field via GPS.
  - Soils: 1 km grid references to preserve site anonymity, with precise field locations determined in the field.
- Documentation and protocols:
  - A protocol document is provided (Protocol CEH Tellus SW.docx) as part of the data package.

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Data governance and access notes
- Exact site coordinates for soils are anonymized at 1 km resolution.
- Some methodological descriptions (soil chemistry procedures and units) were awaiting completion at the time of this document.
- Data are organized to allow cross-referencing across environmental and biodiversity datasets, enabling integrated analysis for monitoring and decision-making.