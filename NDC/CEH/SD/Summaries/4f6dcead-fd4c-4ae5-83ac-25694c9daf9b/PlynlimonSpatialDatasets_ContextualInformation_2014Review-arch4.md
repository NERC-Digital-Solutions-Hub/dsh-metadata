# INTRODUCTION

## Project aims and study context
- Plynlimon experimental catchments in mid-Wales were established in the late 1960s by the Institute of Hydrology (IH, then part of NERC, now CEH).
- Objective: understand how land use affects catchment water availability, flooding, and low flows; compare two upland land uses—coniferous forestry and sheep-grazed grassland—while keeping other environmental factors as similar as possible.
- Catchments host headwaters of the River Severn and River Wye; long-term, high-quality climatic, streamflow, and soil moisture data exist from the late 1960s; extensive surveys of topography, soils, vegetation, and land use were conducted.

## Data assets and structure
- Spatial datasets (layers):
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil parental materials
  - Vegetation map
- Grid product:
  - Hydrologically corrected elevation grid (Plyn_DEM), 15 m cells, British National Grid, floating point
- Shapefiles and attributes:
  - PlynlimonCatchments.shp (catchment and subcatchment names)
  - PlynlimonRiverNetwork.shp (stream IDs, lengths, catchment, type)
  - PlynlimonSpotHeight.shp (HEIGHTS in metres)
  - Plynlimon_WyeElevationContours.shp (10/20 m contours)
  - Plynlimon_SoilParentalMaterials (SOIL code and Descript)
  - Plynlimon_VegetationMap2013 (VegClass, Variants)
- Volume and scope of data support hydrological and land-use modelling efforts.

## Data creation, digitization, and technical details
- Original data derived from 1967–68 Hunting aerial photography; topographic maps produced at 1:5000 and 1:10000 scales.
- Late 1990s: digitisation of topographic/hydrographic data into GIS (Arcinfo); elevation, catchment, and river networks captured as shapefiles.
- Severn catchment contours digitised at Edinburgh University from 1:5000 maps.
- Hydrologically corrected elevation model created by integrating contours, spot heights, river maps, and catchment boundaries; a TIN was used to derive the hydrologically corrected DTM (Plyn_DEM).
- Coordinate system: British National Grid; data formats primarily shapefiles and Arcinfo grids.
- DEM and layer specifics:
  - Plyn_DEM: 15 m grid, hydro-corrected DEM
  - Catchments and river networks with explicit attributes for downstream/upstream relationships and stream types

## Data provenance, sources, and references
- Primary organisations: Institute of Hydrology (IH) under NERC; later part of CEH.
- Key references:
  - Bell, J.P. 1969. The Soil Hydrology of the Plynlimon Catchments (IH Report No. 8)
  - 2005 CEH revised version of Bell’s soil hydrology
  - CEH publications and project pages for Plynlimon datasets
- Vegetation mapping updates linked to CEH Land Cover Map 2000 (LCM2000) for consistency with CEH models and to avoid IP conflicts with LCM2007.

## Vegetation mapping and updates
- Vegetation map (2013) updated from LCM2000 baseline to incorporate heath, bracken, improved grassland, coniferous variations, and other land-cover classes.
- Methodology:
  - Draft map created by interpreting 2009 aerial photography (Next Perspectives), digitised in ArcGIS 10.1
  - Field validation in 2013; discrepancies recorded and used to refine map
  - Classes aligned with LCM2000; coniferous categories stored with a Variants field to enable flexibility (e.g., conifer woodland vs felled/new plantation)
- Final product: Plynlimon_VegetationMap2013 with class codes and descriptions

## Data gaps, access constraints, and governance
- Some datasets are unavailable due to ownership or intellectual property restrictions; some have been lost.
- Not all data were digitised or fully accessible; Severn contour data had partial digitisation with provenance incomplete.
- Access considerations reflect IP issues (e.g., LCM2007 conflicts) and the need for ongoing data stewardship and licensing clarity.
- Data stewardship emphasis:
  - Maintain provenance and documentation
  - Ensure discoverability and future reuse
  - Align with modelling needs and cross-site comparability

## Appendix context: Hunting Survey
- Appendix A documents the Hunting Survey aerial photography basis (1967); film negatives are lost, but printed frames were digitised to preserve footprints and technical specifications.

## Implications and guidance for Data Leaders
- Preserve long-term, multi-source data with clear provenance and documentation to support hydrological and land-use analyses.
- Maintain a robust data model with consistent coordinate systems, metadata, and versioning to enable reuse across CEH models and cross-site studies.
- Balance historical data with updates (e.g., vegetation reclassification to align with LCM2000) to support accurate modelling and trend analysis.
- Acknowledge data gaps and ownership barriers; plan for data recovery, sharing agreements, and licensing to improve discoverability and collaboration.
- Document data processing pipelines (digitization, DEM creation, feature extraction) to enhance reproducibility and institutional learning.