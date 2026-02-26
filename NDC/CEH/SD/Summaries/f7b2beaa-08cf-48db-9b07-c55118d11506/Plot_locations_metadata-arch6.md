# Plot_locations_metadata.rtf

- Purpose: Metadata for Plot_locations.csv, which contains the geographic locations of sampling sites used in the study.

- Experimental design: 
  - Three transects, each 75 m long and 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes extend to bedrock; some locations include a second borehole.
  - Boreholes labeled 'new' do not differ from those labeled 'old'.

- Collection methods and instrumentation:
  - Coordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values:
  - Latitude and Longitude recorded in degrees, minutes, and seconds and converted to decimal degrees.
  - Coordinates also captured as six-figure Ordnance Survey National Grid references.

- Data structure (Plot_locations.csv):
  - Columns: Name, Latitude, Longitude, Date, Time, Easting, Northing, ODN.
  - Date: Date of measurement.
  - Time: Time of measurement in Greenwich Mean Time (GMT).
  - Easting/Northing: British National Grid coordinates.
  - ODN: Elevation in metres above Ordnance Datum Newlyn.

- Projections and base-map considerations:
  - Longitude/Latitude use GCS_WGS_1984 (WKID 4326; EPSG).
  - Eastings/Northings use OSGB1936 British National Grid (WKID 27700; EPSG).
  - Users must ensure the correct projection is used for display and analysis to plot sites accurately.

- Additional notes:
  - An image (Courtesy Welsh Government) accompanying the metadata illustrates correct locations.