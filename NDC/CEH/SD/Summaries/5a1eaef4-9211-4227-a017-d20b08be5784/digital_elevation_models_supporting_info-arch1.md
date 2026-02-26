# Supporting information for NE/W002930/1: High-resolution (2 metre) digital elevation models of landscape affected by the Chamoli ice-debris flow, India, February 2021

## 1.1 What are these data?
- Digital elevation models (DEMs) describing landscape topography.
- Raster (.tif) format, designed for import into GIS for analysis.

## 1.2 Why were the data collected?
- To support analysis of landscape change after the 7 February 2021 avalanche-debris flow in Chamoli District, Uttarakhand, India.
- Used as standalone datasets and to support numerical modelling with CAESAR-Lisflood.

## 1.3 Where were the data collected?
- Area described by a bounding box in WGS 84 / UTM Zone 44, approximate coordinates:
  - Top left: 352312 E, 3385209 N
  - Lower right: 384787 E, 3358896 N

## 1.4 When were the data collected?
- Raw data dates:
  - 10 February 2021
  - 6 June 2021
  - 24/25 December 2021 (composite DEM)
  - 27 January 2022
  - 21 February 2022
  - 2 April 2022
- Derived DEMs created up to 27 April 2022.

## 1.5 How were the data collected?
- DEMs generated from CNES/Airbus Pléiades-HR stereo imagery (along-track mode).
- 2 m grid DEMs created with NASA Ames Stereo Pipeline (v2.6.2_post).
- DEMs registered to a September 2015 composite DEM (demcoreg) and aligned to a post-event DEM (10 February 2021).

## 1.6 Who was responsible for the collection and interpretation of the data?
- Project Principal Investigator (PI) tasked imagery procurement and overall coordination.
- Project partner produced the DEMs using Ames Stereo Pipeline.
- PI refined DEM alignment with demcoreg toolbox.

## 1.7 Completeness of the dataset
- Contains final, aligned Pléiades-derived DEMs created during the project NE/W002930/1.
- Raw data licensing (Airbus) restricts public sharing of raw data, but derived products (DEMs) are distributable and archivable.

## 2. Experimental design and analytical methods
- DEMs produced at 2 m resolution from stereo imagery and aligned to a common reference.
- Alignment to the September 2015 DEM to ensure consistency over time; methods summarized in section 1.5.

## 3. Collection / generation / transformation methods
- See section 1.5 for details on imagery, software (Ames Stereo Pipeline), and alignment procedures.

## 4. Nature and units of recorded values
- Gridded raster data; pixel values represent elevations in metres above mean sea level.

## 5. Quality control
- Holes/gaps occur where photogrammetric reconstruction failed (cloud cover, occlusion, large view-angle offset).
- All new DEMs aligned to the same Sept 2015 DEM; residual alignment errors shown in accompanying PNGs.

## 6. Dataset structure
- Directory: DEMs
- DEM files (GeoTIFF): 210210_DEM.tif, 210606_DEM.tif, 211225_DEM.tif, 220127_DEM.tif, 220221_DEM.tif, 220402_DEM.tif
- Naming convention: YY-MM-DD_DEM
- Accompanying multi-panel PNGs displaying residual errors:
  - 210210_DEM_alignment_stats.png
  - 210606_DEM_alignment_stats.png
  - 211225_DEM_alignment_stats.png
  - 220127_DEM_alignment_stats.png
  - 220221_DEM_alignment_stats.png
  - 220402_DEM_alignment_stats.png

## 7. References
- Shean et al. 2016. Automated pipeline for DEMs from high-resolution stereo imagery.
- Beyer et al. 2018. The Ames Stereo Pipeline (open-source software).
- Bhushan & Shean 2021. Chamoli pre-event 2-m DEM composite (Sept 2015).
- Shean et al. 2021a. dshean/demcoreg: DEM coregistration toolbox.
- Shean et al. 2021b. Chamoli post-event 2-m DEM composite and difference map.