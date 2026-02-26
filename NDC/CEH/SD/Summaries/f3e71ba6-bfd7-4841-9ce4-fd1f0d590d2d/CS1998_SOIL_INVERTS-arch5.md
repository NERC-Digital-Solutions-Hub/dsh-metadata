# Soil invertebrate data 1998 [Countryside Survey], Great Britain Version: 1: 02-6-2016 CS1998_SOIL_INVERTS.csv file details

## Purpose and scope
- Dataset of soil invertebrate (mesofauna) counts from 0-8 cm samples.
- Collected from up to 256 1km squares across Great Britain during 1998.
- Provides counts for a wide range of taxa, plus summary metrics (diversity and abundance).

## Data structure and content
- Core identifiers:
  - SQUARE (1km square site code, text)
  - PLOT (plot within square, text)
  - YEAR (survey year, number)
- Taxon counts (example codes): ACTO, ARAN, CHTO, CHGE, CHLI, COLA, COAD, COEN, CONE, COPU, COSM, COPE, DIPP, DIPL, DILA, DIAD, GAST, HEMI, HYME, ISOP, LEAD, LELA, NEMA, NEMM, OLIG, OPIL, PAUR, PROT, PSEU, PSOC, PULM, SYMP, THYP, THYN, TOTAL_CATCH.
- Totals and diversity metrics:
  - COLL_TOTAL (total Collembola)
  - AC_COLL_TOTAL (acari mites and collembolan total)
  - MC_RATIO (mites:springtails ratio)
  - TOTAL_TAXA (taxa richness)
  - SHANNON (diversity index)
- Metadata/stratification fields:
  - LC07 (ITE Land Class 2007), LC07_NUM
  - COUNTRY (ENG/SCO/WAL)
  - COUNTY07
  - EZ_DESC_07 (environmental zone description)
- Data notes: All taxa were identified to major taxa (Taxonomic level 1); Collembola and mites identified to morphotype level in addition.

## Metadata, standards, and access
- Data ownership: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology (CEH).
- Rights: Countryside Survey © Database Right/Copyright NERC- CEH. All rights reserved.
- Acknowledgement requirement: All use of CS data must acknowledge Countryside Survey data ownership.
- Suggested citation/acknowledgement text to appear on copies, publications, and presentations.
- Field and laboratory methods documented (CS2000 Field Handbook).

## Methods
- Field collection: Soil cores (0-8 cm) from up to 256 1km squares across Great Britain (1988 era data recompiled for 1998 dataset).
- Laboratory extraction: Dry Tullgren extraction over 5 days; collection in bottles with 70% ethanol.
- Identification: Major taxa identified to level 1; Collembola and mites further identified to morphotype level.
- Data handling: Data recorded for each sample; weekly entry into databases; CD-ROM backups.

## Quality control and data management
- Adherence to established methods and protocols; project log books maintained for all samples.
- Recording of identification keys, assessment dates, sample codes, and any issues for follow-up.
- Quality control measures:
  - Approximately 1 in 20 samples re-identified by a second staff member to check consistency.
  - Some samples sent to taxonomic specialists for second-level QC.
- Documentation: Detailed sample-level notebooks recording species, counts, processing dates, sample codes, and higher taxonomic classifications if applicable.
- Data storage and archiving: Data entered weekly into databases, then copied to CD-ROMs; CDs stored in fireproof cabinets or off-site locations for security.

## Related references and publications
- General overview and methodology of Countryside Survey with links to related documents (http://www.countrysidesurvey.org.uk/).
- Key publications detailing soil quality monitoring and Countryside Survey results (e.g., MASQ module, 2002; ITE Land Classification GB 1981–2007; Countryside Survey UK Results 2007, 2008).
- Datasets and classification schemes are archived with NERC Environmental Information Data Centre (EIDC); numerous project reports and technical references cited.

## Data and usage notes
- Data format: CS1998_SOIL_INVERTS.csv (CSV file details).
- Coverage: Soil invertebrate counts for a specific historical survey (1998) in Great Britain.
- Documentation highlights data collection context (field handbook reference) and QA procedures to ensure traceability and reproducibility.
- Embargo or update notes: The document focuses on 1998 data; ongoing updates or embargo specifics are not described within the file details but follow Countryside Survey data governance.

## Practical considerations for data stewards
- Governance: Ensure consistent acknowledgement across all disseminations; maintain linkage to COI and licensing terms.
- Metadata completeness: Maintain alignment between counted taxa, derived metrics, and geographic stratifications (COUNTRY, COUNTY07, LC07, EZ_DESC_07).
- Interoperability: Align taxon coding and field definitions with other Countryside Survey datasets to facilitate cross-year analyses.
- Data sharing: Respect sharing limitations and provide clear pathways for re-use, including access to methods (CS2000 Field Handbook) and QC procedures.
- Retention and preservation: Preserve raw data, processed data, and backups (on-site and off-site) to support auditability and re-analysis.