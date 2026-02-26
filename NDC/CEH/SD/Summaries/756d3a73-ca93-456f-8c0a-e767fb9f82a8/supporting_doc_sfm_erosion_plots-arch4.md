# Collection, generation methods and quality control

## Overview
- Seven erosion plots (~5 × 5 m) were established on Iron Tongue Hill on 26/07/2018 to document burnt moorland surface conditions, erosion, and vegetation recovery.
- Each plot was surveyed ten times (S1–S10) over the period 2018–2019 to build a temporal dataset of surface change.

## Collection method and data generation
- Structure-from-Motion (SfM) photogrammetry used to create models from 40–60 photos per survey.
- SfM models produced for all 70 surfaces; a dense point cloud was generated in Agisoft Photoscan (Metashape).
- Ground Control Points (GCPs) with differential GPS coordinates used to scale and georeference point clouds.
- Reported registration errors are approximately 20 mm.

## Data products
- Outputs include:
  - DEM dense point cloud
  - 1 mm/pixel resolution orthomosaic (orthophoto)
- Both produced as TIFF (.tif) files for each survey and plot.

## Data file organization and naming
- For each plot, two TIFF files exist per survey:
  - P1_S1_DEM.tif (and similarly P1_S1_ortho.tif)
- File structure: 7 plots × 10 surveys × 2 file types = 140 files total.
- Naming convention indicates plot number (P1–P7) and survey number (S1–S10).

## Georeferencing and quality controls
- GCPs used to scale and georeference; alignment relies on differential GPS coordinates.
- Estimated registration accuracy around 20 mm, supporting reliable spatial comparisons over time.