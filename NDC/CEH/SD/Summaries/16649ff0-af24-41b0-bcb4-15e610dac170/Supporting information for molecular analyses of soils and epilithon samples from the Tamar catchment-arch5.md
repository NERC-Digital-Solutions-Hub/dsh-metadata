# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- Suite of molecular analyses conducted on epilithon (water-associated biofilm) and soil samples from the Tamar catchment, collected in winter 2013/2014.
- Data types include environmental chemistry measurements and biodiversity data (bacteria and eukaryotes) derived from DNA sequencing.
- Data are organized with cross-referencing IDs to link environmental data with biodiversity results, enabling integrated analyses.

## Datasets included
- Environmental data:
  - soil_env_data.csv
  - water_env_data.csv
- Biodiversity sequence data:
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
- Protocol/documentation:
  - Protocol CEH Tellus SW.docx

## Data provenance and contributors
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- Description: suite of molecular analyses in epilithon and soil samples from the Tamar catchment (winter 2013/2014)

## Field sampling and locations
- Epilithon (water samples):
  - 20 locations chosen to provide good spatial coverage along the Wolf River to the Tamar River.
  - Exact sampling sites determined in the field; GPS (Garmin GPS12) used for localization.
  - At each location, three stones were sampled (A, B, C). Samples kept cold and processed in the laboratory.
- Soil samples:
  - Targeted a range of soils across the Tamar region reflecting different land uses.
  - Exact sites determined in the field with accessibility/logistics in mind; samples kept cold and processed in the laboratory.
- All site locations and sampling details are documented with cross-references to linked datasets.

## Data structure and cross-referencing
- Water data (water_env_data.csv):
  - Water_lab_ID: unique lab identifier (used to cross-reference biodiversity data)
  - Water_sample_ID: cross-references the SAMPLE ID in WP4 water chemistry data
  - Stone_ID: A, B, or C for each location
  - Sampling date, river, catchment, NGR/Eastings/Northings
- Soil data (soil_env_data.csv):
  - Soil_ID: unique lab identifier (cross-reference with biodiversity data)
  - Sampling date
  - Grid reference: 1 km resolution (anonymizes precise site)
  - Depth of core
  - Soil chemistry measurements (Dry, C-total, Loss on Ignition, N-total, pH, and various elements: Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K)
- Biodiversity data:
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Processing: DNA extracted with MOBIO Powersoil kit; quality check; 454 pyrosequencing; sequences clustered into OTUs; data tables show percent composition of OTUs per sample
  - Cross-referencing: OTU rows with sample columns; column 1 in each sequencing dataset matches the corresponding lab ID in the environmental data (e.g., water_bacteria_seq.csv column 1 = Water_lab_ID in water_env_data.csv)

## Data processing, quality, and outputs
- DNA extraction and sequencing performed for all soil and epilithon samples.
- Sequencing data processed to generate OTU-based community profiles; results provided as percentages of OTUs per sample.
- Metadata establish the linkage between environmental measurements and biodiversity data via unique IDs (Water_lab_ID, Soil_ID).

## Metadata, documentation, and standards
- Documentation available via:
  - Protocol CEH Tellus SW.docx
- Environmental data fields include sampling details, geospatial references (with anonymized grid references for soils), and standard chemistry measurements.
- Clear cross-references between environmental and biodiversity datasets to support integrative analyses.

## Data governance, access, and stewardship considerations
- Anonymization: soil sampling grid references are limited to 1 km to protect site anonymity.
- Data availability and limitations: explicit in the dataset structure to understand disclosure risks, potential proprietary constraints, or embargoes on sharing raw environmental chemistry or sequencing data.
- Publication and sharing: data uploading to appropriate portals and catalogues is anticipated to enhance discoverability and reuse.
- Documentation and provenance: detailed contributor and method information supports reproducibility and data stewardship.

## Practical challenges to anticipate
- Incomplete understanding of user needs and priorities in early planning phases.
- Timely receipt of data from multiple contributors and coordination across systems.
- Ensuring all data creators meet metadata and standardization requirements (e.g., consistent IDs, cross-references, and documentation).
- Managing data across diverse formats and large datasets (OTU tables and environmental chemistry data).
- Integrating legacy databases or non-interoperable formats with newer data management workflows.