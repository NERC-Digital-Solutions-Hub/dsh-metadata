# Metadata: Quality control and data editing

- Purpose and scope
  - Describes the Plynlimon 7-hourly intensive hydrochemistry data set, including its raw data archive (RDA) and the edited data version.
  - Raw data are preserved for documentation and traceability; edited data are recommended for routine analyses due to identified errors in raw measurements.
  - Emphasizes transparency about data editing to reveal how and why values were changed or removed.

- Two versions and sampling details
  - Raw Data Archive (RDA): unaltered measurements with minor, traceable corrections; intended mainly for documentation and potential re-use if new phenomena demand re-examination.
  - Edited data: measurements edited to remove unexplained anomalies and to align with known correlations; higher confidence for analysis.
  - Sampling sites and methods: rainfall at Carreg Wen (CR), streamflow at Lower Hafren (LHF) and Upper Hafren (UHF); 7-hourly autosampled data versus long-term weekly samples; differences in sampling protocols and filtering (unfiltered vs filtered analyses) noted; unit and site codes documented for traceability.
  - Time alignment and comparability: weekly samples used to validate 7-hourly data; expert judgment applied when discrepancies between weekly and 7-hourly data were not large.

- Data editing approach and criteria
  - Editing philosophy: keep data where there is high confidence, remove or correct data when inconsistent with correlations, flow, or other analytes.
  - Consistency checks: used to verify plausibility (e.g., SO4 and S, Alk and pH, charge balance, Gran alkalinity vs. calculated values, etc.); where discrepancies appeared, the problematic analyte or block was removed.
  - Handling of “flyers” and outliers: extensive culling of spurious spikes or drop-outs, particularly at low concentrations or where contamination is suspected.
  - Collaborative checks across analytes: created a matrix of co-varying analytes to distinguish real signals from anomalies for each target analyte.
  - Data blocks and calibration issues: large-scale edits often targeted entire analytical blocks when calibration problems or instrument glitches were evident.
  - Carryover and check standards: identified and culled carryover effects from check standards that produced artificial “picket fence” patterns.
  - Sample handling and potential swaps: corrected evident mislabeling or swaps of acidified vs un-acidified analyses (notably Trips 80 and 81) to restore plausible cross-analytical consistency.
  - Documentation and transparency: notes on modifications accompany time-series plots; red values indicate raw data that were culled or changed, blue values indicate edited data kept or adjusted.

- Analyte-specific editing and notes (high-level)
  - Grouped by measurement method (ion chromatography, electrochemical, autoanalysis; then ICPOES/ICP-MS for cations/metals) and presented in increasing atomic number.
  - Fluoride, DOC, NO3-N, NO2-N, NH4-N, TDN, DON, Cl, Br, I, Li, Be, B, Na, Mg, Ca, K, Sr, Cs, Ba, La, Ce, Pr, Pb, U, and others were edited to varying degrees based on correlations, calibration issues, and block-level anomalies.
  - Common patterns: widespread culling of singles and blocks with calibration problems; removal of spikes not supported by co-varying analytes; culling of entire precipitation series in some elements due to systemic calibration concerns.
  - Specific recurring issues: calibration problems in certain analytical blocks, carryover effects from check standards, background correction issues, and occasional sample swaps affecting multiple analytes simultaneously.
  - Certain elements (e.g., W) were omitted entirely due to pervasive, non-meaningful values; others retained with caution where correlations were strong.

- Practical implications for users
  - Edited data are the recommended dataset for analysis due to greater consistency with inter-analyte relationships and flow dynamics.
  - Raw data remain accessible for transparency and re-interpretation if future information suggests new insights.
  - Users should note potential residual uncertainties in low-concentration analytes and blocks affected by calibration or carryover.
  - Metadata and editing rationale are documented to support reproducibility and audit trails.

- Challenges highlighted for monitoring frameworks
  - Data gaps and limited access in some cases; need for robust metadata to verify data suitability.
  - Silos and fragmented data can hinder data sharing and governance.
  - Balancing openness with data quality and calibration integrity; ensuring transparent data governance and documentation.