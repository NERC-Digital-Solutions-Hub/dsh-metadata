# Chemical Analysis Metadata and Data Quality for Water Samples

## Overview
- The document defines detailed metadata and quality-control information for dissolved chemical determinations in water samples, including methods, units, sample treatment, and QA provenance.
- It covers a wide range of elements and parameters, with emphasis on dissolved fractions, filtration, preservation, and instrument-based analyses.
- Interlaboratory QA references (e.g., Aquacheck LGC, SRM 1643b) are used to assess accuracy.

## Data Schema and Key Fields
- Core fields found throughout the dataset (illustrative examples):
  - DETERMINAND: what is measured (often "Dissolved <element/compound>").
  - UNITS: measurement units (e.g., ug/l, mg/l, mg/l-PO4, etc.).
  - FORM: phase (e.g., Dissolved).
  - FILTRATION: filtration method and membrane (e.g., 47 mm 0.45 μm membrane; GF/C).
  - PRESERVATION: storage/handling (e.g., acidification to 1% HNO3; storage at 4°C in the dark).
  - METHOD: analytical technique (e.g., ICP-MS, ICP-OES, automated colorimetry, titration).
  - COMMENT: notes on methods, data interpretation, or anomalies.
  - LQDC: limits/criteria related to data quantitation (often NA for some parameters).
  - QUOTE TO: rounding/quotation convention for lab standards.
  - ANALYTICAL METHOD QC: quality-control tier for the analytical method.
  - DATA QUALIFIER: QC/qualifier flags (numerical codes like 10, 12, 13, etc.).
- Additional recurring entries include pH, Flow (baseflow vs stormflow), and Flow-related notes for survey sampling.

## Analytical Methods and QA
- Analytical techniques represented include:
  - Inductively Coupled Plasma Mass Spectrometry (ICP-MS).
  - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES).
  - Automated colorimetry (e.g., Technicon Autoanalyzer II) for F, NH4, NO3, Si, SO4, PO4, etc.
  - Titrimetric methods (e.g., Gran plots for alkalinity).
  - pH electrometric measurement.
  - TOC/organic carbon methods for DOC.
- QA/QAQC practices:
  - Interlaboratory proficiency testing and Standard Reference Materials (e.g., Aquacheck LGC, SRM 1643b) used to assess accuracy.
  - Data qualifiers and raw data notes to indicate data quality and potential issues.
  - Notes about method changes affecting sensitivity (e.g., ICP-MS vs ICP-OES transitions, Si interference corrections).

## Sample Handling, Filtration, and Preservation
- Filtration details:
  - Commonly 47 mm filters with 0.45 μm pore size; exceptions with GF/C glass fibre filters or unfiltered (but allowed to settle) for certain parameters.
  - Rain/cloud conditions often noted as exceptions for field filtration.
- Preservation and storage:
  - Acidification to 1% with concentrated high-purity nitric acid.
  - Glass bottle storage to prevent CO2-degassing (for alkalinity and certain parameters).
  - Cold storage (4°C) in the dark to preserve samples (e.g., DOC, Cl, etc.).
- Sample processing notes:
  - Some measurements are effectively “dissolved” due to filtration or settling practices.
  - pH titration ranges and gradients discussed, with notes on data representation (one set vs. two sets).

## Data Provenance and Interpretation
- Proficiency testing and standard references validate instrument accuracy for different determinations:
  - ICP-OES and ICP-MS conceptually validated using external reference materials.
  - Documentation emphasizes accuracy and potential limitations, with repeated notes about data validity.
- Some entries document data issues:
  - Data flagged as problematic or removal-worthy due to unusual patterns or method changes.
  - Notes indicate time-series data at/below detection limits for major portions of the record.

## GIS/Map-Making Implications for Data Products
- Data alignment and standardization:
  - Ensure consistent units across all records (e.g., ug/l vs mg/l in different sections).
  - Harmonize dissolved vs total forms and filtration status to avoid misclassification in maps.
- Attribute schema design:
  - Include fields for DETERMINAND, UNITS, FORM, FILTRATION, PRESERVATION, METHOD, LQDC, QUOTE TO, DATA QUALIFIER, and QC notes.
  - Capture QA provenance (QA/QC status, proficiency results, SRM references) as separate metadata attributes.
- Spatial data integration:
  - Link chemical measurements to precise sampling locations and times to enable gradient mapping (e.g., baseflow vs stormflow).
  - Use Flow-related notes to differentiate hydrological states in spatial analyses.
- Data quality considerations:
  - Use DATA QUALIFIER and ANALYTICAL METHOD QC to filter or annotate symbols on maps (e.g., suppress questionable data, flag below-detection data).
  - Account for data with method changes or corrections (e.g., Si interference corrections) in temporal visualizations.
- Temporal and uncertainty handling:
  - Treat LQDC and QUOTE TO values as controls on data precision for time-series visualizations.
  - For raw/instrumental data notes (LQDC = raw data with no rounding), decide on appropriate aggregation strategy for GIS layers.

## Important Cautions and Notable Points
- Some parameters have multiple entries with slightly differing details by element (e.g., dissolution status, filtration, and preservation nuances).
- A minority of data entries explicitly note removal from databases due to irregular patterns or questionable validity.
- The pH data section notes a comparison between two titration ranges but ultimately presents a single, statistically indistinguishable set.
- Several parameters include explicit references to method-specific QC and interlaboratory calibration practices, underscoring the dataset’s emphasis on validated measurements.

## End Notes
- The document provides a comprehensive framework for dissolved chemical measurements in water with strong emphasis on sample handling, analytical methods, QA, and data provenance, enabling robust GIS-enabled mapping and analysis of spatial patterns in water chemistry.