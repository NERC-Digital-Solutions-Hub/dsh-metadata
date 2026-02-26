# Soil invertebrate data 1998 [Countryside Survey], Great Britain

## Overview
- Dataset capturing soil invertebrate (mesofauna) counts from samples collected at 0–8 cm depth.
- Coverage: up to 256 1 km squares across Great Britain during 1998.
- Data intended for environmental monitoring and assessment, with derived metrics to support biodiversity and soil health indicators.

## Data content and structure
- Sampling framework:
  - SQUARE: 1 km square sampling site code.
  - PLOT: one of five plots within each square.
  - YEAR: survey year (1998).
- Taxa counts (counts are numeric): ACTO (acari), ARAN, CHTO, CHGE, CHLI, COLA, COAD, COEN, CONE, COPU, COSM, COPE, DIPP, DIPL, DILA, DIAD, GAST, HEMI, HYME, ISOP, LEAD, LELA, NEMA, NEMM, OLIG, OPIL, PAUR, PROT, PSEU, PSOC, PULM, SYMP, THYP, THYN.
- Totals and derived metrics:
  - TOTAL_CATCH: total invertebrates per core.
  - COLL_TOTAL: total collembolan per core.
  - AC_COLL_TOTAL: total acari mites and collembolan per core.
  - MC_RATIO: ratio of mites to springtails in soils (0–8 cm depth).
  - TOTAL_TAXA: total invertebrate taxa richness per core.
  - SHANNON: Shannon diversity index (dimensionless) for invertebrates.
- Metadata and classifications:
  - LC07, LC07_NUM: ITE Land Classification 2007 (text and numeric code).
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL).
  - COUNTY07: County or Council (Sco) designation.
  - EZ_DESC_07: Countryside Survey Environmental Zone description.
- Data management fields:
  - AC_COLL_TOTAL, TOTAL_TAXA, SHANNON, etc., to support monitoring indicators.
- Usage acknowledgments:
  - All CS data must be acknowledged as Countryside Survey data owned by NERC - CEH.

## Sampling and laboratory methods
- Field sampling:
  - Soil cores collected and processed in the field as per standard CS protocol.
- Laboratory extraction:
  - Dry Tullgren extraction over 5 days using a heated setup (40 W bulb) to drive fauna into collection bottles with 70% ethanol.
- Taxonomic resolution:
  - Identification to major taxa (Taxonomic level 1) for all groups.
  - Collembola and mites identified further to morphotype level.
- Documentation:
  - Soil samples and extraction processes meticulously recorded in field and lab notebooks.

## Quality control and data management
- Standard operating procedures:
  - Staff follow established methods; project log books maintained.
- Identification verification:
  - Approximately 1 in 20 samples rotated between staff to compare identifications.
  - Some samples re-checked by taxonomic specialists for higher-level QC.
- Data recording and storage:
  - Detailed sample processing records (species list, counts, dates, sample codes).
  - Weekly data entry into databases; data copied to CD-ROMs.
  - Data checked against standard procedures and stored in fireproof or off-site locations.
- Documentation and references:
  - Field Handbook CS2000 used for soil sampling procedures.
  - Acknowledgments and data use conditions explicitly stated for all outputs.

## Publications, references, and data context
- Related guidance and project overviews:
  - General Countryside Survey project information and methodologies (online references provided in the document).
- Key related works:
  - MASQ: Monitoring and Assessing Soil Quality in Great Britain (Soils and Pollution module) and associated CEH reports.
  - ITE Land Classification of Great Britain (1996–2007) and related datasets.
  - Countryside Survey: UK Results from 2007 and associated CEH/NERC documentation.
- Data accessibility and provenance:
  - Data and methodologies linked to CEH/NERC data centers and publications; dataset DOIs and catalog references provided for provenance.

## Relevance for monitoring frameworks
- Supports environmental health monitoring by providing:
  - Taxon-specific and aggregate abundance data across landscape units (1 km squares).
  - Biodiversity indicators (TOTAL_TAXA, SHANNON) and community structure metrics (mites vs. springtails, Collembola totals).
  - Spatially explicit data suitable for trend analysis and policy evaluation at GB scale.
- Emphasizes data quality and governance practices:
  - Detailed QA procedures, traceable sampling and processing logs, and documented data handling standards.
  - Clear data usage obligations and citation requirements to maintain data integrity and reproducibility.

## Accessibility considerations and potential barriers
- Acknowledgement requirements may influence public sharing and reuse.
- Metadata completeness and standardization are present but may require transformation for cross-dataset integration.
- Data format involves specialized field notes and database systems; suitable data governance and metadata provision enhance usability for monitoring frameworks.