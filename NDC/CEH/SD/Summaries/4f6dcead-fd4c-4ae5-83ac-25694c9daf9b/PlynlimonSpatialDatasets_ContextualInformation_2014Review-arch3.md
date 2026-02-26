# Plynlimon Spatial datasets

- The Plynlimon experimental catchments (late 1960s) were created by the Institute of Hydrology (IH) under NERC to study how upland land use (conifer forestry vs. sheep-grazed grassland) affects catchment water availability, flooding, and low flows. The two adjacent headwater catchments feed the River Severn and River Wye and were selected to be as similar as possible otherwise.
- The catchments were heavily instrumented with long-term climatic, hydrological, and soil measurements, supported by surveys of physical characteristics and land use. The resulting datasets include various thematic maps and GIS-ready layers.

## Data layers and datasets (spatial scope)

- Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - Defines upland catchments and major tributary drainage areas
- River network (PlynlimonRiverNetwork.shp)
  - Features stream channels with origin/destination nodes and attributes (type: natural or artificial)
- Spot heights (PlynlimonSpotHeight.shp)
  - Elevation points
- Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Elevation contours at 10/20 m intervals
- Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Elevation contours at 10 m intervals
- Soil Parental Materials (Plynlimon_SoilParentalMaterials)
  - Distribution of soil parent materials with codes and descriptions
- Vegetation map (Plynlimon_VegetationMap2013)
  - Updated vegetation classes aligned with CEH Land Cover Map 2000; 2013 digitised and ground-truthed
- Hydrologically corrected elevation grid (Plyn_DEM)
  - 15 m grid (British National Grid), floating point, DEM corrected for hydrology
- Background layers for topography, soils, and vegetation
  - Documentation of data lineage and metadata

## Data provenance and digitising processes

- Source maps originated from a Hunting Survey aerial photography campaign (1967) supplied by NERC; later digitised into GIS layers in the late 1990s.
- Topography and hydrography were derived from photogrammetric maps:
  - 1:5000 scale topographic maps with 2.5 m contours
  - 1:10000 scale maps produced from photogrammetric reductions of 1:5000 maps
- Field surveys mapped soils, geology, vegetation, and land use; some datasets are now unavailable or constrained by ownership (data owned by other organisations or lost).
- Specific digitising steps:
  - Arcinfo-based digitising from scanned maps
  - Ground control points (GCPs) used to georeference and capture elevation points and contours (10–20 m intervals)
  - Severn contour lines digitised at Edinburgh University with later processing to lines
- Hard-copy maps converted into GIS using shapefiles and GRID formats; entities include catchment boundaries, river networks, contour lines, soils, and vegetation.

## Hydrologically corrected elevation grid and products

- Hydrologically corrected digital terrain model (DTM/DEM) built from:
  - 1:5,000 contour maps, spot heights, river network, and catchment boundaries
  - Creation workflow included TIN construction and generation of a hydrologically corrected grid (Plyn_DEM)
- Product specifications:
  - Plyn_DEM GRID, 15 m cell size, British National Grid, floating point
  - Detailed steps summarized in a flow diagram (Figure 1 in the document)
- Purpose: provides a consistent, hydrologically plausible representation of terrain for hydrological analyses within the Plynlimon catchments

## Vegetation and land cover

- Vegetation map updated in 2013 to support soil carbon and geostatistical analyses ( SoilTrEC project):
  - Based on CEH Land Cover Map 2000 (LCM2000) with updates to include heath, bracken, improved grassland, etc.
  - Classes include conifer plantations (and variants), new/felled plantations, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, and deciduous woodland
  - Final map in Plynlimon_VegetationMap2013 with attributes: id, VegClass, Variants
- Mapping workflow combined interpretation of 2009 aerial photography with ground truthing (2013) and digitisation in ArcGIS 10.1

## Contours and hydrological context by subregion

- Wye catchment contours: Plynlimon_WyeElevationContours.shp (10/20 m intervals)
- Severn catchment contours: Plynlimon_SevernElevationContours.shp (10 m intervals)
- Subcatchments and river network attributes support hydrological modeling and attribution of hydrological responses to land-use change

## Appendix and historical context

- Appendix A: Hunting Survey
  - Details about the 1967 aerial survey by Hunting Survey Ltd; footprints of frames and technical specs; data preservation efforts due to lost film negatives

## Data access, standards, and governance

- Data are described with explicit file names, coordinate system (British National Grid), and data types (Shapefile, GRID)
- Data provenance, transformation steps, and metadata are documented to support reuse in monitoring frameworks
- Some data are restricted or have provenance issues (owned by other organisations or lost), posing limits for full openness or reuse without permissions

## Gaps, limitations, and considerations for monitoring

- Missing or restricted datasets due to data ownership or loss
- Some legacy processes (e.g., Severn contour data) lack full documentation of digitising methods
- Ongoing need for metadata enrichment and data governance to ensure datasets meet standards and remain up to date

## Relevance to monitoring frameworks

- Provides a comprehensive, traceable set of spatial layers essential for long-term hydrological monitoring and land-use impact assessments
- Demonstrates rigorous data provenance, digitising workflows, and transformation to hydrologically consistent terrain representations
- exemplifies integration of topography, soils, vegetation, and hydrology to support environmental monitoring and modeling across catchments with contrasting land uses