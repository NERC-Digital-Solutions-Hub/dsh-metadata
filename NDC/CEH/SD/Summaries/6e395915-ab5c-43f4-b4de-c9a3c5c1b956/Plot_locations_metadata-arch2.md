# Plot_locations_metadata.rtf

- Purpose: Metadata for Plot_locations.csv, which holds the locations of sampling sites and supports the environmental monitoring design.

## Experimental design
- Three transects, each 75 m long, 20 m apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect: four boreholes drilled to bedrock at locations shown in Plot_locations.csv.
- Some locations have a second borehole (labelled 'new'); these do not differ from the 'old' boreholes.

## Collection methods
- Coordinates collected with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude originally collected in degrees, minutes, seconds; converted to decimal degrees.
- Coordinates also captured as six-figure Ordnance Survey National Grid references.

## Data structure
- Plot_locations.csv provides sampling site locations and consists of 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Coordinate systems and projections
- Ensure correct projection for display:
  - Longitude/latitude: GCS_WGS_1984 (WKID 4326, EPSG)
  - Eastings/Northings: OSGB1936 British National Grid (WKID 27700, EPSG)

## Practical notes
- An image (courtesy Welsh Government) illustrates correct locations.
- Users should verify projection alignment with base maps to display sample sites accurately.

## Relevance to environmental monitoring
- Provides standardized geospatial reference for site locations, enabling mapping, spatial analyses, and integration with other environmental datasets for monitoring and policy performance assessment.