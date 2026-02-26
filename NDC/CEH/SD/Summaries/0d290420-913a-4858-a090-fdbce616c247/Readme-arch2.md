# Solid, air and water phase distributions of a UK sandy loam soil packed at five bulk densities, 2018

## Overview
- A dataset of 30 Computed Tomography (CT) based soil microstructures showing distributions of soil, water, and air.
- Two water saturations (20±0.5% and 80±0.5%) across five bulk densities (1.2–1.6 g/cm3); three replicates per density.
- Each 3D image is 512×512×512 voxels; voxel values encode soil, water, and air.

## Data content and structure
- Image set: 30 CT volumes named BDXX_R_SW.tif (bulk density XX, replication R, saturation SW).
- Voxel encoding: soil = 255, water = 127, air = 0.
- Resolution and domain: 512 slices in z direction per image.

## Sample and soil preparation
- Soil origin: sandy loam from Bullion field, James Hutton Institute, Invergowrie, Scotland (collected 2011).
- Composition: sand 55.7%, silt 31.0%, clay 13.3%; organic matter 5.5%; C/N ratio 17.1.
- Preparation: air-dried, sieved to 1–2 mm aggregates, stored at 4°C; autoclaved twice (121°C, 100 kPa, 30 min, 24 h apart).

## Microcosm preparation
- Five bulk densities prepared in polyethene rings (inner diameter 17 mm, height 15 mm).
- Target equal air-filled pore space across treatments by setting gravimetric water contents to 0.13, 0.11, 0.09, 0.07, and 0.06.
- Three replicates per density (15 microcosms total).

## CT imaging and processing
- CT imaging: Metris X-Tek HMX scanner; 24 μm voxel resolution; 105 keV, 96 μA; 2000 projections; Molybdenum target with 0.25 mm Al filter.
- Reconstruction: CT Pro v2.1; volume rendering with VGStudio MAX v2.2; export to 3D stacks (*.bmp).
- Pre-processing: thresholding with an in-house indicator kriging method; unconnected solids removed with ImageJ 3D Fill Holes.

## Air-water distribution modelling
- Saturation targets: Sw = 0.8 and Sw = 0.2 for 80% and 20% water saturation.
- Modelling approach: two-phase single-component lattice-Boltzmann (TRT-LBM) with parameters as described by Ginzburg (2005) and Genty & Pot (2013).
- Boundary conditions: bounce-back at solids; hydrophobic (W = 0) at boundary voxels with air; hydrophilic elsewhere.
- Initialization: density of water particles set from mass-balance equation; two-step initialization followed by main iterative loop.
- Computation: warm-up 2,000 lattice-Boltzmann time units; main loop 10,000 units; tolerance 0.005 (±0.5%).
- Environment: runs on HPC nodes (two Intel E5-2620 v4 CPUs) under Red Hat Linux 7.2.

## Data outputs and encoding
- Post-processing assigns soil, water, and air to voxels as described; outputs are 512-slice volumes saved as .tif with the specified voxel values.
- Enables comparative analyses of pore-scale distributions across bulk densities and saturations.

## Provenance and references
- Deposit reference: EIDCHELP-33383.
- Related methods and background literature referenced for preparation, imaging, preprocessing, and modelling (e.g., Juyal et al., 2018; Houston et al., 2013; Ginzburg, 2005; Genty & Pot, 2013).

## Relevance to environmental monitoring
- Provides standardized, high-resolution, pore-scale representations of soil structure and moisture distribution suitable for monitoring soil health and informing policy performance over time.
- Facilitates data integration with other environmental datasets and supports broader data-sharing and reuse through clear metadata and accessible TIFF outputs.