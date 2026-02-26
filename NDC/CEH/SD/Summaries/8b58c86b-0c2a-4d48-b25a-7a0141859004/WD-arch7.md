# WD Protocol

## Aim
- Continuous recording of river discharge at ECN sites where the entire catchment lies within the ECN site.
- Monitor hydrological response to environmental change (climate, vegetation, soil) via changes in water balance, evaporation, soil moisture, runoff.
- Snow-related precipitation changes may be particularly informative; discharge data serve as a sensitive indicator of environmental change.

## Rationale
- Hydrological conditions at a site reflect climate and soil/vegetation structure.
- Tracking changes in site hydrology helps detect environmental change impacts.

## Equipment Method
- Use a permanently installed weir or flume (BS 3680) matched to site conditions.
- Data collected by a Campbell Scientific CR10 logger; supplemented by an Ott chart recorder where possible.
- A dip-flash device facilitates manual stage readings.

## Location
- Complete installation includes approach channel, measuring structure, and downstream channel.
- Site selection considerations:
  - Adequate length of regular cross-section in the approach channel
  - Regular velocity distribution across the cross-section
  - Avoidance of steep channels if possible
  - Upstream effects from the structure on water levels
  - Impermeable ground for foundation
  - Flood banks capable of containing maximum discharge
  - Stability of the downstream channel
- Full details in BS 3680, Part 4A.

## Operation
- Logger records stage every 10 seconds; values averaged and stored in 5-minute periods.
- A 15-minute discharge value is calculated by averaging three stage values and converting via a rating relationship.
- Both 15-minute stage and discharge are stored for quality control and potential re-calculation if the rating changes.
- A site-specific rating curve converts stage to discharge (m^3 s^-1).
- Calibration (rating curve) with current meters across full flow range every two years; additional recalibration if approach conditions change.
- Dip-flash datum checked every two years.
- Data quality control performed by site staff after initial training (see Appendix I).

## Data Transfer and Recording Conventions
- Data downloaded to a PC fortnightly via a storage module.
- Fortnightly site visit steps:
  - Take dip-flash reading
  - Record time and stage on old/new Ott chart; update chart and time
  - Retrieve data from Campbell logger
  - Check battery voltage; address power if needed
  - Inspect weir approach/crest for debris, sediment, ice; clear safely
  - Duplicate logger program recommended; Ott charts stored for reference
- Calibration/datum and chart handling follow documented protocols.
- Site-specific data transfer documentation and restricted ECN data formats are available via ECNCCU extranet; contact ecnccu@ceh.ac.uk for access.

## Core Measurement and Data Variables (WD Protocol)
- Core measurement: surface water discharge
- Variables recorded automatically at 15-minute intervals:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Recording (Sampling) date
  - Recording (Sampling) time
  - Stage (average) in meters
  - Discharge (average) in m^3 s^-1 (GMT 24-h clock)
- Precision: 0.001 for both stage and discharge

## Quality Control (Appendix I)
- Checks to document data integrity and maintenance:
  - First and last data points align with data removal times
  - Compare manual (dip-flash) and automatic stage readings at start/finish
  - Compare 12:00 noon stage values on steady-flow days
  - Note any missing data or ice-related gaps
  - Record results of all checks, changes, and maintenance (e.g., dredging) for ECN database

## Standards and References
- BS 3680, Method of measurement of liquid flow in open channels, Part 4A (weirs and flumes)
- Authors: R.C. Johnson and T.P. Burt; British Standards Institution, 1965

## GIS-Relevance for This Protocol
- Produces standardized, high-frequency time-series of surface water discharge suitable for GIS-based hydrological mapping and change detection.
- Facilitates data integration across ECN sites with consistent metadata (site, measurement code, location, timestamp, stage, discharge).
- Supports transparent quality control and documentation for reproducible map-based analyses and decision-making.