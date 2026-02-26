# WD Protocol

## Overview
- Purpose: Continuous recording of river discharge at ECN sites where the entire catchment lies within the ECN site.
- Rationale: Hydrological conditions reflect environmental change; monitoring water balance, evaporation, soil moisture, and runoff can indicate climate or soil-vegetation system changes, with particular attention to snow where relevant.

## Equipment & Setup
- Measurement device: Permanently installed weir or flume designed per conditions ( BS 3680, Part 4A).
- Recording hardware: Campbell Scientific CR10 data logger; analogue Ott chart recorder as supplement; dip-flash device for manual readings.
- Data handling: Data downloaded to a PC fortnightly via a storage module.
- Site components: Approach channel, measuring structure, downstream channel; consideration of channel length, velocity distribution, upstream effects, ground permeability, flood banks, and downstream stability.

## Site Selection & Location
- Ensure adequate regular cross-section length and regular velocity distribution.
- Avoid steep channels when possible.
- Consider upstream level effects, ground impermeability, flood bank containment, and downstream stability.
- Full installation details outlined in BS 3680, Part 4A.

## Operation & Recording
- Sampling cadence: Stage recorded every 10 seconds, averaged and stored over 5-minute periods.
- Discharge estimation: 15-minute discharge values derived from stage via a rating curve; both stage and discharge stored for QC and potential re-calculation if rating changes.
- Calibration: Develop rating curve to convert stage to discharge (m3 s-1); calibrate with current meters across full flow range; re-calibrate every two years or if weir conditions change.
- Datum checks: Dip-flash datum checked every two years.
- Data quality control: Site staff perform QC per Appendix I after initial training.

## Calibration & Quality Control
- Calibration protocol: Site-specific procedures; rating relationship adjustments as needed.
- QC procedures (Appendix I): 
  - Verify first and last data points align with data removal times.
  - Compare manual dip-flash and automatic stage readings at start/finish.
  - Compare 12:00 stage values on days with steady flow.
  - Document missing data and potential freezing of weir.
  - Record maintenance activities (e.g., dredging) for ECN database.

## Data Management & Documentation
- Data transfer: Fortnightly download from logger; manual steps include updating charts, verifying voltages, device checks, and debris removal without safety compromise.
- Data provenance: Duplicate logger program recommended; Ott charts archived for future reference.
- Standards: Reference to BS 3680; data formats documented in restricted ECN site extranet; contact ECNCCU for access.

## Data Specification & Recording Conventions
- Core measurement: Surface water discharge (WD Protocol).
- Required dataset fields (first 4): 
  - Site Identification Code (unique ECN site code)
  - Core Measurement Code (e.g., WD)
  - Location Code (replicate sampling locations)
  - Sampling Date/Time (including time element for frequent sampling)
- Recorded variables at 15-minute intervals:
  - Stage (average) in meters
  - Discharge (average) in cubic meters per second (cumecs)
  - Precision: 0.001 m for stage; 0.001 (units) for discharge
  - Time reference: GMT 24-hour clock
- Data formatting: Follow ECN dataset formats as per Data Transfer documentation; stored with metadata in the ECNCCU system.