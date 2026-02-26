# Littlestock Brook Flood Storage Area Monitoring Supporting Documentation

- Purpose and scope
  - Provides high-resolution (5-minute) water level data for 9 flood storage areas (FSAs) in the Littlestock Brook catchment (tributary of the River Evenlode) from 2018–2022.
  - Includes estimated 9 x FSA stored volumes (5-minute resolution) derived from depth-stored volume lookups using DEMs, and a combined 1–5-minute atmospheric pressure time-series.
  - Collected as part of the Littlestock Brook Natural Flood Management (NFM) scheme monitoring, a 5-year EA-funded project using nature-based solutions to mitigate flood risk and diffuse pollution.
  - Data interpreted in two NERC-funded PhD projects; supports data sharing and governance via QA/transformation workflows.

- dataset contents
  - 9 FSA files (P1–P9) containing water level and stored volume data for each FSA at 5-minute resolution; file names include P1-QC-Vol, P2-QC-Vol, …, P9-QC-Vol.
  - 5 atmospheric pressure files (Bruern_Baro_QC_2018–2022) containing combined pressure data from Grange Farm sensors and LR data, with metadata columns.
  - 7 data columns per FSA file: Timestamp, Raw_Pressure, Bruen_Pressure, Raw_level, Corrected_level, MASL, FSA_Volume.
  - Atmospheric pressure files include: Timestamp, Bruern_Pressure, Sensor, Ob_type.
  - Table 3 provides metadata for all data variables (units/formats).

- sites, instrumentation, and data collection
  - 9 FSA monitoring sites located in Littlestock Brook south sub-catchment (headwaters of the Thames basin).
  - 8 FSAs offline, 1 online FSA (P1) monitored with Level TROLL 100 pressure sensors submerged in stilling wells; stage boards used for calibration (surveyed to 1 cm using RTK-GNSS).
  - Atmospheric pressure monitored at Grange Farm (GF) using BAROTROLL 100 sensors; Bruern_1 and Bruern_2 used at GF, with Bruern_LR data used to fill gaps.
  - Data gaps due to periods of dry FSAs or sensor errors; missing data infilled with regression or LR data where appropriate.
  - Volume estimates for each FSA derived from a DEM (1 m LiDAR where available; manual surveys with Natural Neighbor interpolation where LiDAR absent); vertical accuracy expected to be within ±15 cm (RMS error).

- data processing and quality control
  - Atmospheric pressure processing
    - Missing timestamps filled with NA; plausibility checks and removal of outliers.
    - Regression to link LR data with Bruern data to predict GF pressure; equation: Bruern = 1.0047144 × Bruen LR + 6.7531475 (trained July–Dec 2018, tested Jan–Apr 2019).
    - Combined time-series from Bruern_1, Bruern_LR, and Bruern_2; interpolation to 1-minute timestamps where needed.
  - Water level processing
    - Barometric correction applied to water level readings to remove atmospheric pressure effects.
    - Conversion from raw pressure to water level using the specified correction formula, then to stage with site-specific linear regressions.
    - per-site linear regression to convert Corrected_level to mASL (slope, intercept, and offset used to derive MASL values; see Table 2 for P1–P9).
    - QA steps include handling gaps, removing outliers/spikes, and ensuring realism (e.g., no negative water levels).
  - Volume calculation
    - Stored volume per FSA calculated from the depth-area-volume relationship derived from each FSA DEM.
    - Time-series of FSA_Volume produced by matching water level time-series to the corresponding depth-stored volume table.
  - Data structure and labeling
    - FSA files: seven columns (Timestamp, Raw_Pressure, Bruen_Pressure, Raw_level, Corrected_level, MASL, FSA_Volume).
    - Barometer files: four columns (Timestamp, Bruern_Pressure, Sensor, Ob_type).
    - Metadata describes units/formats; documentation includes regression infill formula and model validation figures (Figures 2 and 3 in the document).

- calibration and measurement details
  - Pressure sensors provided with factory calibration; clock drift checked at each site visit with no significant drift observed.
  - Raw pressure units: mbar; water level derived in mm; corrected level in mm; MASL in meters; volumes in cubic meters.
  - Stage boards set as fixed references; readings used to calibrate water level conversions.

- data quality, gaps, and limitations
  - Noted data gaps due to dry periods or sensor errors; P6 data missing July–October 2020 (sensor error).
  - LiDAR data availability varied; manual surveys used where LiDAR absent.
  - Absolute height error between Ground Truth and LiDAR data estimated as ±15 cm (RMS), with relative height error for sensors ±5 cm.
  - Some data were infilled using LR data or site-specific regression; certain periods rely on interpolated or inferred values.

- usage notes and context
  - Dataset supports monitoring framework decisions for environmental health and flood risk management; clearly defined QA, data transformation, and governance steps.
  - Outputs include time-series of FSAs water levels (mm), corrected stage (mm), height above sea level (mASL), and FSA volumes (m3) suitable for hydrological analysis, flood risk assessment, and policy evaluation.
  - Documentation links to broader NFM monitoring program and related PhD projects, illustrating data provenance and methodological transparency.