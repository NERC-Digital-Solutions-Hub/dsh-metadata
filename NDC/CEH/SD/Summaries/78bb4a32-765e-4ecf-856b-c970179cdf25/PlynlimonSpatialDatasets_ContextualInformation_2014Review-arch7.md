# INTRODUCTION

- The Plynlimon experimental/research catchments (late 1960s) were established by the Institute of Hydrology (IH) under NERC, later part of CEH, to study how upland land use affects catchment water availability, flooding, and low flows.
- Two adjacent catchments (headwaters of the River Severn and River Wye in mid-Wales) represent the two main upland land uses: coniferous forestry and sheep-grazed grassland, with other environmental factors kept similar.
- Intensive instrumentation provided long-term climatic and hydrological data from the late 1960s; surveys mapped spatial characteristics (topography, soils, land use) and produced a range of thematic maps.
- GIS-ready spatial datasets and a hydrologically corrected DEM support hydrological and geospatial analyses.

## GIS datasets and data formats

- Plynlimon Spatial datasets:
  - Catchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
  - Soil Parental Materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
- Hydrologically corrected elevation grid:
  - Plynlimon DEM (Plyn_DEM) — GRID format, 15 m cell size, floating point, British National Grid.
- Coordinate system used across shapefiles: British National Grid.

## Data provenance and sources

- Initial topographic maps produced from the Hunting Survey (1967 aerial photography). Later digitised in the late 1990s to create GIS-ready layers (elevation, catchment boundaries, river network).
- Field surveys in early years mapped soils, geology, vegetation, and land use; some datasets are unavailable due to ownership or loss; key soil map: Bell, J.P. 1969 (Soil Hydrology of the Plynlimon Catchments), with CEH 2005 revision.
- Vegetation mapping (2013) updated from 2009 aerial photography (LCM2000 as base) and ground-truthing (2013). Classes aligned to CEH Land Cover Map 2000 (LCM2000) with refinements.

## Data processing workflow

- Digitising of hard-copy maps:
  - CEH digitised most layers using CALCOMP digitising tablet; registration with ground control points; elevation points and contours captured from 1:5000 maps at 10/20 m intervals; Severn contour lines digitised at Edinburgh University and converted to lines.
- Hydrologically corrected elevation grid (DTM):
  - Inputs: 1:5,000 contour maps, spot heights, stream maps, and catchment boundaries derived from photogrammetry.
  - Process: data imported into Arcinfo; TIN created; hydrologically corrected grid derived; resulting Plyn_DEM (GRID, 15 m).
- Individual layers and attributes:
  - Catchment boundaries: names for catchments and subcatchments.
  - River network: node identifiers, length, catchment, type (natural/artificial).
  - Spot heights: elevation values.
  - Elevation contours: Wye and Severn contours at 10/20 m (Wye: HEIGHTS; Severn: HEIGHTS).
  - Soil Parental Materials: soil type code and description.
  - Vegetation map (2013): id, VegClass, Variants (subclasses) to enable flexible use with LCM2000/LCM2007 frameworks.
- Appendix A (Hunting Survey): aerial photo survey details; footprints of frames digitised to preserve data.

## Data quality, gaps, and considerations for use

- Some datasets are unavailable due to ownership restrictions or loss; data completeness varies by dataset.
- Vegetation mapping involved date differences between imagery (2009) and field observations (2013), introducing interpretive differences; final map reconciled with field data and updated to align with LCM2000 classes.
- Severn contour data originated from a separate dataset and required transformation/editing to ensure clean contour lines within the catchment boundary.
- The dataset suite emphasizes GIS readiness for hydrological analysis but users should account for potential legacy data limitations and alignment with contemporary land-cover datasets (LCM2000/LCM2007).

## Appendix and references

- Hunting Survey (1967) aerial photography and subsequent digitisation notes.
- Soil Hydrology of the Plynlimon Catchments (Bell, J.P. 1969) with CEH 2005 update available online.
- CEH project webpages for Plynlimon datasets and related open-access materials.