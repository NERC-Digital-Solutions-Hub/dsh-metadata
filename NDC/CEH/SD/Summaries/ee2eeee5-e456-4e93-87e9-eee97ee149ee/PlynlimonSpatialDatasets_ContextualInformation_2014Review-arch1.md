# Plynlimon Spatial datasets

- The Plynlimon experimental catchments in mid-Wales were established to study how upland land use (conifer forestry vs. sheep-grazed grassland) affects catchment water availability, flooding, and low flows. They provide long-term climatic, hydrological, soils, and land-use data for two headwater catchments of the River Severn and River Wye.

## Data layers and datasets

- Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
- River network (PlynlimonRiverNetwork.shp)
- Spot heights (PlynlimonSpotHeight.shp)
- Wye catchment elevation contours (Plynlimon_WyeElevationContours.shp)
- Severn catchment elevation contours (Plynlimon_SevernElevationContours.shp)
- Soil parental materials (Plynlimon_SoilParentalMaterials)
- Vegetation map (Plynlimon_VegetationMap2013)
- Hydrologically corrected elevation grid (Plyn_DEM; 15 m resolution, British National Grid)
- Additional attribute and metadata details provided for each layer (e.g., FNODE/TNODE, LENGTH, Catchment, Type for rivers; HEIGHTS for elevations; SOIL, Descript for soils; VegClass and Variants for vegetation)

## Data origins and history

- Source maps originate from a 1967 Hunting Survey aerial photography program; large-scale topographic maps produced 1967–68.
- In the late 1990s, topographic and hydrographic data were digitised into GIS layers (elevation, catchment boundaries, river network).
- Soil data come from the 1969 Soil Hydrology Study by J.P. Bell (IH Report No. 8; updated 2005 by CEH).
- Some datasets are unavailable due to ownership, loss, or access barriers; others were created or updated specifically for ongoing projects (e.g., vegetation update in 2013).

## Topography, hydrography, and soils details

- Topography:
  - 1:5000 scale maps with 2.5 m contour interval; 1:10000 scale maps with same contour interval.
  - Aerial photography (1967–68) formed the basis for elevation and drainage features.
- Hydrography:
  - Main streams and forest drains captured from topographic maps; subcatchment boundaries derived from elevation data.
- Soils:
  - Bell’s 1969 soil map shows distribution of soil parent materials; IH Report No. 8 used for hydrological context; CEH updated version (2005) available.

## Digitising methods and data integration

- Digitising performed with CALCOMP digitising table; GCPs used to register maps; elevation points and contour lines captured at 10–20 m intervals; data saved as ArcInfo coverages.
- Severn catchment contour lines digitised separately at Edinburgh University (captured as points then converted to lines).
- Hydrologically corrected DEM created by integrating contour maps, spot heights, stream maps, and catchment boundaries; a TIN was generated and converted to a grid DEM (Plyn_DEM, 15 m cell size, floating point, British National Grid).

## Vegetation map specifics

- Vegetation map (Plynlimon_VegetationMap2013) derived from 2009 aerial photography with 2013 field verification.
- Base used: CEH Land Cover Map 2000 (LCM2000); updated to better represent heath, bracken, and improved grassland, while aligning with LCM2000 classes.
- Classes include conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, and inland water.
- The map supports geostatistical analyses (e.g., soil carbon studies) and allows flexibility with conifer category variants (conifer woodland vs. felled/new plantation).

## Appendices and background

- Appendix A (Hunting Survey) describes the 1967 aerial survey and the digitisation/rectification efforts; film negatives are lost, but printed frames have been digitised and rectified.

## Access, references, and use

- Datasets are documented with file names, coordinate system (British National Grid), and key attributes.
- Related documentation and project context available via CEH websites and SoilHydrology of the Plynlimon Catchments (IH Report No. 8) references.
- The data serve long-term hydrological and land-use impact analyses, with attention to data provenance, scale, access, and compatibility across multiple sources.