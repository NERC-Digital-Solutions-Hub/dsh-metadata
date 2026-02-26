# Littlestock Brook Flood Storage Area Monitoring Supporting Documentation

## Overview and Data Content
- A high-resolution hydrological dataset from the Littlestock Brook Flood Storage Areas (FSAs) covering 2018–2022.
- Includes 9 FSA water level time-series (5-minute resolution) and the estimated 9 x FSA stored volumes (5-minute resolution) derived from depth–area–volume lookups using a DEM-based model.
- A combined atmospheric pressure time-series is provided at 1–5 minute resolution for use in barometric correction.
- The data were collected as part of the Littlestock Brook Natural Flood Management (NFM) scheme (Environment Agency-funded) and interpreted in two NERC-funded PhD projects.
- Some data gaps exist due to dry-period exclusions or sensor errors.

## Data Content and File Structure
- 9 FSA data files: P1-QC-Vol, P2-QC-Vol, P3-QC-Vol, P4-QC-Vol, P5-QC-Vol, P6-QC-Vol, P7-QC-Vol, P8-QC-Vol, P9-QC-Vol.
  - Each file contains 7 columns: Timestamp, Raw_Pressure, Bruen_Pressure, Raw_level, Corrected_level, MASL, FSA_Volume.
- 5 atmospheric pressure files: Bruern_Baro_QC_2018, Bruern_Baro_QC_2019, Bruern_Baro_QC_2020, Bruern_Baro_QC_2021, Bruern_Baro_QC_2022.
  - Columns: Timestamp, Bruern_Pressure, Sensor, Ob_type.
- Metadata: Table 3 detailing variable descriptions and units (e.g., Timestamp in UTC, pressures in mbar, water level in mm, MASL in m, volumes in m3).
- Key supporting sites and coordinates:
  - 9 FSA sites (P1–P9) within Littlestock Brook south sub-catchment.
  - Grange Farm (GF) and Little Rissington (LR) used for atmospheric data infilling.
- Data provenance notes: collected by UKCEH as part of a hydrological monitoring programme; some data gaps and corrections described in the processing notes.

## Data Collection, Instrumentation and Calibration
- Water level monitoring:
  - Level TROLL 100 Data Loggers deployed at each FSA, with pressure sensors submerged in stilling wells; stage boards surmounted on posts for level reference.
  - RTK-GNSS surveys used to calibrate stage boards to mASL with ~1 cm accuracy.
- Atmospheric pressure monitoring:
  - BAROTROLL 100 sensors installed at Grange Farm (GF) for combined atmospheric pressure data.
  - Bruern_1 (2018–2019) and Bruern_2 (2019–) sensors; LR (Little Rissington) data used as fill-in data during gaps.
- Volume estimation:
  - FSA storage volumes derived from a Digital Elevation Model (DEM) built from 1 m LiDAR data; where LiDAR was unavailable, as-built manual survey data were interpolated.
  - Vertical and height accuracy: relative height error ≤ ±5 cm; absolute height error ≤ ±15 cm (RMS).
  - Maximum static water level identified via ArcGIS; depth–area–volume toolset produced depth-stored volume lookups per FSA.
- Calibration and sensors:
  - Pressure sensors factory-calibrated; clock drift checked at site visits; no significant drift detected.
  - Data are processed with site-specific linear regressions to convert raw readings to stage and then to mASL.

## Data Processing, Quality Control and Corrections
- Barometric pressure processing:
  - Missing pressure timestamps filled; consistency checks and outlier handling performed.
  - Regression used to link Little Rissington LR data to Bruern_1 data to produce continuous GF pressure series: Bruern = 1.0047144 × LR + 6.7531475.
  - Bruern_LR data validated against Bruern_1 data from 2019 onward; complete time-series produced by combining Bruern_1, Bruern_LR, and Bruern_2; interpolated to 00:05 intervals.
- Water level processing:
  - Corrected water level derived from Raw_Pressure and Bruern_Pressure; data gaps due to sensor changes or site visits marked as NA.
  - Site-specific linear regression (slope, intercept) used to convert corrected water level to stage; resulting mASL offset (Table 2) applied per FSA.
  - QC steps include checking for stage-board consistency, outliers, negative depths, and implausible steps; infilling used when level could be estimated with high confidence; otherwise data removed.
- Data structure and timestamps:
  - Data aligned to UTC timestamps; 1-minute interpolation applied where necessary to harmonize time series.
- Regression and validation figures:
  - Regression used for pressure infill and validation plots referenced (Figures 2 and 3 in the original docs).

## Data Gaps and Limitations
- Notable data gap: P6 missing from July to October 2020 due to a sensor error.
- Some atmospheric data gaps were filled using LR data, which introduces uncertainty during those periods.

## Practical Use and Data Support Considerations
- The dataset enables self-service analysis of FSA water levels, barometric-corrected levels, and stored volumes across the Littlestock Brook FSAs.
- Potential data products:
  - Per-FSA time-series dashboards of water level, corrected stage, and stored volume.
  - Cross-site comparisons of water level dynamics and storage across FSAs.
  - Integration with rainfall or catchment models for flood risk assessment.
- Important considerations for data support:
  - Be mindful of data gaps (especially P6 2020) and atmospheric data infilling periods; document uncertainties in analyses.
  - Ensure consistent use of site naming (Bruen vs Bruern) and verify correct source for Bruern_Pressure in each time window.
  - Use the site-specific MASL offsets (Table 2) to convert to uniform mASL when aggregating across FSAs.
  - Recognize the reliance on DEM/LiDAR-derived volumes; consider uncertainties in volume estimates due to DEM resolution and interpolation.

## Key Points for Data Support and Reuse
- Rich, multi-stream dataset facilitating comprehensive analysis of both water levels and storage volumes across nine FSAs.
- Clear documentation of data processing steps, QC procedures, and the regression-based infilling approach for atmospheric pressure.
- Well-defined data structure with metadata and per-site calibration parameters enabling reproducibility and cross-site comparisons.
- Caution required around data gaps and the use of infilled atmospheric data; incorporate uncertainty considerations in analyses and visualizations.