# Soil invertebrate data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset of soil invertebrate (mesofauna) counts from 0-8 cm depth, collected from up to 256 1 km squares across Great Britain during the 1998 Countryside Survey.
- Data file: CS1998_SOIL_INVERTS.csv.
- Uses: provides taxon-level counts, summary metrics and metadata for terrestrial biodiversity analyses and data-system planning.

## Data Structure and Variables
- Spatial and sampling identifiers:
  - SQUARE: 1 km square sampling site code (text)
  - PLOT: Plot identifier within each square (text)
  - YEAR: Year of survey (numeric)
- Taxa and counts (numerical counts per sample/core):
  - ACTO, ARAN, CHTO, CHGE, CHLI, COLA, COAD, COEN, CONE, COPU, COSM, COPE, DIPP, DIPL, DILA, DIAD, GAST, HEMI, HYME, ISOP, LEAD, LELA, NEMA, NEMM, OLIG, OPIL, PAUR, PROT, PSEU, PSOC, PULM, SYMP, THYP, THYN
- Summary and diversity metrics (per core):
  - TOTAL_CATCH: total invertebrates (numeric)
  - COLL_TOTAL: total collembolans (numeric)
  - AC_COLL_TOTAL: total acari mites and collembolans (numeric)
  - MC_RATIO: ratio of mites to springtails in soils (numeric)
  - TOTAL_TAXA: total invertebrate taxa richness per core (numeric)
  - SHANNON: Shannon diversity index (dimensionless)
- Land use and location descriptors:
  - LC07: ITE Land Class 2007 (text)
  - LC07_NUM: numeric code for LC07
  - COUNTRY: country where square is located (ENG, SCO, WAL)
  - COUNTY07: county or council area code
  - EZ_DESC_07: environmental zone description
- Additional identifiers:
  - Thank you for acknowledging data use: All CS data must be acknowledged.

## Methods
- Sample collection: Soil cores collected and processed following the CS2000 Field Handbook.
- Laboratory extraction: Soil invertebrates extracted via dry Tullgren method:
  - 5-day extraction using a heated (40 W) light source above a sieve over a collection bottle with 70% ethanol.
- Taxonomic processing: Identifications made to major taxa (taxonomic level 1); Collembola and mites identified to morphotype level.
- Output: Counts per sample/core, with identification and processing details recorded.

## Quality Control and Data Management
- Standard operating procedures observed for all biological assessments; project log books maintained.
- Quality control:
  - Detailed recording of faunal composition, dates, sample codes, and identification keys.
  - Approximately 5% of samples rotated between staff for cross-checking.
  - A subset of samples reviewed by taxonomic specialists for higher-level verification.
- Documentation and traceability:
  - Every sample processed logged in dedicated notebooks; includes species list, counts, dates, sample codes, and any higher-taxon work.
  - Data entered weekly into databases, then copied to CD-ROM.
  - Data undergo standard quality checks and CD-ROM backups stored securely (fireproof or off-site).

## Usage Rights and References
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Copyright: Countryside Survey ©; Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Laboratory and field methods referenced against CS2000 Field Handbook.
- References and related publications (selected):
  - MASQ: Monitoring and Assessing Soil Quality in Great Britain (Soil module)
  - ITE Merlewood Land Classification and 2007 GB land classification datasets
  - Countryside Survey: UK Results from 2007
- Links and citations provided in the dataset documentation (for further methodological and contextual details).

## Relevance for Data Leaders
- Demonstrates end-to-end data handling: from field collection to laboratory processing, taxonomic classification, and metadata-rich outputs.
- Provides rich biodiversity metrics (TOTAL_TAXA, SHANNON, MC_RATIO) suitable for system-wide data governance, cross-project integration, and policy-relevant analyses.
- Emphasizes data discoverability and interoperability through standardized fields (LC07, COUNTRY, COUNTY07, EZ_DESC_07) and clear data lineage (CS1998_SOIL_INVERTS.csv; CS2000 Field Handbook).
- Highlights robust quality control practices and documentation processes essential for trusted data products.
- Clearly defines attribution requirements, supporting responsible data sharing across networks and partners.