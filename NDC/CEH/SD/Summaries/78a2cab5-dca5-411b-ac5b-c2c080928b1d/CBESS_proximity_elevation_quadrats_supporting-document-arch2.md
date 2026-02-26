# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) locations, elevations and proximity metrics of survey quadrats in saltmarsh and mudflat habitats

## Overview
- Dataset of elevations and proximity metrics for CBESS survey quadrats in six UK sites ( Essex and Morecambe Bay ) across saltmarsh and mudflat habitats.
- Each site includes 22 quadrats on the un-vegetated mudflat and 22 quadrats on the salt marsh (1 m square, oriented North-South and East-West).
- Records were calculated in February 2016 after field campaigns.
- Data are provided in common GIS/tabular formats to support standardised environmental monitoring and cross-site comparisons.

## Locations and sampling design
- Sites and locations:
  - Essex: Abbotts Hall (AH) - 51.7833 N, -0.8667 E; Fingringhoe Wick (FW) - 51.8167 N, -0.9667 E; Tillingham Marshes (TM) - 51.6833 N, -0.9333 E.
  - Morecambe Bay: Cartmel Sands (CS) - 54.1667 N, -3.0000 W; Warton Sands (WS) - 54.1333 N, -2.8000 W; West Plain (WP) - 54.1500 N, -2.9667 W.
- Habitat types per site: Saltmarsh and Mudflat.
- Quadrat arrangement: 1 m x 1 m, grid of 22 per habitat per site; quadrat locations indicate the south-east corner.

## Data sources and measurements
- Elevation data:
  - GPS-derived elevations from CBESS_gps_quadrats.csv (OSGB coordinates).
  - Elevations from Ordnance Survey 5 m and 50 m Digital Terrain Model (DTM) rasters (Edina Digimap).
- Tidal context:
  - Tidal height relative to Mean High Water Springs (MHWS) and Mean Low Water Springs (MLWS) using relevant Admiralty Standard Ports data.
- Boundaries and edge metrics:
  - Saltmarsh boundary data from Environment Agency GIS shapefiles; high water line from Ordnance Survey Boundary Line.
  - Mudflat boundary data from Natural England Priority Habitat Inventory and Ordnance Survey Boundary Line.
- Proximity metrics (computed at 5 m scale):
  - Saltmarsh: distance to creek edge (creekdist5) and distance to high water mark (HWdist5).
  - Mudflat: distance to saltmarsh edge and mean high water mark (landdist5).
- Derivations:
  - Distances rasterized from shapefiles (5 m resolution) and reprojected to OS DTM grid.
  - Tidal measurements converted to Ordnance Datum (OD); tidal height computed as GPS/elevation5/elevation50 relative to MLWS to MHWS.

## Variables and data structure
- Core fields (all in metres unless stated):
  - x, y: Easting and Northing (OSGB).
  - elevationGPS: GPS reference elevation (m).
  - elevation5, elevation50: elevations from 5 m and 50 m DTM (m).
  - Tidal gauge: nearest Admiralty tide gauge.
  - Diff.CD-OD: difference between chart datum and Ordnance Datum (m).
  - Port.MLWS, Port.MHWS: mean low/high water springs at nearest Admiralty port (m).
  - Diff.MLWS, Diff.MHWS: adjustments from port to tide gauge (m).
  - MLWS, MHWS: MLWS and MHWS elevations at tide gauge (m).
  - MLWS.OD, MHWS.OD: MLWS/MHWS adjusted to Ordnance Datum (m).
  - tidal.range: MHWS.OD - MLWS.OD (m).
  - tidal.height.GPS, tidal.height.elev5, tidal.height.elev50: relative tidal heights using GPS/elevations (m).
  - creekdist5: distance to creek edge (saltmarsh) (m).
  - HWdist5: distance to mean high water line (saltmarsh) (m).
  - landdist5: distance to land edge (mudflat) (m).
- Additional metadata fields describe row order, season, location, site, habitat, Quadrat, and scale categories.

## Processing, quality and formats
- Data processing:
  - Shapefiles converted to 5 m resolution rasters; elevations extracted from OS DTM; tidal heights calculated relative to MLWS/MHWS.
  - Calculations performed in R; tidal heights derived from OSGB and OD references.
  - Original data stored as .csv, .shp, and .asc; PROJ4 used for coordinate and datum transformations; tidal heights sometimes calculated in Excel.
- Documentation and quality:
  - The dataset includes sections for procedures, calibration, statistical treatment, and data checking, though specific details are marked as NA in this description.
  - Missing values indicate measurements not performed (NA).
- Intended use and accessibility:
  - Data are suited for standardised monitoring and cross-site analysis.
  - Formats support integration with GIS and statistical workflows, enabling assembly with other environmental datasets.

## Personnel
- Staff responsible for the dataset: Thomas P. Adams, Michael T. Burrows.

## Notes for users
- The dataset provides a reproducible framework for linking precise quadrat elevations with tidal context and proximity to habitat edges, enabling analyses of habitat condition, sediment dynamics, and ecosystem service potential across contrasting UK saltmarsh and mudflat environments.
- When combining with other data, the standardized coordinate system, datum conversions, and proximity metrics facilitate cross-site and temporal comparisons.