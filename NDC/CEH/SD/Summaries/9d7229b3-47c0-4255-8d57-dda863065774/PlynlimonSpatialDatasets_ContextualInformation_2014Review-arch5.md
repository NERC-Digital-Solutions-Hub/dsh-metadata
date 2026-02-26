# Plynlimon Spatial datasets

## Overview
- Document describes long-running Plynlimon experimental catchments in mid-Wales, set up in the late 1960s to study land use impacts on catchment water availability, floods, and low flows.
- Two adjacent catchments represent coniferous forestry and sheep-grazed grassland, with extensive hydrological and climatic records and surveys of physical characteristics and land use.
- Spatial datasets include catchment boundaries, river networks, elevations, soils, vegetation, and hydrologically corrected terrain data, with historical and updated layers.

## Spatial data holdings and formats
- Catchment and subcatchment boundaries: PlynlimonCatchments.shp (British National Grid); attributes include Catchment and Subcatch.
- River network: PlynlimonRiverNetwork.shp; attributes include FNODE_, TNODE_, LENGTH, Catchment, Type (natural or artificial).
- Spot heights: PlynlimonSpotHeight.shp; attribute HEIGHTS (elevation in metres).
- Wye catchment elevation contours: Plynlimon_WyeElevationContours.shp; attribute HEIGHTS (metres).
- Severn catchment elevation contours: Plynlimon_SevernElevationContours.shp; attribute HEIGHTS.
- Soil parental materials: Plynlimon_SoilParentalMaterials; attributes SOIL and Descript.
- Vegetation map: Plynlimon_VegetationMap2013; attributes id, VegClass, Varients (sic) for class variants.
- Hydrologically corrected elevation grid (DTM/DEM): Plyn_DEM (GRID, 15 m cell size, British National Grid).
- Additional context layers from topographic sources and related maps.

## Data sources and provenance
- Core data originate from Hunting Survey aerial photography (1967) used to generate large-scale topographic maps (1:5000; 1:10000) with contour intervals of 2.5 m.
- In the late 1990s, topographic and hydrographic data were digitised into GIS layers from those maps.
- Early field surveys mapped soils, geology, vegetation, and land use; some data are currently unavailable due to ownership restrictions or loss.
- Soil hydrology map (Bell, J.P., 1969) underpinning soil parental materials layer; updated version published in 2005 by CEH.

## Digitisation and data capture
- Most shapefiles (except Severn contours) digitised at CEH using CALCOMP digitising table; GCPs used for registration; elevation points and contours captured at 10 and 20 m intervals from 1:5000 maps; data saved as ArcInfo coverages.
- Severn catchment contours digitised at Edinburgh University from 1:5000 maps; later converted from points to lines and edited for artefacts.
- Data captured and stored in ArcInfo/ArcGIS environments; documentation includes workflow diagrams and detailed layer descriptions.

## Creation of hydrologically corrected elevation data
- DEM created by integrating 1:5000 contour maps, spot heights, stream maps, and catchment boundaries.
- Process: import data into ArcInfo, generate a TIN, derive a hydrologically corrected grid-based DEM.
- Final products:
  - Plyn_DEM: 15 m cell size, floating point, British National Grid; description indicates hydrologically corrected DEM.

## Vegetation mapping
- Vegetation map developed to support SoilTrEC project needs and soil carbon analyses, using CEH Land Cover Map 2000 (LCM2000) as a base to avoid IP conflicts with newer maps.
- 2013 vegetation map produced by digitising and refining classes from 2009 aerial photography, with field verification in 2013.
- Classes include conifer plantation (and subtypes), various grassland and heath categories, rough classifications, and water/bare ground; a Variants field allows using polygons as coniferous woodland or as felled/new plantation.
- Final dataset: Plynlimon_VegetationMap2013; attributes id, VegClass, Varients.

## Contour and terrain data by catchment
- Wye and Severn elevation contours produced from different sources:
  - Wye contours: Plynlimon_WyeElevationContours.shp (10/20 m).
  - Severn contours: Plynlimon_SevernElevationContours.shp (10 m, clipped to Severn boundary).
- Data handling includes conversion from points to lines (Severn) and artifact removal/editing for clean contour representations.

## Appendix A Hunting Survey
- Details the 1967 aerial photographic survey by Hunting Survey Ltd; film negatives are lost, but printed frames have been digitised and rectified.
- Footprints of aerial frames documented to preserve historical spatial context.

## Data quality, gaps, and governance considerations
- Some datasets are not available due to intellectual property or ownership restrictions; others have been lost since original surveys.
- Historical data reflect photography dates (2009 imagery) vs field observations (2013), leading to some discrepancies in vegetation mapping.
- Formats and coordinate system standardized to British National Grid; primary data stored as shapefiles and GRID DEM.
- Documentation includes detailed metadata on layer attributes and provenance, aiding data stewardship, reuse, and interoperability.
- CEH provides related publications and web access to dataset context and updates.

## Implications for data stewardship
- Ensure ongoing storage and sharing of the core layers: catchments, river networks, elevations, soils, vegetation, and DEM.
- Maintain clear metadata, including data provenance (Hunting Survey, CEH digitisation, field validation), coordinate system, formats, and attribute definitions.
- Track data availability restrictions and provenance gaps; document any new translations or updates to avoid loss of lineage.
- Preserve historical context (Appendix A Hunting Survey) to support future re-use and reproducibility.
- Establish/update data governance with clear responsibilities for updates, versioning, and access controls across multiple systems and formats.