# Plot_locations_metadata.rtf

## Overview
- Metadata for Plot_locations.csv, which holds the locations of sampling sites used in three 75 m transects across a hillslope, perpendicular to the River Hiraethlyn.
- Boreholes were installed along each transect (four per transect; some locations have a second borehole labelled 'new' that does not differ from 'old').

## Experimental design and sampling regime
- Three transects, 75 m long, 20 m apart, across the hillslope.
- Boreholes drilled to bedrock at locations indicated in Plot_locations.csv; some locations have an additional borehole labeled 'new'.

## Collection methods and instrumentation
- Coordinates collected with a handheld Garmin GPS device.
- Data include latitude/longitude and British National Grid coordinates derived from the measurements.

## Nature and units of recorded values
- Latitude and Longitude recorded in decimal degrees (converted from degrees, minutes, seconds).
- Also provided as six-figure Ordnance Survey National Grid references (Easting/Northing).

## Data structure and file contents
- Plot_locations.csv contains 8 columns:
  - Name: Site identifier
  - Latitude: Latitude in decimal degrees
  - Longitude: Longitude in decimal degrees
  - Date: Date of measurement
  - Time: Time of measurement (GMT)
  - Easting: British National Grid Easting
  - Northing: British National Grid Northing
  - ODN: Elevation in metres above Ordnance Datum Newlyn

## Projections and display notes
- For longitude/latitude values: GCS_WGS_1984 (WKID 4326, EPSG:4326).
- For Easting/Northing values: OSGB1936 British National Grid (WKID 27700, EPSG:27700).
- Users must ensure the correct projection is used and that the base map is in the appropriate projection to display sample sites correctly.
- An image (Courtesy Welsh Government) is noted as illustrating the correct locations.

## Data governance and quality considerations for Data Stewards
- Ensure metadata completeness and accuracy, including clear column descriptions and coordinate reference systems.
- Preserve the distinction between 'old' and 'new' boreholes while acknowledging that 'new' boreholes do not differ in attributes from 'old'.
- Verify consistency between decimal degree coordinates and Easting/Northing values (cross-checks between CRSs).
- Manage data updates, including addition of new boreholes, and maintain an audit trail of changes.
- Support interoperability across systems by adhering to standard coordinate formats and unit definitions.
- Document collection methods, data provenance, and any assumptions (e.g., time zone, measurement date formats).