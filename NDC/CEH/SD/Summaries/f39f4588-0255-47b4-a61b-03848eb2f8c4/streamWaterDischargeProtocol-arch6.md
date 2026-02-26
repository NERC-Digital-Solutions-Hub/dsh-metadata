# WD Protocol

## Aim
- Establish continuous recording of river discharge at ECN sites where the entire catchment lies within the ECN site.
- Monitor hydrological responses to environmental change, informing on water balance, evaporation, soil moisture, runoff, and snow-related effects.

## Rationale
- Hydrological conditions respond to climate and soil/vegetation changes; surface water discharge data serve as sensitive indicators of environmental change.

## Equipment and Method
- Weir or flume with design per site, following BS 3680 (BSI 1965).
- Data logging: Campbell Scientific CR10 logger; optional analogue Ott chart recorder.
- Dip-flash device for manual stage readings.
- Rating curve to convert stage to discharge (m³ s⁻¹).
- Site components: approach channel, measuring structure, downstream channel; site conditions influence accuracy.
- Calibration: develop rating curves via current meters across flow ranges; recalibrate every two years or if approach conditions change.
- Dip-flash datum checked every two years; data quality control by site staff per Appendix I.

## Location and Site Considerations
- Site selection should consider:
  - Adequate length of regular cross-section channel.
  - Regular velocity distribution across the approach channel cross-section.
  - Preference to avoid steep channels.
  - Upstream water level effects due to the structure.
  - Ground impermeability for foundation.
  - Flood banks to contain maximum discharge.
  - Stability of the downstream channel.
- Full details described in BS 3680, Part 4A.

## Operation and Data Capture
- Logger records stage every 10 seconds; values averaged and stored in 5-minute blocks.
- 15-minute discharge values calculated from three 5-minute stage readings using the rating curve; both 15-minute stage and discharge are stored for quality control and potential re-calculation if the rating changes.
- Calibration protocol developed per site; site staff perform quality control and data checks.

## Calibration and Quality Control
- Rating curve developed from full-range condition measurements; recalibrations every two years or when weir conditions change.
- Appendix I details quality control steps and data checks.
- Regular QA checks include verification of first/last data points, cross-checks between manual and automatic stage readings, midday comparisons during steady flow, notes on missing data or ice/dredging events, and maintenance records.

## Data Recording Conventions and Formats
- Core measurement: surface water discharge (WD Protocol).
- Variables recorded automatically at 15-minute intervals:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Recording date
  - Recording time
  - Stage (average)
  - Discharge (average) in m and m³ s⁻¹ (cumecs)
- Data format reference: ECN dataset formats (restricted access) available via the ECN Site Managers' extranet; contact ecnccu@ceh.ac.uk for access.
- First four keys identify data: Site Identification Code, Core Measurement Code, Location Code, Sampling Date/Time.

## Data Transfer and Access
- Data downloaded to a PC at fortnightly intervals via a storage module.
- Fortnightly site visit steps include:
  - Take dip-flash reading and note time/stage on old/new charts.
  - Update charts and synchronize clock; ensure logger is set correctly.
  - Retrieve data from Campbell logger and verify battery/solar power.
  - Inspect weir approach/crest for debris, ice, or sediment; clear if safe.
  - Confirm cables can move freely; keep a duplicate logger program at site.
  - Store Ott charts for reference.
- Data transfer documentation and ECN dataset format specifications are provided in accompanying documentation; access restricted to ECNCCU.

## Appendix I: Quality Control checklist
- Verify agreement of first/last data points with removal times.
- Compare manual (dip-flash) and automatic stage readings at start/end.
- Compare 12:00 noon stage values on steady-flow days.
- Note missing data, potential ice conditions, and maintenance actions (e.g., dredging).
- Record results of all checks and changes for ECN database.

## Practical Data Management Notes
- Core data include 15-minute interval records of stage and discharge with precise time stamps.
- Outputs enable self-service analysis and integration into broader datasets, with attention to data quality and re-use through proper documentation and data formatting.