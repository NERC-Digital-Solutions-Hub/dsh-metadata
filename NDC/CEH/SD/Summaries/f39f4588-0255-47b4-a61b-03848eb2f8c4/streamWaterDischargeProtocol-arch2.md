# WD Protocol

## Aim
- Continuous recording of surface water discharge at ECN sites where the entire catchment lies within the ECN site, to monitor hydrological responses to environmental change.

## Rationale
- Water balance influenced by climate, vegetation, and soil; changes in external climate or soil-vegetation structure affect evaporation, soil moisture, and runoff, making hydrological data a sensitive indicator of environmental change, especially where snow affects precipitation.

## Equipment and Method
- Permanent weir or flume designed per site (BS 3680, Part 4A) with a rating curve to convert stage to discharge.
- Recording instruments: Campbell Scientific CR10 logger plus an analogue Ott chart recorder; dip-flash device for manual stage readings.
- Site components: approach channel, measuring structure, downstream channel; installation quality affects measurement accuracy.

## Location and Site Considerations
- Site selection criteria focus on channel length and cross-section regularity, velocity distribution, avoiding steep or unstable upstream conditions, ground impermeability, flood bank capacity, and downstream stability.
- Full details in BS 3680, Part 4A.

## Operation and Data Handling
- Logger records stage every 10 seconds; data averaged and stored on 5-minute intervals; 15-minute average discharge calculated from the stage-to-discharge rating.
- Rating curve calibration using current meters over the full flow range; calibration every two years or if conditions change; dip-flash datum checked biennially.
- Data quality controlled by site staff per Appendix I.
- Data download to PC every fortnight; workflow includes dip-flash reading, syncing times, retrieving data, checking/charging batteries, clearing debris, ensuring cables move freely; duplicate logger program recommended; Ott charts archived.

## References and Standards
- British Standards Institution. BS 3680. Methods of measurement of liquid flow in open channels. Part 4A. Weirs and flumes (1965).

## Appendix I: Quality Control
- Verify alignment of first/last data points with data removal times.
- Cross-check manual and automatic stage readings at start/end and on steady days.
- Note missing data and conditions (e.g., ice).
- Record maintenance and changes for ECN database.

## Data Specification and Recording Conventions
- Core dataset identifiers required for each recording: Site Identification Code, Core Measurement Code, Location Code, Recording date/time.
- Core measurement: surface water discharge (WD Protocol).
- Variables recorded automatically at 15-minute intervals: site ID, core measurement code, location code, recording date, recording time, stage (average), discharge (average) in cubic meters per second (cumecs); precision 0.001; time in GMT 24-h clock.
- Datasets submitted to ECNCCU using the specified data transfer documentation; access to documentation available via ecnccu@ceh.ac.uk.