# Soil invertebrate data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset: Soil invertebrate (mesofauna) counts from samples 0–8 cm, from up to 256 1 km squares across Great Britain, surveyed in 2007.
- File: CS2007_SOIL_INVERTS.csv detailing counts per taxon and derived metrics.
- Acknowledgement and copyright: Data acknowledged as Countryside Survey data owned by NERC–CEH; all rights reserved; use must include the specified acknowledgement.
- Documentation references: Soils Manual and CS technical reports (Emmett et al. 2008; CS2007 Soils Manual, CS Technical Report No. 3/07).

## Data structure and content
- Core identifiers:
  - SQUARE: 1 km square sampling site code
  - PLOT: Plot within each square (1 of 5)
  - YEAR: Year of survey
- Taxon counts (examples; full list many): ACTO, ARAN, CHTO, CHGE, CHLI, COLA, COAD, COLA, COLM, etc., representing major taxa and subgroups (e.g., acari, araneae, chilopoda, collembola, copepoda, diplopoda, diptera, gastropoda, isopoda, lepidoptera, mites, etc.)
- Derived metrics:
  - TOTAL_CATCH: total invertebrates per core
  - COLL_TOTAL: total collembolan per core
  - AC_COLL_TOTAL: acari mites and collembolan total per core
  - MC_RATIO: mites to springtails ratio (soil depth 0–8 cm)
  - TOTAL_TAXA: total invertebrate taxa richness per core
  - SHANNON: Shannon diversity index
  - LC07, LC07_NUM: ITE Land Class 2007 (text and numeric codes)
  - COUNTRY, COUNTY07, EZ_DESC_07: geographic descriptors
- Data scope and units: Counts are numeric; per-core values; 0–8 cm depth focus for invertebrate sampling.

## Data collection, processing and methods
- Sampling design: Based on Countryside Survey framework; stratified across Great Britain using Land Classes to capture environmental gradients; 591 sample squares in 2007 (289 England, 107 Wales, 195 Scotland).
- Field sampling: Soil cores collected from 1 km squares; 3–5 cores randomly selected from 5 plots per square; soils sampled from top 0–15 cm in historical designs, with 2007 methodology aligning to the CS framework.
- Extraction and processing: Dry Tullgren extraction over 5 days to collect soil fauna into bottles with 70% ethanol; organisms identified to major taxa (Taxonomic level 1); Collembola and mites identified to morphotype level for finer resolution.
- Laboratory workflow: Cores logged in, processed for basic measurements and chemical analyses; samples archived as part of the CS soil protocols.

## Quality control and quality assurance
- Identification checks: After initial taxonomic identification, 1 in 10 of the first 500 samples re-counted and re-identified by a second staff member; discrepancies resolved and corrections recorded.
- Ongoing validation: Reductions in mislabelling; evaluation of data differences; note that small invertebrates may be lost during transfer from extraction tubes to colour-coded tubes.
- QA framework: Adheres to Defra/NERC joint Codes of Practice.
- Documentation and cross-checks: Methods cross-checked when changes occurred; some analyses re-run to ensure consistency with original methodology.

## Sampling strategy, coverage and power
- Stratification and power: Prior power analyses ensured adequate sample sizes to report major habitats and country-level comparisons; sampling designed to enable reliable national statistics and representation of environmental diversity.
- Spatial coverage: 591 squares across GB; distribution: 289 England, 107 Wales, 195 Scotland.
- Temporal scope: Single survey year (2007) with protocols designed for consistency with prior and subsequent CS soils work.

## Documentation, data governance and usage
- Protocol and methodology references: CS 2007 Soils Manual; CS Technical Report No. 3/07; detailed sampling, processing, QC, archiving, and data manipulation procedures.
- Data handling and dissemination: Data and accompanying metadata are prepared for upload to relevant data portals; acknowledged use required in all copies, publications, and presentations.
- Archival and references: Emmett et al. (2008) Countryside Survey: Soils Manual; Carey et al. UK results from Countryside Survey 2007; other linked references provide broader methodological and classification context.
- Metadata completeness: Dataset includes Land Class (LC07), geographic identifiers, and environmental zone descriptions to support discovery, discovery, and reuse by data stewards and users.