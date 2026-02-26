# Headwater stream invertebrate data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Data from the Countryside Survey 1998, module on freshwater habitats, focusing on headwater stream macroinvertebrates.
- Provides two linked data tables: site-level measurements and species-level observations.
- Taxonomic data harmonised to a common modern taxonomy to enable cross-survey comparisons; related to RIVPACS and land classification frameworks.
- Acknowledgement requirements apply to all use of Countryside Survey data.

## Data Collection Methods
- Sampling area: a single stream-bed area sampled within 5–15 m of stream length; three minutes of active sampling plus one minute of hand search.
- Collection tools: standard 1 mm mesh pond net; samples returned to CEH for sorting/identification.
- Supplemental measurements recorded for RIVPACS: stream width, depth at four-quarter points, and substrate characteristics.
- Taxonomy and counting schemes changed across survey years (1990: presence/absence; 1998: presence/absence for species and abundance classes for families; 2007: estimated actual abundances for species). Data harmonised to a common taxonomy; standardisation creates a mutually exclusive taxon list for species richness.

## Data Harmognisation and Taxonomy
- Species data harmonised across survey years to align identifications with a consistent taxonomy.
- Standardisation applied to derive a mutually exclusive list of taxa for calculating species richness.
- Underlying taxonomy revisions acknowledged and accommodated in the dataset.

## Data Tables

### STREAM_INV_SITE_98.csv
- Purpose: Freshwater stream site-level invertebrate data (1998).
- Key fields (examples):
  - YEAR, SQUARE, SITE_ID, SAMPLE_DATE
  - WATER_WIDTH, DEPTH1, DEPTH2, DEPTH3
  - SURF_VEL_CAT, SAMPLING_TIME
  - ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY
  - DOM_PART_SIZE, MACROPHYTE_COVER
  - LC07, LC07_NUM, EZ_DESC_07
  - COUNTRY, COUNTY07
- Notes: Includes land classification and environmental zone descriptors; field values are recorded to support modeling and comparisons across sites and years.

### STREAM_INV_SP_98.csv
- Purpose: Freshwater stream invertebrate species data (1998).
- Key fields (examples):
  - YEAR, SQUARE, SITE_ID, SAMPLE_DATE
  - SPECIES_CODE, NAME
  - LC07, LC07_NUM, EZ_DESC_07
  - COUNTRY, COUNTY07
- Notes: Linked to site-level data via SITE_ID; contains species-level taxonomic identifications and associated classification attributes.

## Data Entry and Quality Control
- Macroinvertebrate identifications conducted in a laboratory.
- Data entered from field sheets and lab sheets into a database; cross-checked against original lab papers; data-entry errors corrected.

## Related Publications and Data Links
- Countryside Survey 2000, Module 2: Freshwater Studies (Environment Agency R&D Technical Report E1-038/TR1) and associated CEH and NERC reports.
- Countryside Survey: Headwater Streams Report from 2007 (CS Technical Report No. 8/07).
- Data availability and documentation referenced via NERC/CEH and Nora links provided in the original material.

## Acknowledgement and Copyright
- All Countryside Survey data must be acknowledged.
- Acknowledgement text: "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and copyright note: "Countryside Survey © Database Right/Copyright NERC-Centre for Ecology & Hydrology. All rights reserved."