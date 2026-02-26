# WD Protocol

## Aim
- Continuous recording of river discharge at ECN sites where the entire catchment area is within the ECN site.

## Rationale
- Environmental change is expected to alter hydrological conditions (evaporation, soil moisture, runoff).
- Climate change, including snow components, may have pronounced effects.
- Monitoring hydrological variables provides a sensitive indicator of environmental change.

## Equipment Method
- Use a permanently installed weir or flume to measure river stage, designed per BS 3680 (Part 4A).
- Data logged by a Campbell Scientific CR10 logger; supplemented by an Ott analog chart recorder where possible.
- A dip-flash device is installed for manual stage readings.

## Location
- The installation includes an approach channel, measuring structure, and downstream channel.
- Site selection criteria emphasize:
  - Adequate length and regular cross-section of the approach channel
  - Regular velocity distribution across the cross-section
  - Preference to avoid steep channels
  - Upstream water level effects, foundation impermeability, need for flood banks
  - Downstream channel stability
- Full details described in BS 3680, Part 4A.

## Operation
- Logger records stage every 10 seconds; values averaged and stored in 5-minute periods.
- 15-minute discharge values calculated from the 15-minute average stage via a rating curve.
- 15-minute stage and discharge stored for quality control and potential re-calculation if the rating changes.
- A rating curve is developed to convert stage to discharge (m3 s-1).
- Calibration via current meters across full flow range; re-calibration every two years or if weir/approach conditions change.
- Dip-flash datum checked every two years.
- Site staff perform data quality control following Appendix I.
- Each site maintains its own calibration protocol.
- A duplicate logger program should be kept on-site; Ott charts stored for reference.

## Procedure (Data Handling and Site Checks)
- Fortnightly data download to PC via a storage module.
- Fortnightly site visit steps include:
  - Take dip-flash reading; note times and stage on charts; update charts as needed.
  - Retrieve data from Campbell logger; check battery voltage; inspect solar panel if present; replace battery if necessary using temporary external power to preserve software.
  - Inspect weir approach and crest for debris, sediment, or ice; clear safely if possible.
  - Check for ice in stilling well and break up if present; ensure cables can move freely.
- Maintain a duplicate logger program on-site.
- Store Ott charts for potential future reference.

## Appendix I. Quality control of surface water discharge data
- Checks include:
  - First and last data points match removal times from the logger.
  - Compare manual (dip-flash) and automatic stage readings at start and end.
  - Compare 12:00 noon stage values on steady-flow days.
  - Note any missing data or times when the weir could be frozen.
  - Document all checks, changes, and maintenance (e.g., dredging) for ECN database.

## Specification of results and recording conventions
- Core measurement: surface water discharge (WD Protocol).
- Automatically recorded at 15-minute intervals:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Recording (Sampling) date
  - Recording (Sampling) time
  - Stage (average) in meters
  - Discharge (average) in cubic meters per second (cumecs)
  - Precision: recording time to 1 minute
- Data formats referenced to ECN dataset formats (ECNCCU Data Transfer documentation; restricted access Site Managers' extranet).
- Example core fields:
  - Site Identification Code, Core Measurement Code, Location Code, Sampling Date/Time, Stage (average), Discharge (average)
- Units and time conventions:
  - Stage: meters (m)
  - Discharge: cubic meters per second (m3 s-1)
  - Time: GMT 24-hour clock
  - Precision: 0.001 for both stage and discharge values at 1-minute precision.