# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- A dataset comprising environmental chemistry Data (soil and water) and biodiversity sequencing data from epilithon (water) and soil samples in the Tamar catchment during winter 2013/2014.
- Aims to support environmental health monitoring by enabling assessment of biodiversity and linked environmental conditions to inform policy and future decisions.

## Datasets and content
- Environmental data files:
  - soil_env_data.csv
  - water_env_data.csv
- Biodiversity sequence datasets:
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
- Protocol document:
  - Protocol CEH Tellus SW.docx
- Metadata and cross-referencing:
  - Cross-referencing keys between biodiversity data and environmental data via unique lab/sample identifiers.

## Sampling design and field methods
- Epilithon (water) sampling:
  - 20 locations along the Wolf/Tamar transect chosen for broad spatial coverage.
  - Exact sample sites determined in the field; GPS coordinates recorded with a Garmin GPS12.
  - Three stones sampled at each location; samples kept cold and processed in the lab.
- Soil sampling:
  - Range of soils across the Tamar region reflecting different land uses.
  - Exact sites determined in the field to ensure broad catchment coverage; GPS-derived coordinates used with anonymized 1 km grid references.
- Identifiers and references:
  - Epilithon: Water_lab_ID (lab identifier), Water_sample_ID (links to WP4 water chemistry dataset), Stone_ID (A, B, C), sampling date, river, catchment, grid references.
  - Soils: Soil_ID (lab identifier), Sampling date, 1 km Grid Reference (anonymized), depth, and a suite of soil chemistry measurements.

## Laboratory analysis and data processing
- DNA extraction: MOBIO Powersoil 96-well kit.
- Sequencing: 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
- Data processing: sequences clustered into operational taxonomic units (OTUs); results presented as the percentage of each OTU within each sample.
- Data structure:
  - Rows: OTU IDs.
  - Columns: Sample references (cross-referenced to environmental data via Water_lab_ID or Soil_ID).

## Cross-referencing and data structure details
- Example mappings:
  - Epilithon bacteria: water_bacteria_seq.csv Column 1 matches Water_lab_ID in water_env_data.csv.
  - Epilithon eukaryotes: water_eukaryotes_seq.csv Column 1 matches Water_lab_ID in water_env_data.csv.
  - Soil bacteria: soil_bacteria_seq.csv Column 1 matches Soil_ID in soil_env_data.csv.
  - Soil eukaryotes: soil_eukaryotes_seq.csv Column 1 matches Soil_ID in soil_env_data.csv.
- This cross-referencing enables linking biodiversity composition with corresponding environmental conditions for each sample.

## Data quality, metadata and governance
- Data provenance includes contributors for sample collection, data processing/mapping, laboratory analysis, planning/management, and general description.
- Environmental chemistry data are reported from CEH Lancaster chemistry facilities; full methodological details and units for some analyses are pending at the time of documentation.
- Metadata supporting cross-dataset linking is provided via designated IDs (Water_lab_ID, Water_sample_ID, Soil_ID).
- Public sharing of underlying data and sufficient metadata is necessary for reuse; documentation notes potential barriers (e.g., data governance and accessibility considerations).

## Limitations and considerations
- Some methodological descriptions are awaited or incomplete, which may affect reproducibility and comparability.
- Site anonymization (1 km grid references) can limit fine-grained spatial analyses.
- Documentation contains formatting inconsistencies and inline cross-references that require careful alignment when integrating with other datasets.
- 454 pyrosequencing is an older sequencing technology; downstream analyses and comparability with newer methods should be considered.

## Potential monitoring indicators and uses
- Biodiversity indicators:
  - Relative abundance and diversity of bacterial and eukaryotic OTUs in epilithon and soils.
  - Community composition shifts across land-use types and water bodies within the Tamar catchment.
- Environment-biology linkages:
  - Correlations between soil/water chemistry (pH, total carbon, nutrients, metal concentrations, etc.) and OTU relative abundances.
  - Spatial patterns of biodiversity and chemistry across the 1 km anonymized grid and sampling sites.
- Outputs for decision support:
  - Reports, charts, and dashboards summarizing biodiversity metrics alongside environmental parameters to inform policy evaluation and future monitoring planning.