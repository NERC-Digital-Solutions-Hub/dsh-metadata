# Field measurements of alkalinity, chloride-ion, conductivity, pH and nutrients in rainwater (2004-2006) [LOCAR] LOCAR BASELINE DATASETS LOCAR

## Overview
- LOCAR baseline dataset of rainwater samples collected 2004–2006 across 7 sites in the Frome/Piddle, Pang/Lambourn, and Tern catchments.
- Measured a suite of anions and nutrients in rainwater to support catchment science.

## Sampling design and locations
- Sites (RNWQ): FP04, FP13, FP35 (Frome/Piddle); PL06, PL11 (Pang/Lambourn); TE11, TE17 (Tern).
- Catchments: FP (Frome/Piddle), PL (Pang/Lambourn), TE (Tern).
- Timeframe: January 2004 – May 2006.
- Sampling frequency: fortnightly in Pang/Lambourn and Tern catchments; roughly monthly in Frome/Piddle catchment.

## Measured variables and analytical methods
- Variables (units):
  - Alkalinity as CaCO3 (mg/L)
  - Ammonia (mg/L as N)
  - Chloride-ion (mg/L)
  - Conductivity at 20°C (µS/cm)
  - Nitrate (mg/L as N)
  - pH (pH units)
  - Phosphorus soluble reactive (SRP, mg/L P)
  - Silicate reactive dissolved (SRD, mg/L SiO2)
  - Sulphate (mg/L)
- Methods (user-facing summary):
  - Lab analyses by Thames Water; chloride, sulphate, nitrate, SRP, SRD, ammonia via Seal discrete analyser; pH by pH electrode; conductivity by conductivity electrode.
  - Nitrate conversion note: measured as NO3 mg/L and converted to mg/L N using X*14/64.
  - Quality indicators reported as calibration constants and performance metrics (e.g., mean concentration measured, uncertainty, detection limits).

## Sampling and processing protocol
- Rainwater collectors collected in the field and returned to the laboratory.
- Alkalinity and pH readings done on unfiltered samples (glass bottle); SRP filtered; other determinands unfiltered.

## Data quality, provenance, and metadata
- Thames Water performed quality control, including weekly duplicate and QC samples for comparison.
- Data include detailed method and quality metrics (calibration standards, percent accuracy, uncertainty, LOD).
- Time data issues:
  - Frome and Piddle catchments lack time stamps; time recorded as 00:00 to indicate missing data.
- Data visualization: box-and-whisker plots generated for all variables to depict range, median, quartiles, and outliers.

## Data structure and discoverability
- Dataset includes site codes, catchment codes, measurement units, and detection limits.
- Documentation provides explicit data processing steps and measurement conversions (e.g., nitrate to nitrogen conversion).

## Implications for data leadership (data governance and reuse)
- Demonstrates importance of comprehensive metadata and provenance to enable cross-site/catchment integration.
- Highlights the need for consistent time stamping across all catchments to support temporal analyses.
- Underlines the value of including quality metrics (uncertainty, LOD, QC results) with data products for trust and reuse.
- Suggests benefits of centralized data storage and standardized metadata schemas to improve discoverability and interoperability.

## Challenges and considerations
- Missing timestamps for half of the dataset (Frome/Piddle) complicates temporal analyses.
- Variation in sampling frequency between catchments.
- Complex calibration/quality metrics that must be preserved for proper interpretation.

## Recommendations for future data management
- Ensure complete, consistent time stamps across all catchments.
- Harmonize units, methods, and metadata standards; retain detailed QC and calibration information.
- Centralize storage with clear data dictionaries and processing steps (e.g., nitrate conversion formula).
- Maintain visibility of data quality indicators (uncertainty, LOD) alongside analytical results.
- Provide accessible data products and visualizations (e.g., distribution plots) to support reuse and governance discussions.