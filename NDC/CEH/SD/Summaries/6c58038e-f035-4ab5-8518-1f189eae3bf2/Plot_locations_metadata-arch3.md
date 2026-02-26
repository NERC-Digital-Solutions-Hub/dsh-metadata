# Plot_locations_metadata.rtf

- Overview
  - Metadata for Plot_locations.csv, which holds the locations of sampling sites.

- Experimental design and sampling regime
  - Three 75 m long transects, 20 m apart, across a hillslope and perpendicular to the river Hiraethlyn.
  - Along each transect, four boreholes drilled to bedrock; some locations have a second borehole labeled 'new' (distinct from 'old' but not functionally different).

- Collection methods and instrumentation
  - Coordinates collected with a handheld Garmin GPS device.

- Nature and units of recorded values
  - Latitude and longitude recorded in decimal degrees (converted from degrees, minutes, seconds).
  - Also recorded as six-figure Ordnance Survey National Grid references.

- Data structure
  - Plot_locations.csv comprises 8 columns:
    - Name: Site identifier
    - Latitude: Latitude in decimal degrees
    - Longitude: Longitude in decimal degrees
    - Date: Date of measurement
    - Time: Time of measurement (GMT)
    - Easting: British National Grid Easting
    - Northing: British National Grid Northing
    - ODN: Elevation in metres above Ordnance Datum Newlyn

- Projections, transformations, and display
  - For longitude/latitude values: GCS_WGS_1984 (WKID 4326, EPSG).
  - For eastings/northings: OSGB1936 British National Grid (WKID 27700, EPSG).
  - Correct projection must be used for display; base map must match the projection to display sample sites accurately.

- Additional notes
  - Image courtesy Welsh Government; location visualization referenced but not included in the text.

- Implications for monitoring frameworks (relevance to Authors of Monitoring Frameworks)
  - Facilitates data quality and interoperability through clear site locations, coordinate systems, timestamps (GMT), and data structure.
  - Supports data governance and reproducibility by specifying projections and data fields, reducing ambiguities across datasets.
  - Highlights practical considerations for data sharing and metadata completeness to enable reuse across monitoring initiatives.