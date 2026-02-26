# Durleigh Reservoir Acoustic Doppler Velocimeter Measurements

- Overview
  - Metadata file for acoustic Doppler velocimeter (ADV) data collected at Durleigh Reservoir in August 2018.
  - Instrument: Nortek Vector ADV measuring near-bed water velocities (10 cm above bed) near surface mixers.
  - Coordinate system: ENU velocities; compass calibrated prior to deployment.
  - Measurement mode: burst mode, 16-second samples every 10 minutes, at 64 Hz.
  - Authors: Emily Slavin and Danielle Wain. Please cite as: Slavin, E.I., Wain, D.J. 2018.

- Location and timing
  - Location: Latitude 51.1215, Longitude -3.0396.
  - Measurements conducted over 5 days (days 1–5, corresponding to Aug 20–24, 2018).

- Data structure and contents
  - File types: dat files and sen files (data and sensor metadata).
  - dat files include:
    - vel_xe (m/s), vel_yn (m/s), vel_zu (m/s)
    - Amp1, Amp2, Amp3 (counts)
    - snr1, snr2, snr3 (dB)
    - corr1, corr2, corr3 (%)
    - pres (dbar)
  - sen files include:
    - Hour, Minute, Second
    - soundspeed (m/s)
    - heading (degrees), pitch (degrees), roll (degrees)
    - tempearture (degrees C) [note: spelling in file; intended as temperature]

- Data collection details
  - ENU velocity measurements with a calibrated compass.
  - Near-bed measurement height: 10 cm above bed.
  - Data cadence: 16-second bursts every 10 minutes, at 64 Hz sampling.

- Provenance and usage notes
  - Data are organized by day with file names corresponding to day1–day5.
  - Measurements provide velocity components, acoustic backscatter indicators (Amp, SNR, CORR), and environmental context (pressure, sound speed, orientation, and temperature).

- Implications for data governance
  - Clear authorship and citation guidance support proper attribution.
  - Well-defined variables and units facilitate reuse and integration into broader data systems.
  - Location, time, and calibration details enhance traceability and quality assessment.