# Supporting information for NE/W002930/1: High-resolution (2 metre) digital elevation models of landscape affected by the Chamoli ice-debris flow, India, February 2021

## 1. What are these data?
- Digital elevation models (DEMs) describing landscape topography.
- Raster format (.tif), 2 m grid resolution.
- Primarily used in GIS for analysis and geospatial modelling.

## 2. Why were the data collected?
- To support analysis of landscape change after the 7 February 2021 avalanche–debris flow in Chamoli District, Uttarakhand, India.
- Used as standalone data for analysis and to support numerical modelling with CAESAR-Lisflood (and related resources).

## 3. Where were the data collected?
- Area bounded by:
  - Top left: 352312 m E, 3385209 m N
  - Bottom right: 384787 m E, 3358896 m N
- Coordinate system: WGS 84 / UTM Zone 44

## 4. When were the data collected?
- Raw data collection dates:
  - 10 February 2021
  - 6 June 2021
  - 24/25 December 2021 (composite)
  - 27 January 2022
  - 21 February 2022
  - 2 April 2022
- Derived DEMs created across dates within this range, up to 27 April 2022

## 5. How were the data collected?
- DEMs created from CNES/Airbus Pléiades-HR stereo imagery (along-track mode).
- 2 m DEMs produced with the NASA Ames Stereo Pipeline (v2.6.2_post).
- DEMs registered to a September 2015 composite DEM using the demcoreg toolbox; post-event DEM (10 Feb 2021) aligned to the same 2015 reference.

## 6. Who was responsible for the collection and interpretation?
- Project Principal Investigator (PI) responsible for tasking and purchasing Pléiades imagery.
- A project partner generated the DEMs with Ames Stereo Pipeline.
- The PI refined the alignment of the DEMs using demcoreg.

## 7. Completeness of the dataset
- The dataset contains final, aligned versions of all new Pléiades-derived DEMs produced during the project.
- Raw Pléiades data are not publicly available due to license restrictions with Airbus; however, derived products (the DEMs) are distributed and archived.

## 8. Experimental design and analytical methods
- Design and methods largely align with Section 1.5 (data collection and processing):
  - Stereo photogrammetry from high-resolution imagery
  - 2 m grid DEM generation via block matching
  - Consistent alignment to a shared September 2015 reference DEM

## 9. Nature and units of recorded values
- DEMs are gridded raster data.
- Pixel values are elevations in metres above mean sea level (m a.s.l.).

## 10. Quality control
- DEMs contain holes/gaps where photogrammetric reconstruction failed (e.g., cloud cover, occlusion, view-angle mismatches).
- To obtain a consistent time series, each new DEM is aligned to the September 2015 reference; residual alignment errors are shown in accompanying PNGs.

## 11. Dataset structure
- DEMs directory includes six TIFF files:
  - 210210_DEM.tif
  - 210606_DEM.tif
  - 211225_DEM.tif
  - 220127_DEM.tif
  - 220221_DEM.tif
  - 220402_DEM.tif
- Alignment diagnostics: six multi-panel PNGs (210210_DEM_alignment_stats.png, 210606_DEM_alignment_stats.png, 211225_DEM_alignment_stats.png, 220127_DEM_alignment_stats.png, 220221_DEM_alignment_stats.png, 220402_DEM_alignment_stats.png) describing residual errors before/after alignment.

## 12. Licensing and access
- Derived data are distributable and archivable under the project license.
- Raw Pléiades imagery is not shareable in the public domain due to the vendor license.