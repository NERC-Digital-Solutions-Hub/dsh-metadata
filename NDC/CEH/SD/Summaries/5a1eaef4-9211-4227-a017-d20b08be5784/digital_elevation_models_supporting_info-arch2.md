# Supporting information for NE/W002930/1: High-resolution (2 metre) digital elevation models of landscape affected by the Chamoli ice-debris flow, India, February 2021

- Digital elevation models (DEMs) describing landscape topography in raster (.tif) format, suitable for import into GIS and geospatial analyses.
- Used as standalone datasets and to support numerical modelling (e.g., CAESAR-Lisflood) of landscape change following the Chamoli avalanche–debris flow.

## What are these data?
- DEMs produced to depict changes in terrain post-event.
- 2 m grid resolution; DEMs aligned to a common reference for time-series consistency.
- Accompanied by alignment quality visualizations.

## Why were the data collected?
- To enable analysis of landscape change after the 7 February 2021 Chamoli incident.
- Support both direct analysis of topographic change and numerical modelling of hydrodynamic/geomorphic processes.

## Where were the data collected?
- Study area bounded in WGS 84 / UTM Zone 44:
  - Top left: 352312 m E, 3385209 m N
  - Lower right: 384787 m E, 3358896 m N

## When were the data collected?
- Raw data collection dates: 10 Feb 2021; 6 Jun 2021; 24/25 Dec 2021 (composite); 27 Jan 2022; 21 Feb 2022; 2 Apr 2022.
- Derived DEMs created between these dates, up to 27 Apr 2022.

## How were the data collected?
- Derived from CNES/Airbus Pléiades-HR stereo imagery (along-track mode).
- DEMs generated at 2 m using NASA Ames Stereo Pipeline (v2.6.2_post).
- DEMs registered to a Sept 2015 composite DEM using the demcoreg toolbox; alignment also used to clip/align a February 2021 post-event DEM.

## Who was responsible for the collection and interpretation of the data?
- Project Principal Investigator (PI) tasked and funded the Pléiades imagery purchase.
- Project partner generated DEMs with Ames Stereo Pipeline.
- PI refined alignment of DEMs with the Sept 2015 reference DEM.

## Completeness of the dataset
- Includes final, aligned Pléiades-derived DEMs produced during the project.
- Raw Pléiades data cannot be shared publicly due to vendor licensing; derived data products (the DEMs) can be distributed and archived.

## Experimental design and analytical methods
- Use of stereo-photogrammetry to produce high-resolution topographic surfaces.
- Time-series DEMs aligned to a common reference DEM to enable consistent change detection.

## Collection / generation / transformation methods
- DEMs created from stereo imagery, then clipped and realigned to a 2015 reference DEM.

## Nature and units of recorded values
- Raster gridded data; pixel values are elevations in metres above mean sea level.

## Quality control
- Some data holes/gaps where photogrammetric reconstruction failed (cloud cover, occlusion, large view-angle offsets).
- All new DEMs aligned to the 2015 reference; residual alignment errors documented in accompanying PNGs.

## Dataset structure
- DEMs directory with files:
  - 210210_DEM.tif
  - 210606_DEM.tif
  - 211225_DEM.tif
  - 220127_DEM.tif
  - 220221_DEM.tif
  - 220402_DEM.tif
- Multi-panel alignment statistics images for each DEM:
  - 210210_DEM_alignment_stats.png
  - 210606_DEM_alignment_stats.png
  - 211225_DEM_alignment_stats.png
  - 220127_DEM_alignment_stats.png
  - 220221_DEM_alignment_stats.png
  - 220402_DEM_alignment_stats.png

## References
- Shean, D.E. et al. (2016). Automated, open-source pipeline for DEMs from very-high-resolution stereo imagery.
- Beyer, R.A. et al. (2018). The Ames Stereo Pipeline.
- Bhushan, S. & Shean, D. (2021). Chamoli Disaster Pre-event 2-m DEM Composite: September 2015.
- Shean, D. et al. (2021a). dshean/demcoreg: v1.1.0.
- Shean, D. et al. (2021b). Chamoli Disaster Post-event 2-m DEM Composite and Difference Map.