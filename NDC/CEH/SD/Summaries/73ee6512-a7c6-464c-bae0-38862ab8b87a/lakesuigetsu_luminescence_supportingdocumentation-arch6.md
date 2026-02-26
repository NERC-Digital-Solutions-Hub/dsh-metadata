# Luminescence signals and estimates of dose rate from sediment cores, Lake Suigetsu, Japan SUPPORTING DOCUMENTATION

## Overview
- Dataset of luminescence signals from Lake Suigetsu sediment cores across four key time periods: the Last 500 Years (~550 cal BP to present), Laschamp geomagnetic excursion (~45,000–35,000 cal BP), Varve Limit (~73,000–69,000 yr BP), and Termination II (~140,000–118,000 yr BP).
- Measurements performed with Portable Optical Stimulated Luminescence (POSL) on bulk sediment (blue and infrared exposures) and laboratory profiling of prepared quartz fine (QF) and polymineral fine fractions (PMF).
- Aims to assess whether luminescence signals can detect past catchment/environmental changes and to estimate burial age through dose-rate calculations.
- Includes estimated dose rates (EDR) at six positions across the four periods to support comparison with luminescence signals and existing Suigetsu chronology.

## Collection and Sampling
- Four distinct time periods chosen for environmental/global significance:
  - Time Period 1: Last 500 Years (~537 cal BP to present) with events like lake-sea connection and local floods.
  - Time Period 2: Laschamp Excursion (~44,828 to 35,550 cal BP).
  - Time Period 3: Varve Limit (~73,130 to 69,413 yr BP) marking onset of varving.
  - Time Period 4: Termination II (~139,499 to 118,001 yr BP) with MIS transitions and monsoon changes.
- Sample source: Lake Suigetsu SG06 cores; total of 60 samples for luminescence characterisation.
- Light exposure control: top 1 mm removed under dim red light to access unexposed material; deeper material deemed less affected by light.
- Sampling strategies by period:
  - Time Period 1: continuous adjacent sampling along core (n=24; 4 cm integrated).
  - Time Period 2: spot sampling every 1,000 years (n=11; 35,000–45,000 cal BP).
  - Time Period 3: sampling depth-based resolution tied to clay layer (n=12; ~230–330 year resolution).
  - Time Period 4: wide interval sampling (~2,000 years apart; n=13; 100-year integrated intervals).
- Additional six samples collected for estimated dose rate (EDR) determination across all periods (one per period at representative depths and two at elevated luminescence positions).

## Measurements and Analysis
- POSL measurements:
  - Instrument: SUERC POSL reader (Wakasa, Japan).
  - Protocol: CWproxy with seven photon-count periods (dark, IR stimulations, dark, blue stimulations, dark).
  - Outputs: POSLnet, PIRSLnet (proxy for age, sensitivity, dose rate); Depletion Indices (blue and IR) and POSL/PIRSL ratio as proxies for mineralogical changes.
- Laboratory profiling (SUERC, UK):
  - Fractions isolated: Quartz Fine (QF) and Polymineral Fine (PMF) via chemical pretreatment (HCl, HF, rinses) and size selection (<90 µm).
  - PMF measurement: IR and blue-light signals; ED e (equivalent dose) estimated using Short/Single Aliquot Regenerative Dose protocol.
  - QF measurement: Blue-light signals only; ED e estimated similarly.
  - Dose measurement sequence: for each aliquot, preheat steps, stimulation, test doses, and TL/OSL readouts documented (specific schemes provided for PMF and QF).
  - Outputs: ED e values for QF-blue, PMF-IR, PMF-blue across samples (N/A where signals were too small).
- Dose rate estimation (EDR):
  - Elemental concentrations measured on dried, ground samples:
    - Uranium (U) and Thorium (Th) by ICP-MS; Potassium (K) by ICP-OES.
  - Two EDR scenarios:
    - Scenario 1: 30 µm mean grain size; activity-free grains.
    - Scenario 2: 30 µm mean grain size; internal grain contents equal to matrix.
  - Corrections and calculations:
    - Alpha, beta, gamma dose rates computed with attenuation factors and water-content corrections.
    - External/internal dose components treated per scenario; cosmic dose included for oldest samples (0.05 mGy/yr for two oldest, omitted for youngest periods).
    - Final ED R per sample derived by combining alpha, beta, gamma, and cosmic components.
  - ED e values used to cross-check with ED R and refine first-order age estimates alongside existing Suigetsu chronology.

## Data Quality and Availability
- Data included only when luminescence signals were quantifiable above background.
- Quality control implemented via instrument standards and empty-chamber checks during batch measurements.

## Data Structure and Files
- Two CSV files:
  - lakesuigetsu_luminescence_profiling_results.csv
    - Time Period (A), Sample Code (B), Lower/Upper Age (C/D; IntCal20 yr BP with age-model references), POSLnet and PIRSLnet values (E-H) with errors, POSL depletion indices (I-L) with errors, POSL/PIRSL ratio (M-N), QF-blue sensitivity and errors (O-R), QF-blue estimated dose and errors (S-V), PMF-IR and PMF-blue sensitivity (W-Z) and estimated doses (AA-AD), PMF-blue and PMF-IR dose-related values (AE-AH, AI-AL).
    - lakesuigetsu_luminescence_doserate_results.csv
      - Time Period, Sample Code, Lower/Upper Age (IntCal20 yr BP or TerminationII), Water content (E), Inferred palaeo-water content (F-G), Thorium (H-K), Uranium (L-O), Potassium (P-S), Total dose rates for Scenario 1 and Scenario 2 (T-AB, AC-AK) with associated errors.
- These files enable linking luminescence signals to age estimates and cross-validating with dose-rate-derived ages.

## Relevance and Potential Uses
- Enables exploration of past environmental changes and catchment dynamics via luminescence signals.
- Provides a basis for self-serve data products and dashboards that compare luminescence proxies with dose-rate-based ages.
- Supports cross-validation of the Lake Suigetsu chronology and refinement of burial age estimates through multi-fraction luminescence analysis and dose-rate modelling.

## References
- Burbidge, C. I., Sanderson, D. C. W., Housley, R. A. & Allsworth Jones, P. (2007). Survey of Palaeolithic sites by luminescence profiling.
- Kinnaird, T. C., Sanderson, D. C. W. & Bigelow, G. F. (2015). Feldspar SARA IRSL dating of low-dose-rate sediments.
- Olive, V., Ellam, R. M. & Wilson, L. A. (2001). Protocol for rare earth elements in rocks by ICP-MS.
- Sanderson, D. C. W. & Murphy, S. (2010). Using portable OSL measurements to understand complex sediment sequences.