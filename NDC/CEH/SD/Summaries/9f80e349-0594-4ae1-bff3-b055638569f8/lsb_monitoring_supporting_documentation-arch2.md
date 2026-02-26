# Overview: This dataset contains measurements of turbidity, suspended sediment concentration, total phosphorus concentration, and discharge at a 5-minute resolution over a period of several years (2017-2021) for three stream sites in the Littlestock Brook catchment (southern England)

- Purpose: Monitoring Littlestock Brook as part of the Natural Flood Management (NFM) scheme to assess environmental health and the policy-relevant effectiveness of low-cost nature-based solutions.
- Sites: LSB_The_Heath; LSB_Upstream_The_Heath; LSB_Church_Meadow (with coordinates provided in the documentation).
- Data span: 2017–2021, with some periods of missing data due to sensor failure; short gaps interpolated where appropriate.

## Data content and time resolution

- Variables measured at 5-minute resolution:
  - Turbidity (NTU) from instream DTS-12 sensors; additional EXO2 turbidity sensor at LSB_The_Heath.
  - Suspended Sediment Concentration (SSC) in mg/L derived from turbidity via site-specific regressions; includes SSC, and 95% confidence intervals (Lower/Upper CI).
  - Total Phosphorus (TP) concentration in mg/L derived from SSC via regression; includes CIs.
  - Discharge (Q) in L/s derived from stage-discharge rating curves; includes CIs.
- Additional columns at LSB_The_Heath: EXO_SSC; EXO_SSC_Lower_CI; EXO_SSC_Upper_CI; SSC_Combined (observations from DTS-12 with EXO_SSC data filling gaps where available).

## Data collection methods and sensors

- Turbidity measurements:
  - DTS-12 sensors (in situ; 5-minute intervals).
  - EXO2 turbidity sensor used to calibrate SSC relationships and extend coverage during low flows.
- Discharge and stage:
  - Stage measured with instream level sensors; discharge estimated from stage-discharge rating curves.
  - Flow gauging using velocity-area method; low-flow discharges via salt-dilution gauging with EXO1 sensor.
- Supporting measurements:
  - Water depth (Level TROLL 500), cross-channel depths, velocity (ECM), and regular site gaugings.
- Analytical methods:
  - SSC via membrane filtration (1.2 µm) and drying oven at 105°C.
  - TP via modified molybdenum blue method.
- Calibration and QA:
  - Turbidity sensors calibrated twice per year against standards; regressions used to convert turbidity to SSC.
  - TP calibrated with external standards and QA checks (Blind standards included).
  - Regression models and confidence intervals explicitly documented (Tables 3–5 in the full text).

## Data processing, structure, and metadata

- File structure:
  - Three CSV files: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
- Columns (typical, with LSB_The_Heath containing extra ones):
  - Timestamp (UTC, YYYY-MM-DD hh:mm:ss)
  - QC_Code (G = Good; I = Interpolated; M = Missing; E = EXO data)
  - Turbidity_Mean, Turbidity_Min, Turbidity_Max (NTU)
  - SSC (mg/L); SSC_Lower_CI; SSC_Upper_CI
  - Q (discharge; L/s); Q_Lower_CI; Q_Upper_CI
  - TP (mg/L); TP_Lower_CI; TP_Upper_CI
  - EXO_SSC; EXO_SSC_Lower_CI; EXO_SSC_Upper_CI (LSB_The_Heath only)
  - SSC_Combined (observations filled with EXO_SSC where DTS-12 data exist)
- Data quality and gaps:
  - Short gaps (<12 hours) interpolated linearly (flagged as Interpolated with QC code 'I'); longer gaps left as missing ('M').
  - Discharge data quality controlled for spurious fluctuations; short gaps (<30 minutes) interpolated; longer gaps left blank.
- Miscellaneous caveats:
  - Periods of very low flow may expose turbidity sensors to air, causing false near-zero readings (some data removed; EXO2 helped reduce loss for LSB_The_Heath).
  - Pressure sensor issue at LSB_Church_Meadow caused discharge interpolation for 2017 mid-year; use with caution for low/baseflows.
  - Catchment interventions (NFM measures) implemented from 2018 onward; potential impacts on hydrology and water quality.

## Calibration, validation, and uncertainty

- Turbidity-to-SSC calibration:
  - Regression-based conversions between turbidity and SSC, with site-specific equations and 95% CIs.
  - EXO_SSC regression used where applicable; strong R^2 values reported (typically around 0.9+ for key relationships).
- SSC-to-TP calibration:
  - Regression of TP on SSC to estimate TP from SSC with CI bounds.
- Stage-to-discharge calibration:
  - Rating curves fitted with non-linear least squares (nls) in R; 95% CIs calculated; note the upper discharge limit for LSB_Upstream_The_Heath (~330 L/s) where applicable.
- Data quality rules for turbidity:
  - Positive values, within sensing range, removal of sensor-drift periods, spike/drop detection, and linear interpolation for small gaps.
  - Interpolated datapoints flagged; large gaps documented as missing.

## Temporal coverage and data availability

- Timeframe: 2017–2021 for all sites.
- Notable data gaps:
  - Early periods at some sites (especially LSB_The_Heath) with turbidity data loss; EXO2 helped mitigate.
  - Church Meadow discharge period interpolated during a sensor fault (2017-07 to 2017-09); recommended caution for low-flow analyses.
- Data interoperability:
  - Data designed for standardised time steps (5-minute resolution) and comparable across sites, enabling time-series analyses and cross-site comparisons.

## Provenance, references, and usage notes

- Monitoring program:
  - Littlestock Brook Natural Flood Management scheme; funded by Environment Agency; data collection overseen by UKCEH; linked to two NERC-funded PhD projects (Robotham et al. 2021).
- Key references for context and methods:
  - Bowes et al. 2018; Dalgaard 2004; Eisenreich et al. 1975; Hongve 1987; Old et al. 2019; Robotham et al. 2021; Standing Committee of Analysts 1984.
- Appendix:
  - Stage-discharge relationships with confidence intervals (A1, A3, A4) illustrating discharge estimation at the three sites.

## How this supports environmental monitoring and data reuse

- aligns with Analysts Monitoring the Environment aim by providing consistent, quality-controlled time-series of turbidity, SSC, TP, and discharge across multiple sites and years.
- enables verification of environmental health against standards and policy performance over time.
- structured to facilitate data sharing and reuse:
  - clear metadata, QC codes, uncertainty bounds, and links to calibration datasets and references.
  - potential to combine with catchment-scale data (e.g., NFM interventions, rainfall, land-use changes) to evaluate diffuse pollution and flood-mrought outcomes.
- caveats and usage considerations:
  - handle interpolated periods and extrapolation limits in discharge (especially at LSB_Upstream_The_Heath).
  - consider data gaps and sensor-related artefacts in low-flow phases or early times (The Heath sites).
  - acknowledge changes in catchment management from 2018 onward when attributing trends or policy effects.