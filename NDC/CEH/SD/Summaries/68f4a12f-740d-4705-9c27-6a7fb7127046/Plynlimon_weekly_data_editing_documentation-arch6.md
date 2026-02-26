# Plynlimon long-term hydrochemistry data base Metadata: Quality control and data editing

- Purpose of the document: describe quality control and data editing applied to the Plynlimon long-term hydrochemistry data base, and explain how two public versions are produced and maintained.

## Data versions and access

- Raw Data Archive (RDA): archive of unaltered measurements as reported by laboratories, with minor transcription corrections traceable to original files.
  - Provides complete documentation and transparency about subsequent data editing.
  - Allows reconstruction of longer time series, but not recommended for routine analyses due to known errors in raw values.
- Edited data: measurements curated with high confidence, excluding unexplained outliers and data artefacts.
  - Aims to remove flyers/outliers and blocks that do not fit usual correlations among analytes or with flow.
  - In rare cases, some correlated exceptional outliers may be retained; otherwise, values are corrected or deleted.
  - Metadata documents the changes and indicates where original raw values can be retrieved.

## Editing philosophy and processes

- Core goals:
  - Understand the data ask and provide suitable, reliable data products (e.g., cleaned time series, relationships, and derived metrics).
  - Clean, transform, and quality-check data; assess patterns and plausibility; and create self-serve data products where possible.
- Consistency checks and corrections:
  - Where possible, perform cross-checks (e.g., pH vs. alkalinity, charge balance, ionic strength vs. conductivity) to identify and correct inconsistencies.
  - Drop analytes that are clearly inconsistent with nearby values in time series.
- Handling analytical changes over time:
  - Document and account for analytical method changes (notably changes in instrumentation and laboratories) that may affect time-series statistics.
  - Assess abrupt changes in mean/variance around method changes and retain data with higher confidence; in some cases, years/decades may be excluded from the edited data if affected.
  - Original measurements remain in the Raw Data Archive for careful reconstruction, with caveats.

## Method changes and laboratory transitions

- Major transitions:
  - Metals: pre-concentration and ICP-OES up to 1988; switch to ICP-MS with continued pre-concentration; later shift to a different instrument and laboratory (Wallingford to Lancaster) around 1998–1999.
- Effects observed:
  - Shifts in mean and variance around laboratory transitions; some data culled or flagged due to calibration or instrument-related artefacts.
  - Cr, Ni, Mo, Zn, Cd, Pb, Sb, Cs, La, Ce, Pr, Be, W, and other elements show site- and time-specific responses to lab changes; some data culled post-transition due to increased variance or negative values.
- Practical guidance:
  - When analyses span laboratory transitions, treat results with caution; some users may need to splice data carefully or analyze segments separately.

## Data quality, consistency checks, and culling criteria

- General approach:
  - Use consistency relationships (e.g., SO4 by ICP vs sulfate measured directly, pH–alkalinity, flow correlations) to identify outliers.
  - Cull singletons or blocks of values that lack plausible links to other variables or flow dynamics.
  - Remove data blocks with calibration problems, anomalous blocks of variability, or likely contamination/ measurement artefacts.
- Specific culling practices:
  - W (tungsten) values omitted due to pervasive analytical noise.
  - Sb (antimony) largely culled except in cloudwater and Nant Iago; cloudwater Sb kept due to correlation with other metals.
  - Cs, La, Ce, Pr, Ba, Pr, La, Ce, Pr: many values culled during periods of calibration issues or coarse reporting intervals; brief windows preserved where data were high enough to be meaningful.
  - Sb, Cs, Ba, La, Ce, Pr, W: multiple periods of calibration issues or coarse reporting leading to selective culling.
  - Cr: notable step changes around lab transitions; culling applied at several sites where transitions caused large artefacts, while acknowledging that Cr patterns differ by site.
  - Ni, Mo, Zn, Cd, Pb: data affected by lab changes or contamination; culling applied selectively; in some sites, pre-transition data retained with caution, while post-transition data culled if artefactual.
  - Sr, Cu, Be, U, Sn, Se, As, Cl, etc.: various site- and period-specific culling based on correlations, calibration issues, or lab-related artefacts.
- Data blocks and time periods:
  - 1992–1998 periods often show calibration issues due to reporting interval changes; many variables affected.
  - 1998–1999 transition from Wallingford to Lancaster often associated with increased variance and artefacts; culling applied as needed.

## Analyte groups and data handling notes

- Grouping approach:
  - Analytes organized by measurement method (e.g., IC, electrochemical, autoanalysis) and then by atomic number, followed by base cations/metals (ICP-OES, ICP-MS) in order of increasing atomic number.
- Notable data handling aspects:
  - Conductivity, pH, Gran alkalinity, and Gran acidity measured on settled (unfiltered) samples; solute concentrations measured on filtered samples. No significant difference found between filtered and unfiltered for these analytes in 1980s tests.
  - ANC calculated from major ions; ionic strength estimated from major ions plus alkalinity and pH.
  - Outlier detection used relationships between pH, Alk, flow, and other derived relationships to identify suspect values.
- Daily measurements:
  - Daily chloride data are unique and part of a separate historical record (over three years); other daily elements subject to the same culling rules as the weekly data.

## Derived metrics and data presentation

- Don and DON:
  - DON is calculated as TDN minus NO3 minus NO2 minus NH4 using edited values; some negative DON values may remain due to uncertainties in DON estimation.
- Specific derived variables:
  - SO4_by_ICP is calculated from ICP-derived S values; SO4 (measured as sulfate ion) kept where consistent with ion measurements.
- Presentation and notes:
  - The document includes time-series plots showing edits; red values indicate raw data changes. Not all analytes have plots for every site due to space.

## Practical guidance for users (data usage and caveats)

- Edited data provide higher confidence for routine analyses, with clearly documented caveats around method changes and calibration periods.
- Raw data remain accessible for transparency and specialized investigations, but users should anticipate calibration issues, blocks of anomalies, and lab-change effects.
- When performing trend analyses, especially across major lab transitions (circa 1998–1999), exercise caution or consider segmenting data by laboratory period.
- Users should reference the included method-change metadata and data notes to understand site-specific edits and the rationale behind culling decisions.
- The data set emphasizes self-contained quality control documentation, enabling users to assess data suitability for their specific analyses and to reproduce edits if needed.