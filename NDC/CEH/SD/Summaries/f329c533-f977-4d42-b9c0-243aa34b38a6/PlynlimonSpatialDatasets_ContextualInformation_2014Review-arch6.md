# INTRODUCTION

## Objective and context
- Plynlimon experimental/research catchments (late 1960s) established by the Institute of Hydrology (IH, NERC) to study how land use affects catchment water availability, flooding, and low flows.
- Two adjacent catchments represent upland Wales’ main land uses: coniferous forestry vs. sheep-grazed grassland; designed to be environmentally similar otherwise.
- Catchments were intensively instrumented; long-term climatic and hydrological data collected; surveys of physical characteristics and land use conducted; datasets include various thematic maps.

## Spatial data assets
- Plynlimon Spatial datasets include:
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil parental materials
  - Vegetation map
- A hydrologically corrected elevation grid (DTM/DEM) is provided.

## Data sources and digitisation
- Hunting Survey (1967–68) produced large-scale topographic maps with streams, drains, tracks, and fence lines.
- In the late 1990s these maps were digitised into GIS layers (elevation, boundaries, river network) after conversion to ArcINFO/managing GIS data.
- Field surveys mapped soils, geology, vegetation, and land use; some datasets are unavailable due to ownership or loss; notable exception is Bell’s 1969 Soil Hydrology map (IH Report No. 8), later updated by CEH (2005) and available online.
- Digitising methods:
  - CEH digitised shapefiles from 1:5000 topographic maps using CALCOMP with ground control points; elevation points and 10–20 m contours captured; saved as ArcInfo coverages.
  - Severn catchment contours digitised at Edinburgh University (described as 10 m interval points later converted to lines).
- Hydrologically corrected DEM construction:
  - Inputs: 1:5000 contour maps, spot heights, stream maps, catchment boundaries.
  - Process: data imported into ArcInfo, TIN created, hydrologically corrected grid-derived DTM produced (Plyn_DEM, 15 m cells, British National Grid).

## Data products and file formats

- Shapefiles and grid products:
  - PlynlimonCatchments.shp — catchment and subcatchment boundaries (British National Grid); attributes include Catchment and Subcatch.
  - PlynlimonRiverNetwork.shp — river network; attributes include FNODE_, TNODE_, LENGTH, Catchment, Type (natural or artificial).
  - PlynlimonSpotHeight.shp — spot heights; attribute HEIGHTS (elevation in m).
  - Plynlimon_WyeElevationContours.shp — Wye contour lines at 10/20 m; attribute HEIGHTS.
  - Plynlimon_SoilParentalMaterials.shp — distribution of soil parent materials; attributes SOIL and Descript.
  - Plynlimon_VegetationMap2013.shp — updated vegetation map (2013) with id, VegClass, Variants.
  - Plynlimon_SevernElevationContours.shp — Severn contour lines at 10 m; attribute HEIGHTS.
- Hydrologically corrected elevation grid:
  - Plyn_DEM (GRID, 15 m cells, floating point, British National Grid) representing the hydrologically corrected DEM.
- Vegetation map details:
  - Updated from CEH Land Cover Map 2000 (LCM2000) base; classes expanded to include heath, bracken, improved grassland, etc.
  - Draft map created from 2009 aerials, refined via 2013 field validation; conifer categories supported via a Variants field to allow use as coniferous woodland or plantation variants.
- Appendix A Hunting Survey:
  - Describes the 1967 Hunting Survey aerial photography data, technical specifications, digitisation status, and footprint documentation.

## Data provenance, gaps, and workflow considerations
- Original data origins in the Hunting Survey (1967–68) and subsequent digitisation in the 1990s; various physical maps and field surveys underpin the layers.
- Some datasets are missing or restricted due to ownership or loss; the Bell soil map (IH Report No. 8) exists in revised CEH form (2005) and is accessible via CEH.
- Vegetation mapping integrated with LC2000 standards to facilitate modeling with CEH tools, ensuring consistency with existing CEH data products.
- Data access and further information referenced via CEH program pages and CEH publications.

## Context within data support
- The collection demonstrates end-to-end data assembly for hydrological and land-use impact research, producing interoperable GIS layers and a hydrologically corrected DEM for upstream/downstream analysis, suitable for self-serve data exploration and integration into broader SoilTrEC analyses and related projects.