# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A dataset suite of molecular biodiversity analyses from epilithon (water) and soil samples in the Tamar catchment, collected in winter 2013/2014.
- Combines environmental chemistry data with high-throughput sequencing to profile bacterial and eukaryotic communities.
- Designed for map-based visualization and spatial analysis across sampling sites along a transect from the Wolf River to the Tamar River.
- Key workflow: field collection → GPS-based site localization → DNA extraction → 454 pyrosequencing → OTU clustering → cross-referencing with environmental data.
- Provenance includes clearly defined roles (sample collection, lab analysis, data processing, planning, management).

## Data files (GIS-relevant and linking keys)
- Environmental data
  - soil_env_data.csv: soil_ID (link to biodiversity data), sampling date, Grid Reference (1 km resolution for anonymity), depth, and soil chemistry (Dry matter, C-total, Loss on Ignition, N-total, pH, and multiple elements: Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
  - water_env_data.csv: Water_lab_ID (lab identifier), Water_sample_ID (cross-reference to WP4 water chemistry dataset), Stone_ID (A, B, C per site), sampling date, RIVER, CATCHMENT, NGR, Eastings, Northings.
- Biodiversity data (OTU-based, map-ready linkage)
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Structure: rows = OTU IDs; columns = sample cross-reference IDs; column 1 matches Water_lab_ID or Soil_ID in the respective environmental CSVs.
- Cross-referencing example
  - Epilithon bacteria: first column in water_bacteria_seq.csv matches Water_lab_ID in water_env_data.csv.
  - Epilithon eukaryotes, Soil bacteria, and Soil eukaryotes follow the same cross-reference pattern with their corresponding env data.

## Field methods and spatial scope
- Epilithon (water samples)
  - Approximately 20 sampling locations chosen to achieve wide spatial coverage from the Wolf River to the Tamar River.
  - Exact sites determined in the field for accessibility; GPS (Garmin GPS12) used to locate sites.
  - Three stones sampled at each location; samples kept cold for laboratory analyses.
- Soil samples
  - Targeted soils across the Tamar region representing varied land uses to capture spatial heterogeneity.
  - Exact site locations determined in the field; GPS used; samples kept cold for lab analyses.
  - 1 km grid reference used to anonymize soil locations.

## Data processing and biodiversity data
- DNA extraction and sequencing
  - DNA extracted from all soil and epilithon samples using MOBIO Powersoil kit.
  - Quality checks performed before 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
- OTU processing
  - Sequences clustered into operational taxonomic units (OTUs).
  - Data tables display the percentage of each OTU within each sample.
- Linking data
  - OTU rows = OTU IDs; OTU values are aligned to samples via cross-referenced IDs (Water_lab_ID, Water_sample_ID, Soil_ID).
  - Example cross-linking notes provided in the documentation to map OTUs to corresponding environmental data files.

## GIS considerations and potential uses
- Spatial localization
  - Coordinates available as NGR and Eastings/Northings; also maintains anonymized 1 km grid references for soils to protect site anonymity.
- Map-based analyses
  - Combine environmental chemistry with OTU profiles to visualize spatial patterns of biodiversity and habitat chemistry across the catchment.
  - Integrate epilithon and soil biodiversity with hydrological context along the Wolf–Tamar transect.
- Data quality and standards
  - Methodological details for soil chemistry procedures are pending; existing data include key chemical measurements and reference IDs for linking datasets.
  - DNA-based biodiversity data are processed to OTUs with clear cross-referencing to environmental measurements.

## Provenance, contributors, and version
- Version: 1.0 (dated 24/03/14); author: R. Griffiths.
- Contributors by role:
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- Scope: winter 2013/2014 sampling; suite of molecular analyses from epilithon and soil samples in the Tamar catchment.