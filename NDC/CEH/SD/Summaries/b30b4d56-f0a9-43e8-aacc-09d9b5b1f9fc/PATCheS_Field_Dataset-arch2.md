# This dataset contains:

- Overview of field site and datasets (this document)
- Field topography (Terrestrial laser scanner data; .pts)
- CT scans (raw and processed; .tif, metadata, .mat)

## Overview and Aim
- Field work aimed to measure grain-scale structure of a gravel-bed river and its variation through a riffle-pool sequence.
- Study site: Bury Green Brook, Hertfordshire (approx. 51.848485, 0.079786), a small ephemeral gravel-bed river with riffle-pool morphology.
- Reach length ~100 m; channel width 3–6 m.
- Fieldwork conducted over five visits: Sep 2014, Jun 2015, Jul 2016, Apr 2017, Oct 2018.
- Outputs support understanding of sediment structure, entrainment, and habitat-scale processes through standardized, shareable data.

## Study Site and Temporal Coverage
- Repeated field campaigns across five years to capture temporal variation in grain-scale structure.
- Site and reference framework described with connection to prior work (Hodge et al., 2013).

## Data Types and Formats
- TLS data: 3D point clouds of channel reach (PTS format) with coordinates and intensity.
- CT data: micro-CT scans of bed sediments (raw and post-processed; TIFF stacks; metadata and .mat files).
- Field documentation: site overview and methodology documentation included.

## Field Site Control and Spatial Referencing
- Establishment of an arbitrary coordinate system in Sep 2014 with 12 temporary benchmarks (2 ground permamarkers, 10 survey discs) on trees/fence posts.
- All subsequent surveys resectioned into this fixed coordinate framework to maintain consistent spatial referencing.

## Terrestrial Laser Scanning (TLS) Data
- Data collected along ~75 m of river reach during each field visit using a Leica P20 scanner.
- 8 high-definition targets used for alignment; scans gathered from 7 positions per visit.
- Resolution: ~3.1 mm at 10 m range; registered to RMSE 0.002–0.005 m.
- Output: text-based PTS files with X, Y, Z, and intensity columns; includes a header row with total point count.

## Computed Tomography (CT) Data
- Purpose: quantify grain-scale structure by burying metal mesh baskets at key riffle-pool locations (riffle crest, pool head, pool shallow/deep/tail).
- Burial/date: 2 Sept 2015; baskets left for ~19 months; recovered 7 Apr 2017.
- CT scanning method: μ-CT imaging (Nikon Metrology) with high-energy X-ray setup; voxel size ~600 μm; 951 projections; extensive artefact corrections referenced to Clausnitzer & Hopmans (2000).
- Data organization: two formats
  - Pre-processed data (HUTCH_files): contains sonograms and metadata for projection reconstruction; multiple baskets per folder when scanned together.
  - Post-processed data: CT image stacks in TIFF; two folders per basket:
    - ParticlesFull: gravel grains
    - Matrix: fine-grained matrix
- Basket locations (Table 1): coordinates in the same total-station coordinate system; examples include locations such as 1BO (Upstream, Pool Head) and 5OO (Downstream, Pool Deep), with X, Y, Z coordinates supplied.

## CT Data Metadata and Basket Locations
- Table 1 enumerates basket IDs, morphologic locations (e.g., Pool Head, Pool Deep, Riffle Crest), and precise XYZ coordinates in the study coordinate system.
- References for CT methodology and imaging discussed (HUTCH and related XCT imaging literature).

## Image Reconstruction Workflow
- Three-step process to convert raw CT data into usable volumes:
  1) Sinograms to radiographs: manage sinogram stacks, create color-coded folders for each sample, run conversion to radiographs to produce per-sample image stacks.
  2) Centre of Rotation (COR): identify COR in reconstructed volumes with Nikon CT Pro 2D, adjust reconstruction radius, label outputs with colour-code suffixes (e.g., CC), and ensure consistent centering for all samples.
  3) Algebraic reconstruction: use DigiXCT (64-bit) with a flat-file Excel-based parameter sheet to configure hardware, input, output, and reconstruction parameters; generate multi-page TIFF stacks with specified data types; select reconstruction method (NOP/FBP alternatives; NITRO highlighted here); save reconstruction settings and outputs with standardized filenames.
- Output: reconstructed image stacks stored under the Recon folder, with explicit naming conventions that embed run number and colour code (e.g., r3yy for Run 3, colour code YY).

## Registration, Clipping, and Volume Export
- Registration in VGStudio Max to align voxel data with gravity (XY plane orthogonal to gravity vector) using a downstream marker and post-processing steps:
  - Import reconstructed stacks, define imaging resolution, and perform Simple 3-2-1 registration to align top rim of baskets.
  - Ensure proper orientation and check registration across 2D slices; adjust if needed via simple re-registration.
- Clipping to isolate the region of interest (the grain sample):
  - Define a selection cube around the sample, ensuring top rim visibility and full enclosure of stones while excluding excess background.
  - Create a Region of Interest (ROI) and export the aligned/clipped volume as a Raw volume (.raw) with accompanying VGL file for reproducibility.
- Fiji (ImageJ) rotation to align downstream marker with the X-axis:
  - Import raw, adjust orientation with 16-bit unsigned format, rotate to align downstream marker, then save as rotated TIFF.
  - Final outputs use matrix contact (Long16) and particle analysis (Short16) data types.
- Documentation emphasizes reproducibility of steps and retention of a vgl/RAW pair for future reprocessing.

## Data Access, Reuse and References
- Data are organized into a standardized, well-documented pipeline to facilitate reuse, cross-study comparisons, and integration with other environmental datasets.
- Key references:
  - Hodge, R. A., Sear, D. A., & Leyland, J. (2013). Spatial variations in surface sediment structure in riffle-pool sequences: a preliminary test of the Differential Sediment Entrainment Hypothesis (DSEH). Earth Surface Processes and Landforms.
  - Voepel, H., Leyland, J., Hodge, R., Ahmed, S., & Sear, D. (2019). Development of a vector-based 3D grain entrainment model with application to X-ray computed tomography (XCT) scanned riverbed sediment. Earth Surface Processes and Landforms.
- The dataset emphasizes data quality, standardization, and the potential to upload and share through appropriate data portals, addressing the challenge of enabling access to underlying data used to generate final outputs.

## Notable Points for Analysts Monitoring the Environment
- Rich, multi-modal dataset enabling assessment of grain-scale sediment structure and riverbed heterogeneity across a riffle-pool sequence.
- Longitudinal dataset with multiple field visits supports temporal analyses of sediment packing, exposure, and entrainment potential.
- Comprehensive processing workflow (TLS to CT) with explicit, reproducible steps and software tools (Leica Cyclone, Nikon CT Pro 2D, DigiXCT, VGStudio Max, Fiji) that can be integrated with other monitoring data.
- Dataset organization and metadata support cross-study synthesis and data integration, aligning with goals of data quality assurance, standardization, and accessibility.