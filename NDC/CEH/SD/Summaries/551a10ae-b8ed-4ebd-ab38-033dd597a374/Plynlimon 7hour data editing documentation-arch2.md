# Metadata: Quality control and data editing

## Overview
- Describes the Plynlimon 7-hourly intensive hydrochemistry data set: rainfall and streamflow chemical analyses collected roughly every 7 hours for nearly two years.
- Data are published in two versions: Raw Data Archive (RDA) and edited data.
- Purpose: enable transparent documentation of data editing and provide high-confidence datasets for routine analyses and long-term environmental monitoring.

## Data Versions: Raw Data Archive and Edited Data
- Raw Data Archive (RDA): unaltered measurements with minor glitches corrected back to original lab files; remains for documentation and potential re-examination.
- Edited data: measurements edited to include only high-confidence values; problematic values removed or corrected where plausible; designed for routine analyses and consistent comparisons.

## Editing Philosophy and Methods
- Core principle: maximize data reliability while preserving genuine signals; maintain transparency about edits.
- Routine analyses favor edited data; the RDA is kept for completeness and re-evaluation if needed.
- Editing criteria include:
  - Consistency checks across related variables (e.g., SO4 with S, Alk with pH, charge balance, ANC, N species with TDN, conductivity).
  - Removal of unexplained flyers or outliers not consistent with time series correlations.
  - Retaining some exceptional outliers if they are correlated with other analytes or attributable to real processes.
  - Exclusion of data blocks or whole analyte series when broad inconsistencies suggest calibration or workflow problems.
- Expert judgment used to decide when to omit entire blocks, especially where patterns shift abruptly or where systematic issues (e.g., calibration) are evident.
- Notable data editing actions include correcting a swap of acidified vs. un-acidified analyses (Trips 80 and 81) to synchronize related signals.

## Sampling Context and Comparisons
- Sampling sites: Carreg Wen (rainfall), Lower Hafren (LHF) and Upper Hafren (UHF) for streamwater; 7-hourly sampling contrasted with long-term weekly sampling at the same sites for cross-validation.
- When substantial discrepancies occur between 7-hourly and weekly data for the same analyte, expert judgment determines which data are more plausible; in some cases, both are retained if the discrepancy is not large.
- Data presentation structure: editing changes documented first, followed by analyte-specific notes.

## Data Quality Issues, Corrections, and Examples
- Common problems addressed:
  - Calibration problems, background corrections, block-to-block shifts, and carryover from check standards causing spurious patterns (e.g., “picket fence” in trace metals).
  - Sample labeling errors, autosampler carryover, and mislabeling between analytical blocks or trips.
  - Periodic anomalous patterns (e.g., Ca spikes at LHF, weekly carryover patterns) attributed to instrument or carousel contamination rather than natural signals.
- Specific corrective actions:
  - Deletion of numerous “flyers” and outliers across many analytes, particularly in low-concentration elements (trace metals, etc.).
  - Culling of entire data blocks or adjusting blocks to align with plausible patterns.
  - Documentation and flagging of culls (shown in red) versus kept data (shown in blue) in revised time series.
- Notable data-handling notes:
  - The first analytical block in precipitates removed due to extreme flyers.
  - Reconciliation of IC and ICP data for sulfate to ensure synchronized signals.
  - Tungsten data omitted entirely due to pervasive negative values and calibration issues.
  - Several blocks adjusted with small offsets to remove artificial step changes at analytical block boundaries.

## Analyte Grouping and Notes (Summary)
- Data are presented in two groups: first, analytes determined by IC, electrochemical methods, etc.; then cations and metals by ICPOES/ICP-MS.
- Per-analyte editing notes exist, but key patterns include:
  - Frequent culling of calibration-related flyers and carryover in many elements (e.g., Cl, Br, Ti, V, Cr, Sn, W, Cu, Zn, Pb, U).
  - Certain elements show persistent correlation with others (used to judge whether a potential flyer is real or artifact).
  - Special attention to Ca spikes at LHF linked to process contamination rather than true groundwater signals.
  - DON calculated from edited TDN, NO3, NO2, NH4; negative DON may occur due to uncertainties in DO/N balance.
  - Low-concentration elements (e.g., U, W) require cautious interpretation due to coarse measurement resolution and check-standard effects.

## Analyte Correlations and Quality Checks
- The team used scatterplot matrices to identify co-varying analytes, aiding discrimination between real signals and spurious data.
- A defined set of co-variation relationships guides editing decisions for individual analytes (e.g., NH4 with TDN, DOC with DON, etc.).
- These correlations underpin decisions to retain or cull data when inconsistencies arise.

## Data Presentation and Documentation
- Edited versus raw values are clearly distinguished in figures (red for culled/edited values, blue for kept).
- The dataset references unique sample codes (CR, LHF, UHF) for individual samples.
- Detailed notes accompany time-series plots to illustrate edits and decisions.

## Practical Guidance for Users
- For routine analyses, use the edited data to ensure consistency and reliability; consult the RDA only for traceability and re-evaluation.
- Be aware of calibration issues, block boundaries, and potential carryover effects, especially in metals and trace elements.
- When interpreting DON, consider its derivation from edited TDN, NO3, NO2, and NH4 and the possibility of negative values.
- Refer to the analyte-specific notes for context on edits, especially for data blocks with known calibration problems or sample mishandling.

## Accessibility and Archiving
- The edited dataset and the RDA are archived to support reproducibility and future methodological evaluation.
- The documentation provides a transparent rationale for each edit, enabling users to reproduce filtering and corrections.