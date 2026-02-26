# Plot_locations_metadata.rtf

## Purpose
- Metadata for Plot_locations.csv, which holds the locations of sampling sites used in environmental monitoring.
- Supports consistent, geo-referenced records to enable scrutiny of environmental health and policy performance over time.

## Experimental design / Sampling regime
- Three transects, each 75 meters long and 20 meters apart, across a hillslope perpendicular to the river Hiraethlyn.
- Along each transect, four boreholes drilled to bedrock; some locations have a second borehole.
- Boreholes labelled as 'new' do not differ from previously labelled 'old' boreholes.

## Collection methods and instrumentation
- Coordinates captured with a handheld Garmin GPS device.

## Nature and units of recorded values
- Latitude and longitude recorded in degrees minutes seconds (DMS) and converted to decimal degrees.
- Coordinates also captured as six-figure Ordnance Survey National Grid references.

## Data structure (Plot_locations.csv)
- Consists of 8 columns:
  - Name: Site identifier
  - Latitude: Decimal degrees
  - Longitude: Decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections / Coordinate systems
- Longitude/Latitude: GCS_WGS_1984 (WKID 4326; EPSG)
- Eastings/Northings: OSGB1936 British National Grid (WKID 27700; EPSG)
- Users must ensure correct projection for display on base maps to locate sample sites accurately.

## Notes
- An image (Courtesy Welsh Government) illustrates correct locations.

## Data governance implications for the Analytics Monitoring the Environment archetype
- Provides standardised, geo-referenced data suitable for mapping, reporting, and temporal comparison.
- Facilitates data quality assurance through explicit coordinate systems and projection guidance.
- Supports data sharing and interoperability by documenting data structure and projection requirements.