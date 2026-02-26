# Supporting information for NE/W002930/1: High-resolution (2 metre) digital elevation models of landscape affected by the Chamoli ice-debris flow, India, February 2021

## Overview
- Provides high-resolution digital elevation models (DEMs) at 2 m grid spacing for the Chamoli District landscape affected by the February 2021 avalanche–debris flow.
- DEMs are raster (.tif) products created from Pléiades-HR stereo imagery and aligned to a 2015 composite DEM to support landscape-change analysis and numerical modelling (e.g., CAESAR-Lisflood).
- Derived data are distributed and archived; raw Pléiades data are not public due to licensing, but derived DEM products are shareable.

## What are these data?
- Geospatial raster DEMs describing topography, elevations in metres above mean sea level.
- Created from CNES/Airbus Pléiades-HR stereo imagery using block matching (NASA Ames Stereo Pipeline v2.6.2_post).
- DEMs are registered/aligned to a September 2015 composite DEM (demcoreg used for alignment).

## Why were the data collected?
- To analyze landscape change after the 7 February 2021 Chamoli avalanche–debris flow.
- DEMs serve as standalone datasets for analysis and to support numerical modelling and further research resources.

## Where and when were the data collected?
- Spatial extent described by the bounding box in WGS 84 / UTM Zone 44 coordinates.
- Raw data acquisition dates: 10 February 2021; 6 June 2021; 24/25 December 2021 (composite); 27 January 2022; 21 February 2022; 2 April 2022.
- Final DEMs produced up to 27 April 2022.

## How were the data collected?
- From Pléiades stereo imagery captured in along-track mode.
- New DEMs grown at 2 m resolution using the Ames Stereo Pipeline.
- DEMs registered to the September 2015 composite DEM; existing post-event DEMs clipped/aligned to the same reference.
- Processed and quality-checked by project PI and a project partner; alignment refined with demcoreg.

## Who was responsible?
- Project Principal Investigator (PI) tasked and funded the imagery.
- Project partner generated the DEMs; PI refined alignment.

## Completeness and licensing
- Dataset contains final, aligned Pléiades-derived DEMs created during the project.
- Complete in terms of final DEMs; six DEMs are provided, plus diagnostic alignment imagery.
- Raw Pléiades data license restricts public sharing; derived DEM products are distributed and archived.

## Nature and units of recorded values
- DEMs are gridded raster data; pixel values are elevations in metres above mean sea level.

## Quality control
- DEMs contain holes/gaps where photogrammetric reconstruction failed (e.g., due to clouds, occlusions, or large view-angle offsets).
- To maintain a consistent time series, each DEM was aligned to the September 2015 reference; residual alignment errors are shown in accompanying alignment statistic images.

## Dataset structure and contents
- Directory: DEMs
- DEM files (naming YY-MM-DD_DEM.tif):
  - 210210_DEM.tif
  - 210606_DEM.tif
  - 211225_DEM.tif
  - 220127_DEM.tif
  - 220221_DEM.tif
  - 220402_DEM.tif
- Additional multi-panel PNGs (alignment diagnostics) for each DEM:
  - 210210_DEM_alignment_stats.png
  - 210606_DEM_alignment_stats.png
  - 211225_DEM_alignment_stats.png
  - 220127_DEM_alignment_stats.png
  - 220221_DEM_alignment_stats.png
  - 220402_DEM_alignment_stats.png

## Experimental design and methods (summary)
- DEMs produced via automated, open-source workflows for high-resolution terrain data from very-high-resolution satellite imagery.
- Alignment to a common reference DEM (Sept 2015) to create a coherent time series.
- Quality indicators provided to assess residual alignment and potential artefacts.

## References (software and related datasets)
- Ames Stereo Pipeline (NASA open-source) for DEM generation.
- demcoreg toolbox for DEM alignment.
- Pre- and post-event DEM composites and related Zenodo datasets for context and provenance.