# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Suite of molecular analyses performed on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
- Includes environmental chemistry data, biodiversity sequencing data (bacteria and eukaryotes), and DNA-based OTU tables.
- Data are organized to enable cross-referencing between environmental metadata and biodiversity observations.

## Data files and contents
- soil_env_data.csv — soil sampling metadata and chemistry data (Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
- soil_bacteria_seq.csv — bacterial biodiversity data for soils (OTU table).
- soil_eukaryotes_seq.csv — eukaryotic biodiversity data for soils (OTU table).
- water_env_data.csv — epilithon water sampling metadata and location data (Water_lab_ID, Water_sample_ID, Stone_ID, SAMPLING DATE, RIVER, CATCHMENT, NGR, EASTINGS, NORTHINGS).
- water_bacteria_seq.csv — bacterial biodiversity data for epilithon water (OTU table).
- water_eukaryotes_seq.csv — eukaryotic biodiversity data for epilithon water (OTU table).
- Protocol CEH Tellus SW.docx — associated field and laboratory protocols.

## Metadata, references, and data linkage
- Water_lab_ID in water_env_data.csv is a unique lab identifier used to cross-reference with water biodiversity data (e.g., water_bacteria_seq.csv, water_eukaryotes_seq.csv).
- Soils use Soil_ID as the cross-reference key to soil biodiversity data (soil_bacteria_seq.csv, soil_eukaryotes_seq.csv).
- Cross-reference approach described: OTU tables are organized with rows as OTU IDs and columns linking to the corresponding environmental data via the sample IDs in the env datasets.

## Field sampling design and methods
- Epilithon (water samples):
  - Sampling sites located to provide broad spatial coverage along the Wolf River through to the Tamar River.
  - Exact site locations determined in the field; GPS coordinates recorded with a Garmin GPS12.
  - Three stones sampled at each of 20 locations; epilithon scraped from a defined area; samples kept cold and sent to the lab for analyses.
- Soil samples:
  - Targeted a range of soils across the Tamar region representing different land uses.
  - Exact sites determined in the field, with logistics considered; GPS coordinates collected via Garmin GPS12.
  - Soil sampling kept cold and taken to the laboratory for analyses.
- Grid references for soils are anonymized at 1 km resolution.

## Biodiversity data and sequencing
- DNA extraction: MOBIO PowerSoil 96-well kit.
- Sequencing: 454 pyrosequencing used to assess bacterial and eukaryotic biodiversity within each sample.
- Data processing: sequences clustered into OTUs; OTU tables show the percentage of each OTU within each sample.
- Data structure:
  - Rows: OTU IDs for each dataset.
  - Columns: sample-to-environment cross-references (via Water_lab_ID or Soil_ID in the corresponding env data files).

## Detailed dataset relationships
- Epilithon bacteria: water_bacteria_seq.csv ↔ water_env_data.csv (Column 1 OTU data linked to Water_lab_ID in env file).
- Epilithon eukaryotes: water_eukaryotes_seq.csv ↔ water_env_data.csv (Column 1 OTU data linked to Water_lab_ID in env file).
- Soil bacteria: soil_bacteria_seq.csv ↔ soil_env_data.csv (Column 1 OTU data linked to Soil_ID in env file).
- Soil eukaryotes: soil_eukaryotes_seq.csv ↔ soil_env_data.csv (Column 1 OTU data linked to Soil_ID in env file).

## Data processing, quality, and outputs
- All biodiversity data are derived from sequencing and processed to OTU level, with percentages of each OTU per sample.
- Metadata provide sampling dates, locations, and grid references to enable spatial analyses and potential linkage to environmental chemistry data.

## Versioning and contributors
- Version 1.0, date 24/03/14.
- Contributors include sampling, data processing and mapping, laboratory analysis, planning and management, and general project description (names listed in the document).

## Related documentation and Protocols
- Protocol CEH Tellus SW.docx provides the procedural context for field and laboratory work.

## Key considerations for analysts
- The integrated dataset enables examining correlations between soil and water chemistry and microbial/eukaryotic community composition across spatially distributed sites.
- Cross-dataset linking via unique IDs (Water_lab_ID, Soil_ID) supports multivariate analyses and predictive modeling.
- Potential challenges to address during analysis include data scale, anonymization of locations, and ensuring alignment between OTU tables and environmental metadata across datasets.