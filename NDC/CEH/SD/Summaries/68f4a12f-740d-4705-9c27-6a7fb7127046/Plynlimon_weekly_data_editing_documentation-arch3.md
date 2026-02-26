# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- Overview
  - Public data base released in two versions: Raw Data Archive (RDA) and edited data.
  - RDA preserves raw measurements with minimal corrections; edited data removes problematic values to enable routine analyses.
  - Raw data supports traceability and potential reconstruction if new information emerges; edited data emphasizes data quality and consistency for interpretation and decision-making.

- Data versions and access
  - Raw Data Archive (RDA): unmodified measurements except for traceable transcription corrections; contains some values considered substantially erroneous; serves documentation and traceability.
  - Edited data: measurements with high confidence; problematic values corrected or removed; excludes unexplained outliers (flyers) and blocks with implausible variability; notes document method changes and rationales.
  - Data notes indicate where original values can be retrieved from the RDA, but edited data should be used for routine analyses.

- Data editing principles and quality assurance
  - Consistency checks across analytes (e.g., SO4 vs S, Alk vs pH, ANC vs conductivity) to identify and drop inconsistent values.
  - Method changes and laboratory transitions carefully evaluated:
    - Shifts from Wallingford to Lancaster (late 1990s) and instrument changes (ICP-OES to ICP-MS) are documented.
    - Time series around method changes are inspected; abrupt shifts may lead to exclusion of affected years or blocks; in some cases, both pre- and post-change data are retained with notes.
  - Expert judgment used to omit blocks or adjust time series when patterns become implausible (e.g., excessive variability, calibration issues, or sampling anomalies).
  - Duplicate samples and obviously erroneous entries (e.g., mislabeling, out-of-range zeros) removed or corrected.
  - For several analytes, different measurement approaches (filtered vs settled samples) are disclosed; tests showed no significant differences for key analytes in settled vs filtered samples, though filtration metadata is provided.

- Handling anomalies, outliers, and culling (general approach)
  - Flyers (outliers) culled based on correlations with other analytes, flow, or known calibration issues.
  - Singletons or blocks lacking plausible context (e.g., abrupt winter peaks without corroborating evidence) may be removed or treated cautiously.
  - Blocks with abnormal variability or calibration problems are omitted; some elements show lab-specific artifacts after method changes, leading to culling of affected data at certain sites.
  - Some analytes exhibit artifacts tied to laboratory transitions, instrument calibrations, or coarse reporting intervals; such periods are flagged and treated accordingly.

- Analyte-specific considerations (high-level examples)
  - DOC: few flyers culled; clear long-term trend with increasing concentration and seasonal amplitude noted.
  - NO3-N, NH4-N, TDN, DON: selective culling of implausible or calibration-related values; DON computed from edited TDN, NO3, NO2, NH4.
  - Major ions and trace metals: many elements have documented blocks or periods culled after lab changes; some elements (e.g., Sb, Cs, La, Pr, W) are heavily restricted or removed in specific periods due to calibration or measurement issues.
  - Chromium (Cr) and others: notable step changes around laboratory transitions; cautious interpretation recommended for trend analyses spanning lab changes.
  - Some elements show lab contamination concerns (e.g., Cu, Zn) or drift in variance post-transition; users are advised to exercise caution when analyzing these periods.
  - Tungsten (W) values culled entirely due to severe calibration problems; other elements may have site-specific culling.

- Data structure and presentation
  - Analytes organized into two groups: (1) those determined by ion chromatography/electrochemical methods, then (2) cations and metals measured by ICP-OES/ICP-MS, arranged by increasing atomic number.
  - Time-series plots indicate edited (non-RDA) values; raw data culled values shown in red in the documentation.
  - Detailed notes accompany time-series plots for each analyte, documenting edits, outliers, and methodological context.

- Practical guidance for monitoring and policy use
  - Be mindful of breaks and shifts associated with method changes and laboratory transitions when interpreting long-term trends.
  - Use edited data for analyses; consult the raw data archive only when reconstructing longer histories or assessing potential artefacts.
  - Reference analyte-specific notes and quality checks to assess suitability for governance decisions, dashboards, or reporting.
  - Ensure metadata about sampling (settled vs filtered), calibration, and lab changes is incorporated into any monitoring framework outputs.

- Data governance and dissemination considerations (alignment with authors’ aims)
  - Public sharing of underlying data is pursued, with transparent documentation of processing steps and quality control.
  - Data editing emphasizes openness about decisions, enabling stakeholders to understand data provenance and justification for exclusions.
  - The editorial approach highlights metadata creation and data management practices to support data governance, quality assurance, and reliable interpretation for informing policy and future decisions.