# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- Purpose and structure
  - The Plynlimon long-term hydrochemistry data base is released in two forms: Raw Data Archive (RDA) containing unmodified laboratory reports with minor transcription corrections, and an edited data set with high-confidence measurements after systematic quality control.
  - The edited data are recommended for routine analyses; the RDA remains for documentation and potential re-examination if new information suggests important phenomena may have been edited out.

- Rationale for editing
  - Edits remove unexplained flyers and data outliers that do not follow typical correlations with flow or other analytes.
  - Exceptional cases may be retained if clearly warranted, but many anomalies are culled to improve data reliability.
  - The edits aim to balance retaining real signals with removing spurious values likely due to labeling errors, contamination, calibration issues, or analytical anomalies.

- Time span, methods, and changes
  - The dataset covers nearly three decades, during which analytical methods and laboratories changed.
  - Metals analyses shifted from ICP-OES (pre-1988) to ICP-MS (1988–1992) and later to a different instrument and lab (Wallingford to Lancaster in late 1998).
  - Time-series around method changes are carefully inspected; periods with abrupt changes are either adjusted or excluded from the edited data to avoid bias in trend analyses.
  - The documentation notes the exact dates and effects of method changes and how they influence mean, variance, and calibration across analytes.

- Data quality assurance and consistency checks
  - Consistency checks link related measures (e.g., SO4 vs S, Alk vs pH, charge balance, Gran Alkalinity vs ANC, N species vs TDN, ionic strength vs conductivity).
  - Outliers are identified and investigated using relationships with flow and other variables; inconsistent analyte values are culled.
  - For some analytes, multiple data sources (e.g., filtered vs unfiltered samples) and sampling conditions are reconciled, with caveats explained.

- Sampling regime and data handling
  - In addition to regular weekly sampling, intensive 7-hourly rainfall and two streams data (2007–2009) are used for cross-checks; discrepancies are judged for plausibility, with some data retained if differences are not large.
  - Data blocks with implausible variability or calibration issues (e.g., blocks of high variability or sudden limits shifts) are omitted from the edited data.
  - Duplicate same-day samples are removed to avoid over-representation of certain events.

- Analyte-specific editing notes (high-level)
  - Some elements are culled or corrected due to calibration problems, laboratory changes, or poor correlations with other variables.
  - Certain elements are entirely omitted from edited data at specific sites or time periods (e.g., tungsten), or heavily culled when appearance of artifacts is evident (e.g., antimony, barium after method transitions).
  - Across transitions (e.g., Wallingford to Lancaster), mean and variance changes may occur; these transitions are treated with caution for analyses spanning the change.
  - Derived and reclassified variables are used where appropriate (e.g., SO4_by_ICP constructed from ICP S measurements for consistency with IC-measured sulfate).

- Sample types and measurement practices
  - Conductivity, pH, Gran alkalinity, and Gran acidity were measured on settled (unfiltered) samples; solute concentrations were measured on filtered samples.
  - Tests in the 1980s suggested no significant difference between filtered and unfiltered samples for the core analytes.

- Data presentation and documentation
  - For each analyte, notes and time-series plots illustrate the editing applied; raw values culled or changed are shown in red.
  - The analytes are organized in two groups: (1) IC/electrochemical/autoanalysis methods by increasing atomic number, and (2) cations/metals (ICP-OES/ICP-MS) by increasing atomic number.
  - Several derived relationships and quality checks are described (e.g., handling of TDN, DON, NO2-N, NO3-N, NH4-N, etc., and the calculation of DON as TDN minus measured nitrogen species).

- Practical guidance for analysts
  - Use edited data for routine analyses and model development; refer to Raw Data Archive only when reconstructing longer histories or when dataset sensitivity to short-term artifacts is critical.
  - Be cautious interpreting trends or cross-site comparisons across laboratory changes; consult the method-change notes and culling decisions.
  - Consider the provided consistency checks (pH-alkalinity, conductivity-ionic strength, etc.) when validating model outputs or performing trend analyses.
  - Acknowledge that some analyte time series include blocks with calibration issues or coarse reporting intervals (e.g., Cs and other trace elements during certain periods).

- Availability and accessibility
  - Both Raw Data Archive and edited data are provided; the edited data are designed to be readily usable for analysis, with notes on data quality and rationale for edits to aid reproducibility and interpretation.