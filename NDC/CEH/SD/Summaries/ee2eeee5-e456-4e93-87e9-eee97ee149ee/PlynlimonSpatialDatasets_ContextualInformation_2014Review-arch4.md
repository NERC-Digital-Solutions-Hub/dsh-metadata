# Plynlimon Spatial datasets and associated data products

## Overview
- Long-running experimental catchment study in mid-Wales (headwaters of the Severn and Wye) comparing upland land uses: conifer forestry vs. sheep-grazed grassland.
- Aimed to elucidate land-use impacts on water availability, flooding, low flows, and hydrological processes.
- Data catalogue covers topo-geospatial layers, soils, vegetation, and hydrologically corrected terrain models, with historical and updated components.

## Spatial data assets (layers and grids)
- Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
- River network (PlynlimonRiverNetwork.shp)
- Spot heights (PlynlimonSpotHeight.shp)
- Wye catchment elevation contours (Plynlimon_WyeElevationContours.shp)
- Severn catchment elevation contours (Plynlimon_SevernElevationContours.shp)
- Soil parental materials (Plynlimon_SoilParentalMaterials)
- Vegetation map (Plynlimon_VegetationMap2013)
- Hydrologically corrected elevation grid (Plyn_DEM; GRID, 15 m cells)
- Coordinate system: British National Grid
- Attributes include: catchment names, subcatchment, river segment IDs, lengths, stream type (natural/artificial), heights, contour elevations, soil codes/descriptions, vegetation class codes/descriptions/variants

## Data creation and provenance
- Origin: Hunting survey aerial photography (June 1967) used to produce large-scale topographic maps (1:5000; 1:10000 for both catchments).
- Digitisation: Maps digitised in the late 1990s into GIS (ArcInfo) to create elevation, catchment boundaries, and river networks; contour data for Severn captured at Edinburgh University.
- Hypsography and terrain: Hydrologically corrected digital terrain model (DTM) created from contours, spot heights, stream maps, and catchment boundaries via TIN and GRID conversion.
- Soil data: Soil Hydrology of the Plynlimon Catchments (Bell, 1969; IH Report No. 8) digitised; updated version published by CEH in 2005.
- Vegetation: Vegetation map updated in 2013 (Plynlimon_VegetationMap2013) using 2009 aerial imagery, ArcGIS 10.1 digitising, and ground-truthing (2013); alignment and reclassification with CEH Land Cover Map 2000 (LCM2000).

## Data content and structure details
- DEM and topography:
  - Plynlimon DEM (Plyn_DEM): 15 m grid, floating point, hydrologically corrected, British National Grid.
  - Elevation contours: Wye and Severn layers at 10 m intervals; Severn contours created from Edinburgh University point dataset and cleaned.
- Vector layers:
  - Catchment boundaries and subcatchments defined for upland areas feeding Severn and Wye.
  - River network includes FNODE/ TNODE identifiers, lengths, catchment association, and stream type.
  - Spot heights provide elevation points.
  - Vegetation map (2013) includes classes such as conifer plantations, new/felled plantations, various grassland and heath classes, and woodlands with a Variant field for coniferous plantation differentiation.
  - Soil Parental Materials map codes and descriptions.
- Data lineage and updates:
  - Original topographic maps and layers derived from Hunting Survey data; later GIS-ready layers created in 1990s.
  - Acknowledges data gaps: some field datasets not available due to ownership, and some data may be lost.
  - Vegetation mapping updated to reflect newer classes and to support soil carbon analyses (e.g., SoilTrEC project).

## Data quality, limitations, and governance
- Data availability: not all layers are available in full due to ownership restrictions or data loss; some historical maps are only partially digitised.
- Transcription and artefacts: digitisation introduced potential artefacts; Severn contour lines required care during transformation and editing.
- Temporal alignment: vegetation data reflect 2009 imagery with 2013 field validation; may differ from other timepoints used in analyses.
- Standards and consistency: attempts to harmonise vegetation classes with CEH LCM2000; additional variants provide flexibility for analysis.
- Discoverability and reuse: metadata and dataset descriptions are provided; primary data are hosted via CEH publications/pages; some data sources (e.g., pre-1990s maps) have restricted access or require provenance tracing.

## Relevance to data leadership and strategic use
- Holistic data system view: integration of boundaries, river networks, terrain, soils, and vegetation supports multidisciplinary hydrological analyses and land-use impact assessments.
- User-adjacent data practices: data structured with clear attributes and coordinate systems, enabling reuse for modelling, dissemination, and policy support.
- Data governance considerations: provenance trails, data ownership notes, and updates highlight governance needs around access rights, updates, and cross-institution collaboration.
- Opportunities for collaboration: open data facets exist through CEH portals; potential for expanding co-ownership and community of practice around hydrological and land-use datasets.

## Appendix reference
- Appendix A: Hunting Survey details, including the 1967 aerial survey specifications, frame footprints, and preservation efforts for historical imagery.