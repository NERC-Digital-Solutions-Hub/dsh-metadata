# Luminescence signals and estimates of dose rate from sediment cores, Lake Suigetsu, Japan SUPPORTING DOCUMENTATION

## Overview
- Dataset of luminescence signals and dose-rate estimates from Lake Suigetsu sediment cores.
- Four time periods: Last 500 years, Laschamp geomagnetic excursion, Varve limit, and Termination II.
- Methods include Portable OSL (POSL) analysis on bulk sediment and laboratory profiling of prepared quartz fine (QF) and polymineral fine (PMF) fractions.
- Aims to assess if luminescence methods can detect past catchment environmental change and to evaluate burial age using dose-rate estimations (EDR).

## Time periods and sampling strategy
- Time Period 1 — Last 500 Years (~550 cal BP to present)
  - Local environmental perturbations; sampling: contiguous 4 cm integrated samples along core A(N)01upper (n=24).
- Time Period 2 — Laschamp Excursion (~45,000 to 35,000 cal BP)
  - Global change context; sampling: spot samples every 1,000 years between 35,000 and 45,000 cal BP (n=11).
- Time Period 3 — Varve Limit (~73,000 to 69,000 yr BP)
  - Initiation of varving; sampling: contiguous samples at ~230–330 year resolution along core A(S)24 (n=12).
- Time Period 4 — Termination II (~140,000 to 118,000 yr BP)
  - MIS 6 to MIS 5e transition; sampling: ~2,000-year-spaced intervals (n=13), 100-year integrated intervals chosen semi-randomly.

## Collection and sample preparation
- Core material from Lake Suigetsu SG06; top 1 mm removed under dim red light to minimize light exposure.
- Storage location: Fukui Prefectural Varve Museum, Wakasa, Japan.
- Preparation varied by period due to material availability and event structure.
- Light exposure controls and sampling strategies tailored to period characteristics.

## Measurement methods
- POSL measurements
  - Instrument: SUERC POSL reader (Wakasa, Japan).
  - Exposure schemes: Continuous Wave Proxy (CWproxy) with seven photon-count periods (dark, IR stimulations, blue stimulations, dark).
  - Derived variables: POSLnet, PIRSLnet; POSL depletion indices; PIRSL/POSL ratio; instrument checks with empty chamber and standards.
- Laboratory profiling (OSL dating)
  - Fractions: Quartz Fine (QF) and Polymineral Fine (PMF).
  - Chemical pretreatments: HCl and HF etching, followed by rinses; grain-size selection <90 µm.
  - PMF: loaded on discs; IRSL and OSL measurements; IR and blue light signals used.
  - QF: HF-etched, loaded on discs; blue-light signals used.
  - DOS protocols: Short Single Aliquot Regenerative Dose (SAR) sequences to derive equivalent dose (EDe) for each fraction (PMF-IR, PMF-blue, QF-blue).
- Dose-rate estimation (EDR)
  - Six samples for down-core dose-rate determination.
  - Elemental concentrations: U, Th (ICP-MS); K (ICP-OES).
  - Dose-rate scenarios:
    1) Scenario 1 — activity-free grains with 30 µm mean grain size.
    2) Scenario 2 — internal contents equal to the surrounding matrix.
  - Corrections: water content, attenuation factors, absorption by water, cosmic component (0.05 mGy/yr for oldest samples).
  - Outputs: EDR values for each sample under both scenarios; used with ED e values to constrain age estimates.

## Data structure and contents
- File 1: lakesuigetsu_luminescence_profiling_results.csv
  - Key fields: Time Period, Sample Code, Lower/Upper Age (IntCal20 yr BP), POSLnet and PIRSLnet, POSL/PIRSL ratio, POSL depletion indices, PMF/QF signals (blue and IR) with sensitivities and estimated doses, and associated errors.
  - Descriptions specify holocene, Laschamp, VarveLimit, TerminationII contexts and age-model references.
- File 2: lakesuigetsu_luminescence_doserate_results.csv
  - Key fields: Time Period, Sample Code, Lower/Upper Age (IntCal20 yr BP), Water content, inferred palaeo-water content, Th/U/K concentrations (ppm), total dose rates for Scenario 1 and Scenario 2, with uncertainties.
  - Includes notes on calculation approach for each scenario and references to age-model information.

## Quality control
- Data included only if luminescence and dose-rate signals were quantifiable above background levels.

## Data interpretation and GIS relevance
- Enables spatial-temporal visualization of luminescence signals and burial ages across key palaeoenvironmental transitions.
- Can be integrated with other chronology datasets (e.g., correlation models, event layers) to map environmental changes over time.
- Requires awareness of age-model uncertainties, two-dose-rate scenarios, varying sampling resolutions, and the light-sensitivity of fractions when incorporating into GIS analyses.

## Limitations and considerations for use
- Variable sampling density across time periods; younger periods have higher resolution than older periods.
- Age estimation combines ED e measurements with EDR under two scenarios; results depend on assumed grain size, internal contents, and water content corrections.
- Light exposure control during sampling and laboratory prep is critical for data integrity.

## References
- Burbidge, C. I., Sanderson, D. C. W., Housley, R. A. & Allsworth Jones, P. Quat. Geochronol. 2, 296-302 (2007).
- Kinnaird, T. C., Sanderson, D. C. W. & Bigelow, G. F. Quat. Geochronol. 30, 168-174 (2015).
- Olive, V., Ellam, R. M. & Wilson, L. A. Geostand. Newsl. 25, 219-228 (2001).
- Sanderson, D. C. W. & Murphy, S. Quat. Geochronol. 5, 299-305 (2010).