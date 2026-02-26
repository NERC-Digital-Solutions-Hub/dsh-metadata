# Plynlimon Spatial datasets

- A historical GIS-focused inventory of spatial datasets from the Plynlimon experimental catchments, the headwaters of the River Severn and River Wye in mid-Wales, prepared to study land-use impacts on hydrology and water status.
- Two primary upland land uses represented: coniferous forestry and sheep-grazed grassland; datasets span topography, soils, vegetation, hydrography, and catchment boundaries, with long-term climatic and hydrological records behind them.

## Core datasets and layers (GIS-ready)

- Catchment and subcatchment boundaries
  - Shapefile: PlynlimonCatchments.shp
  - Coordinate system: British National Grid
  - Description: Upland catchments and subcatchments drained by major tributaries.
- River network
  - Shapefile: PlynlimonRiverNetwork.shp
  - Attributes include FNODE_, TNODE_, LENGTH, Catchment, Type (natural or artificial).
- Spot heights
  - Shapefile: PlynlimonSpotHeight.shp
  - Attribute: HEIGHTS (metres)
- Wye catchment contour lines
  - Shapefile: Plynlimon_WyeElevationContours.shp
  - Attribute: HEIGHTS (metres); contours at 10 and 20 m intervals
- Severn catchment contour lines
  - Shapefile: Plynlimon_SevernElevationContours.shp
  - Attribute: HEIGHTS (metres); contours at 10 m intervals
- Soil parental materials
  - Shapefile: Plynlimon_SoilParentalMaterials
  - Attributes: SOIL (code), Descript (description)
- Vegetation map
  - Shapefile: Plynlimon_VegetationMap2013
  - Attributes: id, VegClass, Varients (Variant descriptions)
  - Description: Updated 2013 vegetation classes based on 2009 aerial imagery and 2013 ground-truthing; linked to CEH Land Cover Map 2000 (LCM2000) classes; supports integration with soil carbon studies
- Hydrologically corrected elevation grid (DTM)
  - Plyn_DEM
  - Format: GRID; Cell size: 15 m; Pixel type: floating point
  - Coordinate system: British National Grid
  - Description: Hydrologically corrected digital terrain model (DTM) for Plynlimon catchments
- Background topo datasets and derivatives
  - Hydrologically corrected DTM derived from 1:5,000 contour maps, spot heights, stream maps, and catchment boundaries
  - Source topography and contours used to derive hydrologically corrected elevation surfaces

## Data provenance and sources

- Hunting Survey (1967)
  - Large-scale topographic maps produced from aerial photography; basis for initial cartography and subsequent digitising.
- Late 1990s digitisation
  - Topographic and hydrography data digitised into GIS layers (elevation, catchment boundaries, river network) using Arc/Info; registration via ground control points.
- Soil and geology
  - JP Bell’s Soil Hydrology Study (1968–1969); IH Report No. 8; soil parental materials map digitised in the late 1990s; updated 2005 CEH version available.
- Field surveys (early years)
  - Maps of soils, geology, vegetation, and land use; some datasets not available due to ownership or loss.
- Vegetation mapping (2013)
  - Photo-interpretation of 2009 aerial photography with 2013 field verification; integration with LCM2000 classes and updates to reflect conifer/woodland dynamics and land cover changes.
- Aerial survey appendix
  - Appendix A describes Hunting Survey details, frame footprints, and data preservation efforts.

## Data creation and GIS workflow

- Topography from photogrammetry
  - 1:5,000 and 1:10,000 scale topographic maps with 2.5 m contour intervals derived from 1967–68 aerials.
- DEM development
  - Creation of a TIN from contour, spot heights, streams, and boundaries; generation of the hydrologically corrected grid (Plyn_DEM) at 15 m resolution.
- Digitising and GIS formats
  - Most layers saved as ArcInfo/ArcGIS-compatible shapefiles; DEM stored as GRID format; Severn contours digitised separately at Edinburgh University from 1:5,000 maps and later converted to lines.
- Data quality and gaps
  - Some datasets are incomplete or withheld by other organisations; some historical maps and data have been lost or are not available at this time.

## Vegetation mapping details

- Purpose
  - Provide a broad vegetation class map to identify soil survey boundaries for SoilTrEC analyses; aligned with LCM2000 as a baseline to minimize IPR conflicts.
- Method and classes
  - Draft map created from 2009 aerial photographs; refined through ArcGIS 10.1 digitising with backdrop imagery; field checks conducted along catchment track networks.
  - Classes include conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, and inland water.
- Classification and variants
  - Classes aligned with LCM2000; conifer-related classes include a Variants field to accommodate different interpretations (conifer woodland vs. felled/new plantation).

## Appendix: Hunting Survey background

- Aerial photography survey performed by Hunting Survey Ltd in June 1967.
- Film negatives are largely lost; printed frames have been digitised and rectified by CEH to preserve footprint data.

End note: The collection provides GIS-ready spatial layers and metadata (coordinate system, data lineage, and creation methods) for analysis of land use, hydrology, soils, and vegetation in the Plynlimon catchments, with particular attention to hydrologically corrected elevation data and vegetation mapping aligned to CEH standards.