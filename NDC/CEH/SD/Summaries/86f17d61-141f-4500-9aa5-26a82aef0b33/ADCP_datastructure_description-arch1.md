# Classic ASCII Output Format

- Purpose and scope
  - Describes how Teledyne WinRiver II writes data to ASCII-out files, including header setup, ensemble structure, and data field organization.

- File-level headers and notes
  - On opening a new ASCII-out data file, WinRiver II writes three header lines (A, B, C) with descriptions.
  - Users can enter notes by right-clicking Transect and selecting Add Note.

- Data segment structure
  - Whenever a new data segment (raw or averaged) is written, the first six rows contain leader, scaling, navigation, and discharge information.
  - Starting with row seven, data is written in columns based on the bin depth for the current ensemble.
  - Ensembles are not split across files; the file grows to fit at least one ensemble.
  - Missing data (data not sent from the ADCP) are not included (no dashes or fill values).
  - Bad data sentinel values:
    - Velocity: -32768
    - Discharge: 2147483647
    - Latitude/Longitude: 30000

- ASCII-Out File Format (key data groups)
  - Ensemble Time and identifiers
    - Year at ensemble start; minute, second, hundredths; ensemble number; number of ensembles in the segment (if averaging/processing).
    - Pitch and Roll for the ensemble.
  - Date and reference information
    - Day, hour, north/south, vertical (up/down), BT (bottom track) reference, velocity references (BT, GPS GGA/VTG).
  - Corrections and temperatures
    - Corrected heading, ADCP temperature for the ensemble.
  - Bottom-tracked vs GPS data
    - Bottom-track velocity (east/west) for the ensemble.
    - GPS/GGA or VTG velocity references (east and north components).
  - Navigation and distance
    - Total elapsed distance and total distance traveled north and east.
    - Total distance made good; latitude/longitude data (DMS/decimal as configured).
    - Discharge-related fields: middle and top/bottom profiles, start-shore and end-shore discharge estimates; sounder-based distances.
  - Depth and bin data
    - Depth per bin (river depth as used; includes ADCP depth and blanking).
    - Depth readings per beam (Beam 1–Beam 4) and vertical beam depth.
    - PERCENT-GOOD and velocity magnitude, plus velocity components (east, north, vertical).
  - Discharge values and references
    - Middle, top, bottom discharge values; reference sources (BT, GGA, VTG, NONE).
  - Other metadata
    - BEAMS data (velocity components for each beam), scale factors, and error fields.
  - Notes on field layout
    - Fields are separated by spaces; the exact column arrangement is defined in the table, with rows and columns corresponding to ensemble and bin data.

- GGA - Global Positioning System Fix Data
  - Purpose: Time, position, and fix-related data from a GPS receiver.
  - Format: NMEA GGA sentence
    - Example structure: Time (UTC), latitude, N/S indicator, longitude, E/W indicator, GPS quality, number of satellites, HDOP, altitude, geoidal separation, DGPS age, DGPS reference station ID.
  - Data organization
    - Provides position and fix-quality details that can be used to reference GPS-derived velocities and positions alongside ADCP data.

- GGA NMEA Format details (Table 27)
  - Field-by-field definitions for:
    - UTC time, latitude, longitude, fix quality, satellite count, HDOP, altitude, geoidal separation, DGPS age, and DGPS reference ID.
  - Representation notes
    - The values follow standard NMEA 0183 GGA formatting, with fixed-length components where applicable.

- Device alignment note
  - The first two characters of the GGA data must match your device, as configured in the Peripheral Configuration Dialog (System Interconnections with the Depth Sounder example).