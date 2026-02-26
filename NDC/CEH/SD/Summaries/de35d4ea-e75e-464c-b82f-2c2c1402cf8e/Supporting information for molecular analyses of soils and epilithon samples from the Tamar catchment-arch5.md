# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Overview
- Suite of molecular analyses on epilithon (water) and soil samples from the Tamar catchment collected in winter 2013/2014.
- Datasets include environmental chemistry data and biodiversity sequencing data for bacteria and eukaryotes (epilithon and soil).
- Associated protocol/documentation: Protocol CEH Tellus SW.docx.
- Multiple contributors across field collection, processing, analysis, and planning; explicit general description of the study.

## Datasets and data model
- Relevant data files:
  - soil_env_data.csv
  - soil_bacteria_seq.csv
  - soil_eukaryotes_seq.csv
  - water_env_data.csv
  - water_bacteria_seq.csv
  - water_eukaryotes_seq.csv
  - Protocol CEH Tellus SW.docx
- Key identifiers and cross-references:
  - Water_env_data.csv
    - Water_lab_ID: unique lab identifier; cross-referenced with biodiversity data.
    - Water_sample_ID: links to WP4 water chemistry dataset sample names; Stone_ID identifies each of three stones at each location.
    - Sampling date, River, Catchment, NGR, Eastings, Northings.
  - Soil_env_data.csv
    - Soil_ID: unique lab identifier; cross-referenced with biodiversity data.
    - Sampling date, Grid reference (1 km resolution to preserve anonymity), depth of core.
    - Soil chemistry columns: Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K (units/methodologies pending full description).
- Biodiversity datasets (OTU-based):
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
- Data organization:
  - DNA extracted with MOBIO Powersoil kit; quality-checked prior to 454 pyrosequencing.
  - Sequences clustered into OTUs; data tables show percentage of each OTU within each sample.
  - Cross-referencing structure:
    - water_bacteria_seq.csv column 1 equals Water_lab_ID in water_env_data.csv
    - water_eukaryotes_seq.csv column 1 equals Water_lab_ID in water_env_data.csv
    - soil_bacteria_seq.csv column 1 equals Soil_ID in soil_env_data.csv
    - soil_eukaryotes_seq.csv column 1 equals Soil_ID in soil_env_data.csv

## Data governance and provenance
- Version 1.0, date 24/03/14; author: R. Griffiths.
- Contributors by area:
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
  - General description: project overview
- Anonymity measures: exact site locations preserved with 1 km grid references.

## Quality assurance, standards, and gaps
- QA: DNA quality checks prior to sequencing; post-sequencing processing yields OTU-based abundance data per sample.
- Metadata gaps: full methodological details for soil chemistry analyses are pending; units for soil chemistry measurements are not specified in the current document.
- Interoperability: relies on consistent ID cross-references between environmental and biodiversity datasets; alignment across files is essential.

## Access, sharing, and publication readiness
- Intention to upload datasets to relevant portals and catalogue data holdings; cross-dataset linking via IDs enhances discoverability and reuse.
- Documentation supports reproducibility, including cross-referencing scheme and the sequencing/OTU framework.

## Challenges and recommendations for Data Stewards
- Data completeness: address pending full soil chemistry methodologies and units.
- Metadata standardization: ensure consistent field naming, units, and reference systems across environmental and biodiversity datasets.
- Data integration: maintain robust cross-referencing mappings between environment and OTU data; monitor for updates from WP4 water chemistry data.
- Data governance: document versioning and provenance for future updates; maintain clarity on embargoes or access restrictions if they arise.