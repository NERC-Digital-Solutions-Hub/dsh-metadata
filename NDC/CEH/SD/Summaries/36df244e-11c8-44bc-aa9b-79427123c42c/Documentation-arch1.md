# A land use map of Peninsular Malaysia for the year 2018 (25m grid)

- A gridded land use map for Peninsular Malaysia at ~25 m resolution for 2018/19.
- Nine land use classes: 
  1) non-paddy agriculture, 2) paddy fields, 3) rural residential, 4) urban residential, 5) commercial/institutional, 6) industrial/infrastructure, 7) roads, 8) urban, 9) others.
- Purpose: produced by integrating state-level land use polygons with auxiliary datasets to fill gaps and improve detail per local context.
- Part of the project Malaysia - Flood Impact Across Scales, funded under Newton-Ungku Omar and MYPAIR, with support from NERC and Malaysia Ministry of Higher Education.

## Datasets used

- State land use polygons (2018/2019) from PLANMalaysia for twelve states of the Malaysian Peninsula.
- Climate Change Initiative Land Cover (CCI LC) from ESA (2015; 300 m resolution) for gap-filling and infill.
- Global Human Settlement Layer Urban Centre Database (GHS-UCDB R2019A, 2015) to distinguish urban vs rural residential areas.
- Rice cultivation maps for Peninsular Malaysia (Begum et al., 2005; FAO, 2005) to identify paddy fields where state data lacked.
- All processing and integration performed in QGIS.

## Data processing and integration

- State land use polygons reclassified to nine target classes; polygons rasterized to 25 m resolution.
- Rural vs. urban residential areas inferred by overlaying state data with GHS-UCDB.
- CCI Land Cover (300 m) reclassified to three classes (urban, agriculture, others) and resampled to 25 m to fill gaps in state data (e.g., Kuala Lumpur).
- Paddy fields:
  - For states with detailed paddy data (Kelantan, Kedah, Johor, Pahang, Perlis, Perak, Penang), used existing paddy polygons.
  - For Melaka, Negeri Sembilan, Selangor, Putrajaya, Terengganu (lacking detailed data), Paddy areas derived from two rice-cultivation maps (Begum et al., 2005; FAO, 2005); vectorised and rasterised to 25 m.
- The mosaic map created by merging state polygons, GHS-UCDB, CCI LC, and paddy-field data; gaps filled with CCI LC where needed.
- Final map presented as a single mosaic raster.

## Paddy fields details

- Paddy fields included in states with explicit data; otherwise inferred from rice-cultivation maps and vectorised before rasterisation.
- Paddy fields merged with other land use classes in the final mosaic.

## Creating the mosaic land use map

- Merged data layers: state polygon data, GHS-UCDB, CCI LC, and paddy fields (vectorised/derived).
- Gaps such as Kuala Lumpur filled using CCI LC data.
- Final visualization and verification steps illustrated in figures showing gaps filled and the Kuala Lumpur example.

## Data structure

- Extent: Peninsular Malaysia.
- Format: raster GeoTIFF.
- Coordinate system: WGS84.
- Resolution: ~25 m per grid cell.
- Each cell has one of the nine land use values.
- Map can be projected and measured in various units using GIS tools.

## Land use classes, rasters values, and datasets used

- 1) Agriculture (non-paddy) — from State polygon data + CCI LC
- 2) Agriculture (paddy) — from State polygon data + Paddy maps (Begum et al. 2005; FAO 2005)
- 3) Rural Residential — from State polygon data + GHS-UCDB
- 4) Urban Residential — from State polygon data + GHS-UCDB
- 5) Commercial and Institutional — from State polygon data
- 6) Industrial and Infrastructure — from State polygon data
- 7) Roads — from State polygon data
- 8) Others (forest, lakes/reservoirs, bare land, beach) — from State polygon data + CCI LC
- 9) Urban — from CCI LC

## File name

- Malaysia_land_use_map.tif

## References

- Begum, M. et al. (2005). Weed diversity of rice fields in four districts of Muda rice granary area, North-West Peninsular Malaysia.
- ESA. Land Cover CCI Product User Guide Version 2 (2017).
- FAO. (2005). Future of large rice-based irrigation systems in Southeast Asia.
- Florczyk, A.J. et al. (2019). GHS-UCDB R2019A.
- Global Administrative Areas (GADM) (2018). GADM v3.6.