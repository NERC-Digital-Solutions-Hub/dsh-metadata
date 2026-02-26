# Plot_locations_metadata.rtf

- What this file is
  - Metadata for Plot_locations.csv, which holds the locations of sampling sites.

- Experimental design
  - Three 75 m long transects, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes installed to bedrock; some locations have a second borehole labelled 'new'.
  - 'New' boreholes do not differ from 'old'.

- Collection methods
  - Coordinates collected with a handheld Garmin GPS device.
  - Latitude and longitude recorded in degrees, minutes, seconds and converted to decimal degrees.
  - Also recorded as six-figure Ordnance Survey National Grid references.

- Nature and units of recorded values
  - Latitude and Longitude: decimal degrees (converted from DMS).
  - Easting and Northing: British National Grid coordinates.

- Data structure (Plot_locations.csv)
  - Columns (8 total): Name, Latitude, Longitude, Date, Time, Easting, Northing, ODN.
  - Descriptions:
    - Name: Site identifier
    - Latitude: decimal degrees
    - Longitude: decimal degrees
    - Date: date of measurement
    - Time: time of measurement (GMT)
    - Easting: British National Grid Easting
    - Northing: British National Grid Northing
    - ODN: Elevation in metres above Ordnance Datum Newlyn

- Projections and map display notes
  - Longitude/Latitude use GCS_WGS_1984 (WKID: 4326, EPSG).
  - Eastings/Northings use OSGB1936 – British National Grid (WKID: 27700, EPSG).
  - Ensure the base map projection matches to display sample sites accurately.

- Additional notes
  - An image courtesy of Welsh Government illustrates the correct locations.