# Plynlimon Spatial datasets

## Purpose and scope
- Document the Plynlimon experimental catchments (established late 1960s) to study land use impacts on catchment hydrology, especially evaporation, flooding, and low flows.
- Represent two upland land uses in mid-Wales (conifer forestry vs. sheep-grazed grassland) with comprehensive climate, hydrology, soil, and land-use data.
- Provide long-term, high-quality measurements and supporting spatial datasets (maps, soils, vegetation, and hydrology) for analysis and modeling.

## Core data layers and file formats
- Catchment and subcatchment boundaries
  - Shapefile: PlynlimonCatchments.shp
  - Description: upland catchments at the headwaters of the Severn and Wye; subcatchments defined by major tributaries
  - Coordinate system: British National Grid
- River network
  - Shapefile: PlynlimonRiverNetwork.shp
  - Attributes include FNODE_, TNODE_, LENGTH, Catchment, Type (natural or artificial)
- Spot heights
  - Shapefile: PlynlimonSpotHeight.shp
  - Attribute: HEIGHTS (elevation in metres)
- Elevation contours
  - Wye catchment: Plynlimon_WyeElevationContours.shp (10 and 20 m intervals)
  - Severn catchment: Plynlimon_SevernElevationContours.shp (10 m intervals)
- Soil parental materials
  - Shapefile: Plynlimon_SoilParentalMaterials
  - Attributes: SOIL (soil type code), Descript
- Vegetation map
  - Shapefile: Plynlimon_VegetationMap2013
  - Attributes: id, VegClass, Varients (variants)
  - Based on updated CEH Land Cover Map 2000 (LCM2000) plus 2013 field validation; classes aligned with LCM2000
- Hydrologically corrected elevation model
  - Plyn_DEM (GRID)
  - Description: 15 m cell size, floating point; British National Grid; derived as a hydrologically corrected digital terrain model (DTM)
- Metadata and provenance notes
  - All layers use British National Grid; data are produced from historic aerial photography and field surveys, with subsequent digitisation and GIS processing

## Data sources and provenance
- Hunting Survey (1967–1968): large-scale topographic maps and key features (streams, drains, tracks, fences) obtained from aerial photography
- Late 1990s: digitisation of topographic and hydrographic data into GIS layers (elevation, catchment boundaries, river network)
- Soil mapping: Bell, J.P. 1969 (Soil Hydrology of the Plynlimon Catchments); Institute of Hydrology Report No. 8; updated in 2005 by CEH
- Vegetation mapping: updated vegetation map created in 2013 using 2009 aerial photography; field validation in 2013; linked to CEH Land Cover Map 2000
- Severn catchment contours: digitised from maps at Edinburgh University; conversion to continuous contour lines

## Data processing and product creation
- Digitising workflow
  - Shape files created from photogrammetric maps; 10 or 20 m contour points captured and converted to lines; GCPs used for registration
  - Severn contour lines digitised separately at Edinburgh University
- Hydrologically corrected DEM
  - Inputs: 1:5,000 contour maps, spot heights, river network, and catchment boundaries
  - Process: creation of a TIN, then hydrologically corrected grid-based DEM
  - Output: Plyn_DEM (GRID, 15 m)
- GIS workflow and formats
  - Desktop GIS: ArcInfo/ArcGIS environments (ArcInfo digitisation; ArcGIS 10.1 for vegetation mapping)
  - Data are stored as shapefiles and GRID formats with explicit coordinate system (British National Grid)

## Vegetation mapping and integration
- Base layer: updated from CEH LCM2000 to better reflect heath, bracken, and improved grassland
- Classification alignment: conifer plantations reclassified as coniferous woodland; distinct classes include new plantation and felled plantation
- Variant handling: an additional Variants column allows users to treat coniferous plantation as woodland or as felled/new plantation depending on analysis needs
- Field validation: discrepancies between 2009 aerial interpretation and 2013 field observations were recorded and incorporated

## Appendix: A Hunting Survey
- Details of the original airborne survey and its technical specifications
- Film negatives are lost; printed frames have been digitised and rectified to preserve data
- Frame footprints documented to aid data reproduction and provenance

## Governance, access, and stewardship considerations
- Data provenance is well-documented but some datasets from early years were owned by other organisations or are lost; awareness of data lineage is essential
- Some datasets originate from older maps and may require careful interpretation for modern analyses
- Metadata and versioning are critical to manage updates (e.g., vegetation map 2013 update; soil map 1969/2005)
- Access notes indicate availability through CEH resources (e.g., Soil Hydrology of the Plynlimon Catchments CEH publication)
- For data stewardship:
  - Maintain clear metadata for each layer, including data source, date, processing steps, and spatial reference
  - Track lineage from original aerial photography to final GIS layers
  - Preserve historical data while noting any gaps or losses
  - Provide documentation on data limitations, especially for older datasets and any inter-organisational data
  - Ensure interoperability by standardising coordinate system, formats, and class definitions

## Key limitations and considerations for use
- Some historical datasets are missing or held by external organisations; not all initial field surveys are recoverable
- Data reflect dates of acquisition (late 1960s through 2013 updates) and may require careful temporal alignment for time-series analyses
- IPR and data-sharing constraints are relevant when choosing base maps or cross-referencing with other CEH datasets (e.g., LCM2000 vs LCM2007)