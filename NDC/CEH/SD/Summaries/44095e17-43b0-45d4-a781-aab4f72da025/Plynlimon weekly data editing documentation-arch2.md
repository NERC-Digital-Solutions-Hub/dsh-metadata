# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- Overview
  - Public release in two versions: Raw Data Archive (RDA) with unaltered raw measurements (except for traceable transcription corrections) and an edited data version with high-confidence measurements.
  - Edited data is intended for routine analyses; raw data retained for documentation and potential re-examination.

- Raw Data Archive vs Edited Data
  - RDA: preserves raw laboratory reports, useful for transparency and reconstructing longer histories, but contains many values believed to be substantially in error.
  - Edited data: removes unexplained flyers and outliers, corrects identifiable issues, and excludes data where quality is uncertain. In rare cases, pre- and post-method-change data are both kept with notes about effects.

- Long-Term Data and Method Changes
  - Time span covers nearly three decades; analytical methods evolved (e.g., metals: ICP-OES until 1988, ICP-MS thereafter; 1998–1999 switch to a different instrument/lab; data largely shifted to Lancaster lab thereafter).
  - When method changes caused abrupt changes in mean/variance, edited data prioritize the period with higher confidence; some years or decades may be omitted from edited series.
  - Original measurements remain in the Raw Data Archive; use caution when reconstructing longer series across method changes.

- Quality Assurance and Consistency Checks
  - Consistency checks across related variables (e.g., SO4 vs S, Alk vs pH, charge balance, Gran alkalinity vs ANC, N species vs TDN, ionic strength vs conductivity).
  - Outliers identified and addressed using relationships with other variables and flow; discrepancies lead to dropping inconsistent analytes.
  - Special consideration given to differences between filtered vs settled samples (conductivity, pH, Gran alkalinity measured on settled samples; solute concentrations on filtered samples).

- Handling of Anomalies, Blocks, and Data Editing Rules
  - Intensive 7-hourly sampling (2007–2009) used for comparison with weekly samples; where discrepancies are large, expert judgment determines which data to keep.
  - Large, abrupt shifts in variability or calibration problems result in omitting problematic blocks or entire series (e.g., trace metals, low-level analytes).
  - Certain elements/values are omitted entirely in edited data due to dominance of analytical noise or calibration issues (e.g., W; Sb largely excluded except in cloudwater/Nant Iago).
  - Duplicate same-day samples omitted to avoid over-representation of events.
  - Occasional corrections of misattributed analyses to the wrong site; corrections applied in edited data (raw archive retains original labels).

- Documentation of Corrections and Notes per Analyte
  - The edited dataset includes notes and plots illustrating editing decisions; red values in notes indicate data culled or changed from raw.
  - Specific correction examples include:
    - Swapping mislabeled samples (e.g., cloud vs South 2 Hore on a given date).
    - Transferring or excising values when site-labels or lab transitions caused misattribution.
    - Deleting anomalous blocks of values tied to calibration issues or instrument changes.
  - In practice, a large portion of the per-analyte notes document culling criteria, calibration issues, and the impact of laboratory transitions on data characteristics.

- Analyte Grouping, Derived Variables, and Special Considerations
  - Analytes are organized by measurement method and atomic number (ion chromatography/electrochemical methods first; cations/metals second).
  - Derived/derived-like variables include:
    - ANC calculated from Na, K, Mg, Ca, SO4, NO3, Cl.
    - Ionic strength estimated from major ions, alkalinity, and pH.
    - SO4_by_ICP created for sulfate derived from ICP-S measurements prior to 2007.
    - DON calculated as TDN minus NO3, NO2, and NH4.
  - Some elements (e.g., Li, Be, Cs, La, Ce, Pr, W) have nuanced handling due to calibration issues, baseline corrections, or coarse reporting intervals; many values were culled or treated with caution.

- Daily and Long-Term Data Availability
  - Daily chloride measurements are available for more than three years.
  - Daily and weekly time series are used to assess short- vs long-term dynamics, with caution advised due to potential short-term analytical noise.

- Guidance for Analysts and Use of Data
  - For routine analyses and trend assessments, use edited data to avoid known artifacts; refer to notes for context on specific corrections and limitations.
  - When reconstructing longer histories, the Raw Data Archive provides the unedited measurements, but users should account for calibration changes, lab transitions, and known issues.
  - Be aware of potential artifacts introduced by laboratory transitions (Wallingford to Lancaster) and calibrations across time, which can affect means, variances, and correlations.

- Access and Transparency
  - Both raw and edited datasets are provided to support transparency and reproducibility.
  - The data notes, time-series plots, and detailed analyte-specific editing rationales are included to help users understand the quality control decisions and their implications for analysis.