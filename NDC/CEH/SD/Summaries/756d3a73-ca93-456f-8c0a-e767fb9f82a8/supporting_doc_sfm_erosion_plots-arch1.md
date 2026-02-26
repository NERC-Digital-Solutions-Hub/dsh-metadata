# Collection, generation methods and quality control

- Study setup: Seven erosion plots (~5 x 5 m) established on Iron Tongue Hill on 26/07/2018 to monitor the burnt moorland surface, erosion, and vegetation recovery. Plot locations provided as seven OS grid references (1–7).
- Data collection: Each plot surveyed 10 times using Structure-from-Motion (SfM) photogrammetry.
  - Survey timeline: S1 (26/07/2018) through S10 (22/11/2019) with intermediate dates [S2] 02/08/2018, [S3] 12/09/2018, [S4] 04/10/2018, [S5] 13/11/2018, [S6] 13/12/2018, [S7] 08/01/2018, [S8] 16/05/2019, [S9] 29/07/2019, [S10] 22/11/2019.
  - Field work: 40–60 photographs collected per survey to build SfM models.
- Data processing and quality control:
  - SfM models created for all 70 surfaces (7 plots x 10 surveys).
  - Dense SfM point clouds generated in Agisoft Photoscan (Metashape).
  - Ground Control Points (GCPs) used to scale and georeference point clouds based on differential GPS data.
  - Reported registration errors are approximately 20 mm.
- Data products and formats:
  - Outputs include cleaned dense DEM point clouds and 1 mm/pixel resolution orthomosaics (orthophotos).
  - File formats: .tif for both DEM and orthomosaic.
- File organization:
  - For each plot and survey, two .tif files exist, e.g. P1_S1_DEM.tif and P1_S1_ortho.tif.
  - Total dataset comprises 140 files: 7 plots x 10 surveys x 2 file types.
- Visualization: Figure 1 provides the location map of the erosion plots on Iron Tongue Hill.