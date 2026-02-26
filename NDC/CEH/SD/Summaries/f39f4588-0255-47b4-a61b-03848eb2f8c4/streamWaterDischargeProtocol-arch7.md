# WD Protocol

## Aim
- Document continuous recording of river discharge at ECN sites where the entire catchment lies within the ECN site.
- Use hydrological data as sensitive indicators of environmental change, reflecting impacts on evaporation, soil moisture, runoff, and snow-related processes.

## Rationale
- Hydrological conditions respond to climate and soil-vegetation changes.
- Monitoring at sites provides insight into environmental change effects on water balance.

## Equipment Method
- Use permanently installed weirs or flumes designed per site conditions, following BS 3680.
- Data collection: Campbell Scientific CR10 data logger; optional Ott chart recorder; dip-flash device for manual stage readings.
- Structure: approach channel, measuring structure, and downstream channel; site selection emphasizes channel length, velocity distribution, slope, upstream stage effects, impermeability, flood banks, and downstream stability.
- Calibration: develop a site-specific rating curve to convert stage to discharge (m3 s-1).

## Location and Site Selection
- Consider: length and regularity of cross-section in approach channel; potential stage effects upstream of the structure; avoidance of steep channels; foundation ground permeability; flood bank capacity; downstream stability.
- Full installation details provided in BS 3680, Part 4A.

## Operation and Data Recording
- Logger records stage every 10 seconds; values averaged and stored in 5-minute periods.
- A 15-minute discharge value is derived by averaging three stage readings and applying the rating relationship.
- 15-minute values for both stage and discharge are stored for quality control and potential recalculation if the rating changes.
- Calibration performed every two years (and when weir approach conditions change) using current meters across flow ranges.
- Dip-flash datum checked every two years.
- Site staff conduct data quality control according to Appendix I.

## Data Management and Transfer
- Data downloaded to a PC fortnightly via a storage module.
- Fortnightly site procedure includes:
  - Take dip-flash reading and record times on old/new Ott charts; update chart, set clock, and align pen at correct time/stage.
  - Retrieve data from Campbell logger; verify and maintain battery and solar connections.
  - Inspect and clear debris, sediment, or ice from weir/crest; ensure cables remain free to move.
  - Maintain a duplicate copy of the logger program at the site.
  - Store Ott charts for reference.
- Data are submitted to ECNCCU; refer to accompanying Data Transfer documentation for ECN dataset formats (restricted access via Site Managers’ extranet). For access: ecnccu@ceh.ac.uk.

## Quality Control and Documentation (Appendix I)
- Verify first and last data points align with data removal times.
- Cross-check manual (dip-flash) vs. automatic stage readings at start and end.
- Compare 12:00 noon stage values on steady-flow days.
- Note missing data, freezing events, and maintenance (e.g., dredging).
- Document results, changes, and maintenance for ECN database.

## Recording Conventions and Core Data (ECN Surface Water Discharge – WD Protocol)
- Core dataset identifiers required for all records:
  - Site Identification Code (unique site code, e.g., T05)
  - Core Measurement Code (e.g., PC)
  - Location Code (e.g., 01)
  - Sampling Date/Time (date and time; includes time element when sampling is more frequent than daily)
- Automatic 15-minute interval variables recorded:
  - Site Identification Code
  - Core Measurement Code
  - Location Code
  - Recording (Sampling) date
  - Recording (Sampling) time
  - Stage (average) in meters
  - Discharge (average) in m3 s-1
  - Precision of recording: 1 minute for time; 0.001 m for stage/discharge
- Data are stored as GMT 24-hour clock values; emphasis on consistent, time-stamped, georeferenced measurements for GIS integration.