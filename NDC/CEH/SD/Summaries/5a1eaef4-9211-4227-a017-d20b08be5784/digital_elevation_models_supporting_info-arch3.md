# Supporting information for NE/W002930/1: High-resolution (2 metre) digital elevation models of landscape affected by the Chamoli ice-debris flow, India, February 2021

## Overview
- High-resolution 2 m digital elevation models (DEMs) of Chamoli District, Uttarakhand, India, created from Pléiades-HR stereo imagery to analyze landscape changes after the 7 February 2021 avalanche-debris flow.
- DEMs are provided as georeferenced raster (.tif) files suitable for GIS analyses and modelling.

## Data content and scope
- DEMs are gridded raster data with elevations in metres above mean sea level.
- Files in the DEMs directory:
  - 210210_DEM.tif
  - 210606_DEM.tif
  - 211225_DEM.tif
  - 220127_DEM.tif
  - 220221_DEM.tif
  - 220402_DEM.tif
- Each DEM is accompanied by multi-panel alignment statistics (.png) illustrating residual errors before/after alignment with a September 2015 reference DEM.
- Additional multi-panel PNGs accompany each DEM to aid interpretation of alignment quality.

## Why these data were collected
- To support analysis of landscape change following the February 2021 Chamoli disaster.
- DEMs also support numerical modelling using CAESAR-Lisflood and related resources.

## Location and timing
- Spatial extent bounded by:
  - Top left: 352312 E, 3385209 N
  - Lower right: 384787 E, 3358896 N
  - Coordinate system: WGS 84 / UTM Zone 44
- Raw data collection dates:
  - 10 Feb 2021
  - 6 Jun 2021
  - 24/25 Dec 2021 (composite DEM)
  - 27 Jan 2022
  - 21 Feb 2022
  - 2 Apr 2022
- Final DEMs created up to 27 Apr 2022.

## Data collection and processing methods
- Data source: CNES/Airbus Pléiades-HR stereo imagery captured in along-track mode.
- DEM generation: Block matching using NASA Ames Stereo Pipeline (v2.6.2_post).
- Georeferencing: DEMs registered to a September 2015 composite DEM (via demcoreg toolbox); alignment with the 10 Feb 2021 post-event DEM for consistency.
- Completeness: The dataset contains the final, aligned Pléiades-derived DEMs produced in NE/W002930/1.

## Responsible parties
- Project PI: Tasked and purchased the underlying Pléiades imagery; refined DEM alignment.
- Project partner: Created the DEMs using Ames Stereo Pipeline.

## Data quality and limitations
- Gaps/holes present in DEMs where photogrammetric reconstruction failed (e.g., due to cloud cover, occlusion, or large view-angle differences).
- Residual alignment errors are documented in accompanying alignment statistic images.
- Raw Pléiades data licensed by Airbus cannot be published publicly; however, derived DEM products are permitted for distribution and archiving.

## Dataset structure and access
- DEMs: .tif files in the DEMs directory, suitable for direct import into GIS software.
- Alignment quality: per-DEM alignment statistics PNGs (e.g., 210210_DEM_alignment_stats.png, etc.).
- Additional annotated multi-panel PNGs accompany the DEMs to aid interpretation.

## Notable references
- Methods and tools:
  - Ames Stereo Pipeline: Shean et al., 2016; Beyer et al., 2018.
  - demcoreg toolbox: Shean et al., 2021a.
- Related datasets:
  - Chamoli Disaster Pre-event 2-m DEM Composite: September 2015 (Bhushan & Shean, 2021).
  - Post-event 2-m DEM Composite and Difference Map: Shean et al., 2021b.