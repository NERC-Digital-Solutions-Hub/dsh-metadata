# Luminescence signals and estimates of dose rate from sediment cores, Lake Suigetsu, Japan SUPPORTING DOCUMENTATION

## Overview
- Dataset of luminescence signals and estimated dose rates from Lake Suigetsu sediment cores across four time periods: the last 500 years (Holocene), the Laschamp geomagnetic excursion, the varve limit, and Termination II.
- Luminescence quantified via Portable Optically Stimulated Luminescence (POSL) analysis on bulk sediment (blue light and infrared) and laboratory profiling of prepared quartz fine fractions and polymineral fine fractions.
- Aims to assess whether luminescence methods can detect past catchment environmental change and to determine burial ages from the cores.
- Data generated alongside estimated dose rates at six sample points to evaluate mineral fractions as potential chronometers and down-core variations in dose rate that could affect dating.

## Collection/Generation Methods
- Time Periods and sampling:
  - Time Period 1 (Last 500 Years): 4 cm integrated samples along core A(N)01upper; contiguous sampling (n = 24).
  - Time Period 2 (Laschamp Excursion): 100-year integrated samples every 1,000 years between 35,000 and 45,000 cal BP (n = 11) — spot sampling.
  - Time Period 3 (Varve Limit): sampling at depth corresponding to varve initiation; contiguous samples along core A(S)24 (n = 12).
  - Time Period 4 (Termination II): ~100-year integrated intervals ~2,000-year apart (n = 13) — semi-random spacing.
- Light exposure protection: top 1 mm removed under dim red light to avoid light exposure; deeper material considered unaffected by light for analytical purposes.
- Dose rate estimation samples: six samples across all periods for ED_R determination (post-luminescence analysis; selected to represent representative natural luminescence values and areas with elevated luminescence).
- POSL measurements:
  - Instrument: SUERC POSL reader in Wakasa, Japan; continuous wave proxy (CWproxy) protocol with seven photon-count periods (dark, IR stimulations, dark, blue stimulations, dark).
  - Calculated variables: POSLnet, PIRSLnet (proxy for age, sensitivity, dose rate); Depletion Indices (Blue and IR); POSL/PIRSL ratio; instrument checks.
- Laboratory profiling (mineral fractions):
  - Fractions: Quartz Fine (QF, predominantly quartz) and Polymineral Fine (PMF, mixed mineralogy).
  - Chemical preparation: removal of grains <90 µm, acid/base washes (HCl; HF in PMF/QF procedures); PMF saturated in acetone; QF subjected to HF etching.
  - Discs prepared for TL/OSL measurements; single aliquot regenerative-dose (SAR) protocol used to estimate equivalent dose (ED_e).
  - Fractions measured under IRSL and/or OSL conditions depending on fraction.
- Data processing and reporting:
  - ED_e values derived from natural signal and response to test doses (50 Gy benchmark; some doses omitted due to low sensitivity).
  - ED_R dose-rate calculations from elemental concentrations (U, Th, K) via ICP-MS/OES; two scenarios for dose rate calculations:
    - Scenario 1: 30 µm mean grain size, activity-free grains.
    - Scenario 2: 30 µm mean grain size with internal contents equal to the surrounding matrix.
  - Water content corrections, attenuation factors, and a small cosmic dose rate component included for oldest samples; others omitted when lake depth was greater.
  - ED_R values combined with ED_e to support first-order age estimates and cross-check with established Suigetsu chronology.

## Quality Control
- Data included only when luminescence signals were quantifiable above background levels.
- Empty chamber measurements and instrument standards run to verify performance.

## Data Structure & Nature and Units
- Two CSV files:
  - lakesuigetsu_luminescence_profiling_results.csv: POSL analysis results and laboratory profiling data.
    - Key fields include Time Period, Sample Code, Lower/Upper Age (yr BP), POSL/PIRSL signals and errors, POSL depletion indices, POSL/PIRSL ratio, QF blue light sensitivity and estimated dose, PMF IR/blue signals and estimated dose, and corresponding errors.
  - lakesuigetsu_luminescence_doserate_results.csv: Dose rate estimation results.
    - Key fields include Time Period, Sample Code, Lower/Upper Age (yr BP), Water content, inferred palaeo-water content, Th/U/K concentrations, and dose-rate components (alpha, beta, gamma, cosmic) for Scenario 1 and Scenario 2, plus total dose rate (mGy/yr) and derived values.
- Data notes:
  - Ages referenced to IntCal20 yr BP; age-model information documented (Correlation Model, Event Layer, Age Model versions).
  - Explicitly records units (Counts, Gy, mGy/yr, % water, ppm, etc.) and the methodological details used to derive each value.

## References
- Burbidge, C. I., Sanderson, D. C. W., Housley, R. A. & Allsworth Jones, P. (2007). Survey of Palaeolithic sites by luminescence profiling.
- Kinnaird, T. C., Sanderson, D. C. W. & Bigelow, G. F. (2015). Feldspar SARA IRSL dating of very low dose rate aeolian sediments.
- Olive, V., Ellam, R. M. & Wilson, L. A. (2001). Protocol for determination of rare earth elements by ICP-MS.
- Sanderson, D. C. W. & Murphy, S. (2010). Using simple portable OSL measurements and laboratory characterization to understand sediment sequences for luminescence dating.