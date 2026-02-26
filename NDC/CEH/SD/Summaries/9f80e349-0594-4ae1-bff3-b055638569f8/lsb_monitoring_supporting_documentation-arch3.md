# Littlestock Brook Monitoring Dataset (Turbidity, SSC, TP, and Discharge, 2017-2021)

## Overview
- A 5-minute resolution dataset of turbidity, suspended sediment concentration (SSC), total phosphorus (TP), and discharge for three Littlestock Brook stream sites in southern England (2017–2021).
- Turbidity measured in situ; SSC and TP derived via regression relationships to turbidity samples; discharge derived from stage-discharge rating curves and gaugings.
- Collected under a Natural Flood Management (NFM) scheme project; dataset overseen by UKCEH with input from two NERC-funded PhD projects.
- Data quality controlled, with missing periods, sensor issues, and interpolation noted.

## Study sites and data collection context
- Sites: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow (headwater tributaries of River Evenlode, within the Thames basin).
- Location details provided (latitude/longitude per site) and cross-referenced with site-specific rating curves and calibration data.
- Part of a monitoring programme aligned with flood risk mitigation and diffuse pollution reduction.

## Measurements and sensors
- Turbidity: 5-minute in situ measurements using DTS-12 sensors; EXO2 turbidity sensor used at LSB_The_Heath for SSC calibration.
- SSC: mg/L, derived from turbidity via regression; validated with hourly EXO2-derived samples at one site.
- TP: mg/L, determined via the modified molybdenum blue method; regression used to link SSC to TP.
- Discharge: L/s, derived from stage-discharge rating curves; flow gauging used velocity-area method and salt-dilution method at low flows; stage measured by instream sensors and fixed stage boards.
- Instrumentation list includes DTS-12, EXO1/EXO2 sondes, CR1000 Datalogger, Level TROLL 500, EC Current Meter, and related equipment.

## Data processing and analytical methods
- SSC regression: turbidity predicts SSC; separate regression equations and confidence intervals per site.
- TP regression: SSC used to predict TP; site-specific equations and R^2 values reported.
- Discharge estimation: stage-discharge relationships developed per site; separate equations for low/high flow conditions; 95% confidence intervals provided.
- Data were quality controlled to ensure sensor readings were plausible; regression-based conversions used to generate 5-minute SSC and TP timeseries.
- The LSB_The_Heath file includes additional columns for EXO_SSC and SSC_Combined (which blends DTS-12 SSC with EXO_SSC data).

## Data structure and metadata
- Three CSV files: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
- Columns (14 total for two sites; LSB_The_Heath has extra columns): Timestamp, QC_Code, Turbidity_Mean, Turbidity_Min, Turbidity_Max, SSC, SSC_Lower_CI, SSC_Upper_CI, Q, Q_Lower_CI, Q_Upper_CI, TP, TP_Lower_CI, TP_Upper_CI; plus EXO_SSC, EXO_SSC_Lower_CI, EXO_SSC_Upper_CI, SSC_Combined for LSB_The_Heath.
- QC_Code meanings: G = Good; I = Interpolated; M = Missing; E = EXO data.
- Units: Timestamp in UTC (YYYY-MM-DD hh:mm:ss); Turbidity in NTU; SSC in mg/L; TP in mg/L; Q in L/s.
- Appendix/Table 6 documents variable descriptions and units; detailed regression equations and confidence intervals are provided in Tables 2–5 (within the document).

## Calibration, quality control, and data handling
- Turbidity calibration: performed ~twice yearly; sensors swapped during calibration periods; linear calibration equations derived per deployment period; drift monitored via pre/post calibration values; uncertainty bounds established from calibration results.
- Phase corrections: raw water depth depths corrected to stream stage via site-specific linear regressions; SSC timeseries computed via turbidity-to-SSC regressions; TP via SSC-to-TP regressions.
- Quality control rules (turbidity): remove negative/zero values, values above sensor range, sensor-failure periods, and erroneous spikes/drops using defined criteria; gaps <= 12 hours interpolated linearly with baytrends in R; interpolated points flagged with QC code 'I'; gaps > 12 hours left as missing ('M').
- Discharge QC: remove obviously erroneous data; short gaps (≤30 minutes) linearly interpolated; longer gaps left as blank.
- Data structure notes: three CSVs reflect separate sites; LSB_The_Heath includes additional EXO-derived SSC columns and a combined SSC column.

## Data gaps, caveats, and misc
- Periods of very low water levels could expose turbidity sensors to air, causing false near-zero readings, particularly at LSB_The_Heath and LSB_Upstream_The_Heath; EXO2 turbidity sensor installation helped mitigate data loss.
- A pressure sensor malfunction at LSB_Church_Meadow (from 05/07/2017 13:20:00 UTC) led to discharge data being linearly interpolated until late September 2017; no major storm events during interpolation period, but users should exercise caution for low/baseflows.
- Catchment interventions under the Natural Flood Management program (storage ponds, arable reversion) were implemented from 2018 onward, potentially affecting hydrology and pollution transport; see related references for intervention details.

## Usage and references
- The dataset has been used in environmental and hydrological research, including two NERC-funded PhD projects; referenced studies include Bowes et al. (2018), Dalgaard (2004), Eisenreich et al. (1975), Hongve (1987), Old et al. (2019), Robotham et al. (2021), and associated methodological guidance.
- Appendix provides site-specific stage-discharge relationships with confidence intervals for low-flow conditions.

## Practical implications for monitoring frameworks
- Demonstrates end-to-end monitoring workflow: in situ turbidity measurement, regression-based SSC/TP estimation, discharge estimation from stage with rating curves, and multi-level QC and data governance.
- Highlights common data governance challenges: data gaps, metadata sufficiency, sensor drift management, data sharing considerations, and the impact of infrastructure changes (NFM interventions) on long-term datasets.
- Provides a transparent, site-specific calibration framework, including uncertainty bounds and clear documentation of processing steps, enabling policy evaluators to interpret temporal trends and compare across sites.