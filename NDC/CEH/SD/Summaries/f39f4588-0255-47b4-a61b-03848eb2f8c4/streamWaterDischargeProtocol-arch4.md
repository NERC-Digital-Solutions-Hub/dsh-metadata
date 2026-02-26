# WD Protocol

## Overview
- Purpose: Continuous recording of river discharge at ECN sites where the entire catchment lies within the ECN site.
- Rationale: Environmental change affects hydrological conditions; monitoring discharge serves as a sensitive indicator of changes in water balance, evaporation, soil moisture, and runoff, with particular emphasis on climate-change effects in snow-dominated areas.

## Equipment and Method
- Measurement device: Permanently installed weir or flume designed per BS 3680 (BSI 1965), using a Campbell Scientific CR10 data logger; optionally supplemented by an analogue Ott chart recorder and a dip-flash manual readout.
- Installation components: Approach channel, measuring structure, and downstream channel; site selection should consider channel length, velocity distribution, slope, upstream effects, soil impermeability, flood banks, and downstream stability.
- Calibration: Develop a site-specific rating curve to convert stage to discharge (m3/s); calibrate with current meters across the full flow range every two years, or if approach conditions change; dip-flash datum checked every two years.
- Documentation: Maintain a duplicate logger program at the site; store Ott charts for reference.

## Operation and Data Handling
- Recording cadence: Stage recorded every 10 seconds; data averaged and stored in 5-minute blocks; 15-minute discharge values calculated from staged-based discharge using the rating curve.
- Data storage: 15-minute values for both stage and discharge stored for quality control and potential re-calculation if rating changes.
- Data download: Fortnightly transfer to a PC via a storage module; procedures include reading/readout, updating charts, checking battery/solar power, debris removal, and ensuring cables can move freely.
- Maintenance: Regular checks of weir approach/crest for debris, sediment, or ice; ensure no safety compromises; keep duplicate software and charts as reference.

## Quality Control and Data Integrity
- Appendix I QC checks: verify first/last data points align with removal times; compare dip-flash and automatic stage readings on steady-flow days; log missing data and potential ice/freeze events; document all maintenance activities for ECN database.
- Data specification and formats: ECN Site Data must include standardized identifiers and timestamps; core measurement WD (surface water discharge) is recorded at 15-minute intervals with:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Recording (Sampling) date
  - Recording (Sampling) time
  - Stage (average) in meters
  - Discharge (average) in cubic meters per second
  - Precision: 1 minute timestamps; 0.001 m and 0.001 m3/s precision

## Data Management and Access
- Data submission: Data are downloaded and submitted to the ECN Central Custody and Control Unit (ECNCCU); refer to accompanying Data Transfer documentation for ECN dataset formats (restricted access Site Managers' extranet).
- Contact for access: ecnccu@ceh.ac.uk

## Context and Standards
- Governing standard: BS 3680, Part 4A – Weirs and Flumes (Thin plate weirs and venturi flumes) for measurement of liquid flow in open channels.
- Document authors: R.C. Johnson and T.P. Burt; British Standards Institution, 1965.

## Key Takeaways for Data Leaders
- Establish standardized, long-term data collection with calibrated, site-specific rating curves to ensure comparability across sites and time.
- Implement rigorous metadata, including site, core measurement, location codes, and precise timestamps, to ensure discoverability and interoperability.
- Maintain regular quality control procedures and documentation to support data reliability, reproducibility, and traceability.
- Centralize data transfer and storage protocols to enable consistent access for analysis and decision-making across networks.