# Overview: This dataset contains measurements of turbidity, suspended sediment concentration, total phosphorus concentration, and discharge at a 5-minute resolution over a period of several years (2017-2021) for three stream sites in the Littlestock Brook catchment (southern England).

## Scope and purpose
- Long-term, high-resolution monitoring dataset as part of Littlestock Brook Natural Flood Management (NFM) scheme.
- Aims to enable analysis of turbidity, sediment, nutrient concentrations, and discharge; supports data-driven understanding and potential dashboards for end users.

## Sites and location
- Three stream monitoring sites in Littlestock Brook, a headwater tributary of the River Evenlode within the Thames basin.
- Site locations and coordinates provided in the accompanying tables.

## Measurements and time resolution
- Turbidity: measured at 5-minute intervals (NTU) using instream sensors; two sensor types (DTS-12 and EXO2) with calibration.
- Suspended Sediment Concentration (SSC): measured in mg/L; derived from turbidity via regressions with site-specific calibrations.
- Total Phosphorus (TP): measured in mg/L; derived from SSC using regression.
- Discharge (Q): measured in L/s; derived from stage-discharge rating curves, with salt-dilution methods used at low flow.
- Data span: 2017–2021, with some gaps due to sensor issues or environmental conditions.
- File structure: three CSV files corresponding to the sites:
  - LSB_The_Heath
  - LSB_Upstream_The_Heath
  - LSB_Church_Meadow
- Extra data at LSB_The_Heath include EXO_SSC and SSC_Combined columns.

## Data collection and instrumentation
- Turbidity sensors: DTS-12 (in situ) and EXO2; depth measured with Level TROLL 500; turbidity calibrated against NTU standards and validated against EXO measurements.
- SSC TP analyses: membrane filtration (GF/C filters) with standard lab protocols; TP via modified molybdenum blue method.
- Discharge measurements: velocity-area method for cross-sections; salt-dilution method for low flows; rating curves relate stage to discharge.
- Instruments listed include DTS-12, EXO1/EXO2 sondes, CR1000 logger, Level TROLL 500, EC meters, UV/Vis spectrophotometer, and other field/lab gear.

## Data processing, calibration, and conversions
- Stage: depth sensor readings converted to stream stage via site-specific linear regressions.
- SSC: turbidity-to-SSC regressions developed per site, with 95% confidence intervals.
- TP: SSC-to-TP regressions, with site-specific coefficients and confidence intervals.
- EXO_SSC at LSB_The_Heath: derived from EXO turbidity with corresponding regression; EXO_SSC values interpolated hourly to generate 5-minute resolution.
- SSC_Combined: observations from DTS-12 (when available) with gaps filled by EXO_SSC data.
- Calibrations:
  - Turbidity sensors calibrated roughly twice per year against standards and cross-validated with an Analite turbidity probe.
  - Pre/post calibration values used to define uncertainty bounds and apply sensor drift adjustments.
- Data corrections: raw water depths corrected against observed stage board readings; gaps ≤12 hours interpolated with baytrends in R; interpolated values flagged (QC code 'I'); longer gaps ('M') left as missing.
- QC Codes: Each turbidity observation has a QC_Code:
  - G = Good
  - I = Interpolated
  - M = Missing
  - E = EXO data
- Discharge QC: similar quality control to remove erroneous data; short gaps (<30 minutes) interpolated; longer gaps left blank.

## Quality control and data integrity
- Turbidity QC rules to remove erroneous measurements due to sensor errors or debris, including:
  - Values >0 NTU and within sensor range (0–1600 NTU range checks)
  - Removal of prolonged sensor failure periods
  - Spike/drop detection using inter-timestep comparisons
  - Linear interpolation for gaps <12 hours; longer gaps marked as missing
- Discharge data QC to remove rapid fluctuations or extreme values; short gaps interpolated.
- Notes on potential false readings when turbidity sensors were exposed to air during very low flows; EXO2 sensor reduced data loss.
- Acknowledgement of NFM interventions (storage ponds, arable reversion) from 2018 onward influencing catchment responses.

## Data structure and metadata
- Each site file contains 14 columns: Timestamp (UTC, YYYY-MM-DD hh:mm:ss), QC_Code, Turbidity_Mean, Turbidity_Min, Turbidity_Max, SSC, SSC_Lower_CI, SSC_Upper_CI, Q, Q_Lower_CI, Q_Upper_CI, TP, TP_Lower_CI, TP_Upper_CI.
- The Heath file includes additional columns: EXO_SSC, EXO_SSC_Lower_CI, EXO_SSC_Upper_CI, and SSC_Combined.
- Table 6 provides units and descriptions for all variables, including the meaning of QC codes and the 95% confidence intervals for SSC, Q, and TP.
- Appendix contains stage–discharge relationships with confidence intervals for low-flow and site-specific relationships (A1–A4).

## Caveats and caveat notes
- Gaps exist due to sensor issues and low-flow exposure of sensors; the EXO2 turbidity sensor helped mitigate data loss.
- A pressure sensor malfunction at LSB_Church_Meadow led to interpolated discharge data from 05/07/2017 to 28/09/2017; use for low-flow analyses with caution.
- Catchment interventions under the Natural Flood Management program from 2018 onwards may affect hydrological responses.

## References
- Bowes et al. (2018); Dalgaard (2004); Eisenreich et al. (1975); Hongve (1987); Old et al. (2019); Robotham et al. (2021); Standing Committee of Analysts (1984).
- Appendix references include site-specific stage–discharge relationship figures (A1–A4).

## Practical notes for data use and potential products
- Data suitable for self-service dashboards and time-series analyses of turbidity, SSC, TP, and discharge at three catchment sites.
- Use site-specific regression equations and their confidence intervals to interpret SSC and TP estimates from turbidity.
- Be mindful of gaps, sensor exposure issues, and post-2018 NFM interventions when analyzing long-term trends or event responses.
- Data are available as three CSV files with standardized metadata and QC annotations to support data discovery and reuse.