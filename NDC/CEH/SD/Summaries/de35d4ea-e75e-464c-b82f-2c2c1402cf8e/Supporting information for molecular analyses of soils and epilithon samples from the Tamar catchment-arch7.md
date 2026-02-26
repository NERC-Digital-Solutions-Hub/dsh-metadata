# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A dataset suite of molecular analyses (bacteria and eukaryotes) from epilithon (water) and soils in the Tamar catchment, collected winter 2013/2014.
- Designed for GIS-enabled mapping and spatial exploration of biodiversity alongside environmental data.

## Spatial data and sampling geometry
- Field sites: 20 locations; sampling aimed for good spatial coverage along the Wolf/Tamar transect; exact sites determined in the field.
- Positioning: Garmin GPS12 used to locate sites; coordinates included or anonymized at 1 km grid for soils.
- Data integration hooks: Cross-referenced identifiers across environmental and biodiversity datasets enable map-based analyses.
- Epilithon sampling: Three stones per location (A, B, C) with water chemistry context referenced in WP4 documentation.

## Datasets and data structure
- Environmental data files
  - water_env_data.csv: Water_lab_ID (unique lab identifier), Water_sample_ID, Stone_ID (A/B/C), Sampling date, River, Catchment, NGR, Eastings, Northings.
  - soil_env_data.csv: Soil_ID (unique lab identifier), Sampling date, Grid reference (1 km BNGR), depth of core, and soil chemistry metrics (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- Biodiversity datasets (OTU tables)
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
- Cross-referencing convention
  - First column of each OTU table is an OTU ID.
  - OTU data columns align with sample IDs that correspond to the respective environmental data (e.g., water_bacteria_seq.csv column 1 equals Water_lab_ID in water_env_data.csv; soil_eukaryotes_seq.csv column 1 equals Soil_ID in soil_env_data.csv).

## Data provenance and processing
- DNA extraction: MOBIO Powersoil 96-well kit; quality checked before sequencing.
- Sequencing: 454 pyrosequencing for bacterial and eukaryotic biodiversity assessment.
- Data processing: Sequences clustered into OTUs; data tables present the percentage composition of each OTU per sample.

## Usage and GIS considerations
- Geographic linkage: Use NGR/Eastings/Northings (and 1 km grid for soils) to map sampling locations and overlay with environmental chemistry and OTU distributions.
- Data integration: Join biodiversity OTU matrices to environmental metadata via Water_lab_ID or Soil_ID to analyze spatial patterns of biodiversity in relation to chemistry and location.
- Data scale: Be mindful of differing resolutions (point locations vs. OTU percentages) and anonymization for soil sites (1 km grid), which affects precision for fine-scale mapping.
- Temporal scope: Snapshot from winter 2013/2014; interpretations constrained to that period.

## Limitations and considerations
- Data compiled from multiple sources; ensure consistent identifiers and units when merging.
- Soil site coordinates are anonymized to 1 km; precision limited for fine-scale mapping.
- Full methodological descriptions for soil chemistry procedures are pending; interpretation of chemical data should consider potential methodological gaps.

## Contributors
- Field collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths

## File list
- soil_env_data.csv
- soil_bacteria_seq.csv
- soil_eukaryotes_seq.csv
- water_env_data.csv
- water_bacteria_seq.csv
- water_eukaryotes_seq.csv
- Protocol CEH Tellus SW.docx