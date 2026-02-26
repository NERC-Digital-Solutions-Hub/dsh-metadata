# Durleigh Reservoir Acoustic Doppler Velocimeter Measurements

- Measurements were collected with a Nortek Vector ADV to capture near-bed water velocities (about 10 cm above the bed) near surface mixers in Durleigh Reservoir.
- The ADV was compass-calibrated prior to deployment and configured to record ENU velocities.

## Instrument and Deployment Details

- Measurement mode: Burst mode, recording for 16 seconds every 10 minutes at 64 Hz.
- Locations: Latitude 51.1215, Longitude -3.0396.
- Authors: Emily Slavin and Danielle Wain.
- Suggested citation: Slavin, E.I., Wain, D.J. 2018. Acoustic Doppler Velocimeter measurements from Durleigh Reservoir, August 2018.

## Measurement Schedule and Coverage

- Timeframe: 5 consecutive days from 20 August 2018 to 24 August 2018.
- File naming corresponds to days 1–5 (day1–day5).

## Data Files and Variables

- File types: dat files and sen files.
- dat files include:
  - vel_xe (m/s), vel_yn (m/s), vel_zu (m/s) — ENU velocity components
  - Amp1, Amp2, Amp3 (counts)
  - snr1, snr2, snr3 (dB)
  - corr1, corr2, corr3 (%)
  - pres (dbar)
- sen files include:
  - Hour, Minute, Second
  - soundspeed (m/s)
  - heading (degrees)
  - pitch (degrees)
  - roll (degrees)
  - tempearture (degrees C) [note the file uses 'tempearture']

## Metadata and Usage Notes

- The dataset provides both time-stamped ancillary data and velocity measurements, enabling self-contained analysis of near-bed flow conditions.
- Users should cite the provided reference when using the data.
- Be aware of the misspelling in the temperature field name (tempearture) in the sen files when parsing metadata.