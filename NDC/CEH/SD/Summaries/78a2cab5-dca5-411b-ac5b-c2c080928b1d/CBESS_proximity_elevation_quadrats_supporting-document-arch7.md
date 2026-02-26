# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) locations, elevations and proximity metrics of survey quadrats in saltmarsh and mudflat habitats

## Overview
- GIS-focused dataset detailing elevations, proximity metrics, and locations of CBESS survey quadrats in six UK coastal sites (saltmarsh and adjacent mudflat habitats).
- Combines GPS positions, terrain model elevations, tidal height calculations, and distance to habitat/edge features for each quadrat.

## Spatial scope and sampling design
- Six sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- At each site: 22 quadrats on un-vegetated mudflat and 22 quadrats on salt marsh (total per site: 44 quadrats; total across all sites: 264 quadrats).
- Quadrat footprint: 1 m x 1 m, oriented north–south and east–west; coordinates indicate the south-east corner of each quadrat.

## Data content and key variables
- Spatial coordinates:
  - x (easting) and y (northing) in metres (OSGB).
- Elevations:
  - elevationGPS (GPS-derived elevation at quadrat).
  - elevation5 (5 m resolution DTM).
  - elevation50 (50 m resolution DTM).
  - Tidal height at quadrat relative to MLWS/MHWS (tidal.height.GPS, tidal.height.elevation5, tidal.height.elevation50).
- Tidal and port datums:
  - Tidal gauge (nearest Admiralty gauge).
  - Diff.CD-OD (datum difference; CD to Ordnance Datum).
  - Port.MLWS and Port.MHWS (mean low/high water springs at port).
  - Diff.MLWS and Diff.MHWS (adjustments at tide gauge relative to port).
  - MLWS, MHWS; MLWS.OD, MHWS.OD (MLWS/MHWS to Ordnance Datum).
  - tidal.range (MHWS.OD – MLWS.OD).
- Edge and proximity metrics (per habitat type, 5 m raster scale):
  - Saltmarsh: creekdist5 (distance to creek edge), HWdist5 (distance to mean high water line).
  - Mudflat: landdist5 (distance to land edge).
- Additional derived fields:
  - tidal.height.GPS Relative, tidal.height.elev5 Relative, tidal.height.elev50 Relative (relative tidal heights to range).
- Data quality indicators:
  - NA entries indicate measurements not performed in some cases.

## Data sources and processing workflow
- Quadrat locations: CBESS_gps_quadrats.csv (GPS coordinates and elevation).
- Terrain elevations: OSGB raster Digital Terrain Model data at 5 m and 50 m resolutions (from Edina Digimap); elevations extracted at quadrat points.
- Tidal datums: Admiralty standard ports and relevant tidal gauges; Mean Low Water Springs and Mean High Water Springs converted to Ordnance Datum.
- Boundary and edge data:
  - Saltmarsh boundary: Environment Agency GIS shapefiles.
  - Mudflat extent: Natural England Priority Habitat Inventory shapefiles.
  - High Water line: Ordnance Survey Boundary Line data.
  - Land edge: Ordnance Survey Vector Map data.
- Processing steps:
  - Shapefiles converted to 5 m rasters to align with OS DTM grid (using R).
  - Distances to edges computed in raster/vector space (5 m scale).
  - Elevations extracted at quadrat locations from 5 m and 50 m DTMs; tide heights computed from MLWS/MHWS adjustments.
  - Tidal heights expressed in metres relative to a common datum (OD).
- Tools referenced:
  - R (Raster/Maptools packages), PROJ4, Microsoft Excel (for tidal height calculations).
- Original data formats: .csv, .shp, .asc; data manipulation and calculations performed in PROJ4/R; tidal heights calculated in Excel.

## Site descriptions and sampling rationale
- Essex sites (AH, FW, TM) and Morecambe Bay sites (CS, WS, WP) chosen to represent contrasting habitats and sediment types (clay vs. sandy; inundation regimes; creek structures and vegetation).
- Saltmarsh quadrats represent two soil types and habitat conditions; mudflat quadrats represent cohesive clays/mud/silt (Essex) or coarse, mobile sediments (Morecambe).

## Temporal scope
- Records and calculations completed in February 2016, after field sampling campaigns.

## Staff and dataset provenance
- Staff responsible: Thomas P. Adams, Michael T. Burrows.
- Data provenance and field methods (calibration, QC, and measurement procedures) are described, with some sections marked NA where not applicable or not provided.

## Data quality, limitations, and usage notes
- Some NA values indicate measurements not performed or unavailable for certain quadrats or variables.
- Data are designed for GIS analyses and map-based visualisation; users should reference the coordinate system (OSGB) and datum conversions (to Ordnance Datum) when integrating with other datasets.