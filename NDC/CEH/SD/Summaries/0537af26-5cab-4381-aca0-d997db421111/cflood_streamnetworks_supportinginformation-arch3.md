# Shapefiles of stream networks for CFLOOD project (Compound flooding from tropical cyclone-induced sea surge and precipitation in Sri Lanka)

## Scope and purpose
- Shapefiles of stream networks (natural and artificial watercourses) created for hydrologic modelling within the CFLOOD project.
- Intended to support analysis of compound flooding from tropical cyclone-induced sea surge and rainfall in eastern Sri Lanka.

## Location
- Three river basins in eastern Sri Lanka: Mundeni Aru, Maduru Oya, and Miyangolla Ela.

## Methods of collection and generation
- Stream networks manually mapped using historic satellite imagery from Google Earth.
- OpenStreetMap (OSM) used as a starting point; watercourses already in OSM were re-mapped.
- Selection criteria for imagery: river level (broader widths preferred at higher levels), image recency, and image quality.
- Centrelines traced in QGIS; flow direction inferred from line point order (downhill); some uncertainty in flat, delta areas due to elevation data limitations.
- Some watercourses not mappable due to dense vegetation; minor watercourses of low relevance to modelling omitted.
- Widths assigned from maximum breadth seen in images; transitions between line segments may require smoothing for modelling use.

## Data content and units
- Files contain centrelines of watercourses in three separate shapefiles (one per basin).
- Coordinate system: Universal Transverse Mercator (UTM) Zone 44N (EPSG:32644).
- Attribute: Width_m — watercourse width in meters, with segments capturing width variation.
- Width measurements are approximate indicators for modelling; not guaranteed to be uniform along entire segment.

## Authors and oversight
- Mapping: J.B.R Matthews.
- Oversight and advisory support: R. Jayaratne and A. Raby.

## Completeness and limitations
- Aims for comprehensive mapping, but dense vegetation and image visibility limited some watercourses (notably in Mundeni Aru southern portion).
- Some canals and minor waterways not mapped; users should account for missing watercourses in hydrologic modelling.
- Breaks occur in stream networks where lakes exist.
- Potential uncertainty in flow direction in flat areas (delta region) due to elevation model limitations.

## Data quality and governance
- Data integrity checked: connections at vertices and flow direction consistency verified.
- Widths are provided for modelling purposes but should be treated as general indicators rather than precise, continuous measurements.
- Data are organized in basins-specific folders:
  - CFLOOD_MundeniAru_StreamNetwork_utm
  - CFLOOD_MaduruOya_StreamNetwork_utm
  - CFLOOD_MiyangollaEla_StreamNetwork_utm
- Only a single attribute per shapefile ('Width_m') is included beyond geometry.