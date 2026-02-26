# Collection, generation methods and quality control

- Objective and site
  - Seven erosion plots (approximately 5 x 5 m) on Iron Tongue Hill, established 26/07/2018 to capture burnt moorland surface state and monitor erosion and vegetation recovery.
  - Plot locations provided via OS Grid References:
    - Plot 1: SK 00834 99983
    - Plot 2: SK 00867 99986
    - Plot 3: SE 00882 00010
    - Plot 4: SE 00987 00113
    - Plot 5: SE 01085 00511
    - Plot 6: SE 01142 00397
    - Plot 7: SE 01042 00206

- Data collection and surveying
  - Each plot surveyed 10 times (including the initial survey) using Structure-from-Motion (SfM) photogrammetry.
  - Survey dates (S1–S10) include 26/07/2018, 02/08/2018, 12/09/2018, 04/10/2018, 13/11/2018, 13/12/2018, 08/01/2018, 16/05/2019, 29/07/2019, and 22/11/2019.
  - Field data consisted of 40–60 photographs per survey to build SfM models.

- Data processing and georeferencing
  - SfM models created for all 70 surfaces.
  - Dense SfM point clouds produced with Agisoft Photoscan (Metashape).
  - Ground Control Point coordinates used to scale and georeference point clouds based on differential GPS data.
  - Reported registration errors are approximately 20 mm.

- Data products and outputs
  - Exported data as:
    - Dense digital elevation model (DEM) point clouds.
    - 1 mm per pixel orthomosaic (orthophoto).
  - File format: .tif for both DEM and orthomosaic.
  - File organization: per plot and per survey, two .tif files exist (DEM and orthomosaic). Example naming:
    - P1_S1_DEM.tif
    - P1_S1_ortho.tif
  - Total data files: 140 (7 plots x 10 surveys x 2 file types) covering 70 surfaces.

- Data organization rationale
  - Clear naming convention (Pn_Sm_DEM.tif and Pn_Sm_ortho.tif) to facilitate retrieval and analysis across plots and survey dates.
  - Each survey-date dataset provides both elevation (DEM) and high-resolution imagery (orthophoto) for downstream analyses.

- Quality control and notes
  - High-resolution outputs (1 mm/pixel) with documented georeferencing accuracy (~20 mm).
  - Data intended for subsequent analysis and monitoring of erosion and vegetation recovery, with a location map referenced (Figure 1).