# Plynlimon Spatial datasets

- Overview
  - Plynlimon experimental/research catchments in mid-Wales, connecting to the headwaters of the River Severn and River Wye.
  - Purpose: understand how upland land use (conifer forestry vs sheep-grazed grassland) affects catchment water availability, flooding, and low flows, using long-term, high-quality climatic, hydrological, and spatial data.
  - Datasets support standardised monitoring outputs and cross-dataset analyses; aimed at storing and providing access to underlying data for scrutiny and reuse.

- Spatial data layers (Plynlimon Spatial datasets)
  - Catchment and subcatchments boundaries
  - River network
  - Spot heights
  - Wye catchment elevation contours
  - Severn catchment elevation contours
  - Soil Parental Materials
  - Vegetation map
  - Hydrologically corrected elevation grid (Plynlimon DEM)

- Data formats and coordinate system
  - File types: shapefiles (boundaries, river network, spot heights, vegetation, contours, soils) and GRID (Plyn_DEM)
  - Coordinate system: British National Grid
  - DEM characteristics: 15 m cell size, hydrologically corrected

- Data provenance and digitisation
  - Initial data from large-scale topographic maps derived from the Hunting aerial survey (1967)
  - 1990s: maps digitised into GIS layers (Arcinfo); elevation, boundaries, river network extracted
  - Severn catchment contours captured separately (Edinburgh University)
  - Some datasets (especially some field-survey data) are missing or held by other organisations
  - Soil hydrology map from JP Bell (1969); IH Report No. 8; revised 2005 by CEH
  - Vegetation map updated in 2013, based on 2009 aerial photography and 2013 ground-truthing

- Topography and hydrography details
  - Topographic maps at 1:5000 (contours 2.5 m) and 1:10000; 1968 references
  - Catchment/subcatchment boundaries derived from elevation data
  - River network includes natural and artificial (man-made) streams
  - Spot heights and contour lines documented for Wye and Severn catchments

- Soils and vegetation
  - Soil Parental Materials map linked to Bell’s 1969 soil hydrology study; descriptions of soil types included
  - Vegetation map (2013): mapped classes include conifer plantation, new/felled plantation, various grasslands, heath, bracken, bare ground, woodland, water; aligned with CEH Land Cover Map 2000
  - Vegetation dataset supports use in soil property analyses and related research

- Data processing and workflow highlights
  - Digitising workflow used CALCOMP digitising table and Arcinfo; GCPs used for georeferencing
  - 10–20 m contour capture from 1:5000 maps; Severn contours captured as line features
  - Hydrologically corrected DEM produced via TIN interpolation and subsequent DEM creation
  - Appendix A documents Hunting Survey data and footprint rectification efforts

- Access, limitations, and references
  - Some datasets are not available due to ownership/IP constraints; others may be lost
  - A revised soil hydrology map (Bell 1969) is available via CEH (2005 edition)
  - Primary CEH website pages provide further information and downloadable publications

- Relevance for environmental monitoring
  - Provides a standardized, long-term spatial framework for hydrology, land use, soils, and vegetation analyses
  - Enables integrated analyses of land-use impacts on water availability, flood risk, and low-flow conditions
  - Supports reproducible GIS workflows and potential data portal deposition for broader access and reuse