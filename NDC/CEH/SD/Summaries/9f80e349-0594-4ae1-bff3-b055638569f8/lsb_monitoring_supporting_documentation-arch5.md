# Overview: This dataset contains measurements of turbidity, suspended sediment concentration, total phosphorus concentration, and discharge at a 5-minute resolution over a period of several years (2017-2021) for three stream sites in the Littlestock Brook catchment (southern England).

## Aim and scope for Data Stewards
- Datasets cover turbidity, SSC, TP, and discharge at 5-minute resolution across three Littlestock Brook sites.
- Data were collected to support the Littlestock Brook Natural Flood Management (NFM) scheme (5-year project funded by the Environment Agency) and interpreted in two NERC-funded PhD projects.
- Data are quality-controlled, with missing periods documented and interpolated where appropriate to enable long timeseries analyses.
- Metadata and data provenance are provided, including calibration and processing steps, to support governance, reuse, and updates.

## Data content and structure
- Three CSV files: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
- Columns (common to two files): Timestamp, QC_Code, Turbidity_Mean, Turbidity_Min, Turbidity_Max, SSC, SSC_Lower_CI, SSC_Upper_CI, Q, Q_Lower_CI, Q_Upper_CI, TP, TP_Lower_CI, TP_Upper_CI.
- Additional columns in LSB_The_Heath: EXO_SSC, EXO_SSC_Lower_CI, EXO_SSC_Upper_CI, SSC_Combined.
- Data are provided with units and formats described in Table 6 (timestamps in UTC; NTU turbidity; SSC in mg/L; TP in mg/L; discharge in L/s).
- QC codes: G = Good, I = Interpolated, M = Missing, E = EXO data.

## Data collection and measurement methods
- Turbidity: 5-minute NTU readings from DTS-12 sensors installed instream; EXO2 turbidity sensor used at LSB_The_Heath for turbidity-SSC calibration; hourly pumped samples for SSC derivation.
- Depth/Stage: Level TROLL 500; stage boards used as fixed references; water depth used to derive stream stage.
- Discharge: Derived from a rating curve linking stage to discharge; stage and velocity-area measurements for cross-sections; salt-dilution gauging used at very low flows.
- SSC and TP: SSC derived from turbidity via regression using sampled SSC; TP via regression of SSC; calibration and regression work documented per site.
- Calibration and regressions: Site-specific turbidity-to-SSC regressions; SSC-to-TP regressions; EXO_SSC used where appropriate; primary regression parameters and 95% CIs provided (Tables 4-5 in the document).

## Analytical methods and calibration
- SSC: Membrane filtration (GF/C, 1.2 µm) with 105°C drying; mass-based SSC.
- TP: Modified molybdenum blue method.
- Turbidity calibration: Twice-yearly calibration of sensors against NTU standards; linear calibration equations per deployment period; sensor drift monitored.
- Stage correction: Linear relationships between sensor depth and observed stage per site.
- Data fusion: EXO_SSC used to interpolate between hourly EXO readings to 5-minute resolution; SSC_Combined combines DTS-12 observations with EXO_SSC when available.
- Confidence intervals: All regressions reported with 95% CIs; ratings and relations restricted by observed flow ranges (e.g., LSB_Upstream_The_Heath valid up to 330 L/s).

## Quality control and data processing
- Turbidity QC rules to remove erroneous values (negatives, values > 1600 NTU, sensor fails, spikes/drops identified and flagged).
- Spikes: Identified by deviations from neighboring values (complex criteria described in the QC rules).
- Drops: Flagged and handled as described (with interpolations where justified).
- Interpolation: Gaps < 12 hours linearly interpolated using baytrends' fillMissing; interpolated datapoints flagged as I; gaps > 12 hours left as M.
- Discharge QC: Removal of erroneous rapid fluctuations or extreme values; short gaps ≤ 30 minutes interpolated; longer gaps left blank.
- Data quality notes: Some turbidity data periods near low water levels may have been exposed to air, causing near-zero readings; EXO2 sensor helped reduce data loss at The Heath; a pressure sensor malfunction at Church Meadow required interpolation for discharge during 2017-07-05 to 2017-09-28.

## Miscellaneous data context and limitations
- Catchment interventions (Natural Flood Management measures) implemented from 2018 onward, potentially affecting hydrology and pollutant storage; see Old et al. 2019 and Robotham et al. 2021 for context.
- Use with caution for low/baseflows during periods with interpolated discharge or turbidity sensor exposure to air.
- Appendix includes stage-discharge relationships and confidence intervals for the sites (A1, A3, A4).

## Data provenance and documentation
- Data collection overseen by UKCEH; development and interpretation tied to two NERC-funded PhD projects (Robotham et al. 2021; Bowes et al. 2018).
- Calibration and validation details, standard references, and methodological notes are provided to support reproducibility and governance.
- References listed for methods and context (Bowes et al., Dalgaard, Eisenreich et al., Hongve, Old et al., Robotham et al., Standing Committee of Analysts).

## Appendix and metadata
- Appendix A1, A3, A4: Stage-discharge relationships for low-flow and site-specific confidence intervals.
- Table 6: Dataset variables with units and formats (describes all variables in the CSV files, including QC codes, turbidity metrics, SSC, TP, discharge, and EXO-derived values).

## Governance and reuse considerations for Data Stewards
- Clear data structure with explicit QC codes facilitates data quality assessment and provenance tracking.
- Documentation covers measurement methods, calibration routines, data processing, and known limitations, supporting responsible data sharing and future updates.
- Users should account for interpolated data (I) and missing data (M) in analyses, and exercise caution with periods of sensor-related data loss or calibration drift.
- When updating or extending the dataset, maintain consistency with the established regression models and calibration references, and document any new calibration periods or sensor deployments.