# Dataset Metadata and QC for Dissolved Chemical Analytes in Water

- Purpose and aim
  - Use standardized data to demonstrate environmental condition over time, enabling scrutiny of environmental health and policy performance.
  - Analysts typically work within organisations with established monitoring responsibilities, applying topic expertise and standardized analytical approaches.

- What the document covers
  - Comprehensive metadata for dissolved chemical determinations across a wide range of elements and compounds (e.g., Al, Gran alkalinity, Cl, NO3, PO4, DOC, pH, Flow).
  - An emphasis on dissolved fractions, with determinations often labeled as “Dissolved” and/or “DISSOLVED” forms.

- Data scope and structure
  - Numerous analytes with consistent fields for each:
    - DETERMINAND, UNITS, FORM, LQDC (limit of quantitation display code), QUOTE TO (reporting scale), ANALYTICAL METHOD QC, DATA QUALIFIER, FILTRATION, PRESERVATION, METHOD, and COMMENT.
  - Units vary by analyte (e.g., ug/l, mg/l, uEq/l, mg/l-NO3, mg/l-PO4, mg/l-SO4, etc.).
  - Filtration and preservation protocols are specified for each analyte (e.g., 47 mm 0.45 μm membranes, acidification to 1% HNO3, storage at 4°C in dark, or unfiltered/dissolved but settled).
  - Analytical methods include Inductively Coupled Plasma Mass Spectrometry (ICP-MS), Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES), automated colorimetry, and specific pH/electrometric titration techniques.
  - Data qualifiers and quality flags accompany measurements (e.g., LQDC values, QUOTE TO, DATA QUALIFIER, and “RAW data” notes).

- Data quality control and validation
  - Instrument accuracy assessed via proficiency testing and reference materials:
    - ICP-OES results checked with Aquacheck LGC Interlaboratory Proficiency Testing Scheme.
    - ICP-MS trace elements checked with Standard Reference Material 1643b from NBS (National Bureau of Standards).
  - Observations about method performance and data quality:
    - Some notes indicate historical method changes affecting sensitivity (e.g., 1992–1998 for certain measurements).
    - Instances of problematic data flagged (e.g., data set 13 described as having very strange patterns and removal from database described as “extreme caution”).
    - Data qualifiers exist to indicate data reliability, detection limits, and potential issues.

- Sample handling, collection, and field practices
  - Sample filtration often performed in the field (47 mm filters, 0.45 μm), with exceptions during rain/cloud events (samples may be returned to lab for processing).
  - Filtration and settling practices described as “effective dissolved” for certain parameters.
  - Preservation strategies include acidification to 1% HNO3 (high purity) and storage conditions to minimize CO2 de-gassing.
  - Field notes reference baseflow vs stormflow conditions for Flow data, illustrating distinct hydrological states in the dataset.

- Temporal and contextual aspects
  - Flow data categorized into baseflow and stormflow, indicating samples collected under varying hydrological conditions.
  - pH measurements taken electrometrically with standard pH meters, with notes on comparability of measurements across the dataset.

- How this supports environmental monitoring aims
  - Provides a standardized, auditable framework for reporting environmental health indicators over time.
  - Facilitates cross-site and long-term trend analyses through uniform determinants, QC practices, units, and reporting conventions.
  - Enables scrutiny of policy performance by ensuring data are quality-assured, properly stored, and accessible through appropriate portals.

- Key considerations for analysts using the dataset
  - Be aware of data qualifiers and flags that indicate detection limits, raw instrument data, and potential data quality concerns (e.g., RAW data entries, “Data at or below detection limit,” and notes of data removal).
  - Interpret historical method-change notes when comparing measurements across decades (e.g., changes in method affecting sensitivity).
  - Account for sample handling differences (field vs lab processing, filtration status, and preservation) when aggregating or comparing results.
  - Use the proficiency-tested reference materials as benchmarks for validating analytical results.