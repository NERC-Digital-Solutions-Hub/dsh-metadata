# Plynlimon Spatial Datasets and Associated Maps

- Overview
  - Plynlimon experimental catchments were established in the late 1960s by the Institute of Hydrology (IH), part of NERC, later CEH.
  - Purpose: study how land use affects catchment water availability, flooding, and low flows; two adjacent catchments represent coniferous forestry and sheep-grazed grassland with similar other environmental characteristics.
  - Datasets span hydrology, climate, topography, soils, and land cover, with long-term high-quality measurements since the late 1960s.

- Datasets and data layers
  - Spatial datasets (layers):
    - Catchment and subcatchment boundaries
    - River network
    - Spot heights
    - Wye catchment contour lines
    - Severn catchment contour lines
    - Soil Parental Materials
    - Vegetation map
  - A hydrologically corrected elevation grid (DTM/DEM) derived for hydrological analyses
  - Topographic and terrain information largely derived from aerial photography and subsequent digitisation

- Data sources and provenance
  - Original data from Hunting survey aerial photography (1967–68) used to produce topographic maps and identify key features (streams, drains, tracks, fences).
  - In the late 1990s, topographic and hydrographic data digitised into GIS layers (elevation, catchment boundaries, river network).
  - Field surveys in early years mapped soils, geology, vegetation, and land use; some datasets owned by other organisations or lost.
  - Soil Hydrology of the Plynlimon Catchments (Bell, 1969) provided the soil parent materials map; updated edition published 2005 by CEH.
  - Vegetation mapping updated in 2013–2014 (Vegetation Map 2013) to align with CEH Land Cover Map 2000 (LCM2000) and support SoilTrEC project analyses (e.g., soil carbon surveys).

- Data formats, structure, and metadata
  - DEM/DTM:
    - Plyn_DEM GRID, 15 m cell size, floating point, British National Grid
    - Hydrologically corrected model derived from 1:5000 contours, spot heights, streams, and catchment boundaries
  - Vector shapefiles (British National Grid):
    - PlynlimonCatchments.shp (catchment and subcatchments)
    - PlynlimonRiverNetwork.shp (FNODE, TNODE, LENGTH, Catchment, Type)
    - PlynlimonSpotHeight.shp (HEIGHTS)
    - Plynlimon_WyeElevationContours.shp (HEIGHTS, 10 and 20 m intervals)
    - Plynlimon_SoilParentalMaterials (SOIL, Descript)
    - Plynlimon_VegetationMap2013 (id, VegClass, Varients)
    - Plynlimon_SevernElevationContours.shp (HEIGHTS)
  - Elevation and contour data were derived from aerial photogrammetry and digitised maps; some processes (e.g., Severn contours) involved multiple institutions (Edinburgh University) and later editing for artefacts.
  - Many datasets document their coordinate system (British National Grid) and attributes to support data discovery and reuse.

- Processing and quality assurance
  - Topographic maps were produced at 1:5000 (2.5 m contours) and 1:10000 scales; vertical accuracy linked to contour intervals and spot heights.
  - Hydrologically corrected DEM created by constructing a TIN from digitised data and deriving a DEM with hydrological corrections; a flow diagram (Figure 1) describes the production workflow.
  - Digitising workflow:
    - CALCOMP digitising table with ground control points (GCPs) for registration
    - Elevation points and contour lines captured at 10–20 m intervals
    - ArcInfo used for data handling; formats converted to ArcInfo coverages and shapefiles
  - Vegetation mapping method:
    - Draft vegetation map created via interpretation of 2009 aerial photography (Next Perspectives) with ArcGIS 10.1
    - Field verification in 2013–2014, adjusting classifications to align with LCM2000
    - Final map supports CEH soil and carbon studies and allows variants for coniferous plantations (to distinguish current vs. felled/new plantations)
  - Quality notes:
    - Some datasets are incomplete due to data ownership, loss, or non-interoperable formats
    - Historical vs. modern data differences acknowledged (e.g., date of imagery vs. field observations)

- Vegetation and land cover context
  - Vegetation categories include conifer plantations, new and felled plantations, rough acid grass, bracken, heath, improved grassland, bare ground, deciduous woodland, and water features
  - Updated vegetation map 2013 uses LCM2000 classes for consistency with CEH models; 2014 update integrated ground-truth observations

- Appendix A: Hunting Survey
  - Details the aerial survey conducted by Hunting Survey Ltd in June 1967
  - Documented frame footprints, with film negatives lost but printed frames digitised and rectified to preserve data
  - Provides context for historical data provenance and spatial extents of the original imagery

- Implications for data stewardship and governance
  - Provenance and lineage: long-running project with multiple data generations; essential to maintain clear metadata on data origins, processing steps, and version history
  - Data quality and interoperability: hydrologically corrected elevation model and standardized coordinate system facilitate cross-layer analyses; some datasets require careful handling due to ownership, updates, or incomplete records
  - Access and reuse: document references to CEH publications for soils and data sharing; some materials may be limited by IP or external ownership
  - Maintenance and updates: vegetation maps updated to align with CEH models; ongoing potential for updates as new imagery and field data become available
  - Documentation needs: ensure comprehensive metadata for each layer, including data source, date, method, scale, accuracy, and any known limitations to support discovery and reuse by researchers and data stewards