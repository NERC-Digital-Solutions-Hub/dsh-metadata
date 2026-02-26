# Soil physico-chemical properties 2007 [Countryside Survey], Great Britain

- Scope and coverage
  - Data from Countryside Survey 2007 covering soils across up to 591 1-km squares in Great Britain (England, Scotland, Wales).
  - Topsoil samples (0–15 cm) collected from the western corner of Main Plots within each square; up to five plots per square.
  - Includes both field measurements and derived quantities for each sample such as carbon and nutrient stocks.

- Dataset structure and key variables
  - SQUARE: 1-km square sampling site code
  - PLOT: Plot identifier within each square
  - YEAR: Year of survey
  - PH: Fresh soil pH in water (method and QA notes below)
  - LOI: Loss on ignition (%)
  - C_CONC_LOI: Carbon concentration derived from LOI (g/kg) using 0.55 x LOI
  - C_STOCK_LOI: Carbon stock derived from LOI (t/ha) using 0.55 x LOI
  - BULK_DENSITY: Bulk density (g/cm3)
  - MOISTURE: Moisture content (%)
  - N_PERCENT: Nitrogen content (%)
  - N_STOCK: Nitrogen stock (t/ha)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
  - LC07 / LC07_NUM: ITE Land Classification 2007 (text and numeric code)
  - COUNTRY: Country (England ENG, Scotland SCO, Wales WAL)
  - COUNTY07: County/region identifiers
  - EZ_DESC_07: Countryside Survey Environmental Zone description
  - All values include units and are accompanied by methodological notes and QA guidance

- Measurement protocols and derivations
  - pH measurements
    - Two measurements per subsample: pH in deionised water and in 0.01 M CaCl2
    - Fresh soil pH in water: 10 g soil with 25 ml deionised water (1:2.5 by weight)
    - Calibration and QA: daily checks with pH 4 and pH 7 buffers; if drift >0.02 pH units, re-calibrate; include standard soil, certified reference soil, and duplicates every 25 samples
    - Consistency: protocols align with CS Soil Manuals; temperature control during calibration and measurement
  - LOI (loss on ignition)
    - Sub-sample: 10 g air-dried soil; dried at 105°C for 16 hours; weighed; combusted at 375°C for 16 hours
    - Reason for method: CS2007 uses the 1978 LOI method to ensure comparability with CS1978 and CS2000 data
    - QA: standard material and duplicate analyses per batch; cross-checks within Defra/NERC joint codes of practice
  - Bulk density (BD)
    - Derived from core measurements; follows LOI protocol for moisture and preparation
    - Note: ISO 11272:1998 method exists but CS uses a bespoke approach; QC limited by lack of control soil, with alternative reliability checks (e.g., comparison to expected values, cross-year consistency)
  - Olsen-P
    - Extraction: 5 g air-dried soil with 100 ml 0.5 M NaHCO3 (pH 8.5)
    - Analysis: colorimetric molybdenum blue with continuous-flow skalar; includes dialysis to mitigate reagent interference
    - QA: replicate, standard soil, and certified reference soil per batch of 25 samples; matched conditions to CS2000
    - Considerations: drying effects, extraction temperature, soil-to-solution ratio, and organic matter interactions noted
  - Total nitrogen (N)
    - Method: CEH Lancaster UKAS-accredited SOP3102; elemental analysis with Vario+EL
    - Procedure: oxidative combustion with subsequent detection of CO2 and N2 (calibrated with acetanilide)
    - QA: in-house reference materials with each batch
  - Quality assurance and governance
    - QA/QC aligned with Defra/NERC/BBSRC Joint Codes of Practice
    - Cross-checks and re-analyses performed where methods changed; validation against prior CS datasets (CS2000)
    - Accreditation status of participating laboratories documented

- Sampling strategy and data governance
  - Sampling design based on Land Classes to capture environmental gradients; ensures national representativeness for Great Britain
  - 591 sample squares surveyed in 2007 (289 England, 107 Wales, 195 Scotland)
  - Power analyses conducted to ensure reliable reporting for major measurements (pH, LOI) and subset analyses for other analytes
  - Field and laboratory protocols documented; archiving and data manipulation procedures described
  - Data ownership and acknowledgement
    - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
    - All use must acknowledge Countryside Survey data; acknowledgement language provided for copies, publications, and presentations
    - Data and methods are documented in CS technical reports and Soil Manual for transparency and reproducibility

- Documentation and references
  - Soils Manual: Emmett et al. 2008 (Countryside Survey. Soils Manual; CS Technical Report No. 3/07)
  - Countryside Survey: Soils Report from 2007 (Emmett et al. 2010)
  - Supporting methodological references and publications related to soil analysis and land classification
  - Data availability and repository references (CS website, NERC Environmental Information Data Centre)

- Practical considerations for data stewardship
  - Metadata completeness: clear variable definitions, units, and derived values
  - Provenance: detailed laboratory protocols and QA steps to support reproducibility and auditing
  - Updates and interoperability: explicit methods to ensure comparability with CS1978 and CS2000 datasets; documentation supports integration with future Countryside Survey iterations
  - Usage guidance: ensure proper acknowledgement in all outputs; monitor for methodological changes that may affect comparability across years

- Summary of end-to-end workflow
  - Field sampling in 591 1-km squares, with standardized collection around Main Plots
  - Laboratory analysis for pH, LOI, BD, Olsen-P, and total N following CS-specific protocols
  - Derivation of carbon stock and concentration from LOI; compilation of nutrient stocks
  - Rigorous QA/QC and adherence to joint codes of practice; archiving and documentation for data sharing and reuse