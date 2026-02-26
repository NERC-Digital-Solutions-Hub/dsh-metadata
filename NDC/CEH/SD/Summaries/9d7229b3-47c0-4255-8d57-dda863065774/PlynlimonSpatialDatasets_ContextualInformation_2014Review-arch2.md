# Plynlimon Spatial datasets

- Introduction and aim
  - The Plynlimon experimental catchments (late 1960s) were established by the Institute of Hydrology (IH) under NERC, later part of CEH.
  - Main aim: understand how land use affects catchment water availability, flooding, and low flows downstream.
  - Two adjacent catchments represent upland Wales’ two major land uses: coniferous forestry and sheep-grazed grassland, designed to be similar in other respects.
  - Intensive instrumentation yielded long-term hydrological and climatic records; surveys mapped physical characteristics and land use; datasets include numerous thematic maps.

- Spatial data that comprise the Plynlimon dataset
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil parental materials
  - Vegetation map
  - Plynlimon hydrologically corrected elevation grid (DTM/DEM)

- Source maps and digitisation history
  - Initial large-scale topographic maps produced from the Hunting survey (1967-68 aerial photography).
  - Late 1990s: topographic and hydrographic data digitised into GIS layers (elevation/DTM, catchment boundaries, river network) from 1:5000 maps.
  - Some field data (e.g., certain soils datasets) are unavailable due to ownership or loss; notable exception is the 1969 Soil Hydrology study (Bell 1969) map, IH Report No. 8 (updated 2005 by CEH).

- Topography and hydrology
  - Photogrammetric derivation of 1:5000 scale topographic maps with 2.5 m contour interval; 1:10000 scale maps also produced.
  - Hydrologically corrected digital terrain model (DTM) created by building a TIN from contour, spot height, stream maps, and catchment boundaries, then deriving a hydrologically corrected grid.
  - Plynlimon DEM details:
    - Name: Plyn_DEM
    - Format: GRID
    - Cell size: 15 m
    - Coordinate system: British National Grid
    - Purpose: hydrologically corrected DEM for catchments

- Datasets and shapefiles (structure and content)
  - PlynlimonCatchments.shp
    - British National Grid
    - Contains catchment and subcatchment boundaries with attributes: Catchment, Subcatch
  - PlynlimonRiverNetwork.shp
    - British National Grid
    - Attributes include FNODE_ID, TNODE_ID, LENGTH, Catchment, Type (natural or artificial)
  - PlynlimonSpotHeight.shp
    - British National Grid
    - Attribute: HEIGHTS (elevation in metres)
  - Plynlimon_WyeElevationContours.shp
    - British National Grid
    - Attributes: HEIGHTS (contour elevation in metres)
  - Plynlimon_SoilParentalMaterials
    - British National Grid
    - Attributes: SOIL (code), Descript (description)
  - Plynlimon_VegetationMap2013
    - British National Grid
    - Attributes: id, VegClass, Varients
  - Plynlimon_SevernElevationContours.shp
    - British National Grid
    - Attributes: HEIGHTS (contour elevation in metres)

- Vegetation mapping and interpretation
  - Updated vegetation map (2013) created to support soil carbon surveys (top 30 cm, 2012, SoilTrEC) and to align with CEH Land Cover Map 2000 (LCM2000).
  - Process: draft vegetation classes derived from 2009 aerial photography, digitised in ArcGIS 10.1, field-verified via ground truthing (2013).
  - Classes include conifer plantation, new/felled plantation, rough acid grass, bracken, heath, improved grassland, bare ground, deciduous woodland, water, etc.
  - Reclassification and variants accommodate flexibility in representing coniferous areas (woodland vs felled/new plantation).

- Appendix and background
  - Appendix A: Hunting Survey
    - Aerial photography survey by Hunting Survey Ltd (June 1967) forming the basis for primary topographic frames.
    - Printed frame footprints have been digitised and rectified to preserve the data; film negatives are lost.
  - Acknowledgement of dating and versioning of basemaps and the evolution of data products.

- Data management, accessibility, and challenges
  - Data quality and provenance: extensive long-term records; some datasets unavailable due to ownership or loss; SoilHydrology (Bell 1969) remains a key reference.
  - Data modernization: digitisation and GIS integration in the late 1990s, migration to ArcInfo/ArcGIS platforms.
  - Challenges highlighted for analysts:
    - Increasing the value of datasets by integrating with other relevant data beyond single-use outputs.
    - Enabling access to underlying data used to create final outputs, improving transparency and reusability.

- Relevant links for additional information
  - CEH project pages on Plynlimon: CEH website and CEH science news blog (about Plynlimon catchments as an open-air lab).