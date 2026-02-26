# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) locations, elevations and proximity metrics of survey quadrats in saltmarsh and mudflat habitats

## Overview
- Dataset of locations, elevations, and proximity metrics for survey quadrats across six UK sites (saltmarsh and adjacent mudflat habitats).
- Sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- Each site includes 22 mudflat and 22 saltmarsh quadrats, totaling 264 quadrats across all sites.
- Data were collected/assembled in February 2016 following field campaigns.

## Data Content and Key Variables
- Spatial coordinates and elevations:
  - x (Easting) and y (Northing) in metres.
  - elevationGPS (GPS-based elevation), elevation5 (5 m DTM), elevation50 (50 m DTM).
  - Tidal height calculations relative to ordinances (OD) for comparisons across gauges.
- Tidal metrics:
  - Tidal gauge (nearest Admiralty gauge).
  - Port.MLWS, Port.MHWS (Mean Low/High Water Springs at port).
  - Diff.MLWS, Diff.MHWS (adjustments between gauge and port).
  - MLWS, MHWS, MLWS.OD, MHWS.OD (tidal extremes in local vs. OD references).
  - tidal.range (MHWS.OD - MLWS.OD).
  - tidal.height.GPS, tidal.height.elev5, tidal.height.elev50 (relative tidal heights based on GPS and DTMs).
- Proximity metrics (5 m scale):
  - creekdist5 (distance to creek edge for saltmarsh quadrats).
  - HWdist5 (distance to mean high water boundary for saltmarsh).
  - landdist5 (distance to land edge for mudflat).
- Data quality and formats:
  - Original formats: .csv, .shp, .asc; processed with PROJ4 and R; tidal heights calculated in Excel.
  - Missing values indicated as NA.
  - All measurement units are metres.

## Spatial and Temporal Scope
- Six sites split between two regions:
  - Essex (AH, FW, TM) representing clay soil saltmarsh and cohesive mudflat habitats.
  - Morecambe Bay (CS, WS, WP) representing sandy soils saltmarsh and corresponding mudflat habitats.
- Sampling basis:
  - Each site includes 44 quadrats (22 mudflat, 22 saltmarsh).
- Date: field campaigns completed prior to February 2016; calculations and assembly completed in February 2016.

## Site Details and Habitat Context
- Essex sites characterized by clay soils, differing inundation frequency, creek structures, and vegetation compared with Morecambe Bay.
- Morecambe Bay sites characterized by sandy soils and different sediment dynamics.
- Quadrats oriented 1 m square, with corners aligned to cardinal directions; precise coordinates correspond to the southeast corner.

## Data Processing and Provenance
- Quadrats located via CBESS GPS readings (OSGB coordinates).
- Elevation values extracted from 5 m and 50 m OS Digital Terrain Models (DTMs) using R.
- Tidal references converted to Ordnance Datum (OD) using Admiralty standards and relevant local gauges.
- Distances to edges derived from Environment Agency GIS (saltmarsh), Natural England Priority Habitat Inventory (mudflat), and Ordnance Survey boundary data; line shapefiles rasterized to 5 m resolution to match DTM grid.
- Data management steps include translation between shapefiles and rasters, and calculation of multiple derived metrics (e.g., tidal heights, distances).

## Formats, Access, and Metadata
- File formats: CSV, SHP (shapefiles), ASC (ASCII rasters); metadata and field descriptions provided.
- Dataset field descriptions include: row number, season, location, site, habitat, quadrat, scale, x, y, elevationGPS, elevation5, elevation50, tidal gauge, port-based tide heights (MLWS/MHWS), OD-adjusted tides, tidal range, tidal height relative measures, and proximity metrics (creekdist5, HWdist5, landdist5).
- All values reported in metres; NA indicates missing measurements.

## Potential Analytical Opportunities
- Examine correlations between elevation (GPS/DTM) and tidal height metrics across habitat types.
- Assess how proximity to creeks, high water marks, and land edges relate to saltmarsh vs mudflat quadrats.
- Compare tidal adjustments and elevations between Essex (clay) and Morecambe Bay (sandy) sites to understand habitat vulnerability to inundation.
- Build predictive models of habitat suitability or risk (e.g., erosion or inundation impact) using combined elevation, tidal, and proximity variables.

## Limitations and Considerations
- Data restricted to six sites surveyed in 2016; spatial and temporal generalizability may be limited.
- Some variables rely on external GIS sources; accuracy depends on the underlying shapefiles and DTMs.
- Missing values present in certain fields; users should review NA entries for analyses.