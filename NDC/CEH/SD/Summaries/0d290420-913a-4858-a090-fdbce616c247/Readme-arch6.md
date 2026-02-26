# Solid, air and water phase distributions of a UK sandy loam soil packed at five bulk densities, 2018

## Overview
- 30 Computed Tomography (CT) based soil microstructures showing distributions of soil, air, and water.
- Two water saturations: 20±0.5% and 80±0.5% (volume ratio of visible pore space), five bulk densities (BD 1.2–1.6 g cm⁻³), 3 replicates per density (total 30 images).
- Each image: 512 × 512 × 512 voxels; domain size fixed across dataset.
- Voxel values: soil = 255, water = 127, air = 0.
- File names: BDXX_R_SW.tif (XX = 1.2, 1.3, 1.4, 1.5, 1.6; R = 1–3; SW = 20±0.5% or 80±0.5%).

## Source and soil preparation
- Soil origin: sandy loam from Bullion field, James Hutton Institute, Invergowrie, Scotland (collected 2011).
- Composition: sand 55.7%, silt 31.0%, clay 13.3%; organic matter 5.5%; C/N 17.1.
- Preparation: air-dried, aggregates 1–2 mm; sterilized by autoclaving twice (121°C, 100 kPa, 30 min each, 24 h apart).

## Microcosm preparation
- Setup: soil packed in polyethylene rings (inner diameter 17.0 mm, height 15.0 mm).
- Five bulk densities: 1.2, 1.3, 1.4, 1.5, 1.6 g cm⁻³.
- Standardized air-filled pore space with gravimetric water contents: 0.13, 0.11, 0.09, 0.07, 0.06 respectively.
- Replicates: three per treatment (15 microcosms total).
- Further details referenced: Juyal et al., 2018.

## CT imaging
- Scanner: Metris X-Tek HMX CT (NIKON Metrology, Tring, UK).
- Acquisition: 24 μm voxel resolution; 105 keV, 96 μA; 2000 angular projections.
- Source optics: Molybdenum target, 0.25 mm aluminium filter.
- Reconstruction: CT Pro v2.1; volume processing with VGStudio MAX v2.2; contrast adjustments and export to image stacks (BMP) for processing.

## Image pre-processing
- Thresholding: in-house indicator kriging method.
- Post-processing: remove unconnected solids with ImageJ 3D Fill Holes plugin.

## Air–water distribution modelling
- Modelling approach: two-phase single-component, two-relaxation times lattice-Boltzmann model (TRT-LBM).
- Target saturations: S_w = 0.8 and S_w = 0.2; parameters set according to Ginzburg (2005) and Genty & Pot (2013).
- Boundary conditions: bounce-back at solid boundaries; hydrophobic (W = 0) at boundary voxels containing air to reflect cut pores; hydrophilic (W > 0) elsewhere.
- Initial water density: computed from mass balance; two-step initialization for density distribution.
- Computation: iterative solver with inner/outer loops; warm-up and main loops (2,000 and 10,000 lattice-Boltzmann time units); tolerance ~0.5%.
- Thresholding: water density from TRT-LBM results thresholded at 1.225.
- Hardware: computations run on cluster nodes with dual Intel E5-2620 v4 CPUs (Red Hat Linux 7.2).

## Data content and formats
- Each microstructure: 512 slices along z, saved as .tif.
- Voxel labeling: soil (255), water (127), air (0).
- Dataset deposit reference: EIDCHELP-33383.

## Potential uses
- Analysis of pore-scale distributions and connectivity across bulk densities and saturations.
- Comparison with other imaging modalities or datasets.
- Development of self-serve data products for exploring phase distributions in sandy loam soils.