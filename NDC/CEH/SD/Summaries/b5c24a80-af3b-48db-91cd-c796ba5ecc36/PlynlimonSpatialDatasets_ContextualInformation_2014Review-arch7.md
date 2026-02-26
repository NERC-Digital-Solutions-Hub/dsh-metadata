# Plynlimon Spatial datasets

## Overview
- Documentation of GIS-ready spatial datasets for the Plynlimon experimental catchments, encompassing the headwaters of the River Severn and River Wye.
- Aims to support hydrological, land-use, and vegetation analyses by providing multiple layers (topography, hydrology, soils, vegetation) derived from historical surveys and digitised maps.
- Datasets prepared to enable map-based data exploration and analysis within GIS, with attention to data provenance and processing methods.

## Datasets and layers
- Hydrologically corrected elevation grid
  - Plyn_DEM (GRID)
  - Cell size: 15 m; floating point; British National Grid
  - Derived from 1:5,000 contour maps, spot heights, stream maps, and catchment boundaries
- Catchment and subcatchments boundaries
  - PlynlimonCatchments.shp
  - British National Grid
  - Attributes: Catchment, Subcatch
- River network
  - PlynlimonRiverNetwork.shp
  - British National Grid
  - Attributes: FNODE_, TNODE_, LENGTH, Catchment, Type
- Spot heights
  - PlynlimonSpotHeight.shp
  - British National Grid
  - Attribute: HEIGHTS
- Wye catchment elevation contours
  - Plynlimon_WyeElevationContours.shp
  - British National Grid
  - Attribute: HEIGHTS
- Severn catchment elevation contours
  - Plynlimon_SevernElevationContours.shp
  - British National Grid
  - Attribute: HEIGHTS
- Soil parental materials
  - Plynlimon_SoilParentalMaterials
  - British National Grid
  - Attributes: SOIL, Descript
- Vegetation map (2013 update)
  - Plynlimon_VegetationMap2013
  - British National Grid
  - Attributes: id, VegClass, Varients
  - Based on updated LCM2000-compatible classes; refined after field checks
- Background reference
  - Soil Hydrology of the Plynlimon Catchments (Bell 1969; IH Report No. 8; revised 2005 by CEH)

## Data production and methods
- Digitisation of hard-copy maps
  - Topographic and hydrographic features digitised from 1:5,000 topographic maps (Hunting survey 1967-68)
  - Scanned into ArcInfo; Ground Control Points used for registration; elevation points and contours captured at 10–20 m intervals
  - Severn catchment contours captured at Edinburgh University; later converted to lines
- Hydrologically corrected elevation grid (DTM)
  - Data sources integrated in ArcInfo to produce a hydrologically corrected grid
  - Flow diagram (Fig. 1) documents steps
  - Output: Plyn_DEM, 15 m resolution, British National Grid
- Digitising workflow and data formats
  - Shapefiles created for boundaries, river network, contours, soils, vegetation
  - Severn contours originally captured as point sequences and converted to lines
  - All primary layers stored in GIS-friendly formats for analysis

## Vegetation map development
- Motivation
  - To assist SoilTrEC project in identifying soil survey vegetation boundaries; base on CEH LCM 2000 to avoid IPR conflicts with LCM2007
- Method
  - Draft vegetation classes interpreted from 2009 aerial photography (Next Perspectives)
  - On-screen digitising in ArcGIS 10.1 with 2009 aerials as backdrop; field verification (2013)
  - Classes aligned with LCM2000; adjustments for conifer categories and variability with a Variants field
- Final product
  - Shapefile: Plynlimon_VegetationMap2013
  - Enables analysis of vegetation impacts on soil carbon and hydrology

## Data sources and background
- Hunting Survey aerial photography (1967)
  - Foundation for the topographic maps; appendix A details technical specifications
  - Footprints of frames digitised and rectified by CEH
- Soil hydrology
  - Bell, J.P. 1969: The Soil Hydrology of the Plynlimon Catchments (IH Report No. 8)
  - Updated version published 2005 by CEH; downloadable from CEH website
- Data gaps
  - Some field data held by other organisations; some datasets have been lost
  - Not all original datasets exist in full

## Appendix A: Hunting Survey
- Details on the 1967 aerial survey conducted by Hunting Survey Ltd
- Includes technical specifications and frame footprints

## Access and usage notes
- Datasets use British National Grid coordinates; formats include shapefiles and GRID rasters
- Data provenances and processing steps are documented to support reproducibility and quality assessment
- Useful for GIS-based analyses of catchment hydrology, land use, soils, and vegetation dynamics over time