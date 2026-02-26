# Solid, air and water phase distributions of a UK sandy loam soil packed at five bulk densities, 2018

## Overview
- CT-based dataset comprising 30 3D soil microstructure volumes (512 × 512 × 512 voxels) describing distributions of soil, air, and water.
- Two water saturations (20±0.5% and 80±0.5%) across five bulk densities (1.2–1.6 g cm⁻³) with three replicates per condition, totaling 30 images.
- Voxel values: soil = 255, water = 127, air = 0.
- Origin: sandy loam soil from Bullion field (Scotland); soil prepared, sterilized, and microcosms assembled to standardize air-filled pore space.
- Included workflow spans CT imaging, preprocessing, and subsequent water–air distribution modeling.

## Dataset contents and file naming
- 30 TIFF volumes, each representing a single microstructure with 512 z-slices.
- File naming convention: BDXX_R_SW.tif
  - BDXX: bulk density (1.2, 1.3, 1.4, 1.5, 1.6 g cm⁻³)
  - R: replication (1, 2, or 3)
  - SW: water saturation (20±0.5% or 80±0.5%)
- Domain size per image: 512 × 512 × 512 voxels.

## Provenance and preparation
- Soil origin and composition: sandy loam; 55.7% sand, 31.0% silt, 13.3% clay; organic matter ~5.5%; C/N ~17.1.
- Sample preparation: air-dried, aggregates 1–2 mm, stored at 4 °C; autoclaved twice for sterilization.
- Microcosm preparation: packed in polyethene rings at five bulk densities; gravimetric water content adjusted per density to equalize air-filled porosity; 3 replicates per treatment.

## Imaging, preprocessing, and data processing
- CT imaging: Metris X-Tek HMX CT scanner; 24 μm voxel resolution; 105 keV, 96 μA; 2000 projections; reconstruction with CT Pro v2.1; visualization and export via VGStudio MAX v2.2.
- Pre-processing: thresholding using an in-house indicator kriging method; removal of unconnected solids with ImageJ 3D Fill Holes.
- Data representation: post-thresholded volumes annotated with soil (255), water (127), and air (0).

## Water–air distribution modeling
- Method: lattice-Boltzmann (TRT-LBM) two-relaxation-time model to obtain expected water–air distributions at target saturations (0.8 and 0.2).
- Key parameters: Λ fixed (3/16), ν chosen for incompressible Stokes flow, boundary conditions with bounce-back at solids; hydrophobic boundaries (W = 0) at boundary voxels containing air, hydrophilic elsewhere; initial water density P_I derived from mass balance.
- Simulation specifics: warm-up and main iteration phases (2,000 and 10,000 time units respectively), convergence tolerance ~0.5%, simulations run on HPC nodes (two Intel E5-2620 v4 CPUs, Red Hat Linux).
- Output preparation: water density predicted by TRT-LBM thresholded to 1.225; results intended to complement the segmented CT volumes.

## Metadata, access, and governance considerations
- Documentation references: preparation details described in Juyal et al. 2018; further methodological context provided within the deposit.
- File formats: TIFF volumes suitable for large-scale 3D imaging; explicit voxel value mapping documented.
- Provenance and reproducibility: explicit imaging, preprocessing, and modeling parameters provided to support reproduction, though some steps rely on specialized software (CT Pro, VGStudio MAX, ImageJ plugins) and bespoke preprocessing methods.
- Data availability and constraints: large, multi-step workflow with substantial data volume; potential interoperability considerations due to bespoke processing and modeling parameters; licensing and reuse terms should be confirmed with the deposit holder.
- Quality and stewardship notes: metadata captures experimental conditions, processing steps, and modeling parameters; completeness supports future reuse and audit trails; notes potential needs for validation or replication due to reliance on specific software versions and computational resources.