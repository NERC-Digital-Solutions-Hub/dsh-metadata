# Luminescence signals and estimates of dose rate from sediment cores, Lake Suigetsu, Japan SUPPORTING DOCUMENTATION

- A dataset characterising luminescence signals from Lake Suigetsu sediment cores across four time periods, to assess past environmental change and burial age using POSL and lab profiling methods.
- Includes estimated dose rates to support luminescence dating and environmental interpretation.

## Data scope and purpose
- Evaluate whether luminescence methods can detect past catchment environmental change.
- Estimate burial age by comparing luminescence signals with dose-rate calculations.
- Provide a standardized dataset for monitoring environmental change and supporting cross-site comparisons.

## Time periods covered
- Time Period 1: The Last 500 Years (~550 cal BP to present) with local perturbations (lake–Sea of Japan connection, floods).
- Time Period 2: Laschamp geomagnetic excursion (~44,828 to 35,550 cal BP) with variable temperatures.
- Time Period 3: Varve limit (~73,130 to 69,413 yr BP) marking varve initiation and lake biogeochemistry shifts.
- Time Period 4: Termination II (~139,499 to 118,001 yr BP) during MIS 6–MIS 5e transition and monsoonal changes.

## Collection and sampling design
- Core material: Lake Suigetsu SG06 cores; total of 60 samples for luminescence characterisation.
- Light protection: top 1 mm removed under dim red light to access unexposed material.
- Sampling strategies:
  - Contiguous sampling for Time Periods 1 and 3 (shorter intervals).
  - Spot sampling for Time Periods 2 and 4 (longer intervals).
- Sampling resolutions:
  - Time Period 1: 4 cm integrated samples (n = 24).
  - Time Period 2: 100-year integrated samples every 1,000 years (n = 11).
  - Time Period 3: sampling at ~230–330 year resolution (n = 12).
  - Time Period 4: ~2,000-year apart, with ~100-year integral intervals (n = 13).
- Additional six samples for estimated dose rate (ED_R) determination, taken across time periods to compare mineral fractions and down-core dose-rate variations.

## Luminescence measurements and laboratory profiling
- In-situ measurements (POSL):
  - Location: SUERC POSL reader in Wakasa, Japan (samples from Lake Suigetsu cores).
  - Protocol: CWproxy seven-count sequence (dark, IR stimulations, dark, blue stimulations, dark).
  - Outputs: POSL net, PIRSL net, POSL/PIRSL ratio, Depletion Indices (Blue and IR), instrument checks with standards.
- Laboratory profiling (SUERC, UK):
  - Fractions: Quartz Fine (QF) and Polymineral Fine (PMF) separated by chemical pretreatments (HF/HCl, size selection 5–50 μm).
  - Measurements: Risø TL/OSL system with 90Sr source; short Single Aliquot Regenerative Dose (SAR) protocols.
  - ED_e (estimated equivalent dose) values derived from natural signal and responses to test doses (50 Gy, with smaller test doses used if sensitivity allowed).
  - PMF measured under IR and blue light (PMF-IR, PMF-blue); QF measured under blue light only (QF-blue).
  - Data used to help derive first-order age estimates and compare with Suigetsu chronology.

## Dose-rate estimation (ED_R)
- Six samples analyzed for ED_R determination across both PMF and QF fractions.
- Elemental concentrations measured:
  - Uranium (U) and Thorium (Th) by ICP-MS; Potassium (K) by ICP-OES.
- Dose-rate scenarios:
  - Scenario 1: Activity-free grains with 30 μm mean size (external alpha/beta/gamma; 1-φ attenuation, alpha efficiency 0.07) plus water content corrections.
  - Scenario 2: Internal contents equal to matrix (internal dose scaled by φ; external dose adjusted; water corrections).
- Water content: Based on direct wet-weight measurements plus time-averaged estimates informed by sedimentology (compression and clay content).
- Cosmic dose rate: 0.05 mGy yr^-1 included for the two oldest samples (shallow lake conditions); omitted for younger, deeper-water deposition.
- Outputs: ED_R values for each sample under both scenarios, used alongside ED_e to refine age estimates.

## Data structure and access
- Two CSV files:
  - lakesuigetsu_luminescence_profiling_results.csv: includes time period, sample code, age bounds (IntCal20 yr BP), POSL and PIRSL signals, depletion indices, POSL/PIRSL ratio, QF PMF sensitivity and dose estimates, and corresponding ED_e values.
  - lakesuigetsu_luminescence_doserate_results.csv: includes time period, sample code, age bounds, water content, palaeo-water content estimates, elemental concentrations (U, Th, K), and total dose-rate calculations for both scenarios (including alpha, beta, gamma, and cosmic contributions) with uncertainties.
- Quality control: Data are included only when luminescence signals exceed background levels.

## Quality and reuse considerations
- Data are produced with standardized methods and quality checks to enable cross-site environmental monitoring and comparison.
- The dataset supports integration with other environmental proxies to enhance understanding of past catchment changes and climate conditions.
- Meticulous documentation of methods facilitates transparency and data reuse, including the potential to upload to data portals and share underlying measurements.

## References
- Burbidge, C. I., Sanderson, D. C. W., Housley, R. A. & Allsworth Jones, P. (2007). Quat. Geochronol. 2, 296-302.
- Kinnaird, T. C., Sanderson, D. C. W. & Bigelow, G. F. (2015). Quat. Geochronol. 30, 168-174.
- Olive, V., Ellam, R. M. & Wilson, L. A. (2001). Geostand. Newsl. 25, 219-228.
- Sanderson, D. C. W. & Murphy, S. (2010). Quat. Geochronol. 5, 299-305.