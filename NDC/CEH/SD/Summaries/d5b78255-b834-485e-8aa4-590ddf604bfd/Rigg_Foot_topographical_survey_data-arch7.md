# Rigg Foot topographical survey data, Sourhope Field Experiment Site, Scotland [Soil Biodiversity Programme] Mick Whelan and Stuart Bradley (University of Stirling)

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biodiversity and its functional roles.
- Sourhope Field Experiment Site in the Scottish Borders as a large field site for monitoring above-ground biomass, species composition, and relative abundance.
- Topographic survey conducted in April–May 2000 to aid integration with soil biodiversity studies; raw data and maps available.
- Two primary data products plus draft maps for site topography.

## Data collection and methods
- Survey conducted by Mick Whelan and Stuart Bradley (Department of Environmental Science, University of Stirling).
- Instrumentation: Leica Geosystems Total Station EDM; initial processing and re-orientation with LISCAD software.
- Purpose: provide accurate topography to support analyses of soil biota and ecological processes.

## Data files and formats
- Rigg_foot_Topographic.csv
  - Original survey data: x, y, z coordinates (meters) with an arbitrary altitude datum.
  - Spatial orientation: bottom-left corner of plot 1A set at (1000, 1000); y axis aligned upslope along plot boundaries.
  - x, y, z units: meters; z is relative altitude.
  - Easting and Northing fields are provided as approximate OSGB 1936 coordinates (meters).
  - Includes notes on location of survey points.
- Rigg_foot_Topographic_newgrdxyz.csv
  - Regular grid across the site at 25 cm intervals with interpolated altitude values.
  - Grid data represented as x-y-z coordinates on a 0.25 m cell grid.
  - Interpolation performed in ArcView 3.1 (ESRI) on a TIN created from survey points.
  - ASCII grid exported from ArcInfo GRID module and saved as CSV.
  - Coordinates in meters; orientation tied to the same plot reference as the original data.

## Spatial reference and coordinate details
- Easting/Northing coordinates approximate OSGB 1936 (OSGB36).
- Original x-y framework anchored with bottom-left of plot 1A at (1000, 1000); y axis runs upslope along plot boundaries.
- Altitude (z) is relative to an arbitrary altitude datum (no geoid alignment implied).

## Data processing, quality and limitations
- Interpolation and gridding performed using ArcView 3.1 and a Triangulated Irregular Network (TIN) of survey points.
- Gap-filling via 25 cm grid interpolation to produce a continuous surface.
- Note: Data are subject to quality assurance procedures; NERC cannot warrant accuracy or fitness for a particular use and disclaims liability for data use.

## Site level maps
- Two first-draft contour maps illustrating overall topography of the Rigg Foot plot at Sourhope.
- Interim results; higher-quality maps with sub-plot boundaries are available in Rigg_Foot_Topo_maps.pdf.

## Usage considerations for GIS specialists
- Useful for integrating topographic context with soil biodiversity data and ecological process analyses.
- Original and gridded surface data allow both point-based and raster-based analyses.
- When applying in other studies, account for:
  - Arbitrary altitude datum for z values.
  - Approximate OSGB36 coordinate references for Easting/Northing.
  - Potential limitations in positional accuracy and elevation fidelity as per QA disclaimer.