# Durleigh Reservoir Acoustic Doppler Velocimeter Measurements

- Purpose and scope
  - Metadata for acoustic Doppler velocimeter (ADV) measurements at Durleigh Reservoir
  - Near-bed water velocities (10 cm above bed) near reservoir surface mixers
  - ENU velocity frame; data collected to inform hydrodynamics and reservoir monitoring

- Instrumentation and deployment
  - Instrument: Nortek Vector ADV
  - Compass calibrated prior to deployment; ENU velocity recording
  - Burst mode: 16 seconds of data every 10 minutes
  - Sampling frequency: 64 Hz
  - Deployment location provided by geographic coordinates: Lat 51.1215, Lon -3.0396

- Authors and citation
  - Authors: Emily Slavin and Danielle Wain
  - Please cite: Slavin, E.I., Wain, D.J. 2018. Acoustic Doppler Velocimeter measurements from Durleigh Reservoir, August 2018.

- Timeline and dataset scope
  - Measurements conducted over 5 days: August 20–24, 2018
  - Day labels correspond to days 1–5 (21 Aug is day 2, etc.)
  - Data organized into dat and sen files

- Data content and structure
  - dat files include:
    - vel_xe (m/s), vel_yn (m/s), vel_zu (m/s) – velocity components
    - Amp1, Amp2, Amp3 (counts) – amplitude metrics
    - snr1, snr2, snr3 (dB) – signal-to-noise ratios
    - corr1, corr2, corr3 (%) – correlation/quality indicators
    - pres (dbar) – pressure
  - sen (metadata) files include:
    - Hour, Minute, Second – timestamp components
    - soundspeed (m/s)
    - heading (degrees), pitch (degrees), roll (degrees)
    - tempearture (degrees C) [note: typographical variation present in source]
  - Overall data provide near-bed velocity time series alongside orientation, environmental and sensor metadata

- Data quality, provenance, and governance
  - Contains quality indicators (snr, corr) and calibration details (compass)
  - Metadata present for sensor configuration, location, and timing
  - Some metadata hyphenation/typo issues noted (e.g., tempearture), which may require careful validation
  - Data published with explicit file structure (dat and sen) for transparency and reproducibility

- Relevance for monitoring and evaluation
  - Example of targeted near-bed flow monitoring to support reservoir hydrodynamics assessments
  - Illustrates practical data management needs: metadata completeness, data formats, data quality checks, and provenance
  - Demonstrates a high-frequency data collection design (64 Hz, burst sampling) integrated with time-lapse sampling cadence
  - Useful for dashboards, reports, and policy-relevant evaluations of reservoir mixing and flow conditions across multi-day campaigns