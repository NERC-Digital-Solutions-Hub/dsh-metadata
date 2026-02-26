# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- Dataset describes a suite of molecular analyses on epilithon (water) and soil samples from the Tamar catchment, winter 2013/2014.
- Data files include both environmental metadata and biodiversity sequencing data.
- DNA was extracted from all samples, sequenced for bacterial and eukaryotic biodiversity, and processed into OTU tables.

## Data files and structure
- Data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Biodiversity data format:
  - OTU tables: rows are OTU IDs; columns cross-reference samples.
  - Columns link to environmental data via IDs:
    - Epilithon bacteria: water_bacteria_seq.csv rows reference Water_lab_ID in water_env_data.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv rows reference Water_lab_ID in water_env_data.csv
    - Soil bacteria: soil_bacteria_seq.csv rows reference Soil_ID in soil_env_data.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv rows reference Soil_ID in soil_env_data.csv

## Field sampling and site design
- Epilithon (water) sampling:
  - Approximately 20 locations along a transect from the Wold River to the Tamar River.
  - Exact sites determined in the field for accessibility; GPS (Garmin GPS12) used to locate sites.
  - At each location, three stones sampled (designated A, B, C); samples kept cold and processed in the lab.
- Soil sampling:
  - Targeted soils across the Tamar region, spanning a range of land uses.
  - Exact sites determined in the field; location generalized to 1 km resolution grid reference for anonymity.
  - Soil cores collected per protocol and kept cold for laboratory analyses.

## Environmental data and metadata
- Epilithon water environment data (water_env_data.csv):
  - Water_lab_ID: unique lab identifier; cross-references biodiversity data
  - Water_sample_ID: cross-references with WP4 water chemistry dataset (sample names e.g., T1:20)
  - Stone_ID: A, B, or C
  - Sampling date, River, Catchment, NGR, Eastings, Northings
- Soil environmental data (soil_env_data.csv):
  - Soil_ID: unique lab identifier; cross-references biodiversity data
  - Sampling date
  - Grid reference: 1 km British National Grid Reference (anonymized)
  - Depth of core
  - Soil chemistry data (columns: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K)
  - Analysis conducted at CEH Lancaster; full methodological descriptions and units pending

## Biodiversity sequencing and processing
- DNA extraction: MOBIO Powersoil 96-well kit
- Quality control: purity and yield checked prior to sequencing
- Sequencing: 454 pyrosequencing to assess bacterial and eukaryotic biodiversity
- Data processing: sequencing reads clustered into OTUs; OTU tables show the percentage of each OTU within each sample

## Data linking and usage notes
- Cross-referencing guidance:
  - Water_bacteria_seq.csv and water_eukaryotes_seq.csv map to water_env_data.csv via Water_lab_ID
  - Soil_bacteria_seq.csv and soil_eukaryotes_seq.csv map to soil_env_data.csv via Soil_ID
- Combining datasets:
  - Join OTU tables with corresponding environmental metadata to explore links between biodiversity and water/soil chemistry, location, and sampling date
- Outputs to support self-service analyses:
  - Per-sample biodiversity profiles (OTU composition)
  - Environmental context (chemistry, geography, sampling dates) for each sample
  - Potential dashboards or reports linking microbial/eukaryotic diversity to environmental variables

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Practical considerations for data support
- Data anonymization: 1 km grid references used for soil sites
- Methodology note: full procedural details for soil chemistry pending; field protocols documented in Protocol CEH Tellus SW.docx
- Data re-use considerations: ensure proper cross-referencing with IDs when merging OTU data with environmental metadata; be mindful of platform-specific formatting (e.g., cross-reference keys) when joining datasets.