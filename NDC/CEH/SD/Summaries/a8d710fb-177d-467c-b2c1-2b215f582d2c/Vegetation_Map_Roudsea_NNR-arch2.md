# Vegetation map of Roudsea Wood National Nature Reserve, 1962

## Overview
- ESRI Shapefile containing polygons that represent vegetation areas within Roudsea Wood NNR (Cumbria).
- Digitized by the Centre for Ecology & Hydrology in 2019 from an original 1962 field map.
- Original field map created by R. Donelly and N. English (1962) at the Nature Conservancy’s Merlewood Research Station.
- Maps the western side of the reserve (the woodland) and was produced by regional Nature Conservancy officers after the reserve designation in 1955.

## Data and Methods
- Vegetation mapped in the field on a basemap as parcels by tree cover type, stocking rates, and ground flora communities.
- The 1962 map was digitized into GIS format in 2019 using ESRI GIS software.
- Species nomenclature follows Flora of the British Isles (1962).
- Data entry values have been range-checked and cross-checked against the original map; formal data quality metadata is not recorded.

## Spatial Reference and Extent
- Coordinate system: British National Grid (OSGB1936).
- Projection: Transverse Mercator.
- Extent: Great Britain.

## Data Content and Attributes
- Shapefile contains polygon geometries for vegetation parcels and tree cover types.
- Key attribute groups and examples:
  - TREE_COV, DESC_TC; TREE_COV2, DESC_TC2: coded tree cover types (e.g., Birch, Oak, Conifer plantations, No tree cover, etc.).
  - STOCKING, DESC_ST; STOCKING2, DESC_ST2: stocking codes and descriptions (e.g., high forest canopy, coppice, scattered trees).
  - GVEG_MAJ, DESC_MAJ; GVEG_MAJ2, DESC_MAJ2: major ground vegetation communities and descriptions.
  - GVEG_MIN, DESC_MIN; GVEG_MIN2, DESC_MIN2: minor ground vegetation communities and descriptions.
  - OTHER: any other information not covered by above.
  - GLOBALID: unique identifier.
  - POLY_AREA: polygon area in square meters.
- Detailed codes and descriptions exist for each attribute, with some fields having optional second codes/descriptions.

## Provenance and Quality
- Original fieldwork conducted after the 1955 designation, mapped in the field on a basemap.
- Digitization performed by CEH in 2019 from the 1962 map.
- Quality assurance performed by range checks and cross-verification against the original map; no explicit quality metadata recorded.

## Access, Storage and Use
- Data provided as an ESRI Shapefile with linked attributes.
- Stored and managed through standard GIS data practices (digitized and archived by CEH; prepared for integration with environmental monitoring datasets).

## Version History
- Document Version 1: 5/6/2019.