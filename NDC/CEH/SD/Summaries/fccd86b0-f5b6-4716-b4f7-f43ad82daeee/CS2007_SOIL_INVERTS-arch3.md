# Soil invertebrate data 2007 [Countryside Survey], Great Britain

## Overview and purpose
- Provides soil mesofauna counts (0–8 cm depth) from up to 256 1 km squares across Great Britain, surveyed in 2007.
- Data intended to support environmental health monitoring, policy scrutiny, and informing future decisions by assessing soil biodiversity.

## Data and file details
- File: CS2007_SOIL_INVERTS.csv
- Contents: Counts of soil invertebrates (mesofauna) from soil cores, plus derived indicators.
- Core structure: 921 soil cores extracted from 5 plots within each 1 km square (across 256 squares in GB).
- Columns include: SQUARE, PLOT, YEAR, and numerous taxa counts (e.g., ACTO, ARAN, CHTO, CHGE, CHLI, COLA, COAD, CONE, COPU, DIPP, DIPL, DILA, DIAD, GAST, HEMI, HYME, ISOP, LEAD, LELA, NEMA, NEMM, OLIG, OPIL, PAUR, PROT, PSEU, PSOC, PULM, SYMP, THYP, THYN, TOTAL_CATCH, COLL_TOTAL, AC_COLL_TOTAL, MC_RATIO, TOTAL_TAXA, SHANNON, LC07, LC07_NUM, COUNTRY, COUNTY07, EZ_DESC_07).
- Taxonomic resolution: Identified to major taxa (Taxonomic level 1) with Collembola and mites identified to morphotype level.

## Protocols and laboratory methods
- Extraction: Dry Tullgren extraction from soil cores, 5-day period, using a 40 W light source and 70% ethanol in collection bottles.
- Processing: Identification of major taxa; Collembola and mites further distinguished to morphotype level.
- Sample handling: Field cores logged and processed promptly after collection.

## Quality assurance and quality control
- Quality control: Every 1 in 10 of the first 500 samples re-counted and re-identified by a second staff member; discrepancies resolved and noted; ongoing checks reduce mislabelling.
- Quality assurance: Adheres to Defra/NERC joint Codes of Practice.
- Uncertainty notes: Small-invertebrate transfer losses during sample handling acknowledged; no significant differences found between original and validated counts in CS200.

## Sampling design and field coverage
- Design: Based on the Countryside Survey’s rigorous statistical framework; GB stratified into Land Classes to represent environmental gradients.
- Coverage: 591 sample squares surveyed in 2007 (289 England, 107 Wales, 195 Scotland).
- Soil depth and sampling: Top 0–15 cm soil sampled; corners of Main Plots used in earlier surveys; re-sampling patterns implemented to maintain comparability over time.
- Power considerations: Pre-study power analyses ensured sufficient sample size for major measurements (e.g., pH, loss-on-ignition) and key taxa analyses, with adjustments for metals and other analytes.

## Data usage, access, and governance
- Acknowledgement: All use of Countryside Survey data must acknowledge the CEH ownership.
- Copyright: Countryside Survey data and database rights are held by NERC-Centre for Ecology & Hydrology.
- Documentation: Protocols and methods documented in the Countryside Survey Soils Manual (CS Technical Report No. 3/07; Emmett et al., 2008).

## Derived metrics and indicators for monitoring
- Total invertebrate activity: TOTAL_CATCH; TOTAL_TAXA (taxa richness).
- Community structure: SHANNON diversity index.
- Collembola and mite focus: COLL_TOTAL; AC_COLL_TOTAL (mites and collembola); MC_RATIO (mites to springtails ratio).
- Geographic and classification fields: LC07 and LC07_NUM (ITE Land Classification 2007); COUNTRY; COUNTY07; EZ_DESC_07.

## References and supporting documentation
- Countryside Survey Soils Manual (Emmett et al., 2008) with sampling strategy, field/lab procedures, QC, archiving, and data manipulation.
- Related Countryside Survey materials and UK results publications (2007 UK results, 2008 data compilations, etc.).

## Practical considerations for monitoring frameworks
- Data quality and metadata: Metadata completeness and consistent data governance are essential for reuse; some data transformation may be required to align with other datasets.
- Transparency and openness: Data sharing is supported but may require careful handling of metadata and governance.
- Policy relevance: Provides baseline soil invertebrate diversity and abundance metrics across GB, enabling trend analysis and assessment of policy-driven soil biodiversity objectives.
- Data gaps and limitations: Acknowledges potential gaps in metadata completeness and small taxa losses; should be considered in uncertainty assessments when informing decisions.