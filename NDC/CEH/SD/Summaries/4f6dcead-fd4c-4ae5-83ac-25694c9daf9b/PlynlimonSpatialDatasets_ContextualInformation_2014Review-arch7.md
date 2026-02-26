# Plynlimon Spatial datasets

- Context and aim
  - Plynlimon experimental/research catchments established in the late 1960s by the Institute of Hydrology (IH), later CEH, to study how land use affects catchment water availability, flooding, and low flows.
  - Located at the headwaters of the River Severn and the River Wye in upland mid-Wales; representative land uses are coniferous forestry and sheep-grazed grassland.
  - Intensive instrumentation and long-term records of climatic parameters, streamflow, and soil moisture; surveys of physical characteristics (topography, soils, land use) underpin the spatial datasets.

- What the spatial datasets comprise
  - Layers
    - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
    - River network (PlynlimonRiverNetwork.shp)
    - Spot heights (PlynlimonSpotHeight.shp)
    - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
    - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
    - Soil parental materials (Plynlimon_SoilParentalMaterials)
    - Vegetation map (Plynlimon_VegetationMap2013)
  - Hydrologically corrected elevation grid (Plynlimon DEM)
    - File: Plyn_DEM
    - Format: GRID, 15 m cell size, floating point, British National Grid
    - Purpose: hydrologically corrected digital terrain model for the catchments
  - Notes on data lineage and formats (mostly ArcInfo/ArcGIS shapefiles; one GRID DEM)

- Source maps and data origins
  - Hunting survey (1967) aerial photography underpinning large-scale topographic maps
  - Topographic maps produced at 1:5000 (2.5 m contours) and 1:10000 scales
  - Ground surveys for soils, geology, vegetation, and land use
  - Some datasets are unavailable due to data ownership/IP issues or loss
  - Soil Parental Materials map originates from JP Bell’s 1969 Soil Hydrology Study (IH Report No. 8); a 2005 CEH revision is provided

- Digitising and data creation workflow
  - Digitisation of most layers in the late 1990s from 1:5000 topographic maps
  - Data captured with GCPs using CALCOMP digitising tablet; elevation points and 10/20 m contours converted to Arcinfo coverages
  - Severn catchment contour lines digitised at Edinburgh University (points converted to lines; later cleaned and merged)
  - Hydrologically corrected DEM produced by:
    - Importing contour maps, spot heights, stream maps, and catchment boundaries into ArcInfo
    - Building a TIN and deriving a hydrologically corrected grid (Plyn_DEM)
  - Data products and file naming conventions:
    - Catchment boundaries: PlynlimonCatchments.shp
    - River network: PlynlimonRiverNetwork.shp
    - Spot heights: PlynlimonSpotHeight.shp
    - Wye elevation contours: Plynlimon_WyeElevationContours.shp
    - Severn elevation contours: Plynlimon_SevernElevationContours.shp
    - Soil parental materials: Plynlimon_SoilParentalMaterials
    - Vegetation map (2013): Plynlimon_VegetationMap2013
    - DEM: Plyn_DEM (British National Grid)

- Vegetation mapping and methodology
  - Base: CEH Land Cover Map 2000 (LCM2000) used due to standard model compatibility and IP considerations
  - Update to include heath, bracken, and improved grassland; align classes with LCM2000
  - Data creation workflow:
    - Draft vegetation map created by interpreting broad classes from 2009 aerial photography
    - On-screen digitising in ArcGIS 10.1 with 2009 imagery; field verification in 2013
    - Adjustments after field observations (e.g., felled vs new plantations; shade artifacts in imagery)
    - Final map edited against digital aerial backdrop; features added (e.g., water features, inland bare ground)
  - Vegetation map details
    - Shapefile: Plynlimon_VegetationMap2013
    - Attributes: id (class code), VegClass (description), Variants (subclass descriptions)
  - Classes include conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, inland water
  - Special feature: Variants column allows users to treat coniferous plantations as woodland or as felled/new plantations for flexibility

- Contours and hydrology specific notes
  - Severn elevation contours derived from Edinburgh University data; converted to lines, edited, and clipped to Severn boundary
  - Wye elevation contours provided similarly; 10 and 20 m intervals

- Appendix A: Hunting Survey
  - Aerial survey from Hunting Survey Ltd (June 1967)
  - Film negatives largely lost; printed frames digitised and rectified; footprints of frame blocks documented

- Technical references and access
  - Initial aims and data context described in Brandt et al. 2004
  - Soil hydrology details available in Bell, J.P. 1969; updated CEH version 2005
  - CEH project pages for Plynlimon datasets and related updates
  - Acknowledgement of data provenance, data quality considerations, and potential gaps due to varying data sources and rights

- Practical considerations for GIS work
  - Coordinate system: British National Grid
  - Data formats: shapefiles and GRID DEM
  - Some datasets are incomplete or missing due to ownership or loss; care needed when integrating with other data
  - Vegetation map updated to align with CEH LCM2000 standards and used to support soil carbon analysis and related modeling
  - Provenance notes important for reproducibility and re-use in hydrological and land-use studies