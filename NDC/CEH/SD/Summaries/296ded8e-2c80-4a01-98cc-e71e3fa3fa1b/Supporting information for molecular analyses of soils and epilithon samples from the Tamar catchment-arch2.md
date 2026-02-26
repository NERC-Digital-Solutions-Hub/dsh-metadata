# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A dataset describing molecular biodiversity analyses of epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Includes environmental chemistry data and biodiversity sequence data (bacteria and eukaryotes) for both water and soil samples.
- Data are structured to allow cross-referencing between environmental measurements and biodiversity outputs via unique sample identifiers.

## Data files and structure
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Data organization:
  - Biodiversity datasets are expressed as OTU (operational taxonomic unit) tables:
    - Rows: OTU IDs.
    - Columns: sample-specific relative abundances.
  - Cross-referencing between datasets:
    - Epilithon bacteria: water_bacteria_seq.csv rows linked to water_env_data.csv via Water_lab_ID.
    - Epilithon eukaryotes: water_eukaryotes_seq.csv linked to water_env_data.csv via Water_lab_ID.
    - Soil bacteria: soil_bacteria_seq.csv linked to soil_env_data.csv via Soil_ID.
    - Soil eukaryotes: soil_eukaryotes_seq.csv linked to soil_env_data.csv via Soil_ID.

## Field sampling methods
- Epilithon (water samples):
  - 20 locations chosen along a path from the Wold River to the Tamar River to ensure spatial coverage.
  - Exact site locations determined in-field; GPS (Garmin GPS12) used for coordinates.
  - At each location, three stones were collected (designated A, B, C) and epilithon material collected from a defined area.
  - Samples kept cold and transported to the laboratory for analyses.
- Soil samples:
  - Targeted a range of soils across the Tamar region reflecting different land uses to capture variability.
  - Exact sampling sites determined in-field; coordinates captured via GPS.
  - Soil cores collected and kept cold prior to laboratory analyses.

## Laboratory methods and biodiversity data
- DNA extraction and sequencing:
  - DNA extracted from all soil and epilithon samples using MOBIO Powersoil 96-well DNA extraction kit.
  - DNA quality checked for purity and yield before sequencing.
  - Sequencing performed using 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
- Data processing:
  - Sequencing reads processed and clustered into OTUs.
  - Results stored as OTU percentage composition per sample.
- Data linking:
  - Detailed cross-referencing between biodiversity OTU tables and environmental data via the sample identifiers described above.
  - Example cross-links:
    - Epilithon bacteria (water_bacteria_seq.csv) column 1 corresponds to Water_lab_ID in water_env_data.csv.
    - Epilithon eukaryotes (water_eukaryotes_seq.csv) column 1 corresponds to Water_lab_ID in water_env_data.csv.
    - Soil bacteria (soil_bacteria_seq.csv) column 1 corresponds to Soil_ID in soil_env_data.csv.
    - Soil eukaryotes (soil_eukaryotes_seq.csv) column 1 corresponds to Soil_ID in soil_env_data.csv.

## Metadata and documentation
- Field and laboratory methods summarized; full methodological details are pending in related documentation.
- Protocol CEH Tellus SW.docx provides the overarching methodological framework referenced by the datasets.
- Environmental data columns include:
  - Water data: Water_lab_ID, Water_sample_ID, Stone_ID, Sampling date, River, Catchment, NGR, Eastings, Northings.
  - Soil data: Soil_ID, Sampling date, Grid reference (1 km resolution), depth of core, and a suite of soil chemistry measurements (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).

## Contributors and management
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses conducted on epilithon and soil samples from the Tamar catchment (winter 2013/2014)

## Access, reuse, and challenges
- Datasets are structured to enable verification and longitudinal comparisons of environmental health and policy performance over time.
- Key challenges and opportunities for analysts:
  - Increase dataset value by integrating these monitoring data with other relevant datasets (beyond single-use analyses).
  - Ensure broad access to underlying data used to create final outputs, enabling broader scrutiny and reuse.