# Analytical Methods and Data Quality Metadata for Dissolved Constituents in Water

## Overview
- Comprehensive metadata for a dissolved-constituent water chemistry dataset, detailing analytes, units, detection/quantitation, sample handling, analytical methods, and data qualifiers.
- Focuses on dissolved species measured by ICP-OES, ICP-MS, colorimetric methods, and TOC, plus key water quality parameters (e.g., pH, alkalinity, flow regime).

## Analytes and Data Structure
- Analytes covered include major and trace elements and compounds such as Al, B, Ba, Be, Ca, Cd, Ce, Cl, Co, Cr, Cs, Cu, DOC, F, Fe, I, K, La, Li, Mg, Mn, Mo, Na, NH4, Ni, NO3, Pb, P04, Pr, Rb, Sb, Sc, Si, S04, Sr, Th, U, Y, Zn, and dissolved organic carbon (DOC); plus pH and flow.
- Each analyte entry includes:
  - FORM: primarily Dissolved
  - DETERMINAND: the dissolved species being measured
  - UNITS: ranges from mg/l, ug/l, to mg/l-NO3, etc.
  - LQDC: lower quantification data (numeric values or NA)
  - QUOTE TO: laboratory reporting convention
  - ANALYTICAL METHOD QC: quality control category per analyte
  - DATA QUALIFIER: data quality flags
  - FILTRATION: field filtration or unfiltered (e.g., 47 mm 0.45 µm membrane, GF/C glass fiber, or unfiltered with settling)
  - PRESERVATION: sample preservation (e.g., acidification to 1% HNO3; storage at 4°C in the dark)
  - METHOD: instrumental/analytical method (ICP-OES, ICP-MS, Autoanalyzer colorimetry, TOC analyzer, electrometric pH, etc.)
  - COMMENT: occasional methodological notes

## Sample Handling and Filtration
- Filtration commonly involves 47 mm 0.45 µm membranes in the field (except rain/cloud events) with samples returned to lab; some analyses are unfiltered or unfiltered but allowed to settle (effectively dissolved).
- Preservation frequently includes acidification to 1% nitric acid; some samples stored at 4°C in the dark; others stored in the dark at 4°C or unpreserved.
- pH samples measured electrometrically; special note about pH titration ranges (4.5–4.0 or 4.0–3.0) and comparing two data sets with statistically insignificant gradient difference.

## Analytical Methods
- ICP-OES (Inductively Coupled Plasma Optical Emission Spectroscopy)
  - Examples: ARL 34000C, Perkin Elmer style implementations
- ICP-MS (Inductively Coupled Plasma Mass Spectrometry)
  - Instrument examples: VG PlasmaQuad PQ1
- Colorimetric/Autoanalyzer methods
  - Technicon Autoanalyzer II system for Cl, NH4, NO3, PO4, F, etc. often using mercuric thiocyanate, Berthelot reaction, or molybdenum blue procedures
- DOC/TOC
  - TOC sin II Aqueous Carbon Analyzer; sample prepared by thermal oxidation
- pH
  - pH measured with Radiometer pH meter and electrode
- Si interference corrections noted in later entries
- Documentation of method changes and notes about sensitivity changes over time (e.g., 1992–1998 Si interference corrections; method changes affecting sensitivity)

## Data Quality and Qualification
- Data qualifiers and flags documented per analyte (e.g., LQDC values, QUOTE TO, DATA QUALIFIER)
- Raw instrument data flagged separately:
  - 10: Raw data from the instrument with no LQD
  - 11: Raw data with data at or below detection limits
  - 12–14: Additional notes on instrument data, corrections (e.g., Si interference) or data quality issues
  - 13: Very strange data with systematic weekly patterns; removal from database discussed but not justified in the note
  - 14: Data corrected for Si interference; long storage times may lead to degradation for low concentrations
- Interlaboratory QA:
  - ICP-OES accuracy evaluated using Aquacheck LGC Interlaboratory Proficiency Testing Scheme
  - ICP-MS trace element accuracy evaluated using Standard Reference Material 1643b from NBS
- Data provenance and QA emphasis on maintaining discoverable datasets with metadata

## Flow and Sampling Regime
- Flow parameter descriptions indicate sampling during different hydrological states:
  - Baseflow (after extended dry periods)
  - Stormflow (during intense wet periods)
- This suggests an aim to capture both low-flow and high-flow water chemistry contexts for temporal and event-based analyses.

## Endnotes and Anomalies
- Some entries include notable caveats (e.g., data affected by method changes, corrections for Si interference, and occasional anomalous data that may warrant exclusion).
- A few common themes across analytes: standardized sample handling, centralised instrument-based measurement, and robust QA/QAQC practices to support downstream correlations and interpretation.

## Implications for Analysis and Modeling
- Rich, standardized metadata enables:
  - Comparing concentrations across numerous dissolved constituents with consistent units and QC
  - Calibration and cross-method comparisons (ICP-OES vs ICP-MS vs colorimetric methods)
  - Temporal analyses across different flow regimes (baseflow vs stormflow)
  - Integration with QA flags and LQDC/QUOTE TO mechanics to handle data below detection limits and raw instrument values
- Data are well-suited for correlational analyses, trend analyses, and predictive modeling of how action (e.g., remediation, land-use change) may affect dissolved constituents in water bodies.