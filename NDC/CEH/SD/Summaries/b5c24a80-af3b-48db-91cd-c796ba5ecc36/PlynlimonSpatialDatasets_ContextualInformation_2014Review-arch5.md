INTRODUCTION

- Purpose and context
  - The Plynlimon experimental/research catchments were established in the late 1960s by the Institute of Hydrology (IH, later CEH) to study how upland land use affects catchment water availability, flooding, and low flows.
  - Two adjacent catchments represent the two major upland land uses in Wales: coniferous forestry and sheep-grazed grassland, chosen to be as similar as possible in other environmental respects.
  - The catchments were heavily instrumented with long-term climatic and hydrological records; surveys also captured spatial characteristics (topography, soils, land use) and several thematic maps.

- Data landscape and governance relevance
  - Datasets comprise spatial layers, elevation data, soils, vegetation, and historic topographic maps digitized for GIS analysis.
  - Some datasets are owned by other organisations or have rights/issues that limit availability; some data have been lost.
  - Historical data sources include the Hunting aerial survey and the 1969 Bell soil hydrology study; later CEH updates and publications provide revised metadata and access points.
  - Data were created and maintained with long-term monitoring in mind, enabling reuse for hydrological and land-use research.

DATASETS AND DATA PRODUCTS

- Spatial data layers (Plynlimon Spatial datasets)
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
    - Coordinate system: British National Grid
    - Attributes: Catchment, Subcatch
  - River network (PlynlimonRiverNetwork.shp)
    - Attributes: FNODE, TNODE, LENGTH, Catchment, Type (natural or artificial)
  - Spot heights (PlynlimonSpotHeight.shp)
    - Attribute: HEIGHTS (elevation in metres)
  - Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
    - Attributes: HEIGHTS (metres)
  - Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
    - Attributes: HEIGHTS (metres)
  - Soil Parental Materials (Plynlimon_SoilParentalMaterials)
    - Attributes: SOIL (soil type code), Descript
  - Vegetation map (Plynlimon_VegetationMap2013)
    - Attributes: id, VegClass, Varients
  - Hydrologically corrected elevation grid (DEM)
    - Plyn_DEM (GRID, 15 m cells, British National Grid, float)
    - Description: hydrologically corrected digital terrain model of the catchments
- Data characteristics and usage
  - Datasets derived from a combination of historical maps, field surveys, and modern GIS processing (Arcinfo/ArcGIS environments).
  - Used to support hydrological analyses, soil-vegetation interactions, and landscape characterization in studies like SoilTrEC.
  - Vegetation map update (2013) aligned with CEH Land Cover Map 2000 classes; includes reclassification and a Variants field to balance use with LCM2000 classes and to accommodate distinctions like felled/new plantations.

DATA CREATION, PROVENANCE, AND METHOD

- Source maps and digitization
  - Initial base: large-scale topographic maps from the Hunting aerial photography survey (1967).
  - Late 1990s: topographic and hydrographic data digitised into GIS layers (elevation-derived DTM, catchment boundaries, river network).
  - Some early datasets mapped by field surveys for soils, geology, vegetation, and land-use; ownership restrictions and data losses affected availability.
  - Severn catchment contours digitized by Edinburgh University from 1:5000 maps; manual cleaning and line construction performed in ArcGIS.

- Hydrologically corrected elevation data
  - DEM created from 1:5,000 contour maps, spot heights, stream maps, and catchment boundaries.
  - Process: data imported into Arcinfo, TIN created, then hydrologically corrected grid-based DTM produced.
  - Output: Plyn_DEM (GRID, 15 m, British National Grid).

- Vegetation and land cover
  - 2013 vegetation map created by photo-interpretation of 2009 aerial photography, with 2013 field verification.
  - Base class mapping drew from CEH Land Cover Map 2000 (LCM2000); updates allowed better representation of heath, bracken, improved grassland, and conifer-related classes.
  - Final map (Plynlimon_VegetationMap2013) supports analysis of soil properties and vegetation interactions; includes an optional Variants field for flexible use of coniferous classifications (woodland vs. felled/new plantation).

- Appendix: Hunting Survey
  - Aerial survey conducted by Hunting Survey Ltd (June 1967); film negatives are largely lost, but printed frames have been digitised/rectified to preserve data.
  - Footprints of aerial frames documented for reference.

BACKGROUND AND DOCUMENTATION

- Historical references and related materials
  - Bell, J.P. (1969) The Soil Hydrology of the Plynlimon Catchments (IH Report No. 8); updated 2005 CEH edition available online.
  - Acknowledgement of data provenance and connections to IH/NERC CEH programs and the SoilTrEC project for context on soil-vegetation interactions.
  - CEH provides links to publications and data products related to Plynlimon datasets.

DATA ACCESS, LIMITATIONS, AND GOVERNANCE CONSIDERATIONS

- Data availability and rights
  - Some datasets are owned by other organisations or are not available due to IP or rights restrictions.
  - Certain early datasets are unavailable or partially lost, which can impact replication or full re-use.
- Data quality and lineage
  - Datasets build on long-term measurements and well-documented digitization processes; provenance is recorded (Hunting Survey, Bell 1969, IH reports, CEH updates).
  - Vertical and horizontal accuracy tied to 1:5000 topographic sources and subsequent DEM creation methods; contour lines and grid data reflect metadata from original surveys and digitization steps.
- Metadata and interoperability
  - Datasets use British National Grid coordinates; standard shapefile formats and ArcGIS-compatible structures support interoperability.
  - Vegetation classification aligns with LCM2000 classes with explicit reclassifications and an optional Variants field to maintain compatibility with other CEH models.
- Updates and maintenance
  - The vegetation layer was updated in 2013; other components reflect the digitization and processing performed in the project’s timeframe.
  - Data custodianship appears to be CEH with links to public CEH resources; some datasets may require permission or special access due to ownership.

APPENDIX AND ADDITIONAL NOTES

- Appendix A: Hunting Survey
  - Details technical specifications of the 1967 aerial survey; footprints of frames are documented to support georeferencing of original topographic data.

End of summary.