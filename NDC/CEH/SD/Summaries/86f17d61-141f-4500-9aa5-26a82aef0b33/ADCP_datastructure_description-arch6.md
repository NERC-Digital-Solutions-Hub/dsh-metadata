# Classic ASCII Output Format

- Purpose
  - Describes how WinRiver II writes ASCII-out data files, including header notes, ensemble data, and GPS fix data formatted as NMEA GGA.

- File initialization
  - On opening a new ASCII-out data file, WinRiver II writes three header lines (A, B, C) with notes and field descriptions.
  - Header A and B include user-enterable notes; Header C describes DEPTH CELL LENGTH and other initial field descriptions.

- Ensemble data structure
  - When a new data segment (ensemble) is displayed, the file gets written with:
    - The first six rows containing leader, scaling, navigation, and discharge information.
    - Starting with row seven, information is written in columns based on bin depth.
    - The file does not split ensembles across multiple files.
    - The file grows automatically to include at least one ensemble.
    - Missing data (not sent from the ADCP) are not included (no dashes or fill values).
    - Bad data values: velocity = -32768; discharge = 2147483647; Latitude/Longitude = 30000.

- Data field layout and references (Table 7)
  - Ensemble time section includes:
    - Year, minute, second, ensemble number (or segment number for processed/averaged data), number of ensembles in the segment (if averaging/processing), pitch, and roll for the ensemble.
  - Date and reference section includes:
    - Day, month, year; a reference indicator (BT for Bottom-Track or GGA for GPS); and related time/navigation fields.
  - Navigation and velocity data include:
    - GPS-derived and bottom-track velocity components, bearing, and related corrections.
  - Discharge and depth data include:
    - Measured and estimated discharge profiles, depth-related fields, and use-depth indicators.
  - Beam and depth readings:
    - Depth readings per beam and vertical depth readings, with fields arranged by bin depth.
  - Reference behavior:
    - Row three fields reference Bottom-Track if the reference is set to Bottom-Track; otherwise, they reference the GPS GGA string.
  - Note on corrections:
    - Beam depths are not corrected for Pitch and Roll.

- GGA - Global Positioning System Fix Data
  - Function: Provides time, position, and fix-related data from a GPS receiver.
  - NMEA format example: $__GGA,hhmmss.ss,llll.ll,a,yyyy.yy,a,x,xx,x.x,x.x,M,x.x,M,x.x,xxxx*hh<CR><LF>.
  - Field meanings (Table 27):
    - UTC time, latitude (degrees/minutes) and hemisphere, longitude (degrees/minutes) and hemisphere.
    - GPS Quality indicator (0-9, various fix states).
    - Number of satellites, horizontal dilution of precision (HDOP).
    - Antenna altitude above mean sea level (and units), geoidal separation (and units).
    - Age of differential GPS data, and differential reference station ID.
  - Important detail:
    - The first two characters of the GGA sentence must match your device and are configured in the Peripheral Configuration Dialog (example: with the Depth Sounder interconnection).

- Practical implications for data support
  - The ASCII-out format yields a structured, ensemble-based dataset suitable for extraction into dashboards or data products, with clear per-ensemble, per-bin organization.
  - Data quality considerations to monitor:
    - Potential gaps due to patchy data or missing ensembles.
    - Use of Bottom-Track vs GPS-based navigation data as references.
    - Beam depths not corrected for Pitch/Roll, which may affect depth-related interpretations.
  - When integrating with GPS data, align GGA-derived navigation fields with the appropriate reference (BT vs GGA) as described.