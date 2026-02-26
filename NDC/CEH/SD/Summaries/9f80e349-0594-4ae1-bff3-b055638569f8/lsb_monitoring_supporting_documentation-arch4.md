# Littlestock Brook monitoring dataset (2017-2021): turbidity, suspended sediment concentration, total phosphorus concentration, and discharge at three stream sites

- Purpose and scope
  - Dataset of five-minute resolution measurements for turbidity, suspended sediment concentration (SSC), total phosphorus (TP), and discharge across three Littlestock Brook sites (2017–2021) in southern England.
  - Turbidity is measured in situ; SSC and TP derived via regressions from turbidity and sampled data; discharge derived from stage-discharge rating curves.
  - Collected for the Littlestock Brook Natural Flood Management (NFM) scheme to mitigate flood risk and diffuse pollution; UKCEH led data collection; linked to two NERC-funded PhD projects.

- Sites and temporal coverage
  - Three monitoring sites in Littlestock Brook, a headwater tributary of the River Evenlode (upper Thames basin).
  - Sites: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
  - Time period: 2017–2021, with some gaps due to sensor failures and other issues.

- Measurements and variables
  - Turbidity: measured at 5-minute intervals using DTS-12 sensors (NTU; median used per period) and EXO2 turbidity sensor (NTU) for cross-calibration.
  - SSC: derived from turbidity via site-specific regressions (mg/L) with 95% CI bounds.
  - TP: concentration (mg/L) derived from SSC via regression.
  - Discharge: derived from stage-discharge rating curves (L/s) with 95% CIs; external gauging and salt-dilution methods used for calibration under low/high flows.
  - Additional data: EXO_SSC (from EXO turbidity readings), SSC_Combined (observations where DTS-12 data available, with gaps filled using EXO_SSC).

- Data resolution and structure
  - Resolution: 5-minute intervals for turbidity, SSC, TP, and discharge time series.
  - Files: three CSVs - LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
  - Columns (common to all files): Timestamp, QC_Code, Turbidity_Mean, Turbidity_Min, Turbidity_Max, SSC, SSC_Lower_CI, SSC_Upper_CI, Q, Q_Lower_CI, Q_Upper_CI, TP, TP_Lower_CI, TP_Upper_CI. LSB_The_Heath has extra columns: EXO_SSC, EXO_SSC_Lower_CI, EXO_SSC_Upper_CI, SSC_Combined.
  - QC_Code meanings: G = Good, I = Interpolated, M = Missing, E = EXO data.

- Calibration, processing and quality control
  - Turbidity calibration: performed ~twice yearly; sensor drift monitored by replacing sensors and calibrating against NTU standards and independent EXO turbidity probe.
  - Stage and depth corrections: depth log corrected to stream stage via site-specific linear relationships.
  - SSC and TP regressions: turbidity to SSC regression (per site) and SSC to TP regression (per site) with reported R^2 values and 95% CIs.
  - Quality control (turbidity): rules to remove erroneous data (negative or over-range values, sensor failure periods, spikes/drops, etc.); spikes detected as abrupt changes relative to neighboring values; drops flagged using average-based criteria.
  - Gaps and interpolation: gaps < 12 hours linearly interpolated (fillMissing in R); interpolated points flagged as I; gaps > 12 hours left as missing and flagged M.
  - Discharge quality control: removal of erroneous periods; short gaps (≤30 minutes) linearly interpolated; longer gaps left blank.
  - Miscellaneous data notes: there are periods where sensors may have exposed to air at very low flows; the EXO2 sensor helped reduce data loss at The Heath sites. A pressure sensor malfunction at Church Meadow caused interpolation of discharge data from 2017-07-05 to 2017-09-28; caution advised for low/baseflows during this period.
  - Catchment interventions: NFM-related interventions (e.g., storage ponds, land-use changes) implemented from 2018 onward; potential impacts on flow and pollutant dynamics; see accompanying references for context.

- Data and metadata details
  - Data structure notes: TS, QC_Code, turbidity and derived variables with associated confidence intervals; SSC and TP uncertainties provided; EXO_SSC and SSC_Combined provide alternative estimates where applicable.
  - Units and formats: Timestamp in UTC (YYYY-MM-DD hh:mm:ss); Turbidity in NTU; SSC and TP in mg/L; Discharge in L/s; confidence intervals aligned with respective predictor variables (SSC, EXO_SSC, Q, TP).
  - Appendix references: stage-discharge relationships and associated 95% CIs for low-flow conditions at each site (A1, A3, A4).

- Data provenance and references
  - Data collection overseen by UKCEH; part of Littlestock Brook NFM project funded by Environment Agency.
  - Related usage: data have been employed in two NERC-funded PhD projects and cited in Bowes et al. (2018), Dalgaard (2004), Eisenreich et al. (1975), Hongve (1987), Old et al. (2019), Robotham et al. (2021), and others.

- Practical considerations for data use
  - Be aware of potential low-flow issues (air exposure of turbidity sensors) and dataset gaps; the EXO2 sensor mitigated some data loss.
  - Caution advised for discharge data during the 2017 low-flow interpolation period at Church Meadow.
  - Data reflect catchment interventions from 2018 onward; interpretation should consider altered hydrology and pollutant storage/removal dynamics.

- Appendix highlights
  - Stage-discharge relationships and 95% confidence intervals for the three sites, especially at low flows, are provided to support interpretation of discharge estimates.