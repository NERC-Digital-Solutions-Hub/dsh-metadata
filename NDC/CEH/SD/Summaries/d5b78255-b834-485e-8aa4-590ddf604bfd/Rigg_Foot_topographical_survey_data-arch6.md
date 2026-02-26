# Rigg Foot topographical survey data, Sourhope Field Experiment Site, Scotland [Soil Biodiversity Programme]

## Background and aims
- The NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biota diversity and functional roles in key ecological processes at Sourhope, Scottish Borders.
- The Sourhope Field Experiment Site was monitored for above-ground biomass production, species composition, and relative abundance to link soil biodiversity with ecosystem processes.
- A topographic survey was conducted at Sourhope in April–May 2000 by Mick Whelan and Stuart Bradley (University of Stirling) to support matching field data and analyses with topography.
- Initial processing and re-orientation of survey data were performed using LISCAD software.

## Data files
- Rigg_foot_Topographic.csv
  - Original survey data: x, y, z coordinates in metres (arbitrary altitude datum).
  - Coordinate origin: bottom left corner of plot 1A at 1000, 1000; y-axis aligned upslope along plot boundaries.
  - Includes definitions and units for x, y, z.
- Rigg_foot_Topographic_newgrdxyz.csv
  - Regular grid across the site at 25 cm intervals with interpolated altitude values.
  - Grid is x-y-z coordinates on a regular grid (cell size 0.25 m) derived from a Triangulated Irregular Network (TIN) of survey points.
  - Interpolations performed in ArcView 3.1 (ESRI); data exported as ASCII grid and saved as CSV.

## Data contents and coordinate conventions
- Coordinates are provided in metres; x-y origin (1000,1000 at bottom-left of plot 1A) and y-axis orientation follow the upslope direction.
- z represents altitude relative to an arbitrary datum.
- Easting/Northing values are approximate OSGB 1936 references accompanying the data.

## Site level maps
- Two first-draft topographic maps depict the Sourhope Sourhope field plot topography.
- These provide an overall view; higher-quality maps with sub-plot boundaries are available in Rigg_Foot_Topo_maps.pdf.

## Data quality, usage, and liability
- Data have undergone quality assurance procedures; however, NERC cannot guarantee accuracy for any particular use.
- NERC Disclaims liability for accuracy, fitness for purpose, or any loss or damage arising from use of the data.
- Data can be used to match with other datasets or to perform further analyses; initial processing included re-orientation, and interpolation used established GIS tools.