# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Aimed at characterising bacterial and eukaryotic biodiversity in epilithon (water-bound biofilms on stones) and soils across the Tamar catchment during winter 2013/2014.
- Data comprise environmental chemistry, sample metadata, and amplicon sequencing datasets clustered into OTUs.
- Data files include both environment/chemistry data and biodiversity sequence data, plus a protocol document.

## Datasets and data files
- soil_env_data.csv
- soil_bacteria_seq.csv
- soil_eukaryotes_seq.csv
- water_env_data.csv
- water_bacteria_seq.csv
- water_eukaryotes_seq.csv
- Protocol CEH Tellus SW.docx

## Sampling and field methods
- Epilithon (water samples):
  - 20 locations along a transect from the Wolf River to the Tamar River with spatial coverage planned using maps; exact sites chosen in the field for accessibility.
  - GPS locations recorded with a Garmin GPS12.
  - Three stones sampled at each location; epilithon scraped from a defined area; samples kept cold and processed in the lab.
- Soil samples:
  - Targeted a range of soils from the Tamar region representing different land uses.
  - Exact sites determined in the field; samples collected and location recorded to 1 km grid reference to preserve anonymity.
  - Cores sampled from multiple depths; samples kept cold and transported to the lab.

## Data content and structure
- Epilithon water environment data (water_env_data.csv):
  - Water_lab_ID: unique lab identifier for cross-referencing with biodiversity data.
  - Water_sample_ID: cross-references to the WP4 water chemistry dataset (sample names, e.g., T1:20).
  - Stone_ID: A, B, or C for each location.
  - Sampling date, River, Catchment, NGR, Eastings, Northings.
- Soil environment data (soil_env_data.csv):
  - Soil_ID: unique lab identifier for cross-referencing with biodiversity data.
  - Sampling date: date cores were taken.
  - Grid reference: 1 km British National Grid Reference (anonymised).
  - Depth of core.
  - Soil chemistry measurements: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K.
  - Note: Methodological details and units for soil chemistry are described as forthcoming in the document.
- Biodiversity datasets (OTU tables; post-sequencing processing):
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
  - DNA extraction: MOBIO Powersoil 96-well kit; quality checked for purity and yield.
  - Sequencing: 454 pyrosequencing to assess biodiversity within each sample.
  - Data representation: OTU tables with rows as OTU IDs and columns as sample IDs; each cell shows the percentage of that OTU within the sample.
  - Cross-referencing: Column 1 in each OTU table matches the corresponding sample ID in the environmental data file (e.g., water_bacteria_seq.csv column 1 matches Water_lab_ID in water_env_data.csv; soil_bacteria_seq.csv column 1 matches Soil_ID in soil_env_data.csv).

## Cross-referencing and data integration
- Explicit cross-referencing scheme to link biodiversity data with environmental data:
  - Epilithon bacteria: water_bacteria_seq.csv column 1 = Water_lab_ID in water_env_data.csv.
  - Epilithon eukaryotes: water_eukaryotes_seq.csv column 1 = Water_lab_ID in water_env_data.csv.
  - Soil bacteria: soil_bacteria_seq.csv column 1 = Soil_ID in soil_env_data.csv.
  - Soil eukaryotes: soil_eukaryotes_seq.csv column 1 = Soil_ID in soil_env_data.csv.
- This structure enables integrative analyses of OTU abundance with corresponding water/soil chemistry and spatial metadata.

## Data provenance and contributors
- Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
- Data processing and mapping: Gearóid Webb
- Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
- Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Versioning and documentation
- Version control: 1.0, date 24/03/14; description: created; author: R. Griffiths
- Protocol: Protocol CEH Tellus SW.docx
- General description emphasizes a suite of molecular analyses across epilithon and soils, with data designed for downstream ecological and environmental analyses.