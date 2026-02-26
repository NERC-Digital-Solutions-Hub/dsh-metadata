# Plot_locations_metadata.rtf

- Purpose: Metadata for Plot_locations.csv, which holds the locations of sampling sites along three transects across a hillslope near the river Hiraethlyn. Some locations have an additional borehole labelled 'new' that does not differ from 'old'.

- Experimental design and sampling regime:
  - Three 75 m long transects, 20 m apart, perpendicular to the river.
  - Along each transect, four boreholes drilled to bedrock; some sites have a second borehole.

- Collection methods and instrumentation:
  - Co-ordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values:
  - Latitude and Longitude recorded in degrees, minutes, seconds and converted to decimal degrees.
  - Co-ordinates also provided as six-figure Ordnance Survey National Grid references.
  - Time recorded in Greenwich Mean Time (GMT).

- Details of data structure (Plot_locations.csv):
  - Eight columns:
    - Name: Site identifier
    - Latitude: Latitude in decimal degrees
    - Longitude: Longitude in decimal degrees
    - Date: Date of measurement
    - Time: Time of measurement (GMT)
    - Easting: British National Grid Easting
    - Northing: British National Grid Northing
    - ODN: Elevation in metres above Ordnance Datum Newlyn

- Projections and display considerations:
  - For longitude/latitude values, use GCS_WGS_1984 (WKID 4326, EPSG).
  - For Eastings/Northings, use OSGB1936 British National Grid (WKID 27700, EPSG).
  - Users should ensure the correct projection is used and the base map is in the correct projection to display sample sites accurately.

- Visual aid:
  - An image (Courtesy Welsh Government) is noted as illustrating correct locations.