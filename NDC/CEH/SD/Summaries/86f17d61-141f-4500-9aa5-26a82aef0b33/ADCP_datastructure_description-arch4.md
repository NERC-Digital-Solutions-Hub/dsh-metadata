# Teledyne WinRiver II Software User's Guide

- This excerpt describes the Classic ASCII Output Format and the GGA NMEA data format used by WinRiver II (P/N 957-6231-00, August 2016).

## Overview of Classic ASCII Output

- When a new ASCII-out data file is opened, WinRiver II writes three header lines (A, B, C) describing notes and configuration fields such as DEPTH CELL LENGTH, NUMBER OF DEPTH CELLS, NUMBER OF PINGS PER ENSEMBLE, TIME PER ENSEMBLE, and PROFILING MODE.
- For each new data segment (ensemble), the program writes six header/leader lines containing leader, scaling, navigation, and discharge information.
- After the initial six lines, information for all bins in the current ensemble is written starting at row seven; the process then repeats for the next ensemble.
- Missing data are not inserted with placeholders; bad data values are designated with specific sentinel values (e.g., velocity = -32768; discharge = 2147483647; Latitude/Longitude = 30000).
- Ensembles are not split across files; the file grows to accommodate at least one ensemble.

## ASCII-Out File Format (Table 7) – Key Content

- Ensemble time and identifiers:
  - ENSEMBLE TIME: year, minute, second, hundredths of seconds; ENSEMBLE NUMBER (or SEGMENT NUMBER for processed/averaged data); number of ensembles in segment (if averaging/processing); PITCH and ROLL (average for the ensemble).
  - ENSEMBLE DATE: day; hour; North/South indicator; vertical orientation; BT (Bottom-Track) reference; velocity-related fields.
- Navigation and reference data:
  - Latitude and Longitude (decimal degrees); velocity references from BT, GGA, VTG, or NONE; speed/direction components (East/West, North/South, Vertical).
  - GPS/GGA-related fields include GPS altitude, geoidal separation, HDOP, satellites in use, and related timing references.
- Discharge and depth data:
  - Discharge values (top/middle/bottom estimates and measured values); start/shore discharge estimates; depth readings (river depth, depth from depth sounder); per-bin depth with corresponding beam depths.
  - Depth-related metadata such as depth cell information, reading units, and depth-related scale factors.
- Per-ensemble and per-bin specifics:
  - TOTAL ELAPSED DISTANCE, TOTAL DISTANCE TRAVELED NORTH/EAST, and TOTAL DISTANCE MADE GOOD (based on bottom-track or GPS data).
  - Per-bin velocity components (East/West, North/South, Vertical) and velocity quality/error indicators.
  - Velocity backscatter and related quality metrics (PERCENT-GOOD, etc.) and DISCHARGE values (top/middle/bottom estimates).
- Depth sounder and related fields:
  - Depth sounder readings and corresponding depth-related fields; integration between river depth, bottom track depth, and vertical beam depth.
- Notes:
  - The first two characters of the GGA header must match the device, as configured in the Peripheral Configuration Dialog (example: System Interconnections with the Depth Sounder).

## GGA - Global Positioning System Fix Data

- GGA provides time, position, and fix information for the GPS receiver.
- Format reflects standard GGA fields: UTC time, latitude, longitude, fix quality, number of satellites, HDOP, altitude, geoidal separation, and differential GPS data.
- The GGA data are used as a velocity/navigation reference alongside Bottom-Track data (BT) and other references (GGA, VTG).

## Device Interconnections and Configuration

- The first two characters in the GGA data must match the connected device, a setting defined in the Peripheral Configuration Dialog (illustrated by examples in system interconnections with the depth sounder).

## Data Governance and Leadership Takeaways

- The ASCII output embeds substantial metadata within header lines and ensemble fields, improving context for downstream data users.
- Data quality requires attention to:
  - Handling of missing data (data not sent are omitted, not replaced with placeholders).
  - Monitoring sentinel values for bad data (e.g., velocity, discharge, lat/lon).
  - Consistency of GPS vs Bottom-Track references across ensembles.
  - Dependency on device configuration for correct interpretation (e.g., GGA header matching the device).
- For effective data management, ensure:
  - Metadata and configuration details (depth cell length, number of depth cells, pings per ensemble, time per ensemble, profiling mode) are captured and cataloged.
  - Parsing pipelines account for per-ensemble and per-bin structure, and correctly handle the absence of fill values.
  - Clear provenance is maintained by linking ASCII outputs to the device configuration and GGA/GPS references used per ensemble.