# Luminescence signals and estimates of dose rate from sediment cores, Lake Suigetsu, Japan SUPPORTING DOCUMENTATION

## Overview
- Dataset documents luminescence signals from Lake Suigetsu sediment cores across four time periods: the last 500 years (537 to -47 cal BP), the Laschamp geomagnetic excursion (44,828 to 35,550 cal BP), the varve limit (73,130 to 69,413 yr BP), and glacial termination I (139,499 to 118,001 yr BP).
- Luminescence quantified by Portable Optically Stimulated Luminescence (POSL) analysis of bulk sediment (blue and infrared exposures) and laboratory profiling of prepared quartz fine (QF) and polymineral fine (PMF) fractions.
- Aims to determine if POSL and lab profiling can detect past catchment environmental change and to estimate burial age via dose-rate calculations.
- Dose rate estimates (six points across the four time periods) were produced to evaluate whether luminescence signals can underpin burial-age determinations.

## Collection and Generation Methods
- Four time periods chosen for distinctive environmental contexts, spanning local and global relevance.
- Materials sourced from Lake Suigetsu SG06 cores; total 60 samples for luminescence characterisation.
- Light exposure mitigation: top 1 mm removed under dim red light; deeper material considered unaffected by light beyond analytical error.
- Sampling strategies:
  - Time Period 1 (Last 500 Years): continuous sampling (4 cm integrated) along core A(N)01upper; n=24.
  - Time Period 2 (Laschamp): spot sampling with 100-year integrated intervals every 1,000 years; n=11.
  - Time Period 3 (Varve Limit): contiguous samples at varve-deposit boundary depth; n=12.
  - Time Period 4 (Termination II): ~2,000-year-spaced samples with 100-year integrated intervals; n=13.
- Additional six samples for estimated dose rate (EDR) determination, taken post-luminescence analysis at representative depths.

## Luminescence Measurements (POSL) and Lab Profiling
- POSL measurements conducted at SUERC POSL reader (Wakasa, Japan) using Continuous Wave Proxy (CWproxy) scheme, yielding:
  - POSLnet and PIRSLnet (proxy ages, sensitivity, dose rate)
  - Depletion indices (Blue and IR) and POSL/PIRSL ratio (mineralogical changes and bleaching history)
- Quality checks: empty chamber measurements every two samples; standard checks with MOTAR Sand and Granulite standards.
- Laboratory profiling at SUERC (Risø TL/OSL system) to isolate:
  - Polymineral Fine (PMF; ~5–50 μm) and Quartz Fine (QF; HF-etched quartz) fractions.
  - Chemical preparation: disaggregation, HCl and HF etching, size-selection, and disc loading onto measurement discs.
  - Short SAR protocols to determine equivalent dose (EDe) for each fraction:
    - PMF measured under IR and blue (PMF-IR, PMF-blue)
    - QF measured under blue (QF-blue)
- EDe estimation uses natural signals and responses to calibration doses (50 Gy; some 5 Gy doses included but not used due to low sensitivity).

## Dose Rate Calculations (EDR) and Scenarios
- Six samples used for EDR determination; elemental concentrations measured after drying and homogenisation.
- Elemental analyses:
  - Uranium (U) and Thorium (Th) by ICP-MS; Potassium (K) by ICP-OES.
- Two dose-rate scenarios:
  1) Scenario 1: 30 μm mean grain size with activity-free grains.
     - Compute effective alpha, beta, gamma dose rates; alpha efficiency 0.07; apply water-content corrections.
  2) Scenario 2: 30 μm mean grain size with internal contents equal to matrix.
     - Internal dose rates scaled by absorption fraction; external dose rates scaled by (1−φ); apply water-content corrections.
- Cosmic dose rate: 0.05 mGy yr−1 for the oldest two samples; omitted for younger samples (marine/monsoon context).
- Combined to yield ED R for each sample under each scenario.
- ED R values evaluated alongside QF-blue, PMF-IR, and PMF-blue EDe to converge on first-order age estimates compatible with the Lake Suigetsu chronology.

## Quality Control
- Data inclusion restricted to signals quantifiable above background levels.

## Data Structure and Units
- Two CSV files:
  - lakesuigetsu_luminescence_profiling_results.csv
    - Contains Time Period, Sample Code, Lower/Upper Age (IntCal20 yr BP), POSL and PIRSL signals, depletion indices, POSL/PIRSL ratio, QF blue-sensitivity (counts/Gy), QF-blue estimated dose (Gy), PMF-IR and PMF-blue signals, PMF blue sensitivity, and PMF/PMF-blue estimated doses (Gy).
  - lakesuigetsu_luminescence_doserate_results.csv
    - Contains Time Period, Sample Code, Lower/Upper Age (IntCal20 yr BP), water content, inferred palaeo-water content, Th, U, K concentrations, dose-rate calculations for Scenario 1 and Scenario 2 (including contributions from alpha, beta, gamma, and cosmic components) and resulting total dose rates (mGy/yr).
- Columns labeled with time period names (Holocene, Laschamp, VarveLimit, TerminationII) and sample-specific measurements, including natural signals, dose responses, and calculated ages.

## Significance for Monitoring Frameworks
- Demonstrates an end-to-end workflow for environmental-historical monitoring: from real-world sampling and contamination control to multi-fraction luminescence analysis and robust dose-rate modeling.
- Highlights the importance of:
  - Clear, hierarchical data provenance and time-slice definitions (distinct time periods with defined age models).
  - Transparent measurement protocols (POSL CWproxy scheme, lab-profiling fractions, and measurement sequences).
  - Rigorous QA/QC and background-level thresholds to ensure data reliability.
  - Metadata-rich data structures and openly shared datasets to enable reproducibility and cross-study comparisons.
  - Documentation of data processing choices (e.g., two EDR scenarios, handling of water content, internal vs external dose-rate assumptions).
- Potential data governance considerations for monitoring programs:
  - Availability of detailed methodological metadata to ensure comparability across projects.
  - Managing access to underlying core materials and measurement instruments.
  - Ensuring data standardization and provenance to facilitate integration into broader environmental-monitoring datasets.
  - The need to balance openness with sensitive or large-volume data, particularly when sharing measurement details and calibration standards.

## References
- Burbidge, C. I., Sanderson, D. C. W., Housley, R. A., & Allsworth Jones, P. (2007). Survey of Palaeolithic sites by luminescence profiling, Quat. Geochronol. 2, 296-302.
- Kinnaird, T. C., Sanderson, D. C. W., & Bigelow, G. F. (2015). Feldspar SARA IRSL dating of very low dose rate aeolian sediments, Quat. Geochronol. 30, 168-174.
- Olive, V., Ellam, R. M., & Wilson, L. A. (2001). Protocol for determination of rare earth elements by ICP-MS, Geostand. Newsl. 25, 219-228.
- Sanderson, D. C. W., & Murphy, S. (2010). Simple portable OSL measurements and laboratory characterization, Quat. Geochronol. 5, 299-305.