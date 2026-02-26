# Classic ASCII Output Format

- When WinRiver II opens a new ASCII-out data file, it writes three header lines:
  - A, Description notes (NOTE 1)
  - B, Description notes (NOTE 2)
  - C, Description of DEPTH CELL LENGTH and related fields (e.g., ADCP depth, configuration details)
- For each new data segment (ensemble), the program writes:
  - The first six rows: leader, scaling, navigation, and discharge information
  - Starting from row seven: data organized by bin depth; all bins in the current ensemble are written, then the next ensemble begins
  - Fields within a line are separated by one or more spaces
  - Ensembles are not split across files; the file grows to include at least one ensemble
- Missing data:
  - Data not sent from the ADCP are omitted (no dashes or fill values)
  - Bad data sentinel values include velocity = -32768; discharge = 2147483647; Latitude/Longitude = 30000
- Layout and content (Table 7 – ASCII-Out File Format):
  - Ensemble header information includes:
    - ENSEMBLE TIME (year, month, day, hour, minute, second, hundredths)
    - ENSEMBLE NUMBER, number of ensembles in segment, PITCH, ROLL
    - Reference time fields and navigation indicators (BT/GPS references)
    - GPS or BT velocity data and related bearing/heading information
    - Temperature, corrected heading, and other ensemble-wide measurements
  - Bin-level data per ensemble include:
    - DEPTH, depth cell information, and velocity components (east, north, vertical)
    - Beam 1–4 data, velocity magnitude, velocity direction, and velocity error
    - Discharge values (measured, estimated, and related metrics)
    - Depth-related notes for follow-on cells (sounding, depth readings, etc.)
  - Navigation and distance data:
    - TOTAL ELAPSED DISTANCE and TOTAL ELAPSED TIME
    - Distances traveled north/east and distance made good
    - Latitude and Longitude references (GGA or VTG) for current velocity references
  - Discharge data sections:
    - Middle, top, and start-shore discharge estimates and related depth information
- Data interpretation notes:
  - Beam depths are not corrected for Pitch and Roll
  - Reference to Bottom-Track vs GPS (GGA) affects how certain fields are interpreted in row three
- Units:
  - VELOCITY: cm/s (or ft/s, depending on settings)
  - DEPTH: meters (or feet, depending on settings)
  - Other measurements may be in meters, feet, or other configured units

- Additional note:
  - The first two characters of the GGA data must match the device and are configured in the Peripheral Configuration Dialog (System Interconnections with the Depth Sounder example)

## GGA - Global Positioning System Fix Data

- Purpose: Time, position, and fix-related data for a GPS receiver
- NMEA format example:
  - $__GGA,hhmmss.ss,llll.ll,a,yyyy.yy,a,x,xx,x.x,x.x,M,x.x,M,x.x,xxxx*hh<CR><LF>
- Fields (general):
  - 1: UTC time of position
  - 2: Latitude (ddmm.mmmm)
  - 3: Latitude hemisphere (N/S)
  - 4: Longitude (dddmm.mmmm)
  - 5: Longitude hemisphere (E/W)
  - 6: GPS quality indicator (0-9)
  - 7: Number of satellites in use
  - 8: Horizontal dilution of precision (HDOP)
  - 9: Antenna altitude above mean sea level, units indicated
  10: Altitude units (M)
  - 11: Geoidal separation
  - 12: Geoidal separation units (M)
  - 13: Age of differential GPS data (seconds)
  - 14: Differential reference station ID
- Note:
  - The first two characters must match your device and are set in the Peripheral Configuration Dialog (see system example)