# Collection, generation methods and quality control

## Purpose and scope
- Document the collection, generation methods, and quality control procedures for monitoring erosion and vegetation recovery on burnt moorland.

## Study site and sampling design
- Seven erosion plots (approximately 5 x 5 m) on Iron Tongue Hill.
- Plot locations provided by OS grid references:
  - 1: SK 00834 99983
  - 2: SK 00867 99986
  - 3: SE 00882 00010
  - 4: SE 00987 00113
  - 5: SE 01085 00511
  - 6: SE 01142 00397
  - 7: SE 01042 00206

## Survey schedule
- Each plot surveyed 10 times (S1–S10), including the initial survey date.
- Survey dates:
  - S1: 26/07/2018
  - S2: 02/08/2018
  - S3: 12/09/2018
  - S4: 04/10/2018
  - S5: 13/11/2018
  - S6: 13/12/2018
  - S7: 08/01/2018
  - S8: 16/05/2019
  - S9: 29/07/2019
  - S10: 22/11/2019

## Data collection and processing methods
- Structure-from-Motion (SfM) photogrammetry used to monitor erosion and vegetation recovery.
- Field photography per survey: 40–60 photos collected.
- SfM models created for all 70 surfaces (7 plots × 10 surveys).
- Dense SfM point cloud generated in Agisoft Photoscan (Metashape).
- Ground Control Points (GCPs) used to scale and georeference point clouds with differential GPS coordinates.
- Reported registration errors approximately 20 mm.

## Data products and outputs
- Outputs per survey: a dense digital elevation model (DEM) point cloud and a 1 mm/pixel orthomosaic (orthophoto).
- File format: .tif for both DEM and orthomosaic.

## Data organization and file structure
- For each plot survey, two .tif files exist:
  - P1_S1_DEM.tif
  - P1_S1_ortho.tif
- Example naming convention:
  - P1 = Plot number (1–7)
  - S1 = Survey number (1–10)
- Total files: 7 plots × 10 surveys × 2 file types = 140 files.

## Georeferencing and metadata
- Georeferencing achieved via Ground Control Points using differential GPS coordinates.
- DEM dense point cloud and 1 mm/pixel orthomosaic exported as .tif for downstream analysis.

## Quality control and considerations
- Registration errors around 20 mm indicate high-precision alignment of SfM outputs with ground controls.
- Consistent data collection across all plots and surveys supports longitudinal analysis of erosion and vegetation recovery.

## Figure reference
- Figure 1: Location map of erosion plots on Iron Tongue Hill.