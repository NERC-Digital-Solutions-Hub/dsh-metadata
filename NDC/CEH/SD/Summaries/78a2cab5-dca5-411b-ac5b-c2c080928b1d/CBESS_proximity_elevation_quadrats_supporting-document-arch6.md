# Dataset name, Details = Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) locations, elevations and proximity metrics of survey quadrats in saltmarsh and mudflat habitats

## Overview
- Describes observed and calculated elevations and proximity metrics for survey quadrats across saltmarsh and mudflat habitats.
- Designed to support analysis of coastal biodiversity and ecosystem services by enabling elevation, tidal, and distance-to-edge calculations at fine spatial scales.

## Sampling design and sites
- Six UK sites: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain).
- At each site: 22 un-vegetated mudflat quadrats and 22 saltmarsh quadrats (44 per site; total 264 quadrats).
- Quadrats are 1 m x 1 m, oriented north-south and east-west; quadrat locations derived from CBESS GPS data.

## Data collection and sources
- GPS locations and elevations from CBESS_gps_quadrats.csv (OSGB coordinates).
- Elevation data from raster Digital Terrain Models (DTM) at 5 m and 50 m resolution (Edina Digimap).
- Tidal heights referenced to Admiralty standards (Mean Low Water Springs and Mean High Water Springs) and converted to Ordnance Datum.
- Saltmarsh: distances to creek edge and high water mark derived from Environment Agency GIS shapefiles and OS boundary data.
- Mudflat: distance to saltmarsh edge and mean high water mark derived from Natural England Priority Habitat Inventory mudflat data and OS boundary data.
- Shapefiles converted to rasters at 5 m resolution for distance calculations.

## Computation and data transformations
- Elevations computed for each quadrat using GPS, 5 m and 50 m DTMs.
- Tidal heights calculated relative to MLWS and MHWS and converted to Ordnance Datum.
- Distances calculated at 5 m resolution: creekdist5 (saltmarsh), HWdist5 (saltmarsh), landdist5 (mudflat).
- Distances and tidal metrics standardized to port references (Port.MLWS, Port.MHWS) and diffs (Diff.MLWS, Diff.MHWS) with OD adjustments (MLWS.OD, MHWS.OD).
- Tidal range and relative tidal height metrics computed (tidal.range, tidal.height.GPS, tidal.height.elevation5, tidal.height.elevation50).

## Variables and formats
- Core spatial/observational fields: x (eastings), y (northings), elevationGPS, elevation5, elevation50.
- Tidal fields: Tidal gauge, Diff.CD-OD, Port.MLWS, Port.MHWS, Diff.MLWS, Diff.MHWS, MLWS, MHWS, MLWS.OD, MHWS.OD, tidal.range, tidal.height.GPS, tidal.height.elevation5, tidal.height.elevation50.
- Distance fields: creekdist5 (saltmarsh), HWdist5 (saltmarsh), landdist5 (mudflat).
- Metadata: Row number, Season (Winter/Summer), Location (Morecambe/Essex), Site (CS, WS, WP, AH, FW, TM), Quadrat (1–22), Scale (A-D corresponding to 1 m, 1–10 m, 10–100 m, 100 m+).
- All distance and elevation values are in metres.
- Original data formats: .csv, .shp, .asc; data manipulated with PROJ4 and R; tidal heights calculated in Microsoft Excel.
- NA entries indicate measurements not performed.

## Data quality and notes
- Some fields marked NA where data were not collected.
- Clear documentation of coordinate systems (OSGB) and datum conversions to ensure interoperability and comparability with other coastal datasets.

## Access and usage considerations for data support
- Suitable for creating self-serve analyses on elevation, proximity to edge features, and tidal influence across saltmarsh and mudflat habitats.
- Can be integrated with additional environmental or biodiversity data to examine habitat suitability, erosion risk, or ecosystem service provision.
- The dataset’s structured fields and explicit unit conventions facilitate cross-dataset merging and reproducible analyses.
- Useful for quality checks when combining with external coastal datasets, given explicit provenance of GPS, GIS shapefiles, and raster-derived measurements.