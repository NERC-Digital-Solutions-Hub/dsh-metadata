# Littlestock Brook Flood Storage Area Monitoring Supporting Documentation

- Purpose and scope
  - High-resolution (5-minute) water level data, atmospheric-corrected and mean sea level adjusted, for 9 flood storage areas (FSAs) in the Littlestock Brook catchment (tributary of the River Evenlode) from 2018 to 2022.
  - Includes estimated 9 x FSA stored volumes at 5-minute resolution, derived from depth-stored volume lookups using a DEM-based depth-area-volume approach.
  - Combined atmospheric pressure time-series (1 to 5-minute resolution) used to support water level corrections.
  - Part of the Littlestock Brook Natural Flood Management (NFM) scheme monitoring; funded by the Environment Agency; data interpreted in two NERC-funded PhD projects.
  - Some data gaps due to dry FSAs or sensor errors; supported by SPITFIRE and SCENARIO NERC DTPs.

- Data collection and locations
  - 9 FSA monitoring sites (P1–P9) in Littlestock Brook south sub-catchment; one online and eight offline FSAs.
  - 5 atmospheric pressure files from Grange Farm (GF) and nearby LR data, covering 2018–2022.
  - Site coordinates provided (Table 1) for all FSAs and atmospheric pressure monitoring points.
  - Data collected using field instrumentation and RTK GNSS survey for stage boards to enable conversion to meters above sea level (mASL).

- Measurements and sensors
  - Water pressure: Level TROLL 100 data loggers (5-minute intervals) at P1–P9, submerged in stilling wells.
  - Atmospheric pressure: BAROTROLL 100 sensors at GF (Bruern_1, Bruern_2) with infilling from LR data when needed; 5-minute to 15-minute intervals, interpolated to 1-minute timestamps as required.
  - Stage markers: Stage boards read during visits; used to calibrate water level readings to stage.
  - Volume estimation: DEM-based depth-stored volume lookup tables created per FSA using 1 m LiDAR data (or as-built manual surveys where LiDAR was unavailable).

- Data processing and corrections
  - Atmospheric pressure data infilled using a regression: Bruern = 1.0047144 × Bruen LR + 6.7531475 (trained on 2018 Jul–Dec, tested 2019 Jan–Apr).
  - Barometric correction applied to water level: Water Level (mm) = 1000 × [100 × (Raw Pressure − Bruern_Pressure)] / (1000 × 9.81).
  - Water levels converted to mASL using site-specific linear regressions between sensor readings and observed stage boards (see per-site slope and intercept; mASL offsets provided in Table 2).
  - Corrected water levels (Corrected_level) used to compute MASL (metres above sea level) via a datum offset.
  - FSA volumes computed by mapping water level to the depth-area-volume table derived from the DEM.
  - Data quality control includes handling gaps, removing implausible values, and visually inspecting for anomalies; data gaps due to sensor issues or dry FSAs noted.

- Volume estimation and DEM details
  - Depth-area-volume toolset applied to raster DEMs (1 m LiDAR or as-built surveys) to generate depth-stored volume lookup tables for each FSA.
  - Maximum static water level defined by the lowest elevation of the FSA bund, with a raster-based approach to determine the maximum possible storage.
  - Continuous water level time-series linked to depth-stored volume tables to produce FSA_Volume (m3) time-series.

- Data structure and contents
  - 9 FSA data files: P1-QC-Vol, P2-QC-Vol, P3-QC-Vol, P4-QC-Vol, P5-QC-Vol, P6-QC-Vol, P7-QC-Vol, P8-QC-Vol, P9-QC-Vol.
  - 9 columns per FSA file: Timestamp, Raw_Pressure, Bruen_Pressure, Raw_level, Corrected_level, MASL, FSA_Volume.
  - 5 atmospheric pressure files: Bruern_Baro_QC_2018, Bruern_Baro_QC_2019, Bruern_Baro_QC_2020, Bruern_Baro_QC_2021, Bruern_Baro_QC_2022.
  - Atmospheric pressure files include: Timestamp, Bruern_Pressure, Sensor, Ob_type (Observed/Interpolated).
  - Metadata table (Table 3) describes each variable’s units and formats; timestamps are UTC (YYYY-MM-DD hh:mm:ss).

- Calibration and quality assurance
  - Pressure sensors: factory calibration with clock drift checks; no significant drift observed.
  - Atmospheric pressure quality control steps: timestamp checks, NA handling, outlier checks, regression-based infill from LR data to GF data, interpolation to 00:05 intervals.
  - Water level QA steps: NA handling for log changes and submersion outages, regression-based correction to stage, plausibility checks for steps/outliers, anomaly removal, and visual inspection.
  - Calibration details include per-site regression parameters for converting corrected level to MASL (slope, intercept, MASL offset) as listed in Table 2.

- Data gaps and limitations
  - Occasional data gaps due to dry FSAs or sensor errors.
  - P6 data missing July–October 2020 due to a sensor error.
  - LiDAR data gaps corrected with as-built survey data where necessary; expected height error roughly ±5 cm random error; absolute height error target by EA: ±15 cm.

- Usage context and provenance
  - Data collected as part of the Littlestock Brook NFM monitoring programme (5-year project).
  - Data interpreted in the context of two NERC-funded PhD projects.
  - Data intended to support analyses of flood storage, stage-volume relationships, and the effectiveness of nature-based flood management strategies.