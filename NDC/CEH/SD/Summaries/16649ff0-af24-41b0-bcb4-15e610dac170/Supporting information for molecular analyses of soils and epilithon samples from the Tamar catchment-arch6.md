# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.

## Overview
- Suite of molecular analyses conducted on epilithon (water) and soil samples collected from the Tamar catchment in winter 2013/2014.
- DNA was extracted from all samples, quality checked, and subjected to 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
- Sequencing data were processed into OTUs, with data tables showing the percentage of each OTU within each sample.
- Datasets include environmental (soil and water) metadata and biodiversity (OTU) data, enabling cross-referenced analyses.

## Datasets included
- Soil_env_data.csv: soil sample metadata and chemistry results.
  - Key fields: Soi l_ID, Sampling date, Grid reference (1 km resolution), depth of core, and chemical measurements (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- Water_env_data.csv: epilithon (water) sample metadata.
  - Key fields: Water_lab_ID (unique lab identifier), Water_sample_ID, Stone_ID (A/B/C), Sampling date, River, Catchment, NGR, Eastings, Northings.
  - Water_sample_ID cross-references the WP4 water chemistry dataset’s sample names.
- Biodiversity datasets (OTU abundance matrices):
  - water_bacteria_seq.csv (epilithon bacteria)
  - water_eukaryotes_seq.csv (epilithon eukaryotes)
  - soil_bacteria_seq.csv (soil bacteria)
  - soil_eukaryotes_seq.csv (soil eukaryotes)
  - Structure: rows = OTU IDs; columns cross-reference with environmental data via sample IDs.
- Cross-reference guidance:
  - Epilithon bacteria: first column equals Water_lab_ID in water_env_data.csv
  - Epilithon eukaryotes: first column equals Water_lab_ID in water_env_data.csv
  - Soil bacteria: first column equals Soil_ID in soil_env_data.csv
  - Soil eukaryotes: first column equals Soil_ID in soil_env_data.csv
- Protocol CEH Tellus SW.docx referenced for methodology details.

## Field methods and sample collection
- Epilithon (water): sampling sites chosen from maps to ensure broad spatial coverage from the Wolf River through to the Tamar River; exact sites determined in the field for accessibility; GPS via Garmin GPS12; three stones sampled per location (20 locations); samples kept cold and transported to the lab.
- Soil samples: targeting a range of soils across the Tamar region representing diverse land uses; approximate site locations from maps; exact sites determined in the field; GPS recorded; samples kept cold and transported to the lab.
- DNA extraction: MOBIO Powersoil 96-well kit; quality checked for purity and yield; proceeded to 454 pyrosequencing.

## Data processing and outputs
- Sequencing: 454 pyrosequencing performed to quantify bacterial and eukaryotic biodiversity.
- Processing: sequences clustered into OTUs; abundance tables show the percentage of each OTU within each sample.
- Data structure: biodiversity tables (OTU x sample) linked to environmental metadata via sample IDs (Water_lab_ID or Soil_ID).
- Outputs enable self-service data exploration and cross-analysis with environmental variables.

## Data quality and notes
- Some soil chemistry procedures' full methodological descriptions and units were pending at the time of documentation.
- Cross-referencing between biodiversity and environmental data is clearly defined to support integrative analyses.

## Provenance and contributors
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- Version: 1.0; date: 24/03/14; author: R. Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014.