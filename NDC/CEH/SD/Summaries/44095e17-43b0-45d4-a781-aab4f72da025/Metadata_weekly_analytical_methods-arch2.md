# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

## Overview
- A comprehensive metadata and data dictionary for environmental analytical data collected at multiple Welsh catchments (e.g., Tanllwyth, Lower Hafren, Hafren), covering rainfall, cloudwater, stream, borehole, and input samples.
- Documents the full chain from sample collection to laboratory analysis, including pre-concentration steps, filtration, preservation, analytical methods, labs, and quality control.
- Time span largely from 1983 to 2007 with multiple laboratories (Wallingford, Lancaster, Staylittle, Bangor, Lancaster) and a range of instrumental techniques (ICP-OES, ICP-MS, AAS, ion chromatography, colorimetry, TOC analyzers).

## Key data content and structure
- For each analyte (e.g., Aluminium, Ammonium, Antimony, Arsenic, Barium, Beryllium, Boron, Bromide, Cadmium, Caesium, Calcium, Cerium, Chloride, Chromium, Cobalt, Conductivity, Copper, Dissolved organic carbon, Fluoride, Nitrate, Nitrite, Orthophosphate, pH, Potassium, Sulphate, Sodium, Zinc, and many others):
  - Form: mostly dissolved; some measurements include total or operationally defined forms.
  - DETERMINAND: the chemical species measured (e.g., Al, NH4-N, Cl, NO3-N).
  - UNITS: e.g., ug/l, mg/l, mg/l - N, uS/cm, etc.
  - LQDC (lower quantification data qualifier) and QUOTE TO: specify detection/quantification thresholds.
  - START/END: time ranges for data series (often 1983–2007 with gaps).
  - LOCATION OF ANALYSIS: labs and sites (Wallingford, Lancaster, Staylittle, Bangor, etc.).
  - ANALYSIS/METHOD: lab technique (ICP-OES, ICP-MS, AAS, colorimetry, ion chromatography, TOC analyzer, etc.) and any special pre-concentration (evaporation, dilution) or pre-concentration details.
  - FILTRATION: filter types and field vs lab handling (often 0.45 μm membranes; field rain/cloud vs lab return).
  - PRESERVATION: storage conditions and media (e.g., dark storage at 4°C; chemical preservation like nitric acid or permanganate).
  - PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE DETECTION LIMIT: describes concentration steps (e.g., evaporate 400 mL to concentrate 20x; dilutions for ICP analysis).
  - METHOD QC QUALIFIER and NOTES: qualitative and procedural notes; sometimes multiple methods used over time with averaging noted.
- Data primarily capture long-term monitoring using standardized formats to enable cross-site comparability and temporal trend analysis.

## Data quality and QC
- ANALYTICAL METHOD QC CODES describe how accuracy was validated (e.g., proficiency testing materials from Aquacheck LGC, ISO 17025 accreditation status).
- DATA QUALIFIER CODES provide flags for data quality and data state, such as:
  - 10 Raw data from instrument (uncorrected).
  - 11 Data at or below detection limit for most of the series.
  - 12 Sensitivity issues due to method change (198...1998 period).
  - 13–17 Various data issues or contextual notes (patterns, time-of-sampling, corrections, etc.).
- Codes also note calibration/accuracy provenance and instrument-specific considerations.

## Data processing, transformations, and calculations
- Includes explicit conversion between streamflow (cumecs) and area-weighted runoff (mm/15 min) using catchment areas:
  - mm/15min = cumecs × 0.9 / catchment area (km^2)
  - cumecs = (mm/15min) × catchment area / 0.9
- Sampling times are defined relative to sample type:
  - Stream and borehole samples are grab samples at the specified time.
  - Rainfall, Throughfall, Stemflow, and Cloud are time-integrated samples with intervals between successive samples or defined suspension gaps.
- Volume-weighted sampling time is used to compute Year Mean Sampling and to align precipitation/runoff timing with chemical measurements.
- Different sample matrices have specific handling rules (e.g., cloud catch, throughfall, hourly rainfall, cloudwater tests).

## Practical implications for Analysts Monitoring the Environment
- The document provides a standardized framework to store and interpret extensive environmental chemistry data, enabling:
  - Consistent data verification, quality assurance, and transformation before analysis.
  - Clear documentation of analytical methods, sample handling, and QC processes to support scrutiny of environmental health and policy performance over time.
  - Cross-site comparability and robust temporal trend analyses by harmonizing units, detection limits, pre-concentration steps, and data qualifiers.
- It emphasizes accessibility and transparency of underlying data through standardized metadata (lab, method, QC, filtration, preservation) and explicit data qualifiers.

## Takeaway
- This metadata repository underpins rigorous environmental monitoring by detailing the full analytical workflow, quality controls, and data processing rules necessary to compare environmental data across time, sites, and analytical methods. It supports the Analysts Monitoring the Environment archetype in delivering consistent, auditable assessments of environmental health and policy outcomes.