# Data dictionary for water quality analyses (Plynlimon dataset)

- The document provides a comprehensive metadata schema for a wide range of dissolved constituents measured in water samples, detailing per-analyte attributes, field and lab methods, and quality flags.

## Purpose and Scope
- Defines metadata for dissolved analytes (e.g., Al, Ca, Cl, NO3, PO4, pH, etc.) across field and laboratory analyses.
- Captures how samples are collected, preserved, filtered, analyzed, and quality-checked.
- Includes data quality flags, raw vs processed data notes, and provenance elements to support discoverability and reuse.

## Data Model and Key Metadata Elements
- For each analyte, the following fields are specified (with many entries repeated across elements):
  - FORM: typically Dissolved
  - DETERMINAND: the analyte measured
  - UNITS: measurement units (e.g., ug/l, mg/l, uEq/l)
  - LQDC ˙: lower/limit of detection or data qualifier placeholder
  - QUOTE TO: quotation/reference level for lab standards
  - ANALYTICAL METHOD QC: QC code for the analytical method
  - DATA QUALIFIER: numeric flag indicating data quality or status
  - FILTRATION: filtration method/particle size used in field (e.g., 47 mm 0.45 µm membrane; GF/C)
  - PRESERVATION: chemical preservation (e.g., acidification to 1% with high purity nitric acid)
  - METHOD: analytical technique (e.g., ICP-MS, ICP-OES, automated colorimetry, titration)
  - COMMENT: additional notes
- Examples covered include Al, Gran alkalinity, Ba, Be, Ca, Cd, Ce, Cl, Co, Cr, Cs, Cu, DOC, F, Fe, I, K, La, Li, Mg, Mn, Mo, Na, NH4, Ni, NO3, Pb, pH, PO4, Pr, Rb, Sb, Sc, Si, SO4, Sr, Th, U, Y, Zn, and a Flow entry for survey-based flow regimes.
- Data qualifiers and notes appear repeatedly (e.g., 10 for raw data, 11–14 for various data states), with some entries indicating data that were corrected (Si interference), raw data without lower-quantitation data (LQD), or data flagged as problematic (e.g., “Very strange data … removal from database”).

## Data Collection, Processing, and Storage
- Field filtration and handling:
  - Usually field filtration using 47 mm 0.45 µm membranes, with exceptions for rain/cloud events.
  - Some analyses are unfiltered or allow settling to effectively measure the dissolved fraction.
- Preservation and storage:
  - Samples preserved by acidification to 1% HNO3 and stored at 4°C in darkness to minimize CO2 degassing and degradation.
  - For some constituents (e.g., Cl, DOC), specific storage and handling notes apply (e.g., dark storage, at 4°C, etc.).
- Analytical methods:
  - Inductively Coupled Plasma Mass Spectrometry (ICP-MS) and Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES) using VG PlasmaQuad PQ1 or ARL 34000C systems.
  - Automated colorimetry (Technicon Autoanalyzer II) for various species.
  - pH determined electrometrically; DOC measured by TOC analyzer.
  - Gran alkalinity determined by manual titration followed by auto-titration and Gran plots.
  - NO3, PO4, F, and others via colorimetric methods or specific reagent-based assays.
- QA and interlaboratory checks:
  - Accuracy validated using materials from Aquacheck LGC Interlaboratory Proficiency Testing Scheme.
  - For certain elements, Standard Reference Materials (e.g., SRM 1643b) used for method validation.

## Data Quality, Provenance, and Flags
- Data qualifiers and flags provide context on data quality and processing state:
  - 10: Raw data from instrument, not rounded; reference to LQDC and Quote To for lab standards.
  - 11: Raw data from instrument, data at or below detection limit for most of the time series.
  - 12: Raw data with notes on method changes; some method-change caveats.
  - 13: Raw data with unusual patterns; removal from database considered; treated with caution.
  - 14: Data corrected for known interferences (e.g., Si interference).
- Notes also indicate that some data (e.g., pH gradient data) were limited to a single set due to statistical similarity between runs.
- Raw data entries emphasize preservation of instrument outputs prior to processing.

## Data Lifecycle, Discoverability, and Access
- Data are designed to be uploaded to relevant portals and catalogued as part of a larger dataset.
- Metadata supports traceability from field sampling through laboratory analysis to final data products.
- Presence of QC and QA evidence (interlaboratory checks, SRMs) supports data reliability and auditability.

## Particular Challenges for Data Stewards
- Incomplete picture of user needs and priorities for dataset use.
- Timely delivery of data from data creators and ensuring standards are met across contributors.
- Heterogeneous systems and formats across field and lab workflows; legacy databases require bespoke solutions.
- Handling large datasets and ensuring efficient transfer, storage, and accessibility.
- Managing updates, embargoes, and disclosure constraints while maintaining data lineage.

## Implications and Recommendations for Data Stewardship
- Standardize metadata model across all analytes with consistent definitions for FORM, DETERMINAND, UNITS, LQDC, QUOTE TO, METHOD, FILTRATION, PRESERVATION, and DATA QUALIFIER.
- Enforce uniform field and lab procedures (filtration, preservation, storage) or clearly document any deviations.
- Maintain thorough data provenance, including method changes, QA checks, and interlaboratory validation results.
- Clearly document and justify data qualifiers (especially 10–14) and any data removals or corrections.
- Ensure raw data, processed data, and derived QA metrics are preserved and linked to analyte metadata.
- Improve discoverability by publishing comprehensive catalog records that map each analyte to its metadata fields and QA status, including notes on data limitations and historical method changes.
- Develop data pipelines to harmonize legacy formats and support ongoing updates, while capturing versioning and audit trails.
- Consider special handling for Flow-related data (baseflow vs stormflow) and ensure consistent definitions and metadata tagging.