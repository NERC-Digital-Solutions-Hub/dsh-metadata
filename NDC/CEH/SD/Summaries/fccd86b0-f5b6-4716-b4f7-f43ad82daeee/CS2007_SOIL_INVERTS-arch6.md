# Soil invertebrate data 2007 [Countryside Survey], Great Britain

- Overview
  - A dataset of soil mesofauna counts from 0–8 cm depth, collected in 2007 across up to 256 1 km squares in Great Britain.
  - File: CS2007_SOIL_INVERTS.csv
  - Includes counts for numerous taxonomic groups, summary metrics, and geographic classifications. Acknowledgement of Countryside Survey data is required.

- Data structure and key variables
  - SQUARE: 1 km square sampling site code
  - PLOT: Plot within each square (1–5)
  - YEAR: Year of survey
  - Taxon counts (examples): ACTO, ARAN, CHTO, CHGE, CHLI, COLA, COAD, CONE, COPU, DIPP, DIPL, DILA, DIAD, GAST, HEMI, HYME, ISOP, LEAD, LELA, NEMA, NEMM, OLIG, OPIL, PAUR, PROT, PSEU, PSOC, PULM, SYMP, THYP, THYN
  - Totals and diversity: TOTAL_CATCH, COLL_TOTAL, AC_COLL_TOTAL, MC_RATIO, TOTAL_TAXA, SHANNON
  - Location/classifications: LC07 (text), LC07_NUM (numeric), COUNTRY, COUNTY07, EZ_DESC_07
  - Note: TOTALS and diversity indices describe overall invertebrate community characteristics per core

- Data collection and laboratory methods
  - Sampling design: 921 soil cores were analyzed; 3–5 cores randomly selected from 5 plots per square across 256 squares
  - Extraction: dry Tullgren extraction over 5 days; samples heated with a 40 W lamp and collected into 70% ethanol
  - Identification: organisms identified to major taxonomic level 1; Collembola and mites identified to morphotype
  - Standard references: Procedures drawn from Countryside Survey Soils Manual

- Quality control and assurance
  - QA: Standardised reagents and blind replicates included; cross-checks when methods changed
  - Re-counts: 1 in 10 of the first 500 samples re-counted/identified by a second staff member; discrepancies resolved and records updated
  - Data integrity: Small losses of the tiniest invertebrates possible during transfer; validated with t-tests showing no significant differences between original and revised data
  - Governing framework: Defra/NERC joint Codes of Practice adhered to

- Sampling strategy and scope (QA context)
  - Based on rigorous CS sampling design with Land Classes to capture environmental gradients
  - Coverage: 591 sample squares in 2007 (England 289, Wales 107, Scotland 195)
  - Temporal continuity: Soil samples collected from top 0–15 cm; sampling aligned with Main Plots across survey years (1978, 1998, 2007)
  - Power analyses conducted to ensure reliable reporting for major measurements and country-level summaries

- Data usage, rights and acknowledgement
  - All uses must acknowledge Countryside Survey data owned by NERC – Centre for Ecology & Hydrology
  - Countryside Survey ©, with relevant copyright restrictions

- Documentation and references
  - Core methods and QA procedures documented in Emmett et al. 2008: Countryside Survey. Soils Manual (Technical Report No. 3/07)
  - Related publications include UK Results from Countryside Survey 2007 and ITE Land Classification references
  - Access and supplementary documentation available through Countryside Survey resources and CEH/NERC data centers

- Practical notes for data users
  - Be aware of potential minor losses of the smallest taxa during transfer between containers
  - Ensure acknowledgement statements are included in publications and presentations
  - Consult the Soils Manual for detailed sampling, processing, QC, and data manipulation procedures