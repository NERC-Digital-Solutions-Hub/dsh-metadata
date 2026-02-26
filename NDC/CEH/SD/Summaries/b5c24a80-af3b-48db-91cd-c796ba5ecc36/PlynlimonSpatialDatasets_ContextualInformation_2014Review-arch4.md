# Plynlimon experimental/research catchments

## Overview
- Set up in the late 1960s by the Institute of Hydrology (IH), later part of CEH, to study how land use affects catchment water availability, flooding, and low flows.
- Adjacent catchments represent two upland land uses in Wales: coniferous forestry and sheep-grazed grassland, chosen to be environmentally similar otherwise.
- Catchments were intensively instrumented with long-term climatic, hydrological, and soil moisture records; aims include high-quality measurements and understanding land-use impacts on hydrology.

## Data assets and layers
- Spatial datasets (Plynlimon Spatial datasets):
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil parental materials
  - Vegetation map
- Derived hydrographic grid:
  - Plynlimon hydrologically corrected digital terrain model (DTM/DEM)
  - DEM details: 15 m grid, floating point, British National Grid
- Additional data files:
  - PlynlimonCatchments.shp (catchment/subcatchment attribution)
  - PlynlimonRiverNetwork.shp (FNODE/TNODE, LENGTH, Catchment, Type)
  - PlynlimonSpotHeight.shp (HEIGHTS)
  - Plynlimon_WyeElevationContours.shp (10/20 m contours)
  - Plynlimon_SoilParentalMaterials.shp (SOIL, Descript)
  - Plynlimon_VegetationMap2013.shp (VegClass, Variants)
- Vegetation map (2013): updated from CEH Land Cover Map 2000 to include heath, bracken, improved grassland, and updated classifications; field-verified 2013 against 2009 aerials; supports linking with soil carbon analyses.

## Data creation, provenance, and workflow
- Topographic maps produced from the Hunting Survey aerial photography (1967–68); later digitised into GIS (late 1990s) to produce elevation, catchment, and river layers.
- Ground surveys for soils, geology, vegetation, and land use; some datasets are unavailable due to ownership or loss (except the Soil Hydrology Study map).
- Soil Hydrology map (Bell, 1969) digitised; revised edition published 2005 by CEH.
- Digitising process:
  - Hard-copy maps digitised with GCPs, 10–20 m contour intervals, using Arc/Info; Severn contours digitised at Edinburgh University with irregular interval points later converted to lines.
- Hydrologically corrected DEM:
  - Derived by integrating 1:5,000 contour data, spot heights, river maps, and catchment boundaries; creates a hydrologically-aware terrain model (Plyn_DEM) with 15 m cells.
- Appendix A describes the Hunting Survey’s technical specifications and footprint details.

## Data formats, standards, and metadata
- Coordinate system: British National Grid (EPSG: 27700)
- Data formats:
  - DEM: GRID format (Plyn_DEM)
  - Vector layers: Shapefiles (PlynlimonCatchments.shp, PlynlimonRiverNetwork.shp, PlynlimonSpotHeight.shp, Plynlimon_WyeElevationContours.shp, Plynlimon_SoilParentalMaterials, Plynlimon_VegetationMap2013)
- Attributes examples:
  - River network: FNODE_, TNODE_, LENGTH, Catchment, Type (natural/artificial)
  - Contours/spot heights: HEIGHTS
- Metadata notes:
  - Documentation links to foundational publications (Brandt et al. 2004; Bell 1969; CEH 2005) and CEH project pages
  - Vegetation map alignment with CEH Land Cover Map 2000 (LCM2000); cross-walks to LCM2000 classes

## Data gaps, quality, and governance
- Not all field data are available; some datasets are owned by other organisations or have been lost.
- Verification of content and format can be challenging; some provenance details (especially for the Severn contour creation) are not fully recorded.
- Data access barriers exist where ownership or rights restrict availability (notably not described as paywalled in this document, but ownership issues are noted).
- A 2005 CEH revision updated the Soil Hydrology map; vegetation mapping was updated in 2013 to support soil carbon analyses (within SoilTrEC context).
- The data model supports reuse in hydrological studies and cross-project analyses (e.g., SoilTrEC) but requires careful attention to lineage and metadata for proper interpretation.

## Appendix: Hunting Survey
- Describes the aerial photography survey used to generate initial topographic data (1967, Hunting Survey Ltd).
- Film negatives are lost; prints digitised and rectified; frame footprints documented to preserve historical data lineage.