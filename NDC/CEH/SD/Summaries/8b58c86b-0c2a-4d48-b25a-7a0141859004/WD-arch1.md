# WD Protocol

## Aim
- Continuously record river discharge at ECN sites where the full catchment lies within the ECN site.
- Monitor hydrological response to environmental change; changes in climate, vegetation, or soil affect evaporation, soil moisture, and runoff, with snow-related effects being particularly important in some sites.

## Equipment Method
- Use a permanently installed weir or flume designed per site, following BS 3680.
- Data collected by a Campbell Scientific CR10 logger; supplemented by an analogue Ott chart recorder.
- A dip-flash device installed to facilitate manual stage readings.

## Location
- The installation comprises: approach channel, measuring structure, and downstream channel.
- Site selection considerations:
  - Adequate length of regular cross-section in the channel.
  - Regular velocity distribution across the approach channel cross-section.
  - Prefer avoiding steep channels.
  - Consider effects of upstream water level increases due to the structure.
  - Impermeable foundations; flood banks capable of containing maximum discharge.
  - Stability of the downstream channel.
- Full details described in BS 3680, Part 4A.

## Operation
- The logger records stage every 10 seconds; data are averaged and stored over five-minute periods.
- A 15-minute discharge value is derived by averaging three stage readings and converting to discharge using a rating relationship.
- Both 15-minute stage and discharge values are stored for quality control and potential re-calculation if the rating changes.
- A rating curve is developed to convert stage to discharge (m3 s-1).
- Calibration with current meters over the full range of flow conditions; calibration every two years, and whenever weir approach conditions change.
- Dip-flash datum checked every two years.
- Data quality control performed by site staff following Appendix I procedures.

## Authors Reference
- R.C. Johnson and T.P. Burt
- British Standards Institution. 1965. BS 3680. Methods of measurement of liquid flow in open channels. Part 4A. Thin plate weirs and venturi flumes.

## Procedure
- Fortnightly data downloads to a PC via a storage module.
- Site visit steps:
  1. Take dip-flash reading.
  2. Note time and stage on old and new Ott chart; update charts as needed.
  3. Retrieve data from Campbell logger and verify battery voltage; address power issues if necessary.
  4. Inspect weir approach/crest and clear debris if safe.
  5. Check for ice in the stilling well and ensure cables can move freely.
- A duplicate copy of the logger program should be kept on site.
- Ott charts stored for reference.

## Appendix I. Quality control of surface water discharge data
- Checks for data integrity and continuity:
  - First and last data points align with data removal times.
  - Compare manual dip-flash and automatic stage readings at start and end.
  - Compare 12:00 stage values on steady-flow days.
  - Note any missing data or times when the weir could be frozen.
  - Document results of all checks, changes, and maintenance for ECN database.

## Specification of results and recording conventions
- Core measurements for each WD sampling location are recorded at 15-minute intervals.
- Essential identifying fields required for all datasets:
  - Site Identification Code (e.g., T05)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling date/time (including time element when sampling is more frequent than daily)
- Recorded variables at 15-minute intervals:
  - Stage (average) in meters
  - Discharge (average) in m3 s-1 (cumecs)
- Data precision:
  - Time precision: 1 minute
  - Values: 0.001 m for stage and 0.001 m3 s-1 for discharge
- Data transfer and formats are specified in ECN dataset documentation (restricted access via Site Managers' extranet); contact ecnccu@ceh.ac.uk for access.