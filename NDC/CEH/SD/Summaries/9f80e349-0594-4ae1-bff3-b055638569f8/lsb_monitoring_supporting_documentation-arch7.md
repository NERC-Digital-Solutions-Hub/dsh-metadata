# Littlestock Brook monitoring dataset (2017-2021): Turbidity, Suspended Sediment Concentration, Total Phosphorus, and Discharge

- Overview
  - A 5-minute resolution dataset covering turbidity, suspended sediment concentration (SSC), total phosphorus (TP), and discharge for three Littlestock Brook sites (southern England) from 2017–2021.
  - Turbidity measured in situ; SSC and TP derived via regression relationships with turbidity and SSC samples.
  - Discharge derived from stage–discharge rating curves built per site; flow gauging methods include velocity–area and salt-dilution when needed.
  - Collected under the Littlestock Brook Natural Flood Management (NFM) scheme; UKCEH oversaw collection; linked to two NERC-funded PhD projects.
  - Some data gaps due to sensor failures; quality-controlled with linear interpolation for short gaps; longer gaps remain blank.
  - Intended for GIS-enabled analysis and map-based data visualization; suitable for monitoring pollution and flood-risk indicators.

- Spatial and temporal coverage
  - Three stream monitoring sites: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
  - Site coordinates (example): 
    - LSB_The_Heath: 51.865283, -1.6180989
    - LSB_Upstream_The_Heath: 51.868396, -1.6316682
    - LSB_Church_Meadow: 51.864193, -1.6187105
  - Timeframe: data collected 2017–2021; with differing start times per site for some sensors and regression calibrations.

- Data files and structure
  - Three CSV files: LSB_The_Heath, LSB_Upstream_The_Heath, LSB_Church_Meadow.
  - Common columns (14) for Upstream and Church Meadow: 
    - Timestamp, QC_Code, Turbidity_Mean, Turbidity_Min, Turbidity_Max, SSC, SSC_Lower_CI, SSC_Upper_CI, Q, Q_Lower_CI, Q_Upper_CI, TP, TP_Lower_CI, TP_Upper_CI
  - Additional columns in LSB_The_Heath file: EXO_SSC, EXO_SSC_Lower_CI, EXO_SSC_Upper_CI, SSC_Combined
  - Column descriptions and units are defined in Table 6 of the document.

- Measurements and units
  - Turbidity: NTU (nephelometric turbidity units)
    - Turbidity_Mean derived from calibration period, with Min/Max values representing calibration-based bounds
  - SSC: mg L^-1
  - TP: mg L^-1
  - Discharge (Q): L s^-1
  - Confidence intervals provided for SSC and TP estimates; 5-minute resolution time series derived from regression models

- Measurement methods and instrumentation
  - Turbidity sensors: DTS-12 (instream) and EXO2 optical turbidity sensor (EXO2 at The Heath since 2017)
  - Discharge measurements: velocity–area method; cross-sectional depth measurements; ECM for velocity; salt-dilution method used at low flows
  - Depth/Stage: Level TROLL 500 data logger with stilling well; site flow gaugings
  - SSC reference: field sampling with membrane filtration (GF/C filters) and drying oven
  - TP reference: modified molybdenum blue method
  - Calibration equipment: standards for NTU, plus independent EXO turbidity measurements

- Data processing, calibration, and regression models
  - Turbidity calibration: sensor-specific linear calibration using NTU standards; drift monitoring via pre/post deployment calibrations
  - Stage correction: raw water depth corrected to stream stage using linear regressions per site
  - SSC estimation: turbidity-to-SSC regression per site (various equations and R^2 values provided)
  - TP estimation: SSC-to-TP regression per site (R^2 values; site-specific equations)
  - EXO_SSC (where available) used to supplement SSC; SSC_Combined combines DTS-12 SSC observations with EXO_SSC (where data exist)
  - Confidence intervals: 95% CIs calculated for regression-based estimates

- Quality control and data cleaning
  - Turbidity QC rules:
    - Remove negative, zero, above-detection-range values
    - Remove data during confirmed sensor failure periods
    - Remove erroneous spikes and drops using relative-change criteria
    - Interpolate gaps < 12 hours (fillMissing from baytrends in R); interpolated points flagged with QC code 'I'
    - Gaps > 12 hours left as missing and flagged 'M'
  - Discharge QC: remove erroneous values; interpolate short gaps ≤ 30 minutes; longer gaps left blank
  - Miscellaneous data quality notes:
    - Occasional false low turbidity readings during very low flows when sensors exposed to air; some gaps remain, especially at The Heath sites
    - 2018 onwards: catchment interventions (NFM ponds, arable reversal) may influence hydrology and pollutant transport

- Special considerations and caveats for GIS use
  - The Upstream The Heath discharge curve is limited to estimates up to ~330 L s^-1 due to sparse low-flow gauging data
  - Some periods (e.g., 05/07/2017 13:20:00 UTC to 28/09/2017) at Church Meadow had sensor issues; discharge data were interpolated across that interval
  - EXO2 data improved turbidity coverage at The Heath; some periods still rely on DTS-12-based estimates
  - Catchment interventions (post-2018 NFM measures) may affect flows and pollutant loads; consider when comparing across years

- References and metadata
  - Key references for methodology and context (Bowes et al., Dalgaard, Eisenreich et al., Hongve, Old et al., Robotham et al., etc.)
  - Appendix includes stage–discharge relationships and confidence intervals for site-specific curves

- Practical GIS implications
  - Use the three site coordinates to map sampling locations and join to the 5-minute time series
  - Temporal analyses can leverage the 2017–2021 window for trend assessment in turbidity, SSC, TP, and discharge
  - Combine with catchment shapefiles and NFM intervention layers to examine spatial patterns of pollutant transport and flood mitigation effects
  - Pay attention to QC flags and interpolation notes when filtering or aggregating data (e.g., avoid interpolated periods for baseflow analyses)