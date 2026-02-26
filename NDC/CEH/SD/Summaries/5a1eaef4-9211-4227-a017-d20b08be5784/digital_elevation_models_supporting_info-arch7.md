# Supporting information for NE/W002930/1: High-resolution (2 metre) digital elevation models of landscape affected by the Chamoli ice-debris flow, India, February 2021

- What are these data?
  - Digital elevation models (DEMs) describing landscape topography, in raster (.tif) format.
  - Primarily designed for import into GIS software to support geospatial analysis.

- Why were the data collected?
  - To analyze landscape change after the 7 February 2021 avalanche–debris flow in Chamoli District, Uttarakhand, India.
  - Used as standalone DEMs and to support numerical modelling with CAESAR-Lisflood.

- Where were the data collected?
  - Area bounded roughly by:
    - Top left: 352,312 m E, 3,385,209 m N
    - Bottom right: 384,787 m E, 3,358,896 m N
  - Coordinate system: WGS 84 / UTM Zone 44

- When were the data collected?
  - Raw data dates: 10 Feb 2021; 6 Jun 2021; 24/25 Dec 2021 (composite); 27 Jan 2022; 21 Feb 2022; 2 Apr 2022.
  - Final DEMs created up to 27 Apr 2022.

- How were the data collected?
  - Generated from CNES/Airbus Pléiades-HR stereo imagery (along-track mode).
  - New 2 m DEMs produced with NASA Ames Stereo Pipeline (v2.6.2_post).
  - DEMs registered to an existing Sept 2015 composite DEM using demcoreg; post-event DEMs aligned to Sept 2015 DEM.

- Who was responsible for the collection and interpretation?
  - Project Principal Investigator (PI) tasked and purchased Pléiades imagery.
  - Project partner produced the DEMs with Ames Stereo Pipeline.
  - PI refined alignment using demcoreg.

- Completeness of the dataset
  - Contains final, aligned Pléiades-derived DEMs produced during NE/W002930/1.
  - Raw Pléiades data are not publicly shareable due to license, but derived products (the DEMs) are distributable and archivable.

- Experimental design and analytical methods
  - Refer to section 1.5: DEM creation from stereo imagery, alignment to 2015 baseline, and quality assessment via alignment residuals.

- Collection / generation / transformation methods
  - See section 1.5 for details on processing workflow (stereo photogrammetry, alignment, clipping, and realignment).

- Nature and units of recorded values
  - DEMs are gridded raster data with pixel values in metres above mean sea level (m a.s.l.).

- Quality control
  - DEMs contain gaps where photogrammetric reconstruction failed (e.g., due to cloud cover, occlusion, or large view-angle offsets).
  - All new DEMs are aligned to the Sept 2015 baseline DEM; residual alignment errors are shown in accompanying PNGs.

- Dataset structure
  - Directory: DEMs
  - DEM files (TIFF):
    - 210210_DEM.tif
    - 210606_DEM.tif
    - 211225_DEM.tif
    - 220127_DEM.tif
    - 220221_DEM.tif
    - 220402_DEM.tif
  - Corresponding multi-panel alignment statistics images (PNG):
    - 210210_DEM_alignment_stats.png
    - 210606_DEM_alignment_stats.png
    - 211225_DEM_alignment_stats.png
    - 220127_DEM_alignment_stats.png
    - 220221_DEM_alignment_stats.png
    - 220402_DEM_alignment_stats.png

- References
  - Shean et al., 2016. Automated, open-source pipeline for DEM creation from high-resolution stereo imagery.
  - Beyer et al., 2018. The Ames Stereo Pipeline.
  - Bhushan & Shean, 2021. Chamoli Disaster Pre-event 2-m DEM Composite: September 2015.
  - Shean et al., 2021a. dshean/demcoreg: demcoreg v1.1.0.
  - Shean et al., 2021b. Chamoli Disaster Post-event 2-m DEM Composite and Difference Map.