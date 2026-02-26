# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) locations, elevations and proximity metrics of survey quadrats in saltmarsh and mudflat habitats

## Overview
- A geospatial dataset describing elevations and proximity metrics for survey quadrats in saltmarsh and adjacent mudflat habitats across six UK sites.
- Integrates GPS-derived positions, varied-resolution digital terrain models (5 m and 50 m), tidal height adjustments, and edge proximity metrics.

## What the dataset contains
- Quadrat-level observations: x, y (Easting, Northing; OSGB), elevationGPS, elevation5, elevation50, tidal height relative to MLWS/MHWS, and proximity metrics.
- Proximity metrics:
  - Saltmarsh: distance to creek edge (creekdist5) and distance to high water mark (HWdist5).
  - Mudflat: distance to saltmarsh edge and distance to mean high water mark (landdist5).
- Tidal context: tidal gauge reference, port-based MLWS and MHWS values, and adjustments to OD, plus tidal range and relative tidal heights.

## Study sites and sampling design
- Locations: Essex (AH, FW, TM) and Morecambe Bay (CS, WS, WP) in the UK.
- Sites chosen to represent contrasting habitats, sediment types, inundation regimes, creek structures, and vegetation.
- Each site comprises 22 quadrats on the unvegetated mudflat and 22 quadrats on the salt marsh (total per site: 44 quadrats per habitat type combination).
- Quadrat layout: 1 m² quadrats with boundaries aligned NS and EW; coordinates refer to the south-east corner of each quadrat.

## Variables and data fields (highlights)
- Spatial and location fields: row number, location (Morecambe or Essex), site, habitat (Mudflat or Saltmarsh), quadrat number, and scale category (A-D).
- Coordinates and elevations: x (Eastings), y (Northings), elevationGPS, elevation5, elevation50.
- Tidal context: tidal gauge, Diff.CD-OD, Port.MLWS, Port.MHWS, Diff.MLWS, Diff.MHWS, MLWS, MHWS, MLWS.OD, MHWS.OD, tidal.range, tidal.height.GPS, tidal.height.elev5, tidal.height.elev50.
- Proximity metrics (5 m scale): creekdist5 (saltmarsh, to creek edge), HWdist5 (saltmarsh, to high water line), landdist5 (mudflat, to land edge).
- Data units: all values in metres.

## Data sources, processing, and provenance
- Spatial and elevation data:
  - GPS quadrat positions from CBESS (OSGB coordinates).
  - Elevation data from 5 m and 50 m Digital Terrain Models (DTMs) via Edina Digimap.
  - Saltmarsh/mudflat boundary data from Environment Agency and Natural England Priority Habitats Inventory; mean high water lines from Ordnance Survey data.
- Data processing:
  - Rasterization of line shapefiles to 5 m rasters to align with DTM grid.
  - Elevations derived at quadrat locations from 5 m and 50 m DTMs.
  - Tidal heights computed by converting Admiralty MLWS/MHWS to Ordnance Datum and calculating height relative to the tide range.
  - Distances calculated using 5 m resolution rasters; saltmarsh distances use creek edge and high water line; mudflat distances use land edge.
- Software and tools:
  - R (Raster/Maptools) for extracting elevations and generating metrics.
  - PROJ4 for coordinate and datum transformations.
  - Microsoft Excel for tidal height calculations.
- Original data formats: .csv, .shp, .asc; intermediate manipulations documented.

## Data quality, procedures, and checks
- Data collection completed February 2016 (post-field campaigns).
- Documentation includes procedures for observations, calibrations (where applicable), and statistical treatment; quality control aspects noted with multiple NA entries where not applicable or not performed.
- Indicates careful linking of field data with multiple GIS-derived layers to ensure consistent spatial alignment.

## File formats and access
- Original data formats: CSV, shapefiles (.shp), ASCII grids (.asc).
- Processed outputs were produced using R and PROJ4; tidal heights calculated in Excel.
- Metadata provides clear variable definitions and field descriptions for reuse and integration.

## Relevance for Data Leaders
- Demonstrates end-to-end data integration across field collection, GIS processing, and standardization of measurements (elevations, tidal context, and proximity metrics).
- Highlights the importance of harmonizing disparate datasets (GPS, DTMs, boundary lines, tidal gauges) to create a coherent, reusable dataset with clear provenance.
- Illustrates practical challenges and solutions for data discoverability, standardization, and cross-site comparability in coastal ecological datasets.
- Provides rich metadata options (site, habitat, quadrat, scale, coordinates, derived metrics) to support data governance, lineage tracking, and potential collaborations across networks.