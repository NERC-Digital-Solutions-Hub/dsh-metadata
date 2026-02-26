# Plynlimon experimental/research catchments spatial datasets

## Overview
- Established in the late 1960s by the Institute of Hydrology (IH) as part of NERC, now CEH.
- Aim: understand how upland land use affects catchment water availability, flooding, and low flows.
- Two adjacent catchments at the headwaters of the River Severn and River Wye in mid-Wales; chosen to represent coniferous forestry vs sheep-grazed grassland while keeping other conditions similar.
- Intensively instrumented with long-term climatic, hydrological, and soil moisture data; includes surveys of physical characteristics and land use; supports development of high-quality, discoverable datasets and models.

## Datasets and data layers
- Spatial layers:
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Soil Parental Materials (Plynlimon_SoilParentalMaterials.shp)
  - Vegetation map (Plynlimon_VegetationMap2013.shp)
- Hydrologically corrected elevation data:
  - Plynlimon DEM (Plyn_DEM, GRID, 15 m cell size, British National Grid)
- Note: Some historic datasets may be unavailable due to IP rights or loss; others have been updated for compatibility and reuse.

## Data provenance, digitisation, and processing
- Original mapping derived from the Hunting Survey aerial photographs (1967) used to create topographic maps (1:5000 and 1:10000 scales; 2.5 m contour interval).
- Late 1990s: topographic and hydrographic data digitised into GIS layers (elevation, catchment boundaries, river network) from these maps.
- Soil map: Bell, J.P. (1969) The Soil Hydrology of the Plynlimon Catchments (IH Report No. 8); updated in 2005 by CEH.
- Digitisation workflow:
  - CEH digitised most shapefiles on CALCOMP digitising tables with ground control points (GCPs).
  - Severn contour lines captured at Edinburgh University; later converted to lines in ArcGIS and clipped to catchment boundaries.
  - Hydrologically corrected DEM created by integrating contours, spot heights, streams, and boundaries; TIN used to produce a 15 m GRID DEM.
- Metadata and structure follow GIS conventions, with explicit file names and attributes described for each layer.

## Data formats, coordinate systems, and technical details
- Coordinate system: British National Grid for all shapefiles and rasters.
- DEM:
  - Plyn_DEM: GRID, 15 m cell size, hydrologically corrected DEM.
- Shapefiles and attributes:
  - PlynlimonCatchments.shp: Catchment/Subcatchment names.
  - PlynlimonRiverNetwork.shp: FNODE, TNODE, LENGTH, Catchment, Type.
  - PlynlimonSpotHeight.shp: HEIGHTS (elevation in metres).
  - Plynlimon_WyeElevationContours.shp: HEIGHTS (metres); 10 and 20 m intervals.
  - Plynlimon_SevernElevationContours.shp: HEIGHTS (metres); 10 m intervals.
  - Plynlimon_SoilParentalMaterials: SOIL (code), Descript (description).
  - Plynlimon_VegetationMap2013.shp: id, VegClass, Varients (Variants) describing vegetation classes (aligned with CEH LCM2000 with updates such as converting conifer categories and adding a variants field for flexibility).
- Vegetation mapping methodology:
  - Updated LCM2000-based class structure to include coniferous woodland, new plantation, felled plantation, and other classes (e.g., rough acid grass, bracken, heath, improved grassland).
  - Draft map created from 2009 aerial imagery; refined with 2013 field observations; discrepancies due to date differences between imagery (2009) and fieldwork (2013) were noted and addressed.
  - Final digital vegetation dataset supports alignment with LCM2000 classes and enables more nuanced analyses (e.g., soil carbon studies within SoilTrEC).

## Data quality, gaps, and governance
- Some older datasets are not available due to ownership or loss; others have restricted rights (IPR issues) that may limit sharing.
- A revised soil hydrology map (Bell 1969, IH Report No. 8) was published in 2005 by CEH and is accessible via CEH publications.
- Vegetation mapping emphasizes compatibility with CEH Land Cover Map 2000 (LCM2000) to avoid licensing conflicts and to support integration with CEH models.
- The dataset includes a clear provenance trail: original aerial survey, digitisation steps, processing to DEM, and subsequent updates to vegetation and contours.

## Appendix: hunting survey and data history
- Appendix A documents the Hunting Survey (June 1967) aerial photography used to derive base topography; film negatives are lost, but printed frames were digitised and rectified to preserve footprints and data context.

## Access, use, and stewardship implications for data stewards
- Maintain clear, linked metadata for all layers (names, descriptions, coordinate systems, attributes).
- Manage data rights and access constraints, especially for historical datasets with IP constraints.
- Ensure traceability of data lineage from original surveys through digitisation, processing, and updates.
- Facilitate interoperability by keeping coordinate systems consistent (British National Grid) and aligning vegetation classes with CEH LCMap standards.
- Plan for ongoing updates (e.g., vegetation map updates and compatibility with newer land cover datasets) and document revision histories.
- Provide guidance on data quality considerations and known limitations (gaps due to lost datasets; differences arising from imagery dates vs. field validation).