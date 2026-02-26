# Plot_locations_metadata.rtf

- Purpose: Metadata for Plot_locations.csv, which holds the locations of sampling sites.

- Experimental design and sampling regime:
  - Three 75 m long transects, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes drilled to bedrock; some locations have a second borehole.
  - Boreholes labeled 'new' do not differ from those labeled 'old'.

- Collection methods and instrumentation:
  - Coordinates collected using a handheld Garmin GPS device.

- Nature and units of recorded values:
  - Latitude and longitude collected in decimal degrees (converted from degrees, minutes, seconds).
  - Coordinates also recorded as six-figure Ordnance Survey National Grid references.

- Data structure (Plot_locations.csv):
  - Consists of 8 columns: Name, Latitude, Longitude, Date, Time, Easting, Northing, ODN (elevation in metres above Ordnance Datum Newlyn).

- Projections and display considerations:
  - Users must ensure the correct projection is used and the base map is in the correct projection to display sample sites accurately.
  - Longitude/Latitude: GCS_WGS_1984 (WKID: 4326, EPSG).
  - Eastings/Northings: OSGB1936 British National Grid (WKID: 27700, EPSG).

- Additional notes:
  - An image courtesy of Welsh Government illustrates the correct locations. Time values are recorded in Greenwich Mean Time.