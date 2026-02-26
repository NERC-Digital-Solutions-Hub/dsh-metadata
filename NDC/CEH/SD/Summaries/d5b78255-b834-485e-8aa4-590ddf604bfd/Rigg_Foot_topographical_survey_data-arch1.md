# Rigg Foot topographical survey data, Sourhope Field Experiment Site, Scotland [Soil Biodiversity Programme]

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study at Sourhope Farm, Scottish Borders.
- Aimed to understand soil biodiversity and the functional roles of soil organisms through multiple projects examining soil structure, carbon and nitrogen cycles, and micro-, meso-, and macro-fauna groups.
- A topographic survey was conducted at Sourhope in 2000 to document site topography alongside above-ground productivity and diversity assessments.

## Survey and data collection
- Locations and period: Sourhope Field Experiment Site (Grid reference NT8545019630); surveys conducted April 4–6 and May 11–12, 2000.
- Survey team: Mick Whelan and Stuart Bradley (Department of Environmental Science, University of Stirling).
- Equipment: Leica Geosystems Total Station EDM.
- Data processing: Initial processing and re-orientation performed using LISCAD software.

## Data files and contents
- Rigg_foot_Topographic.csv
  - Contains original survey data (x-y-z coordinates).
  - Coordinates stored in metres with an arbitrary altitude datum.
  - Spatial orientation: bottom-left corner of plot 1A at (1000, 1000); y axis aligned upslope parallel to plot boundaries.
  - x, y: co-ordinates in metres; z: altitude (metres) relative to the arbitrary datum.
  - Easting and Northing provided as approximate OSGB 1936 coordinates (metres).
- Rigg_foot_Topographic_newgrdxyz.csv
  - Regular grid across the site at 25 cm intervals with interpolated altitude values.
  - Data represent x-y-z coordinates on a grid (cell size 0.25 m).
  - Interpolations created in ArcView 3.1 (ESRI) on a Triangulated Irregular Network (TIN) of survey points.
  - Output exported as ASCII grid (CSV) via ArcInfo GRID module; coordinates oriented as in the raw data.

## Site level maps and documentation
- Two draft topographic maps accompany the data, providing an overall view of site topography.
- Sub-plot boundaries within each treatment are not shown on these first drafts; improved maps with detailed subplots are available in Rigg_Foot_Topo_maps.pdf.
- The maps are interim; they should be refined for final analyses.

## Data quality, limitations, and disclaimers
- Data are subject to quality assurance procedures but are not guaranteed by NERC for accuracy or fitness for any particular use.
- NERC cannot be held liable for any loss, damage, or injury arising from the use of these data.
- Data may be provided without detailed administrative boundaries and may require careful interpretation within intended applications.

## Access and provenance
- The raw 2000 topographic data and the 25 cm grid interpolations are provided for researchers wishing to match these data to their own datasets or to perform further analyses.
- Original processing and grid creation details (LISCAD, ArcView 3.1, ArcInfo GRID) are documented to facilitate reproducibility.