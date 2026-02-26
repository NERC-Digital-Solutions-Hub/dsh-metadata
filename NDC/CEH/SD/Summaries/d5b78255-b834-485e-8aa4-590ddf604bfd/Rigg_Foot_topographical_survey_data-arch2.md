# Rigg Foot topographical survey data, Sourhope Field Experiment Site, Scotland [Soil Biodiversity Programme] Mick Whelan and Stuart Bradley (University of Stirling)

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999), focused on Sourhope Field Experiment Site in the Scottish Borders to study soil biota and its functional ecological roles.
- Topographic survey conducted to support understanding of site conditions and aid integration with soil biodiversity data.
- Two survey campaigns in early 2000; raw data and preliminary maps are provided for further analysis and cross-assembly with other datasets.

## Data Collection and Processing
- Survey dates: April 4–6, 2000 and May 11–12, 2000.
- Instrument: Leica Geosystems Total Station EDM.
- Processing: initial processing and re-orientation performed using LISCAD software.
- Coordinates and datum:
  - x-y coordinates oriented so the bottom left corner of plot 1A is at 1000, 1000; y axis upslope.
  - Units: meters.
  - z: altitude relative to an arbitrary datum.
  - Easting/Northing: approximate values in OSGB 1936.
- Raw data option: original survey data available for matching or detailed analysis.

## Data Files
- Rigg_foot_Topographic.csv
  - Contains original x-y-z co-ordinates (in metres) with descriptive metadata for each axis.
  - x-y origin defined as above; z = altitude with arbitrary datum.
- Rigg_foot_Topographic_newgrdxyz.csv
  - Regular grid across the site at 25 cm intervals (cell size 0.25 m).
  - x-y-z coordinates on a regular grid interpolated from a Triangulated Irregular Network (TIN) of survey points.
  - Interpolations performed in ArcView 3.1 (ESRI) and exported via ArcInfo GRID module to CSV.
- Both files maintain consistent coordinate definitions and relative altitude datum.

## Site Level Maps
- Two first-draft contour maps illustrating the site’s topography at the Rigg Foot plot.
- Interim results; higher-quality maps with sub-plot boundaries available in Rigg_Foot_Topo_maps.pdf.
- Map key includes features such as the field boundary fence.

## Data Quality, Access, and Liability
- Data subject to quality assurance procedures.
- NERC cannot warrant the accuracy of data or determine fitness for a specific use.
- No liability accepted for loss, damage, injury, or other occurrences arising from data use.
- Raw data are available for researchers wishing to match with their datasets or conduct deeper analyses.