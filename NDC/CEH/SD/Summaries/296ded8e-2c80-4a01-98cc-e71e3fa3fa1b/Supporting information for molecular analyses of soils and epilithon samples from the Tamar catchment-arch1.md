# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A suite of molecular analyses conducted on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Aims to assess biodiversity (bacterial and eukaryotic) and relate it to environmental chemistry data.
- Field sampling covered a broad spatial area with anonymized location references (1 km grid) to protect site confidentiality.
- Cross-referenced datasets enable linking of chemical, geographic, and biodiversity information.

## Data files and structure
- soil_env_data.csv
  - Soil_ID (unique lab identifier)
  - Sampling date
  - Grid reference (1 km resolution; anonymity)
  - Depth of core
  - Soil chemistry data: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K
- water_env_data.csv
  - Water_lab_ID (unique lab identifier)
  - Water_sample_ID (cross-referenced to WP4 water chemistry dataset)
  - Stone_ID (A, B, C)
  - Sampling date
  - River, Catchment
  - NGR, Eastings, Northings
- Biodiversity datasets
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Each dataset: rows = OTU IDs; columns = samples
  - Data represent relative abundance (percentage) of OTUs per sample after 454 pyrosequencing and clustering
- Cross-references between biodiversity tables and environmental data
  - Epilithon bacteria: column 1 corresponds to Water_lab_ID in water_env_data.csv
  - Epilithon eukaryotes: column 1 corresponds to Water_lab_ID in water_env_data.csv
  - Soil bacteria: column 1 corresponds to Soil_ID in soil_env_data.csv
  - Soil eukaryotes: column 1 corresponds to Soil_ID in soil_env_data.csv
- Protocol CEH Tellus SW.docx (methodological reference)

## Sampling design and methods
- Field sampling
  - Epilithon (water): 20 locations along the Wolf/Tamar transect; three stones sampled per location; site locations chosen for broad spatial coverage; exact sites determined in the field; GPS12 used for coordinates; samples kept cold and transported to the lab.
  - Soils: range of soils across the Tamar region representing different land uses; exact sites determined in the field; location anonymized with 1 km grid references; samples kept cold and processed in the lab.
- Molecular analyses
  - DNA extraction: MOBIO Powersoil kit
  - Quality control: purity and yield checked prior to sequencing
  - Sequencing: 454 pyrosequencing to assess bacterial and eukaryotic biodiversity
  - Data processing: sequences clustered into OTUs; output tables show percentage of each OTU per sample

## Data provenance and cross-linking
- Unique identifiers (Water_lab_ID and Soil_ID) enable linking environmental data to biodiversity data.
- Data were processed and curated by multiple contributors across sampling, data processing/mapping, laboratory work, and project management.

## Data quality, notes, and limitations
- Soil chemistry methodology and units are not fully described in this document; full methodological descriptions are awaited.
- Water chemistry references exist in WP4 documentation for proximate datasets.
- Spatial data are anonymized to 1 km resolution for site confidentiality.
- As with many ecological datasets, integration across abiotic and biotic data relies on consistent sample IDs and cross-referencing columns.

## Usage considerations for analysts
- Rich, multi-layer dataset suitable for correlating soil/water chemistry with microbial and eukaryotic community composition.
- Cross-referenced OTU tables enable linking biodiversity patterns to specific environmental contexts (location, date, chemical variables).
- Potential data gaps due to awaiting methodological details for soil chemistry; users may need to consult WP4 documentation and Protocol CEH Tellus SW for full procedures.