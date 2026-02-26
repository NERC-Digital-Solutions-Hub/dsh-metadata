# Plynlimon experimental/research catchments

## Aim
- Establish long-term, high-quality climatic, hydrological, and soil moisture records to study how upland land use affects catchment water availability, flooding, and low flows downstream.
- Compare two representative upland land uses in mid-Wales: coniferous forestry (Severn catchment) and sheep-grazed grassland (Wye catchment).
- Generate and compare datasets including land use distribution, topography, soils, and hydrology to understand water status and environmental health over time.

## Monitoring and data outputs
- Intensive instrumentation since the late 1960s delivering detailed hydrological and climatic records.
- Surveys of spatial physical characteristics (topography, soils, land use) and production of thematic maps.
- Outputs intended for consistent formats to support policy performance assessment and environmental health scrutiny over time.

## Spatial datasets and grids
- Datasets (layers):
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil parental materials
  - Vegetation map (updated 2013)
- Grid:
  - Plynlimon hydrologically corrected elevation grid (DTM/DEM)
  - File: Plyn_DEM (15 m cells, British National Grid, floating point)
- Shapefiles and attributes include catchment names, subcatchment identifiers, river segment types (natural/artificial), elevations, and soil/vegetation descriptors.

## Source maps and topography
- Original topographic maps produced from the Hunting survey (1967–1968) at scales 1:5000 and 1:10000 with 2.5 m contour intervals.
- Later digitisation in the late 1990s into GIS layers (elevation, catchment boundaries, river network), using ground control points for registering elevation data.
- Severn catchment contour lines digitised separately at Edinburgh University (10 m intervals).

## Hydrography and catchment delineation
- Main stream channels and forest drains on large-scale maps; catchment and subcatchment boundaries derived from elevation data.
- Some historical boundaries exist only in maps/reports and may not be cleanly outlined in the digital dataset.

## Soils
- Bell’s Soil Hydrology study (1968–1969) mapped soil parent materials to understand soil hydrological processes affecting runoff.
- IH Report No. 8 (1969), with a revised CEH version published in 2005, accompanies the dataset.

## Digitising of hard copy maps
- Most shapefiles digitised at CEH using CALCOMP digitising tables, with ground control points guiding elevation capture at 10–20 m intervals.
- Severn contour lines digitised separately at Edinburgh University (method not fully documented).

## Creation of hydrologically corrected elevation grid (DTM)
- Integrated data sources (contours, spot heights, stream maps, catchment boundaries) to create a hydrologically corrected DTM.
- Process documented with a flow diagram; deliverables include:
  - Plyn_DEM: Hydrologically corrected DEM (15 m cells, British National Grid)
  - PlynlimonCatchments.shp: Catchment and subcatchment boundaries
  - PlynlimonRiverNetwork.shp: River network with attributes

## Vegetation mapping (2013 update)
- Vegetation map updated to improve compatibility with CEH Land Cover Map 2000 (LCM2000) and to reflect heath, bracken, improved grassland, etc.
- Base from 2009 Next Perspectives aerial photos; digitised in ArcGIS 10.1 with field verification (2013) to align with LCM2000 classes.
- Classes include conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, and inland water.
- Final shapefile: Plynlimon_VegetationMap2013 with attributes for vegetation class and variants.

## Severn and Wye contour maps
- Severn elevation contours derived from a separate shapefile produced at Edinburgh University; lines created from point data and merged/clipped to the Severn boundary.
- Wye contour dataset provided as Plynlimon_WyeElevationContours.shp with 10/20 m contour intervals.

## Background and data accessibility
- Background: Vegetation boundaries and soil surveys support SoilTrEC project; LCM2000 used as a base to avoid IP conflicts; a 2012 soil carbon survey informs geostatistical analyses.
- Some datasets are unavailable due to ownership or loss of source data; others have undergone updates or revisions (e.g., revised soil report in 2005, vegetation update 2013).

## Appendix A – Hunting Survey
- Aerial photography survey conducted in June 1967 by Hunting Survey Ltd; original film negatives lost, but printed frames digitised and rectified by CEH to preserve data.
- Footprints of all frames documented to aid spatial reference and future data integration.