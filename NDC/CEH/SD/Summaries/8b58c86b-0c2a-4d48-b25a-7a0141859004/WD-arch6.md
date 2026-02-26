# WD Protocol

## Aim
- Surface water discharge: continuous recording of river discharge at ECN sites where the entire catchment lies within the ECN site.
- Use as a sensitive indicator of environmental change through hydrological responses to climate, vegetation, soil properties, and snow.

## Rationale
- Hydrological conditions respond to external climate and internal soil/vegetation structure changes.
- Monitoring provides insight into evaporation, soil moisture, and runoff changes; snow-affected sites may show pronounced climate-change signals.

## Equipment Method
- Recording of river stage using a permanently installed weir or flume (design per site, BS 3680 guidance).
- Data logged by a Campbell Scientific CR10 logger; supplemented by an analogue Ott chart recorder where possible.
- A dip-flash device installed for manual stage readings.

## Location
- Complete installation: approach channel, measuring structure, downstream channel.
- Site selection considerations:
  - Adequate length and regular cross-section of approach channel.
  - Regular velocity distribution across cross-section.
  - Prefer non-steep channels; manage upstream water elevations due to structure.
  - Impermeable foundations; flood banks to contain maximum discharge.
  - Downstream channel stability.
- Full details described in BS 3680, Part 4A.

## Operation
- Logger records stage every 10 seconds; values averaged and stored over 5-minute periods.
- 15-minute discharge value calculated by averaging three stage-derived discharges via a rating relationship.
- Both 15-minute stage and discharge stored for quality control and potential recalculation if the rating changes.
- A rating curve is developed to convert stage to discharge (m3 s-1).
- Calibration: rating relationship developed using current meters across full flow range; repeated every two years or if conditions change; site-specific calibration protocol.
- Dip-flash datum checked every two years.
- Data quality control conducted by site staff after training (per Appendix I).
- Reference: BS 3680 (British Standards Institution, 1965).

## Data Handling and Transfer
- Data downloaded to a PC fortnightly via a storage module.
- Fortnightly site visit steps:
  - Take dip-flash reading.
  - Note time and stage on old/new Ott chart; update charts and clock; set pen to correct time/stage.
  - Retrieve data from Campbell logger; check battery/voltage; address power or solar panel issues; avoid removing the old battery without temporary external power.
  - Inspect weir approach/crest for debris, sediment, or ice; clear safely if possible.
  - Duplicate logger program should be kept on-site; Ott charts stored for reference.

## Appendix I. Quality control of surface water discharge data
- Checks include:
  - Consistency of first/last data points with removal times.
  - Consistency between manual (dip-flash) and automatic readings at start/end.
  - Comparison of 12:00 stage values on steady-flow days.
  - Documentation of missing data or frozen weirs; notes on maintenance (e.g., dredging).

## Specification of results and recording conventions
- Core dataset identifiers (required for ECN dataset formats):
  - Site Identification Code (unique to ECN site)
  - Core Measurement Code (e.g., WD)
  - Location Code (replicate sampling points per site)
  - Recording Date/Time (date and time; time element if more frequent than daily)
- Core measurement: surface water discharge (WD Protocol)
- Variables recorded at 15-minute intervals:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Recording (Sampling) date
  - Recording (Sampling) time
  - Stage (average) in meters
  - Discharge (average) in cubic meters per second (cumecs)
  - Precision: 1 minute; values to 0.001 for stage and discharge