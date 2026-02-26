# Luminescence signals and estimates of dose rate from sediment cores, Lake Suigetsu, Japan SUPPORTING DOCUMENTATION

- Purpose and scope
  - Provides luminescence signal data from Lake Suigetsu sediment cores across four time periods: Last 500 Years (Holocene), Laschamp excursion, Varve Limit, and Termination II.
  - Combines Portable Optically Stimulated Luminescence (POSL) analysis of bulk sediment with laboratory profiling of prepared mineral fractions to evaluate dating potential and environmental change signals.
  - Includes estimated dose rates (EDR) at six positions to assess whether luminescence signals can constrain burial ages.

- Data uses and aims for data leaders
  - Enables testing whether luminescence methods detect past catchment/environmental change and yield burial ages.
  - Provides multilevel measurements (field-style POSL signals and laboratory-derived equivalent doses) for cross-validation.
  - Supports comparisons of mineral fractions (Quartz Fine and Polymineral Fine) and exposure schemes (blue light and infrared) to understand dating sensitivities.
  - Offers dose-rate calculations under two scenarios to capture uncertainties related to grain size, internal contents, water content, and cosmic contributions.

## Collection and generation methods

- Time periods and significance
  - Time Period 1: Last 500 Years (~550 cal BP to present) with local environmental perturbations.
  - Time Period 2: Laschamp Excursion (~45,000–35,000 cal BP) with geomagnetic and climate variability.
  - Time Period 3: Varve Limit (~73,000–69,000 yr BP) marking initial varving and lake biogeochemistry changes.
  - Time Period 4: Termination II (~140,000–118,000 yr BP) during MIS transitions with monsoon variability.

- Sampling and materials
  - Lake Suigetsu SG06 cores; total of 60 samples collected.
  - Light-exposure precautions: top 1 mm removed under dim red light to access unexposed material.
  - Sampling strategy varied by period (continuous for shorter intervals; spot sampling for longer intervals).

- Luminescence measurements and lab profiling
  - POSL measurements performed on core sections using a POSL reader in Wakasa, Japan.
  - Continuous Wave Proxy (CWproxy) scheme yields POSLnet, PIRSLnet, depletion indices, and POSL/PIRSL ratios as proxies for age, sensitivity, dose rate, mineralogy, and bleaching history.
  - Laboratory profiling at SUERC (UK) isolating two fractions from each sample:
    - Quartz Fine (QF): predominantly quartz, HF-etched.
    - Polymineral Fine (PMF): mixed mineralogy, 5–50 µm.
  - Fractions measured with Risø TL/OSL system using Short Aliquot Regenerative Dose (SAR) protocols to estimate equivalent dose (EDe) for each fraction.
  - Additional pretreatments (HCl, HF) and sieving steps to target appropriate grain sizes and mineralogy.

- Dose-rate estimation (EDR)
  - Six samples analyzed for mineralogical/elemental concentrations (U, Th, K) via ICP-MS and ICP-OES to compute palaeo-dose rates.
  - Two scenarios:
    - Scenario 1: activity-free grains with external and internal contributions modeled using attenuation factors.
    - Scenario 2: internal contents equal to matrix; internal dose scaled accordingly.
  - Water-content corrections applied; cosmic dose rate included for oldest samples; oreiented to match sediment conditions (varved vs non-varved contexts).
  - Comparison of QF-blue, PMF-IR, and PMF-blue ED values with EDR to constrain ages.

## Quality control and data structure

- Quality control
  - Data included only when luminescence signals were quantifiable above background.

- Data structure and units
  - Two CSV files provided:
    - lakesuigetsu_luminescence_profiling_results.csv: contains Time Period, Sample Code, Age ranges (IntCal20 yr BP), POSL and PIRSL signals, depletion indices, POSL/PIRSL ratio, and joint results for QF and PMF fractions (blue and IR sensitivities, dose estimates).
    - lakesuigetsu_luminescence_doserate_results.csv: contains Time Period, Sample Code, Age, water content, elemental concentrations (U, Th, K), and calculated dose rates for both scenarios, plus the total dose-rate components (alpha, beta, gamma, cosmic) and final EDR estimates.
  - Units and metadata follow IntCal20 year conventions and Gy for doses; values include uncertainties as reported in the measurements and modeling steps.

- Documentation and data provenance
  - Method details reference established protocols (CWproxy, SAR, IRSL/OSL, HF/HCl pretreatments) and prior work (Burbidge et al., Kinnaird et al., Olive et al., Sanderson & Murphy).

## Endnotes and references

- Key sources for methods and context
  - Burbidge, C. I. et al. (2007); quartz/polymineral luminescence dating protocol.
  - Kinnaird, T. C., Sanderson, D. C. W. & Bigelow, G. F. (2015); feldspar IRSL dating.
  - Olive, V. et al. (2001); elemental analysis protocol for geochronology.
  - Sanderson, D. C. W. & Murphy, S. (2010); portable OSL measurements and laboratory characterization.

- Purpose of the dataset
  - Supports evaluation of luminescence-based burial age estimation and detection of past environmental changes using Lake Suigetsu sediments, with carefully documented sampling, preparation, measurement, and dose-rate modeling to enable reproducibility and cross-validation.