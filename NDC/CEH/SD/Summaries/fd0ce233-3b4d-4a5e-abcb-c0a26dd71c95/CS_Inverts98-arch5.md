# Headwater stream invertebrate data 1998 [Countryside Survey] Data Table Descriptions

## Overview
- Describes macroinvertebrate data from Countryside Survey headwater streams (1998), including two CSV tables and documentation for data collection, processing, and reporting.
- Data are owned by NERC - Centre for Ecology & Hydrology (CEH); references to supporting field and technical reports are provided.
- Data are prepared to support integration with RIVPACS (River Invertebrate Prediction and Classification System) and cross-survey comparability.

## Data tables and structure
- STREAM_INV_SITE_98.csv: site-level data
  - Key fields: YEAR, SQUARE (1 km grid code), SITE_ID, SAMPLE_DATE, WATER_WIDTH, DEPTH1/2/3, SURF_VEL_CAT, SAMPLING_TIME, substrate and habitat cover (ROCK_PAVEMT, BOULDER_COBBLE, PEBBLE_GRAVEL, SAND, SILT_CLAY), MACROPHYTE_COVER, LAND CLASS (LC07, LC07_NUM), ENVIRONMENTAL ZONE (EZ_DESC_07), COUNTRY, COUNTY07, and related geographic indicators.
  - Describes the sampling site context and physical habitat characteristics used for analysis and for running RIVPACS.
- STREAM_INV_SP_98.csv: species-level data
  - Key fields: YEAR, SQUARE, SITE_ID, SAMPLE_DATE, SPECIES_CODE, NAME (scientific name), LC07, LC07_NUM, EZ_DESC_07, COUNTRY, COUNTY07.
  - Links each observed taxon to taxonomy codes, land classification, and environmental zone information for the site.

## Data collection and processing methods
- Field sampling protocol
  - Single stream-bed sample area per site, sampled within three minutes of active searching plus one minute of hand searching.
  - Surveyed river length typically 5–15 m.
  - Macroinvertebrates collected with a standard 1 mm mesh pond net and later sorted/identified in the lab; accompanying physical measurements recorded for RIVPACS.
- Data entry and quality control
  - Field data and lab-identified specimens entered onto a database from paper sheets; cross-checked against original lab sheets with corrections applied as needed.
- Taxonomy and standardisation
  - Taxonomic identifications and abundance counting methods have changed across survey periods (1990, 1998, 2007). To enable comparability:
    - Species data harmonised to a common modern taxonomy.
    - A standardisation process derives a mutually exclusive list of taxa for calculating species richness.
  - Abundance recording evolved from presence/absence (1990) to species-level presence/absence (1998) and abundance classes for families, then to actual species abundances (2007).
- Data processing context
  - Data are aligned with CEH field handbooks and Countryside Survey Technical Reports to support reproducibility and method traceability.

## Metadata, provenance, and data quality
- Documentation and supporting references
  - Field handbook and Countryside Survey reports cited for method context (1998, 2000, 2007 updates).
- Provenance and lineage
  - Data collected in the Countryside Survey program, then harmonised and standardised for cross-survey comparability.
  - Links to Land Classification (ITE 2007) and Environmental Zone descriptors for context and downstream analyses.
- Data quality considerations for stewardship
  - Changes in identification level and taxonomy over time necessitate explicit standardisation.
  - Quality checks include cross-verification against original lab sheets and documented processing steps.

## Access, use, and licensing
- Acknowledgement requirements
  - All uses of Countryside Survey data must include the following acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
- Copyright
  - Countryside Survey ©; Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Licensing implications
  - Data users should apply the required acknowledgement text on all copies, publications, or presentations derived from the data.

## Implications and considerations for Data Stewards
- Governance and standards
  - Two-table relational structure (SITE and SPECIES) enables clear data linkages via SITE_ID, supporting data discovery and reuse.
  - Harmonisation to modern taxonomy and standardisation for species richness enhance interoperability across surveys.
- Metadata and provenance
  - Maintain versioning (the document is Version 1: 19/10/2016) and provide clear lineage from field methods to processed data.
  - Capture references to underlying field handbooks and technical reports to support reproducibility.
- Data quality and updates
  - Document and preserve QC steps (paper to database, cross-checks with lab sheets) to enable traceability of corrections.
  - Plan for updating taxonomy mappings and enrichment of metadata as taxonomic references evolve.
- Access and reuse
  - Enforce and communicate acknowledgment requirements to data users.
  - Ensure licensing terms and rights are clearly applied in all distributions and publications.
- Practical stewardship notes
  - Keep the linkage between site-level and species-level data explicit, using SITE_ID as the consistent key across updates.
  - Track any changes to taxonomic concepts or classification schemes and maintain a crosswalk/metadata note describing changes and their impact on analyses (e.g., species richness calculations).