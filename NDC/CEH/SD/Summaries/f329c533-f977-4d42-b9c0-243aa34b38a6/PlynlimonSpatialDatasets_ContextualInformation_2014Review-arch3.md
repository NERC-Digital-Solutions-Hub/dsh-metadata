# Plynlimon Catchments Spatial Datasets

- The Plynlimon experimental/research catchments were established in the late 1960s by the Institute of Hydrology (IH), part of NERC, now within CEH.
- Primary aim: understand how land use affects catchment water availability, flooding, and low flows; compare upland land uses (coniferous forestry vs. sheep-grazed grassland) using two adjacent catchments (headwaters of the River Severn and River Wye in mid-Wales).
- The catchments have been intensively instrumented with long-term climatic, hydrological, and soil moisture records, alongside surveys of physical characteristics (topography, soils, land use) and several thematic maps.
- Datasets support analysis of land-use effects on hydrology and provide a basis for monitoring and policy evaluation.

## Spatial datasets included

- Catchment and subcatchment boundaries (PlynlimonCatchments.shp)
- River network (PlynlimonRiverNetwork.shp)
- Spot heights (PlynlimonSpotHeight.shp)
- Wye catchment contour lines (Plynlimon_WyeElevationContours.shp)
- Severn catchment contour lines (Plynlimon_SevernElevationContours.shp)
- Soil parental materials (Plynlimon_SoilParentalMaterials)
- Vegetation map (Plynlimon_VegetationMap2013)
- Hydrologically corrected elevation grid (Plyn_DEM; 15 m cell size; British National Grid)
- Background datasets include topographic maps and aerial photography-derived layers from 1967–68 Hunting Survey

## Data creation and processing workflow

- Topographic maps created from the Hunting aerial photography survey (1967–1968) at 1:5000 and 1:10000 scales.
- In the late 1990s, topographic and hydrological data digitised into GIS layers (elevation, catchments, river network).
- Hard-copy maps digitised using CALCOMP digitising tables; ground control points used for registration; elevation and contour data captured at 10–20 m intervals; data stored as ArcInfo coverages.
- Severn catchment contour lines digitised at Edinburgh University with 10 m interval points later converted to lines and cleaned.
- Hydrologically corrected DEM created by integrating contours, spot heights, streams, and catchment boundaries, generating a TIN and a hydrologically corrected GRID (Plyn_DEM, 15 m, floating point).
- Metadata and attributes maintained in each shapefile, enabling downstream analysis and visualization.

## Datasets and attributes

- Catchment and subcatchments: names of catchments/subcatchments.
- River network: upstream/downstream node IDs, segment length, catchment association, type (natural or artificial).
- Spot heights: elevation in metres.
- Contour lines (Wye and Severn): elevation values (10 or 20 m intervals for Wye; 10 m intervals for Severn).
- Soil parential materials: soil type code and description.
- Vegetation map (2013): vegetation class code, description, and variant descriptions; updated from CEH Land Cover Map 2000 to include heath, bracken, improved grassland, etc.; linked to LCM2000 classes and allows flexible use of conifer classifications via a Variants field.
- DEM: hydrologically corrected digital terrain model (Plyn_DEM), 15 m grid, British National Grid, used for hydrological analysis.

## Vegetation mapping approach

- Supported by vegetation classes aligned with LCM2000 (updated to reflect local variation: conifer plantation, new plantation, felled plantation, rough acid grass, bracken, open dwarf shrub heath, improved grassland, inland bare ground, deciduous woodland, inland water).
- Draft map created via ArcGIS 10.1 using 2009 aerial photography as a base, refined through 2013 field observations and ground truthing.
- Differences between aerial interpretation and field observations addressed; final map integrates, edits, and adds features observed in the field (e.g., water features, bare ground).
- The map is designed to support soil carbon analyses and to be compatible with CEH data standards, with a Variant field to accommodate plantation status.

## Data provenance, access, and limitations

- Some data are owned by other organisations or have been lost; not all historical datasets are fully accessible.
- A revised Soil Hydrology study (Bell, 1969; IH Report No. 8) was updated by CEH in 2005 and is available via CEH.
- The primary data products are CEH-derived and documented for reuse, but data governance and openness depend on dataset provenance and permissions.
- Appendix A Hunting Survey provides context on the original aerial survey, including that negatives are lost, but printed frames have been digitised and rectified to preserve footprints.

## Appendix A Hunting Survey

- Aerial photography survey conducted by Hunting Survey Ltd (June 1967) to support topographic mapping.
- Film negatives are lost; prints have been digitised and rectified by CEH to preserve spatial footprints.
- Footprints of all frames are documented to aid historical data reconstruction and reference.

## Relevance for monitoring frameworks

- Demonstrates a structured approach to assembling, validating, and linking long-term environmental datasets for policy scrutiny and decision support.
- Emphasises the need for metadata, data provenance, data transformation records, and data governance, aligning with requirements to share underlying data and ensure data quality.
- Highlights challenges common to monitoring frameworks: data gaps or loss, access barriers, organizational silos, metadata inadequacy, and the effort required to transform data into usable formats.
- Provides a concrete example of building a multi-layered environmental data repository (topography, hydrology, soils, vegetation) to support analysis of land-use impacts on hydrological processes, with explicit data standards and documentation to facilitate reuse and policy evaluation.