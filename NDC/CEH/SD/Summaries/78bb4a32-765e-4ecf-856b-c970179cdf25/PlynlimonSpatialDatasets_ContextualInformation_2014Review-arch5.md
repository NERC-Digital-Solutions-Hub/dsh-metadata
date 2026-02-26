# Plynlimon Catchments Spatial Data Documentation

## Overview
- Describes long-running Plynlimon experimental catchments in mid-Wales, designed to study land use impacts on catchment hydrology, particularly evaporation, flood risk, and low flows.
- Contains a rich suite of spatial data and derived products (topography, soils, vegetation, hydrology) collected from the late 1960s onward and updated in later years.

## Datasets and layers
- Spatial datasets (Plynlimon Spatial datasets) include:
  - Catchment and subcatchment boundaries
  - River network
  - Spot heights
  - Wye catchment contour lines
  - Severn catchment contour lines
  - Soil Parental Materials
  - Vegetation map (updated 2013)
- Grid dataset:
  - Plynlimon hydrologically corrected elevation grid (Plyn_DEM), 15 m cell size, GRID format, British National Grid
- Vegetation mapping details:
  - Update of CEH Land Cover Map 2000 classes to include heath, bracken, improved grassland, with reclassification (e.g., conifer plantations as coniferous woodland)
  - Version allows use of conifer variants for different analyses
- Severn and Wye elevation contours:
  - Wye contours derived from 1:5000 topographic maps; Severn contours initially captured from 1:5000 maps with separate workflow
- Data formats and standards:
  - Shapefiles for boundaries, networks, heights, and vegetation classes
  - Grid-based DEM for hydrological analyses
  - Coordinate system: British National Grid

## Data creation and provenance
- Hunting Survey (1967) provided initial large-scale topographic maps, including major channels, forest drains, tracks, and fence lines
- Digitising phase (late 1990s) converted maps to GIS layers:
  - Elevation, catchment boundaries, river network
  - Ground control points used for registration; elevation points and contours captured at 10–20 m intervals
  - ArcInfo coverage files produced (except Severn contours, captured at Edinburgh University)
- Hydrologically corrected DEM:
  - Derived from 1:5000 contours, spot heights, stream maps, and catchment boundaries
  - Process documented in a flow diagram (Figure 1)
- Soils:
  - Bell, J.P. Soil Hydrology of the Plynlimon Catchments (1969) IH Report No. 8; 2005 CEH revised edition
- Vegetation map (2013):
  - Draft created from 2009 Next Perspectives aerial photography
  - Field validation conducted in 2013
  - ArcGIS 10.1-based digitising; backdrops include digital aerials
  - Classes aligned with CEH LCM2000; included refinements and a Variants field for coniferous plantation status
- Appendices and notes:
  - Appendix A documents Hunting Survey technical specifications and frame footprints
  - Some datasets are owned by other organizations or have been lost, affecting availability

## Data governance and sharing
- Ownership and access: parts of data are owned by other organizations; some data have been lost or are not readily available
- Documentation and provenance: extensive metadata within this document (capture methods, coordinate systems, data lineage)
- Data updates: Vegetation map updated in 2013; DEM and contour datasets maintained with workflow to support ongoing analyses
- References and access: related publications and data products available via CEH (e.g., CEH website publications page and CEH science news blog)

## Data quality, limitations, and considerations
- Data gaps: some datasets unavailable due to ownership; some historical records lost
- Interoperability challenges: multiple sources and capture methods (in-house CEH digitising vs. Edinburgh University for Severn contours)
- Temporal mismatches: differences between 2009 aerial imagery and 2013 field observations affected vegetation classifications
- Data volume and formats: legacy ArcInfo formats and large shapefiles; explicit versioning and documentation recommended for reuse

## Practical considerations for Data Stewards
- Governance and standards:
  - Maintain clear provenance and licensing notes for all layers; document data owners and any restrictions
  - Ensure consistent coordinate system usage (British National Grid) and provide transformation guidance for users
- Metadata and discoverability:
  - Provide detailed metadata for each layer (source, scale, date, methods, quality checks, and limitations)
  - Link to related CEH publications and data products
- Interoperability and updates:
  - Track versioned updates (e.g., VegetationMap2013) and plan for future harmonisation with newer land-cover datasets (LCM2000/LCM2007 family)
  - Consider migrating legacy ArcInfo data to modern GIS formats as part of archival preservation
- Data usability:
  - Provide context on data applicability (e.g., hydrological modelling with the Plynlimon DEM, vegetation classes for soil carbon analyses)
  - Include guidance on integrating datasets from different capture histories (1960s maps vs. 1990s digitising vs. 2013 vegetation update)

## References and access
- CEH project pages and publications:
  - CEH website: Plynlimon project and datasets
  - CEH Soil Hydrology of the Plynlimon Catchments (Bell, 1969; updated 2005 CEH)
- Data products:
  - Plynlimon_DEM, PlynlimonCatchments.shp, PlynlimonRiverNetwork.shp, PlynlimonSpotHeight.shp
  - VegetationMap2013, Plynlimon_SevernElevationContours.shp, Plynlimon_WyeElevationContours.shp
- Appendix A: Hunting Survey technical details and frame footprints