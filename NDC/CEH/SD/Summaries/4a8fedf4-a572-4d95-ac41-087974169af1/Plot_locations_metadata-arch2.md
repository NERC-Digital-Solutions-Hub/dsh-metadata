# Plot_locations_metadata.rtf

## Purpose
- Metadata describing Plot_locations.csv, which holds sampling-site locations for environmental monitoring.

## Experimental design / Sampling regime
- Three transects, each 75 m long, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole.
- Boreholes labeled "new" do not differ from those labeled "old."

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and Longitude recorded in decimal degrees (converted from degrees, minutes, seconds).
- Coordinates also provided as six-figure Ordnance Survey National Grid references.

## Data structure
- Plot_locations.csv contains 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (UTC)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and display guidance
- Ensure correct projection alignment when displaying sample sites:
  - Longitude/Latitude: GCS_WGS_1984 (WKID 4326, EPSG)
  - Easting/Northing: OSGB1936 British National Grid (WKID 27700, EPSG)

## Elevation reference
- ODN denotes elevation in metres above Ordnance Datum Newlyn.

## Additional notes
- An image (Courtesy Welsh Government) accompanies the metadata to illustrate correct locations.
- The metadata emphasizes proper projection usage to ensure accurate site visualization.