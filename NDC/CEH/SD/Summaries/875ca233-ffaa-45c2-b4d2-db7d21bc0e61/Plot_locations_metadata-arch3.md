# Plot_locations_metadata.rtf

- Purpose
  - Metadata file for Plot_locations.csv, which contains sampling site locations and associated contextual data.

- Experimental design / Sampling regime
  - Three transects, each 75 m long, spaced 20 m apart.
  - Transects run across a hillslope and perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes drilled to bedrock at locations specified in Plot_locations.csv.
  - Some locations have a second borehole labeled 'new' that do not differ from 'old'.

- Collection methods and instrumentation
  - Coordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values
  - Latitude and Longitude recorded in degrees, minutes, seconds, then converted to decimal degrees.
  - Coordinates also recorded as six-figure Ordnance Survey National Grid references.

- Details of data structure
  - Plot_locations.csv provides locations of sampling sites.
  - 8 columns:
    - Name: Site identifier
    - Latitude: Decimal degrees
    - Longitude: Decimal degrees
    - Date: Date of measurement
    - Time: Time of measurement (GMT)
    - Easting: British National Grid Easting
    - Northing: British National Grid Northing
    - ODN: Elevation in metres above Ordnance Datum Newlyn

- Projections and basemap considerations
  - Longitude/Latitude values use GCS_WGS_1984 (WKID 4326, EPSG).
  - Eastings/Northings use OSGB1936 British National Grid (WKID 27700, EPSG).
  - Users should ensure the correct projection is used and the base map aligns with the projection to display sites accurately.
  - An image (courtesy Welsh Government) illustrates correct locations. 

- Implications for monitoring frameworks
  - Provides spatially explicit site data essential for mapping, trend analysis, and policy evaluation.
  - Clear metadata on coordinate systems supports data governance, interoperability, and transparent sharing.
  - Documentation of sampling design aids reproducibility and assessment of coverage within hillslope-river context.