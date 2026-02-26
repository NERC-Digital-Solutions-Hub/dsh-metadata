# Details of data structure to ' Digestate_HF_and_NW_NH3_cum.csv '

## Overview
- Supplement to supporting documentation for data series related to the Digestate NH3 emissions study.
- Dataset: 6 columns, 32 rows from the 2017 digestate wheat trial conducted at Henfaes Research Center (HF) and North Wyke (NW).
- Emissions: cumulative NH3-N over 7 days from plots treated with various digestate formulations and inhibitors.
- Digestate sources: from anaerobic digestion of food waste (Fre-energy, Wrexham for HF; Holsworthy for NW).
- Sites and researchers: Henfaes and North Wyke (Rothamsted Research network).

## Dataset structure and variables
- File: Digestate_HF_and_NW_NH3_cum.csv
- Columns (6 total):
  - Site: HF or NW
  - Block: 1, 2, 3, 4 (randomised block design)
  - Plot: HF plots (5, 6, 8, 10, 13, 14, 15, 18, 24, 28, 29, 30, 33, 36, 38, 40) and NW plots (1–16)
  - Treatment: D (digestate), AD (acidified digestate, pH 5.5 HF / pH 3 NW), DNI (digestate with DMPP), ADNI (acidified digestate with DMPP)
  - NH3_qa1: cumulative NH3-N emissions over the 7-day measurement period (kg N ha^-1)
  - NH3_qa2: same as NH3_qa1 but with negative NH3 fluxes replaced by 0
- Notes:
  - NH3_qa1 and NH3_qa2 provide two ways to handle potential data values (with and without negative flux adjustments).

## Data collection and measurement protocol
- NH3 capture method: gas traps with phosphoric acid to trap NH3; NH4 captured and later analyzed (NH4 converts from NH3 upon contact with acid).
- Air sampling setup: two pipes positioned at the beginning and middle of each wind tunnel to move air from the wind tunnel to the traps (via an extractor).
- NH4 trap handling frequency:
  - HF/NW: traps changed 2–3 times per day on the first day due to high volatilization rates.
- Reporting limit:
  - Detection limit: 0.01 mg NH4-N L^-1.
- Emission measurement timing:
  - HF: measurements at 4 hours, 24 hours, and days 2–7 post-digestate application.
  - NW: measurements at 1 hour, 3 hours, 6 hours, 24 hours, and days 2–7 post-application.

## Data quality and governance notes
- Data provenance: linked to supplementary documentation for broader CINAg experiments; dataset details align with the supporting documentation framework.
- Formatting and standards: clearly defined column headers, units, and coded treatments to support interoperability and reuse.
- Data processing decisions:
  - NH3_qa2 substitutes negative flux values with zero, enabling alternative analyses without negative emissions.
- Limitations and considerations:
  - Small dataset (32 rows) across two sites with multiple treatments; ensure proper context when aggregating or comparing across plots or treatments.
  - Source materials include digestates from different facilities; note site-specific pH adjustments in treatment definitions.
- Metadata and discoverability:
  - Dataset name, site identifiers, block design, plot identifiers, treatment codes, and measurement period are explicitly documented.
  - Clear documentation of measurement timing and methodology to facilitate replication and secondary analyses.

## Implications for data stewardship
- Ensure ongoing data governance by maintaining:
  - Versioned updates to NH3 emission data as experiments progress.
  - Consistent mapping of treatment codes to full methodological definitions.
  - Preservation of measurement protocols and trap-handling procedures for future users.
  - Clear provenance trail linking this dataset to the broader CINAg experiment documentation.
- Data access and reuse:
  - Provide dataset with accompanying metadata and method notes to support reuse in meta-analyses or cross-study comparisons.
  - Maintain data quality flags or notes for any anomalous rows or outliers identified during future reviews.