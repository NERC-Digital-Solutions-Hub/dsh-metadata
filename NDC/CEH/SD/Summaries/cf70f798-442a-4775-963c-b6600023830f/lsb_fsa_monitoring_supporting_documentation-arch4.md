# Littlestock Brook Flood Storage Area Monitoring Supporting Documentation

## Purpose and scope
- Datasets from Littlestock Brook NFM monitoring (2018–2022) covering 9 flood storage areas (FSAs) in the Littlestock Brook catchment, a tributary of the River Evenlode.
- Includes high-resolution water level data, estimated stored volumes, and atmospheric pressure time-series to support flood risk management and diffusion mitigation.
- Collected by UKCEH as part of the Littlestock Brook NFM hydrological monitoring programme; linked to two NERC-funded PhD projects.
- Funded and supported by Environment Agency and SPITFIRE/SCENARIO NERC DTPs.
- Acknowledges data gaps due to dry periods or sensor errors; data intended for analysis and interpretation within NFM context.

## Data content
- Water level data: 9 FSA time-series at 5-minute resolution (corrected and mean sea level-adjusted).
- Stored volume: estimated 9 x FSA stored volumes at 5-minute resolution derived from depth-stored volume lookups using a DEM-based approach.
- Atmospheric pressure: combined atmospheric pressure time-series at 1–5 minute resolution.
- Data products are organized into 9 FSA files (P1–P9) and 5 atmospheric pressure files (Bruern_Baro_QC_2018–2022).
- Additional metadata: Table 3 describing variables, units, and formats; coordinates for all monitoring sites provided.

## Data collection and instrumentation
- FSAs: monitored at 8 offline FSAs and 1 online FSA (P1); sites located in Littlestock Brook south sub-catchment.
- Water level instrumentation: Level TROLL 100 data loggers in a stilling well; stage boards surveyed to 1 cm accuracy using RTK-GNSS to convert to meters above sea level (mASL).
- Atmospheric pressure instrumentation: Rugged BAROTROLL 100 sensors at Grange Farm (GF); Bruern_1, Bruern_2, and Bruern_LR data used to create continuous pressure series.
- Data cadence: water levels logged at 5-minute intervals; atmospheric pressure from sensors with 15-minute to 5-minute intervals, infilled with LR data where necessary.
- Spatial data: LiDAR-derived 1 m DEM used to model FSAs and generate depth-area-volume relationships; where LiDAR was unavailable, as-built survey data were spatially interpolated.

## Data processing and corrections
- Volume estimation: maximum static water level identified from DEMs, then depth-area-volume toolset applied to create per-FSA lookup tables; continuous water level time-series mapped to stored volumes.
- Atmospheric pressure infill: regression to estimate Bruern_Pressure from Bruern_LR data (Bruern = 1.0047144 × LR + 6.7531475); model trained 2018 H2 2019 testing period.
- Barometric correction: water level corrected using a specified formula that incorporates raw and Bruern pressures to yield corrected water levels in millimetres.
- Stage conversion: water levels converted to mASL via site-specific linear regression between TROLL readings and stage-board readings; per-FSA slope, intercept, and mASL offsets provided (Table 2).
- Data structure: nine P1–P9 QC files (P1-QC-Vol … P9-QC-Vol) with columns: Timestamp, Raw_Pressure, Bruen_Pressure, Raw_level, Corrected_level, MASL, FSA_Volume; five Bruern_Baro_QC files with: Timestamp, Bruern_Pressure, Sensor, Ob_type.
- Data quality: standard QA steps for pressure and water level data, including timestamp checks, NA handling, outlier checks, regression validation, and interpolation where appropriate.

## Data quality, validation, and limitations
- Missing data: gaps due to sensor errors or dry periods; some data infilled using regression or LR data.
- Known gap: no P6 data from July–October 2020 due to a sensor error.
- Uncertainties: estimated height error ±5 cm (relative), absolute height error ≤ ±15 cm (RMS) for the DEM-based volume estimates.
- QA processes include verification against stage-board measurements, identification of anomalies, and conservative data exclusion when confidence is low.

## Data structure and documentation
- FSA data files: 9 CSVs named P1-QC-Vol through P9-QC-Vol; each contains 7 columns as described.
- Barometric pressure files: Bruern_Baro_QC_2018–2022 with 4 columns; also includes metadata about sensor/source and observation type (Observed/Interpolated).
- Table 3 provides comprehensive definitions of all dataset variables and their units/formats.

## Usage, applications, and governance considerations
- Suitable for hydrological modelling, flood risk assessment, and evaluation of Nature-based Solution performance within the Littlestock Brook NFM scheme.
- Enables cross-site comparison through standardized QA, calibration, and correction workflows; supports transparency via documented metadata, processing steps, and uncertainty estimates.
- Data provenance and processing traceability are emphasized through sensor calibration records, regression-based corrections, and explicit metadata on data sources and interpolation status.
- Potentially useful for data strategy activities around data quality, interoperability, and governance in multi-site, cross-organisational data initiatives.

## Summary of key points for data-led decision making
- A well-documented, multi-site hydrological dataset with high temporal resolution, combining water levels, volumes, and atmospheric pressure corrections.
- Robust processing chain: from sensor data through QA, correction (barometric and stage), to volume estimation using DEM-derived depth-area-volume tables.
- Clear data gaps and uncertainties identified, with explicit remediation steps and site-specific calibration parameters.
- Rich metadata and file-level schemas enabling discoverability, reuse, and integration with broader data ecosystems for flood management and policy analysis.