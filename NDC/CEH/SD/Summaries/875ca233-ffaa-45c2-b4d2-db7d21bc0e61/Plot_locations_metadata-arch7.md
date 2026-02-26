# Plot_locations_metadata.rtf

- This metadata document describes the corresponding Plot_locations.csv, which holds the locations of sampling sites used in the study.

## Experimental design and sampling regime
- Three transects, each 75 meters long and spaced 20 meters apart.
- Transects run across a hillslope, perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes were installed to bedrock at locations listed in Plot_locations.csv.
- Some locations include a second borehole labeled as 'new'; these do not differ from the 'old' boreholes.

## Collection methods and instrumentation
- Coordinates were collected using a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude captured in degrees, minutes, and seconds, then converted to decimal degrees.
- Coordinates also recorded as six-figure Ordnance Survey National Grid references.

## Data structure
- Plot_locations.csv provides the locations of sampling sites.
- Contains 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (Greenwich Mean Time)
  - Easting: British National Grid Easting (OSGB)
  - Northing: British National Grid Northing (OSGB)
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate systems and projection notes
- For longitude/latitude values: GCS_WGS_1984 (WKID 4326, EPSG)
- For Eastings/Northings: OSGB1936 British National Grid (WKID 27700, EPSG)
- Users must ensure the correct projection is applied and that the base map uses the same projection to display sample sites accurately.

## Usage considerations
- The accompanying image (credited to the Welsh Government) illustrates the correct locations.
- The dataset supports GIS analyses and map-based visualisations of sampling-site locations, with attention to consistent projections across data layers.