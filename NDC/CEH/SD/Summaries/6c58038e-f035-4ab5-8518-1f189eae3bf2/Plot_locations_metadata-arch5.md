# Plot_locations_metadata.rtf

- Purpose: Metadata for Plot_locations.csv, which holds the locations of sampling sites used in the study.

- Experimental design and sampling regime:
  - Three transects, each 75 m long, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
  - On each transect, four boreholes drilled to bedrock; some locations have a second borehole labeled 'new' (not different from 'old').

- Collection methods and instrumentation:
  - Coordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values:
  - Latitude and longitude initially in degrees, minutes, seconds; converted to decimal degrees.
  - Coordinates also recorded as six-figure Ordnance Survey National Grid references.

- Details of data structure (Plot_locations.csv):
  - 8 columns:
    - Name: Site identifier
    - Latitude: Decimal degrees
    - Longitude: Decimal degrees
    - Date: Date of measurement
    - Time: Time of measurement (Greenwich Mean Time)
    - Easting: British National Grid Easting
    - Northing: British National Grid Northing
    - ODN: Elevation in metres above Ordnance Datum Newlyn

- Projections and base maps:
  - Longitude/Latitude use GCS_WGS_1984 (WKID 4326, EPSG).
  - Eastings/Northings use OSGB1936 British National Grid (WKID 27700, EPSG).
  - Ensure base maps and display projections match these coordinate systems to show accurate locations.

- Key notes for data stewardship:
  - Verify correct projection and base map alignment to display sites accurately.
  - Maintain consistent naming and units across metadata and data files.
  - Be aware of potential need to update coordinates or borehole classifications ('new' vs 'old') and reflect updates in metadata.
  - The accompanying image (not included) illustrates correct locations; rely on the specified projections when visualizing.