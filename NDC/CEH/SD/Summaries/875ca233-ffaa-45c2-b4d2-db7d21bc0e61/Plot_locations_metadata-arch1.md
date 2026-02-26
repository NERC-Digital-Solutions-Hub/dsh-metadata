# Plot_locations_metadata.rtf

- Purpose
  - Metadata for Plot_locations.csv, which holds the locations of sampling sites for the study.

- Experimental design / Sampling regime
  - Three transects, each 75 meters long and 20 meters apart, across a hillslope perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes drilled to bedrock at locations listed in Plot_locations.csv.
  - Some locations have a second borehole; boreholes labeled 'new' do not differ from 'old'.

- Collection methods and instrumentation
  - Coordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values
  - Latitude and Longitude captured in degrees, minutes, and seconds, converted to decimal degrees.
  - Coordinates also recorded as six-figure Ordnance Survey National Grid references (OSGB36).

- Data structure (Plot_locations.csv)
  - Contains 8 columns:
    - Name: Site identifier
    - Latitude: Decimal degrees
    - Longitude: Decimal degrees
    - Date: Date of measurement
    - Time: Time of measurement (GMT)
    - Easting: British National Grid Easting
    - Northing: British National Grid Northing
    - ODN: Elevation in metres above Ordnance Datum Newlyn

- Projections / coordinate systems
  - Ensure base map uses correct projection to display sample sites accurately.
  - Longitude/Latitude: GCS_WGS_1984 (WKID 4326; EPSG)
  - Eastings/Northings: OSGB1936 British National Grid (WKID 27700; EPSG)

- Additional notes
  - An image courtesy of Welsh Government illustrates the correct locations.