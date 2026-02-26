# Durleigh Reservoir Acoustic Doppler Velocimeter Measurements

## Overview
- Metadata description for acoustic Doppler velocimeter (ADV) data collected at Durleigh Reservoir from 20/08/2018 to 24/08/2018.
- Instrument: Nortek Vector ADV used to measure near-bed water velocities (about 10 cm above the bed) near surface mixers.
- Deployment details: ADV compass calibrated prior to deployment; configured to record ENU velocities.

## Data collection and instrumentation
- Sampling mode: Burst mode — 16 seconds of data every 10 minutes, at 64 Hz.
- Location: Latitude 51.1215, Longitude -3.0396.
- Measured variable set: Near-bed velocity components and ancillary sensor data.

## Data structure and contents
- Data files:
  - .dat files: vel_xe (m/s), vel_yn (m/s), vel_zu (m/s), Amp1/2/3 (counts), snr1/2/3 (dB), corr1/2/3 (%), pres (dbar).
  - .sen files: Hour, Minute, Second, soundspeed (m/s), heading (degrees), pitch (degrees), roll (degrees), temperature (degrees C).
- Time coverage: Measurements taken over 5 days; daily files labeled day1 to day5 corresponding to 20–24 August 2018.
- File naming convention indicates day-specific datasets.

## Metadata, provenance, and citation
- Authors: Emily Slavin and Danielle Wain.
- Dataset citation: Slavin, E.I., Wain, D.J. 2018. Acoustic Doppler Velocimeter measurements from Durleigh Reservoir, August 2018.
- Data provenance: Measurements captured near the reservoir bed with standardised ENU velocity outputs and calibrated instrumentation.

## Quality, methods, and uncertainties
- Data cleaner and standard: Compass calibration prior to deployment; ENU velocity convention ensures consistency with common environmental monitoring outputs.
- Near-bed focus (10 cm above bed) and proximity to surface mixers relevant for reservoir hydrodynamics and mixing assessments.
- Burst sampling provides high temporal resolution within the 10-minute window but limited to 16-second bursts.

## Relevance for environmental monitoring
- Provides standardized near-bed flow and water property data that can be integrated into broader environmental health assessments and policy performance monitoring.
- Useful for evaluating reservoir hydrodynamics, mixing processes, and near-bottom velocity structure.
- Data structure (DAT and SEN with clear units and timestamps) supports reproducibility and cross-dataset comparisons.

## Access, storage, and usage considerations
- Datasets are organized by day and stored in pairings of .dat and .sen files.
- Proper attribution required via the provided citation; data intended for upload to appropriate data portals as part of standard monitoring data management.

## Considerations for analysts
- QA steps: verify compass calibration records, check ENU convention alignment, confirm time synchronization between .dat and .sen files.
- Data integration: combine velocity components with accompanying sound speed, temperature, and heading/pitch/roll for comprehensive hydrodynamic analyses.
- Enhancement opportunities: link with additional environmental datasets (e.g., water quality, meteorological data) to maximize dataset value beyond single-use analyses.