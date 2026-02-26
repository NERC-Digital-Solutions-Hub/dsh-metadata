# This dataset contains:

- Field site overview and datasets (document describing the data)
- Field topography (Terrestrial Laser Scanner data; .pts)
- CT scans (raw and processed; .tif, metadata, .mat)

## Field site overview
- Aim: measure grain-scale structure of a gravel-bed river and its variation through a riffle-pool sequence.
- Study site: Bury Green Brook, Hertfordshire (latitude 51.848485, longitude 0.079786); small ephemeral gravel-bed river with riffle-pool morphology.
- Site length and channel width: ~100 m long; channel width 3–6 m.
- Field visits: five visits on September 2014; June 2015; July 2016; April 2017; October 2018.
- Field site documentation references: Hodge et al. (2013).

## Field site control network
- An arbitrary coordinate system was established with 12 temporary benchmarks (2 ground permamarkers and 10 survey discs) attached to trees and fence posts.
- Surveying used a reflectorless Leica total station; site origin set to X=1000, Y=1000, Z=100 m, with resectioning to the arbitrary system for subsequent surveys.

## TLS data (Terrestrial Laser Scanning)
- Coverage: 75 m along thalweg of the channel, scanned at all five field visits.
- Targets: 8 High Definition Survey Targets placed along the reach; surveyed into the same arbitrary coordinate system.
- Scanning: 7 scanner positions; resolution 3.1 mm at 10 m range.
- Processing: scans registered together using target locations (arbitrary grid) with Leica Cyclone; registration RMSE ~0.002–0.005 m.
- Output: data exported as text (PTS) files with columns X, Y, Z, intensity.

## CT data (Computed Tomography)
- Objective: measure grain-scale bed structure at different locations.
- Retrieval method: 250 mm diameter metal mesh baskets buried with rims 1.5 × D below surface; baskets located at riffle crest, pool head, pool shallow, pool deep, pool tail locations.
- Burial and retrieval: buried 2 Sept 2015; left for 19 months; excavated 7 Apr 2017; washed in liquid wax to fix in situ arrangement before scanning.
- CT scanning: μ-CT imaging at the μ-VIS X-Ray Imaging Centre, University of Southampton; 450 kVp X-ray source; 2048-pixel CLDA; 951 projections; 440 kV, 922 μA; voxel size 600 μm; interactive volume registration with VGStudio Max 2.1.
- Data formats: pre-processed (HUTCH_files folders with sonograms and metadata) and post-processed (CT image stacks in .tiff).
  - ParticlesFull: gravel grains only.
  - Matrix: fine-grained matrix only.
- Tank/basket locations: Table 1 lists coordinates (X, Y, Z) and morphological locations for each basket (e.g., 1BO upstream pool head, 4GO riffle crest, etc.) in the same coordinate system as the total station and TLS data.
- Metadata and references: detailed references and site-specific information provided (Hodge et al. 2013; Voepel et al. 2019).

## Data processing workflow (overview)
- End-to-end pipeline to transform raw CT sinograms into usable 3D volumes for analysis, including alignment to the gravity frame and extraction of sample volumes.
- Reconstruction and alignment:
  - Sinograms converted to radiographs; determine centre of rotation (COR); reconstruct volumes.
  - COR and reconstruction parameters configured per dataset; 3D volumes produced as float32 TIFF stacks.
  - Reconstruction used options such as NITRO/NITRO-based methods; optional volume processing for artifact removal.
- Data organization:
  - Reconstructed data stored under a Recon folder with standardized naming conventions.
  - Folder structure and file naming designed to encode run numbers and color codes for each sample basket.

## Registration and clipping (VGStudio Max)
- Purpose: reorient each sample so the XY plane is orthogonal to gravity (Z axis).
- Registration steps:
  - Import DigiXCT reconstruction; orient to gravity using 3D and 2D views; verify alignment with markers (downstream marker) and adjust orientation as needed.
  - Use Simple 3-2-1 registration to align top rim points; ensure basket rim remains visible.
  - If rotation becomes excessive, re-run simple registration to restore proper orientation.
- Clipping and ROI:
  - Define a selection cube around the sample, excluding background while enclosing stones.
  - Create a Region of Interest (ROI) and extract Region 1 of Volume 1; lock views to maintain alignment during edits.
  - Export aligned/clipped volume as Raw volume (.raw) with a descriptive filename including run and color code.
  - Optionally export a VGL file for later reuse.
- Output: aligned and clipped raw volumes (and VGL files) for subsequent processing, with filenames including RR (run) and CC (color code), plus grid sizes.

## Fiji/ImageJ processing (for downstream marker orientation)
- Rotate to align downstream marker with downstream X-axis:
  - Import raw volume as 16-bit unsigned data; set dimensions from filename; transform to align with downstream direction using Rotate tool (bilinear interpolation).
  - Save as TIFF in Recon folder with filename indicating rotation (e.g., ..._Rotated.tif).
  - Ensure the image data type remains 16-bit unsigned for compatibility with downstream analysis.

## Outputs and file naming conventions
- Reconstructed data:
  - Reconstructed TIFF stacks stored under Recon folders with informative filenames (including run and color code).
  - When exporting, use 32-bit float format for intermediate exports and keep simple, descriptive names.
- Aligned/clipped data:
  - Raw volumes named to reflect run, color code, and processing steps.
  - Corresponding VGL files saved for reproducibility.
- Rotated TIFFs:
  - TIFFs named with suffix _Rotated to indicate orientation adjustments.
  - Matrix contact and particle analyses prepared with appropriate 16-bit data types (Long16 for matrix contact, Short16 for particle analysis) as part of downstream analysis.

## References
- Hodge, R. A., Sear, D. A., & Leyland, J. (2013). Spatial variations in surface sediment structure in riffle-pool sequences: a preliminary test of the Differential Sediment Entrainment Hypothesis (DSEH). Earth Surface Processes and Landforms, 38(5), 449-465.
- Voepel, H., Leyland, J., Hodge, R., Ahmed, S., & Sear, D. (2019). Development of a vector-based 3D grain entrainment model with application to X-ray computed tomography (XCT) scanned riverbed sediment. Earth Surface Processes and Landforms, 44(15), 3057-3077.