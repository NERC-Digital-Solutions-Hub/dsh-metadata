# Chemical Analysis Data Table

## Overview
- A comprehensive laboratory data table detailing dissolved constituents and related measurements for water samples.
- Records cover a wide range of elements and compounds (e.g., Al, Cl, NO3, NH4, Ca, Na, Mg, Fe, Si, SO4, PO4, etc.) plus ancillary data such as pH and alkalinity.
- Includes metadata fields for each determinate: form (dissolved), units, detection qualifiers, laboratory QC, filtration, preservation, analytical methods, and data qualifiers.
- Also documents flow conditions (baseflow vs stormflow) and general data handling notes.

## Data Structure and Fields
- Repeated field groups for each determinate include:
  - DETERMINAND (the chemical species measured)
  - FORM (e.g., Dissolved)
  - UNITS (e.g., ug/l, mg/l, uEq/l)
  - LQDC (low quantity detection control) and QUOTE TO (data quotation scale)
  - ANALYTICAL METHOD QC (quality control level)
  - DATA QUALIFIER (data quality flags)
  - FILTRATION (membrane or glass fibre filter type and field vs lab handling)
  - PRESERVATION (sample storage conditions)
  - METHOD (analytical technique, e.g., ICP-MS, ICP-OES, automated colorimetry, electrometric pH)
  - COMMENT (supplementary notes)
- Notable patterns include many elements with consistent formats and a few exceptions/notes:
  - Common measurement techniques: ICP-MS (VG PlasmaQuad PQ1..), ICP-OES (ARL 34000C..), automated colorimetry, TOC for DOC, pH electrometry.
  - Filtration often specified as 47 mm 0.45 µm membrane (field) or GF/C glass fibre (field) with return to lab.
  - Preservation usually acidification to 1% HNO3 or storage at 4°C in dark.
- Some entries provide additional process context:
  - Flow definitions: baseflow versus stormflow sampling.
  - Baseflow/stormflow definitions used to categorize samples in the Flow section.

## Analytical Methods and Quality Control
- Inductively Coupled Plasma techniques:
  - ICP-MS (e.g., VG PlasmaQuad PQ1..) for multielement determinations; includes QC qualifiers and calibration notes.
  - ICP-OES (e.g., ARL 34000C) for several metals (Ca, Mg, etc.).
- Colorimetric and other methods:
  - Automated colorimetry (Technicon Autoanalyzer II) for Cl, NO3, NH4, F, Si (molybdenum blue, Berthelot reaction, etc.).
  - TOC for DOC (TOCsin II Aqueous Carbon Analyser).
- pH measurement via electrometric method with detailed notes on range and data handling.
- Alkalinity:
  - Gran alkalinity measured by titration (manual, later auto-titration with Metrohm Titrino) using Gran plots; pH titration ranges documented.
- Flow-related data:
  - Mention of “baseflow” and “stormflow” in the Flow section to distinguish sample states.

## Data Quality and Provenance
- External proficiency and standards referenced:
  - Accuracy of ICP-OES determinations evaluated with Aquacheck LGC Interlaboratory Proficiency Testing Scheme.
  - Accuracy of ICP-MS trace element determinations evaluated with Standard Reference Material 1643b (NBS).
- Data qualifiers and raw data handling:
  - Several data qualifiers indicate raw instrument data not yet rounded (LQDC 10), or raw data with no LQD (10) for quotation to lab standards.
  - Entries labeled with LQDC values 10, 11, 12, 13, 14 indicate varying data quality and processing status:
    - 10: Raw data, not yet LQD-rounded.
    - 11: Raw data with notes about detection limits.
    - 12: Raw data with method-change-related sensitivity issues.
    - 13: Very odd data with systematic weekly-pattern issues; removal from database considered but not justified.
    - 14: Data corrected for interference (e.g., Si interference) and notes on storage time effects.
- Overall data quality guidance:
  - Users should treat datasets 10–14 with corresponding caveats; dataset 13 requires extreme caution or exclusion.
  - The presence of proficiency testing references suggests formal QA/QAQC processes, but some data require careful interpretation.

## Data Processing, Usage, and Governance
- Outputs are designed to support self-service data exploration and dashboards for end users, with associated guidance on data usage.
- Data governance considerations include the need to:
  - Track sample state (baseflow vs stormflow) and time-related storage/preservation conditions.
  - Distinguish data that has been flagged or corrected (Si interference, raw vs processed) from finalized results.
  - Decide on retention or removal of problematic records (e.g., dataset 13 and certain raw-data entries).
- The dataset provides a comprehensive metadata framework to document how each determinate was measured, stored, and validated, enabling cross-project comparability and traceability.

## Endnotes and Notable Observations
- The document captures both routine measurements across a broad suite of elements and explicit notes on data quality and processing status.
- It highlights the importance of:
  - Rigorous QC and proficiency testing alignment for element determinations.
  - Clear labeling of raw vs processed data and the implications for downstream analyses.
  - Documentation of sample handling (filtration, preservation, storage) to ensure data interpretability.
- For practitioners, key actions include:
  - Filtering out or separately flagging data with LQDC 11–14 in analyses, per project policy.
  - Verifying flow-state context (baseflow vs stormflow) when interpreting concentration trends.
  - Consulting the provenance notes when reconciling ICP-MS vs ICP-OES results for the same determinate.