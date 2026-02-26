# Luminescence signals and estimates of dose rate from sediment cores, Lake Suigetsu, Japan SUPPORTING DOCUMENTATION

- Overview
  - Dataset of luminescence signals measured from Lake Suigetsu sediment cores across four time periods: last 500 years; Laschamp geomagnetic excursion; varve limit; Termination II.
  - Luminescence measured using Portable OSL (POSL) with blue and IR exposures, plus laboratory profiling of prepared quartz fine (QF) and polymineral fine (PMF) fractions using blue and IR exposures.
  - Accompanied by estimated dose rate (ED R) at six points across the four periods to assess whether luminescence can inform burial age.

- Time periods studied
  - Time Period 1: Last 500 years (~550 cal BP to present)
  - Time Period 2: Laschamp excursion (~45,000 to 35,000 cal BP)
  - Time Period 3: Varve limit (~73,000 to 69,000 yr BP)
  - Time Period 4: Termination II (~140,000 to 118,000 yr BP)

- Materials and sampling strategy
  - Core material: Lake Suigetsu SG06 cores; 60 samples for luminescence characterization.
  - Light protection: Top 1 mm removed under dim red light to access unexposed material.
  - Sampling approaches: Contiguous sampling for Time Periods 1 and 3; spot sampling for Time Periods 2 and 4.
  - Time-period-specific sampling details (examples):
    - Time Period 1: 4 cm integrated samples along A(N)01upper (n=24)
    - Time Period 2: 100-year integrated samples every 1,000 years (n=11)
    - Time Period 3: Depth-based contiguous samples along A(S)24 (n=12)
    - Time Period 4: ~2,000-year spaced samples with ~100-year integrated intervals (n=13)
  - Six additional samples for ED R determination, taken to assess mineral fractions and down-core dose-rate variations.

- Measurement methods
  - POSL measurements (CWproxy protocol) at SUERC POSL reader:
    - Two stimulations: IR 830 nm and blue 470 nm with dark counts in between.
    - Outputs: POSL net, PIRSL net, POSL and PIRSL depletion indices, POSL/PIRSL ratio.
  - Laboratory profiling at SUERC (Risø TL/OSL system) for two mineral fractions:
    - Polymineral Fine (PMF): ~5–50 µm, IR-stimulated and blue-stimulated signals.
    - Quartz Fine (QF): ~5–50 µm, blue-stimulated signals after HF/HCl pretreatments.
    - Procedures: Preheat, stimulation sequences, and measurements to derive equivalent doses (ED e) via single-aliquot regenerative-dose (SAR) protocols.
  - Dose-rate estimation (ED R)
    - Elemental concentrations measured on dried, ground samples:
      - Uranium (U) and Thorium (Th) by ICP-MS; Potassium (K) by ICP-OES.
    - Dose-rate calculations under two scenarios:
      - Scenario 1: 30 µm mean grain size, activity-free grains.
      - Scenario 2: 30 µm mean grain size with internal contents equal to the matrix.
    - Components considered: alpha, beta, gamma, and cosmic dose rates; corrections for water content and absorption; small cosmic component added for oldest samples.
    - ED R combined with ED e values to verify primary age estimates.

- Data structure and access
  - Two CSV files:
    - lakesuigetsu_luminescence_profiling_results.csv
      - Columns include Time Period, Sample Code, Lower/Upper Age, POSL net signals, depletion indices, POSL/PIRSL ratio, quartz blue and PMF infrared/blue sensitivities and estimated doses (S-V, AA-AD, etc.).
      - Units: counts, counts/gy, Gy, etc.; age information in IntCal20 yr BP; referenced age model versions.
    - lakesuigetsu_luminescence_doserate_results.csv
      - Columns include Time Period, Sample Code, Lower/Upper Age, Water content, Inferred palaeo-water content, Thorium/Uranium/Potassium concentrations, Dose rates for Scenario 1 and Scenario 2 (with errors), and total dose rate calculations (mGy/yr).
      - Units: ppm, % dry weight, mGy/yr, Gy, etc.
  - Data quality: Only records with signals above background are included.

- Quality control and data provenance
  - Quality control: Data included only when luminescence signals were quantifiable above background levels.
  - Provenance: Samples decontaminated from light exposure; measurement and lab profiling performed at SUERC; cores stored at Fukui Prefectural Varve Museum, Wakasa, Japan.
  - References for methods and calibration schemes included to support reproducibility (e.g., CWproxy, SAR schemes, and standard references for luminescence dating protocols).

- Potential uses for analysis
  - Correlate luminescence signals with environmental change across the four distinct time periods.
  - Cross-validate luminescence-based burial ages with ED e values and ED R estimates.
  - Compare PMF and QF fractions to assess robustness of age estimates across mineral fractions.
  - Integrate dataset into broader environmental or palaeogeographic models, accounting for uncertainties in dose rates and water content.