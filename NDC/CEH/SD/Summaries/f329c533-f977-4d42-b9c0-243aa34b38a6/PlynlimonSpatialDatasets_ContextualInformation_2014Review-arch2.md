# Plynlimon Catchments Spatial Datasets

- Purpose and context: The Plynlimon experimental catchments in mid-Wales were established to study how upland land use (coniferous forestry vs sheep-grazed grassland) affects catchment water availability, flooding, and low flows. The two adjacent catchments feed the headwaters of the River Severn and River Wye and were densely instrumented with long-term climatic, hydrological, soil moisture, and land-use data.
- Core aim for analysis: Provide consistent, long-term environmental baselines that support monitoring of environmental health and policy performance over time, with standardized outputs suitable for comparison, reporting, and modeling.

Key datasets and outputs

- Spatial data layers (PlynlimonSpatial datasets)
  - Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
  - River network (PlynlimonRiverNetwork.shp)
  - Spot heights (PlynlimonSpotHeight.shp)
  - Wye catchment elevation contours (Plynlimon_WyeElevationContours.shp)
  - Severn catchment elevation contours (Plynlimon_SevernElevationContours.shp)
  - Soil parental materials (Plynlimon_SoilParentalMaterials)
  - Vegetation map (Plynlimon_VegetationMap2013)
- Hydrological surface model
  - Hydrologically corrected elevation grid (Plyn_DEM, GRID, 15 m cell size)
- Data characteristics
  - Coordinate system: British National Grid
  - Vector and grid formats suitable for GIS analysis (Arcinfo/ArcGIS)
  - Attributes described for river network (node IDs, length, catchment, type) and vegetation classes (VegClass, Variants)
- Vegetation mapping
  - Updated vegetation map (2013) developed from 2009 aerial photography and refined to CEH Land Cover Map 2000 (LCM2000) classes; supports better integration with soil carbon analyses and hydrological modeling
- Data provenance and processing
  - Original topographic maps from Hunting Survey (1967) created via photogrammetry; later digitised in the 1990s
  - Soil hydrology map (Bell, 1969) updated in 2005 by CEH
  - DEM created by integrating 1:5000 and 1:10000 contours, spot heights, river maps, and catchment boundaries; hydrologically corrected via TIN-to-grid workflow
- Accessibility and formats
  - Data stored as shapefiles and GRID DEM; descriptions and attributes provided for reuse
  - Appendix A documents the Hunting Survey and data lineage

Data sources, history, and processing workflow

- Topography
  - 1:5000 scale maps (contours at 2.5 m) and 1:10000 scale maps produced from 1967–68 aerial photography
  - Contours digitised from maps; Severn contours captured separately
- Hydrography and boundaries
  - Catchment and subcatchment boundaries digitised from topographic maps; river network derived from maps
- Soils
  - Bell’s Soil Hydrology study (1968–1969) produced a soil parental materials map; IH Report No. 8; CEH updated version (2005)
- Digitising and GIS
  - Data digitised into Arcinfo; CALCOMP digitising table used; ground control points deployed for georeferencing
  - Severn contour lines digitised at Edinburgh University from 1:5000 maps
- Hydrologically corrected DEM
  - Integrated inputs to produce a hydrologically corrected DTM/DEM (Plyn_DEM) at 15 m resolution
- Vegetation mapping approach
  - Draft vegetation classified in ArcGIS 10.1 from 2009 aerial photos; field validation in 2013; map refined to match LCM2000 classes; conifer-related classes reclassified into woodland with an additional Variants field to capture plantation status

Data accessibility, gaps, and considerations

- Data gaps and caveats
  - Some datasets are not available due to ownership restrictions or loss
  - Ongoing alignment of legacy classifications with modern CEH schemes (e.g., LCM2000) to enable consistent analyses
- Access and reuse
  - Outputs are designed for clear presentation (maps, charts) and for integration with other environmental datasets
  - Underlying data are intended to be accessible for reuse and cross-dataset analyses, aligning with standard monitoring practices

Relevance for Analysts Monitoring the Environment

- Provides a robust, long-term baseline for evaluating land-use effects on hydrology, flood risk, and water availability
- Uses standardized GIS formats and a documented data lineage to support quality assurance, traceability, and reproducibility
- Enables cross-dataset analyses by offering interoperable layers (catchments, river networks, contours, soils, vegetation) and a hydrologically corrected DEM for hydrological modeling
- Facilitates data integration with external datasets to extend the value of the monitoring datasets beyond single-use applications

Appendix and references

- Appendix A: Hunting Survey details (1967 aerial photography technical specifications and frame footprints)
- Foundational references: Brandt et al. (2004) on the project aim; Bell (1969) on soil hydrology; CEH publications and CEH Land Cover Map 2000 documentation

Operational note for ongoing monitoring

- Maintain data quality through standard QA, data cleaning, and transformation practices
- Store and publish datasets via appropriate portals to ensure broad accessibility and reuse
- Continue harmonizing legacy datasets with current classification schemes and explore combining these datasets with other relevant environmental data to enhance analytical value and policy insight