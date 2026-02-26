# This dataset contains:

## Overview
- Field site: Bury Green Brook, Hertfordshire (51.848485, 0.079786); small ephemeral gravel-bed river with riffle-pool morphology.
- Study aim: measure grain-scale structure of the river bed and its variation through riffle-pool sequences.
- Field site covered ~100 m of channel; width 3–6 m.
- Fieldwork conducted across five visits: Sep 2014; Jun 2015; Jul 2016; Apr 2017; Oct 2018.
- Related references: Hodge et al. (2013); Voepel et al. (2019).

## Field site control network
- An initial arbitrary coordinate system established around the site with 12 temporary benchmarks (2 ground permamarkers, 10 survey discs) fixed to trees/posts.
- Surveyed with reflectorless Leica total station; total station location set to X=1000, Y=1000, Z=100 m.
- All subsequent surveys resectioned into the same coordinate system.

## Terrestrial Laser Scan (TLS) data
- 75 m reach scanned per visit using Leica P20 laser scanner; 7 scan locations per visit; 8 High Definition targets distributed across reach.
- Scans registered within an arbitrary grid to RMSE of 0.002–0.005 m (via Leica Cyclone).
- Data exported as text PTS files with:
  - Row 1: total number of points
  - Rows 2+ contain: X, Y, Z, intensity (4 columns)

## CT data
- Objective: quantify grain-scale bed structure using CT scanning of buried sediment baskets.
- Field procedure: bury 250 mm baskets (rim 1.5 × D below surface) at riffle crest, pool head/shallow/deep/tail locations; baskets excavated after ~19 months and scanned.
- CT scanning details: Nikon μCT scanner (450 kVp; 2048 CLDA; 440 kVp, 922 μA; 951 projections; 60 ms exposure); isometric voxel size 600 μm.
- Data processing steps:
  - Pre-processed data provided in HUTCH_files folders with sonograms and metadata for reconstruction.
  - Post-processed data provided as CT image stacks in TIFF format.
  - Post-processed datasets separated into Matrix (fine-grained matrix) and ParticlesFull (grains).
- Basket burial locations (example coordinates provided in Table 1; coordinates use the same total-station coordinate system as TLS data).

## Image reconstruction (X-ray CT workflow)
- Overall three-step reconstruction pipeline:
  1) Convert raw sinograms to radiographs.
  2) Determine centre of rotation (COR).
  3) Algebraic reconstruction to obtain 3D volumes.
- Detailed process and folder structure:
  - Create DigiXCT workflow folders (DigiXCT, with subfolders Radio, Recon, Sino) and color-code samples (e.g., 1YY, 2RB, 5PY).
  - Copy sinograms into color-named folders; run sinogram-to-radiograph converter; output radiographs per color code.
  - COR steps using Nikon CT Pro 2D: select sample stacks, adjust volume radius, locate CORs, set output to 512×512, 32-bit floats, and centring results; save centred radiographs with suffixes like _CCRecon.
  - Batch processing with DigiXCT3 64-bit: edit flat-file information, set up camera and geometry definitions, define input radiographs, choose 0: Image stack output in TIFF (32-bit float), specify file naming like r3yy (Run3, color code YY), set grid size and resolution, choose reconstruction method (NITRO recommended), and run reconstruction to produce a stacked TIFF sequence.
  - Preview and adjust steps to optimize geometry, resolution, and ROI selections; save reconstruction configuration for reproducibility.
- Output: reconstructed image stacks saved under Recon folders; accompanying VIGL/VGL files created for reproducibility.

## Registration and clipping (VGStudio Max and Fiji)
- Goal: reorient data so XY plane is orthogonal to gravity (Z-axis), register to downstream marker, and clip to a consistent region around the top rim of the basket.
- VGStudio Max workflow:
  - Import DigiXCT reconstruction stack; load as image stack with correct resolution (e.g., 0.5999 mm).
  - Use Simple 3-2-1 registration to align with gravity; place three markers on the basket rim; verify registration with 2D/3D views; ensure minimal rotation error (prefer vertical alignment).
  - Clip image at the third ring down from the top rim (and fourth ring from bottom) by drawing a selection cube around the sample and excluding background; create Region of Interest (ROI) and extract Region 1 of Volume 1.
  - Export aligned/clipped volume as a raw file (Raw volume (*.raw)) with a filename encoding Run and color code (e.g., RRCC_Registered_Clipped_x<>,y<>,z<>.raw) and generate a corresponding VGL file for future reloading.
  - If needed, rotate the downstream marker to align with X axis using Fiji later in the workflow.
- Fiji (ImageJ) workflow for downstream marker alignment:
  - Import the raw 16-bit unsigned stack; orient so downstream tab aligns with positive X-axis.
  - Rotate and save as rotated TIFF (16-bit) to the Recon folder; filename example: RRCC_Registered_Clipped_Rotated.tif.
  - Ensure 16-bit matrix (Long16) and particle (Short16) data types are used for consistent analysis.

## Data outputs and organization
- Primary data types:
  - TLS: text-based PTS point clouds with X, Y, Z, intensity.
  - CT pre-processed data: HUTCH_files with sinograms and metadata.
  - CT post-processed data: Matrix and ParticlesFull TIFF stacks for each basket.
  - Reconstructed CT data: radiographs, COR centring results, and 3D volumes (RAW) with VGL metadata.
  - Registered and clipped volumes: raw volumes and rotated TIFFs stored under Recon folders.
- Coordinate system: all CT, TLS, and control network data are referenced to the same total-station coordinate system.
- Documentation and references included for site context and methodology:
  - Hodge, R. A., Sear, D. A., & Leyland, J. (2013)
  - Voepel, H., et al. (2019)

## Notes for GIS and data users
- The dataset brings together field-derived spatial data (TLS) and high-resolution 3D bed-material information (CT) in a geospatially consistent framework.
- Data are organized to support multi-resolution analysis of grain-scale processes within riffle-pool morphologies.
- The workflow emphasizes reproducibility and traceability through explicit folder structures, naming conventions, and processing steps across multiple software tools.