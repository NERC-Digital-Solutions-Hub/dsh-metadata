# Plynlimon experimental/research catchments

## Overview
- Established in the late 1960s by the Institute of Hydrology (IH), now part of the Centre for Ecology & Hydrology (CEH).
- Main aim: understand how land use affects catchment water availability, flooding, and low flows.
- Two adjacent catchments represent upland Wales land uses: coniferous forestry and sheep-grazed grassland; designed to be similar in all other environmental aspects.
- Intensively instrumented with long-term climatic, streamflow, and soil moisture records; used to compare evaporation losses and hydrological responses.

## Data assets (spatial and grid datasets)
- Shapefiles (British National Grid) illustrating key features:
  - PlynlimonCatchments.shp – catchment and subcatchment boundaries; attributes: Catchment, Subcatch.
  - PlynlimonRiverNetwork.shp – river network; attributes: FNODE_, TNODE_, LENGTH, Catchment, Type (natural or artificial).
  - PlynlimonSpotHeight.shp – spot heights; attribute: HEIGHTS.
  - Plynlimon_WyeElevationContours.shp – Wye catchment contour lines; attribute: HEIGHTS.
  - Plynlimon_SevernElevationContours.shp – Severn catchment contour lines; attribute: HEIGHTS.
  - Plynlimon_SoilParentalMaterials.shp – soil parent materials; attributes: SOIL, Descript.
  - Plynlimon_VegetationMap2013.shp – vegetation map; attributes: id, VegClass, Varients.
- Hydrologically corrected elevation grid (DEM):
  - Plyn_DEM.grid (15 m cells, floating point, British National Grid); description: hydrologically-corrected digital terrain model (DTM) of Plynlimon catchments.
- Soil hydrology map:
  - Bell, J.P. 1969 (IH Report No. 8); updated 2005 CEH version provided; used to understand soil hydrological processes.

## Data creation and GIS workflow
- Topography and basemaps:
  - Initial large-scale topographic maps produced from the Hunting Survey aerial photography (1967–68) at 1:5000 and 1:10000 scales with 2.5 m contour intervals.
  - In the late 1990s, topographic and hydrographic data were digitised into GIS layers (elevation, catchment boundaries, river network).
- Digitising process:
  - Hard-copy maps digitised using CALCOMP digitising table; ground control points (GCPs) registered data; elevation points and contours captured (10–20 m intervals) and saved as ArcInfo coverages.
  - Severn catchment contours digitised at Edinburgh University from 1:5000 maps; converted from points to lines with some artefacts corrected.
- Hydrologically corrected DEM:
  - Integrated 1:5000 contour data, spot heights, stream maps, and catchment boundaries to build a TIN, then derived a hydrologically corrected grid-based DEM (Plyn_DEM, 15 m).
- Data formats:
  - Shapefiles in British National Grid; DEM in GRID format (Arc/Info).

## Soil and land cover evolution
- Soil map (Bell, 1969) and its 2005 CEH revision underpin soil hydrology interpretation.
- Vegetation mapping (updated 2013):
  - Based on CEH Land Cover Map 2000 (LCM2000) with updates to reflect heath, bracken, and improved grassland.
  - Draft vegetation map created from 2009 Next Perspectives aerial photography; refined via field validation (2013) along tracks; differences due to date and conditions noted.
  - Final vegetation classes include: conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, inland water.
  - Variants column enables using coniferous plantation as woodland or as felled/new plantations, offering flexibility for analyses.

## Source data provenance and limitations
- Some data layers are unavailable due to ownership restrictions or loss; field-survey data documented but not all materials are recoverable.
- Appendix A (Hunting Survey) provides details on aerial photography scope and frame footprints; negatives are lost, but printed frames have been digitised.

## Usage and applications
- Provides a geospatial infrastructure for hydrological studies, land-use impacts, soil-vegetation interactions, and long-term climate/hydrology research.
- Supports geostatistical analyses (e.g., SoilTrEC project) and integration with other CEH models.
- Enables self-serve access to DEM, catchment boundaries, river networks, contour lines, soils, and vegetation data for researchers and policy-focused use.

## Access and references
- CEH project pages and related CEH science blogs provide background and data context.
- Foundational references:
  - Bell, J.P. 1969. The Soil Hydrology of the Plynlimon Catchments (IH Report No. 8).
  - 2005 CEH revision of Bell’s soil hydrology map.
- Data documentation and products hosted by CEH; related publications and datasets described in the project materials.