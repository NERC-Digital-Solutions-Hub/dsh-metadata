# Supporting information for NE/W002930/1: High-resolution (2 metre) digital elevation models of landscape affected by the Chamoli ice-debris flow, India, February 2021

## What are these data?
- Digital elevation models (DEMs) describing landscape topography in raster (.tif) format.
- 2-metre grid resolution DEMs commonly used in GIS for geospatial analysis.

## Why were the data collected?
- To support analysis of landscape change after the 7 February 2021 avalanche-debris flow in Chamoli District, Uttarakhand, India.
- Used as standalone datasets and to support numerical modelling with CAESAR-Lisflood.

## Where were the data collected?
- Area bounded within a rectangular box described in WGS 84 / UTM Zone 44 coordinates.
  - Top left: 352312 m E, 3385209 m N
  - Lower right: 384787 m E, 3358896 m N

## When were the data collected?
- Raw data collection dates: 10 Feb 2021; 6 Jun 2021; 24/25 Dec 2021 (composite DEM); 27 Jan 2022; 21 Feb 2022; 2 Apr 2022.
- Derived DEMs created up to 27 Apr 2022.

## How were the data collected?
- DEMs created from CNES/Airbus Pléiades-HR stereo imagery (along-track mode).
- Processing: block matching with NASA Ames Stereo Pipeline (v2.6.2_post); DEMs registered to a Sept 2015 composite DEM using demcoreg; post-event DEMs aligned to the same reference DEM.

## Who was responsible for the collection and interpretation of the data?
- Project PI: tasked and procured Pléiades imagery.
- Project partner: generated DEMs using Ames Stereo Pipeline.
- Project PI: refined alignment with demcoreg toolbox.

## Completeness, licensing, and data access
- Dataset is complete with final, aligned Pléiades-derived DEMs produced during NE/W002930/1.
- Licensing: raw Pléiades data license with Airbus prohibits public sharing of raw data; derived products (the DEMs) are distributable and archivable under the terms of the licence.
- The dataset includes aligned DEMs and associated documentation as derived products.

## Experimental design and analytical methods
- See section 1.5: DEM generation from stereo imagery, alignment to reference DEM, and clipping/alignment procedures.

## Collection / generation / transformation methods
- See section 1.5 for detailed workflow and tools (Ames Stereo Pipeline; demcoreg).

## Nature and units of recorded values
- Raster DEMs with pixel values representing elevations in metres above mean sea level.

## Quality control
- DEMs contain holes/gaps where photogrammetric reconstruction failed (cloud cover, occlusions, large view-angle offsets).
- To maintain a consistent time series, each DEM was aligned to the Sept 2015 reference DEM; residual alignment errors are shown in accompanying PNGs.

## Dataset structure
- Directory: DEMs containing:
  - 210210_DEM.tif
  - 210606_DEM.tif
  - 211225_DEM.tif
  - 220127_DEM.tif
  - 220221_DEM.tif
  - 220402_DEM.tif
- Naming convention: YY-MM-DD_DEM
- Accompanying multi-panel PNGs describing residual errors (same naming convention):
  - 210210_DEM_alignment_stats.png
  - 210606_DEM_alignment_stats.png
  - 211225_DEM_alignment_stats.png
  - 220127_DEM_alignment_stats.png
  - 220221_DEM_alignment_stats.png
  - 220402_DEM_alignment_stats.png

## References
- Shean et al. (2016): Automated, open-source pipeline for DEM production from very-high-resolution stereo imagery.
- Beyer et al. (2018): Ames Stereo Pipeline overview.
- Bhushan & Shean (2021): Chamoli Disaster pre-event 2-m DEM composite (Sept 2015).
- Shean et al. (2021a, 2021b): demcoreg toolbox and Chamoli post-event DEM composite and difference maps.