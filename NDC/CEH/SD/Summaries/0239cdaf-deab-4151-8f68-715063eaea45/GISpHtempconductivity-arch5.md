# Standard operating procedure for pH meters and EC/TDS/Temperature Testers NERC project NE/N019555/1

- This document describes the operation of two instruments used in the NERC study:
  - pH meter HI 98127
  - EC/TDS/Temperature tester HI 98311
- It also notes how GPS coordinates of downstream river water samples are recorded and referenced.

## Equipment and measurement capabilities

- pH meter (HI 98127)
  - pH range: -2.0 to 16.0; accuracy ±0.1 pH
  - Temperature range: -5.0 to 60.0°C (23.0 to 140.0°F)
- EC/TDS/Temperature tester (HI 98311)
  - Conductivity (EC) range: 0–3999 µS/cm; accuracy ±2% F.S.
  - Total dissolved solids (TDS) range: 0–2000 ppm; accuracy ±2% F.S.
  - Temperature range: 0.0–60.0°C (32.0–140.0°F); accuracy ±0.5°C/±1°F

## Geographical coordinates and sample tagging

- GPS coordinates of sample points recorded with Garmin GPS (Model etrex 10)
- Coordinates stored as GIS northing/easting in degrees and minutes and as latitude/longitude

## Data collection procedures

- Turning on the instrument and verifying battery
  - Hold MODE (HI 98127 or HI 98311) until the LCD lights up
  - Battery life shown as a percentage (e.g., %100 BATT)

- Taking measurements (pH)
  - Submerge electrode in sample and stir gently
  - Wait for stability symbol to disappear before recording
  - Primary LCD displays pH with automatic temperature compensation; secondary LCD shows sample temperature

- Freezing the display (pH)
  - In measurement mode, press SET/HOLD to freeze; HOLD appears on the secondary display
  - Press any button to resume normal mode

- Taking measurements (EC/TDS)
  - Submerge probe in sample
  - Use plastic beakers to minimize electromagnetic interference
  - Select EC or TDS mode with SET/HOLD
  - Wait for stability symbol to disappear; primary LCD shows temperature-compensated EC or TDS, secondary shows sample temperature

- Freezing the display (EC/TDS)
  - Press SET/HOLD for 2–3 seconds until HOLD appears on the secondary display
  - Press any button to return to normal measuring mode

## Safety and maintenance

- Handle the electrode glass bulb with care to avoid electrostatic discharge
- After use, rinse electrode with water; store with storage solution in the protective cap
- Do not store with distilled or deionized water
- If the electrode is dry, soak in storage solution for at least one hour to reactivate

## Documentation and references

- Reference manuals:
  - HI 98127 pH meter instruction manual
  - HI 98311 EC/TDS/Temperature tester instruction manual

## Data management considerations for Data Stewards

- Ensure alignment of measurements with device specifications and documented units (pH, EC in µS/cm, TDS in ppm, temperatures in °C/°F)
- Capture and retain GPS coordinates alongside sample measurements for traceability
- Maintain metadata about instrument models, measurement conditions, and temperature compensation
- Consider logging calibration events and measurement timestamps to support data quality and provenance
- Record any data processing steps (e.g., stabilization criteria, HOLD captures) to preserve data integrity
- Monitor storage and maintenance practices for electrodes to avoid data contamination or biased results
- Acknowledge potential gaps not covered by the SOP (e.g., explicit calibration procedures, measurement uncertainty reporting) and consider integrating these into a data governance plan