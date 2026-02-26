# Collection, generation methods and quality control

- Overview
  - Seven erosion plots (approximately 5 x 5 m) on Iron Tongue Hill established 26/07/2018 to capture burn impact, erosion, and vegetation recovery.
  - Each plot surveyed 10 times (S1–S10) between 2018 and 2019.

- Methods and data collection
  - Structure-from-Motion (SfM) photogrammetry used to generate models from 40–60 photos per survey.
  - SfM models created for all 70 surfaces; dense SfM point clouds produced with Agisoft Photoscan (Metashape).
  - Ground Control Points with differential GPS coordinates used to scale and georeference point clouds.
  - Reported registration/geo-reference accuracy: ~20 mm.

- Outputs and data products
  - For each plot and each survey, two TIFF files:
    - DEM dense point cloud: P1_S1_DEM.tif (example naming)
    - Orthophoto: P1_S1_ortho.tif
  - Orthomosaic resolution: 1 mm per pixel.

- Data organization and provenance
  - File naming convention: P{Plot}_S{Survey}_{DEM|ortho}.tif
  - Plots: P1–P7; Surveys: S1–S10
  - Total files: 7 plots × 10 surveys × 2 types = 140 TIFF files
  - Documentation note: Figure 1 provides location map of erosion plots.

- GIS-friendly implications
  - Provides high-resolution, georeferenced DEMs and orthophotos suitable for time-series erosion and vegetation analyses in GIS.
  - Facilitates map-based visualization and spatial analysis across multiple dates.