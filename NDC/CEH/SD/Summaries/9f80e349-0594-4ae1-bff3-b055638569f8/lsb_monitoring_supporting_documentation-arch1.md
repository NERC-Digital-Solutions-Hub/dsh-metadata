# Overview:

- This dataset contains 5-minute resolution time series (2017–2021) of turbidity, suspended sediment concentration (SSC), total phosphorus concentration (TP), and discharge for three Littlestock Brook stream sites (LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow) in southern England.
- Turbidity is measured in NTU with instream sensors; SSC and TP are derived from turbidity measurements via site-specific regressions using sampled data; discharge is derived from stage–discharge rating curves (with gauging data), supplemented by salt-dilution methods at low flows.
- The monitoring supported the Littlestock Brook Natural Flood Management (NFM) scheme (5-year project funded by the Environment Agency) and was developed/interpreted in two NERC-funded PhD projects; UKCEH oversaw data collection.

- Data quality and gaps:
  - Periods of missing data due to sensor failures; data quality controlled to remove erroneous measurements; short gaps (less than 12 hours) interpolated, with interpolated points flagged.
  - Low-flow periods may expose turbidity sensors to air, causing near-zero readings; EXO2 turbidity sensor helped reduce data loss; some gaps remain, particularly at LSB_The_Heath and LSB_Upstream_The_Heath.
  - A pressure sensor malfunction at LSB_Church_Meadow caused discharge data to be interpolated for a period in 2017; use caution for low/baseflows.

- Data structure and variables:
  - Three CSV files corresponding to each site: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
  - Core columns (all sites except The Heath have 14 columns): Timestamp, QC_Code, Turbidity_Mean, Turbidity_Min, Turbidity_Max, SSC, SSC_Lower_CI, SSC_Upper_CI, Q, Q_Lower_CI, Q_Upper_CI, TP, TP_Lower_CI, TP_Upper_CI.
  - The Heath file includes additional columns: EXO_SSC, EXO_SSC_Lower_CI, EXO_SSC_Upper_CI, SSC_Combined.
  - Units: Timestamp in UTC; Turbidity in NTU; SSC in mg/L; TP in mg/L; Q in L/s. QC_Code indicates data quality (G=Good, I=Interpolated, M=Missing, E=EXO data).
  - SSC and TP values are derived via regressions using turbidity (and, for SSC, EXO data where applicable); discharge uses rating curves with confidence intervals.

- Calibration, analysis, and metadata:
  - Turbidity sensors calibrated roughly twice per year using lab standards and independent measurements; calibrations used to derive sensor-specific linear conversion and to bound uncertainty due to drift.
  - Water depth readings corrected to stream stage via site-specific linear regressions; regressions used to convert sensor depth to stage.
  - SSC × Turbidity regression established per site (all significant at p < 0.001; R² values around 0.93–0.94 across sites).
  - SSC × TP regression used to estimate TP (TP ~ small linear function of SSC) with site-specific R² values (e.g., ~0.94 for The Heath and upstream Heath, ~0.79 for Church Meadow).
  - Discharge estimated from stage–discharge rating curves (with 95% CIs); for LSB_Upstream_The_Heath the curve is valid only up to ~330 L/s due to limited gauging data.
  - Key calibration and validation references cited (Bowes et al., Dalgaard, Eisenreich et al., Hongve, Old et al., Robotham et al., Standing Committee of Analysts).

- Methodological notes and appendices:
  - Stage–discharge relationships and their 95% CIs are provided in Appendix figures (A1–A4).
  - Data processing includes: removal of erroneous turbidity values, interpolation of short gaps (<12 hours) using baytrends’ fillMissing, and flagging interpolations ('I') or missing data ('M').
  - EXO_SSC values are interpolated hourly to generate 5-minute resolution timeseries; SSC_Combined uses DTS-12SSC where available and fills gaps with EXO_SSC data.

- Miscellaneous caveats:
  - Large gaps in turbidity data at the start of the timeseries, particularly at The Heath and upstream Heath; EXO2 sensor installation reduced data loss.
  - Catchment underwent Natural Flood Management interventions from 2018 onward, potentially affecting flow and pollutant retention; see Bowes et al. (2018), Old et al. (2019), Robotham et al. (2021) for context.
  - Users should consider data gaps, sensor exposure events, and interpolation when analyzing low-flow periods or performing trend analyses.