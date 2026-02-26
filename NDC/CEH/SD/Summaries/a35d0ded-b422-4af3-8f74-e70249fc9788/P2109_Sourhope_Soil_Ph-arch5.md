# SOURHOPE FIELD DATA HANDBOOK 2003

## Overview
- Describes the Sourhope Field Experiment as part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on soil biota diversity and functional roles in ecological processes.
- The project spanned 24 sub-projects studying soil structure, soil processes (carbon and nitrogen cycles), micro- and macro-fauna, and root interactions.
- Provides baseline soil chemistry data (pH and moisture) and detailed soil profile descriptions across multiple blocks at Sourhope, including site specifics and horizon-level information.

## Datasets and Metadata
- Baseline soil pH and moisture data collected from central areas of experimental plots (March and September 1999; March 2000; March 2001; March 2002) with additional sampling in April 2000 and July 2003.
- Datasets referenced:
  - P2109_BASELINE_PH.csv: baseline pH and moisture by date, block, main plot, and cell coordinates.
  - P2109_BASELINE_PHSUB.csv: sub-plot pH measurements with project sample IDs (SUID), sub-plot identifiers, and coordinates.
- Data provenance linked to the SOURHOPE FIELD DATA HANDBOOK (Scott et al., 2003) and available via the EIDC catalogue (Supporting Information).

## Sampling Details and Methods
- Baseline sampling used 5 cm diameter by 10 cm depth cores from the centre of each plot; later moisture content calculated from fresh/dry weights.
- Sub-plot sampling collected 20–30 g of soil from the top 5 cm in two adjacent cells per main-plot (except Control 2), with pH readings on fresh samples.
- pH measurement protocol:
  - Use ~10 cm3 soil with ~40 ml deionised water (adjusted in March 2000 to 20–30 g soil with 40 ml water).
  - Mix, wait 20 minutes, calibrate pH meter with buffers pH 7 and 4, measure.
- Moisture content calculation: 100 x (fresh weight − dry weight) / dry weight.
- Baseline sampling timeline includes pre-1998 baseline, with multiple campaigns through 2003.

## Data Structure and Content
- Two comma-separated value (CSV) files:
  - P2109_BASELINE_PH.csv
    - SAMPLE_DATE, Description; SAMPLE_DATE, Units; TREATMENT, Description/Units; BLOCK; MAIN_PLOT; CELL_X; CELL_Y; SOIL_PH; MOISTURE (Units: pH; %).
  - P2109_BASELINE_PHSUB.csv
    - SUID; SAMPLE_DATE; TREATMENT; BLOCK; MAIN_PLOT; SUB_PLOT; CELL_X; CELL_Y; SOIL_PH (Units: pH).
- Substantial site and field details provided for context:
  - SITE DETAILS for blocks 1–5, including grid references, altitude, slope, drainage, soil subgroups, rock types, and base/pit horizons.
  - For each block, horizon-level descriptions (LF, FH, H, Ah, AB, BCx, etc.) with depth ranges and qualitative soil descriptions.
- Data structure supports cross-block comparison and temporal trend analysis, with consistent fields across baseline and sub-plot datasets.

## Quality Control, Limitations, and Disclaimers
- Quality control steps included numeric range checks, format validation, and logical integrity checks.
- Data are subject to QA procedures, but NERC does not warrant the accuracy or fitness for purpose; no liability for use.
- Licensing/usage terms are not fully specified here; users should refer to the EIDC catalogue entry for access rights and licensing details.
- Documentation cites the Sourhope Field Data Handbook (2003) and associated dataset documentation, implying a need to harmonize with broader metadata standards when republishing.

## Provenance and Access
- Origin: NERC Soil Biodiversity Programme; Sourhope Field Experiment at Sourhope Farm, Scottish Borders.
- Related publication: Sourhope Field Data Handbook 2003 (Scott et al., 2003).
- Access: Datasets are available as Supporting Information via the EIDC catalogue record; exact access conditions and licensing should be confirmed via the catalogue entry.

## Governance Considerations for Data Stewards
- Data standardization:
  - Ensure consistent metadata across CSVs (units, date formats, treatment coding, plot identifiers).
  - Validate that BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X/CELL_Y conventions are harmonized with other Sourhope datasets.
- Metadata completeness:
  - Preserve horizon nomenclature and depth ranges (LF, FH, H, Ah, AB, BCx, etc.) for reproducibility.
  - Maintain site-level context (grid refs, altitude, drainage, soil series, rock type) as essential provenance.
- Data quality and liability:
  - Clearly document QA procedures and limitations; retain the liability disclaimer for downstream users.
- Access, licensing, and updates:
  - Capture licensing terms from the EIDC catalogue; specify versioning if datasets are updated or extended.
  - Consider publishing a machine-readable metadata record (e.g., ISO 19115/DE or Dublin Core) to improve discoverability.
- User needs and interoperability:
  - Align fields with user needs for soil chemistry and profile analyses; consider exposing additional derived fields (e.g., moisture content by date, summary statistics) to improve usability.
- Documentation and citations:
  - Include proper citation guidance (Scott et al., 2003) and link to the primary data handbook to support reproducibility and reuse.