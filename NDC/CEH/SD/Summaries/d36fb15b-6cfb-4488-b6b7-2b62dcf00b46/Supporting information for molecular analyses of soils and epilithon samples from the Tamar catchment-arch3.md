# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- Dataset description of molecular analyses on epilithon (water) and soil samples from the Tamar catchment, collected in winter 2013/2014.
- Aims to capture biodiversity and environmental conditions through DNA sequencing and soil/water chemistry data to support environmental health monitoring.

## Datasets included
- soil_env_data.csv
- soil_bacteria_seq.csv
- soil_eukaryotes_seq.csv
- water_env_data.csv
- water_bacteria_seq.csv
- water_eukaryotes_seq.csv
- Protocol CEH Tellus SW.docx

## Sampling design and field methods
- Epilithon (water) samples:
  - Location planning used maps to achieve broad spatial coverage from the Wold River to the Tamar River.
  - Exact sampling sites finalized in the field; GPS12 used for precise location.
  - Three stones sampled at each of 20 locations; epilithon collected from defined area; samples kept cold and transported to laboratory.
  - Water data labeled with Water_lab_ID and Water_sample_ID; Stone_ID designates sample stone (A, B, or C).
- Soil samples:
  - Targeted across the Tamar region to cover various land uses.
  - Spatially distributed to provide good catchment coverage; exact sites determined in the field.
  - GPS used for precise location; samples kept cold and brought to laboratory.
  - Soils recorded with SoIL_ID, sampling date, and Grid reference (restricted to 1 km resolution to preserve anonymity).

## Data content and structure
- Water chemistry data (referenced in WP4 documentation) linked to epilithon samples.
  - water_env_data.csv includes: Water_lab_ID, Water_sample_ID, Stone_ID (A/B/C), Sampling date, River, Catchment, NGR, Eastings, Northings.
- Soil chemistry data (analyzed at CEH Lancaster chemistry facility) includes:
  - soil_env_data.csv columns: SoIL_ID, Sampling date, Grid reference (1 km, anonymized), depth of core, plus chemistry metrics (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- Biodiversity datasets (DNA-based):
  - DNA extracted with MOBIO Powersoil 96-well kit; quality checked; 454 pyrosequencing performed to assess bacterial and eukaryotic biodiversity.
  - Sequencing results clustered into OTUs; outputs are OTU tables showing percentage of each OTU within each sample.
  - Datasets:
    - Epilithon bacteria: water_bacteria_seq.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv
    - Soil bacteria: soil_bacteria_seq.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Data organization: Rows represent OTU IDs; Columns correspond to samples; cross-referencing required with the respective environmental data files (e.g., water_lab_ID in water_env_data.csv aligns with columns in the sequencing data).

## Data linking and cross-references
- Unique laboratory identifiers (Water_lab_ID, SoIL_ID) used to cross-reference biodiversity data with environmental data.
- Example cross-references:
  - water_bacteria_seq.csv and water_env_data.csv linked via Water_lab_ID.
  - water_eukaryotes_seq.csv linked via Water_lab_ID.
  - soil_bacteria_seq.csv and soil_env_data.csv linked via SoIL_ID.
  - soil_eukaryotes_seq.csv linked via SoIL_ID.
- Cross-referencing ensures each OTU table can be related to corresponding sampling dates, locations, and environmental chemistry data.

## Data processing, quality, and governance
- Sequencing data processed to OTU level; percentage composition per sample is reported.
- Metadata and full methodological details for procedures and units are awaited or referenced in accompanying documentation.
- Data management practices include clear labeling, data cleaning and organization, and sharing of outputs through reports or dashboards; notes indicate potential barriers to data sharing (e.g., metadata completeness, anonymization, governance considerations).

## Contributors and roles
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- Scope: Suite of molecular analyses across epilithon and soil samples in the Tamar catchment.