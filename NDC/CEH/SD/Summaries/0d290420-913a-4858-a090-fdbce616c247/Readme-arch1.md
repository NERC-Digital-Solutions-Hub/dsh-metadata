# Solid, air and water phase distributions of a UK sandy loam soil packed at five bulk densities, 2018

## Overview
- A dataset of 30 Computed Tomography (CT) based soil microstructures showing distributions of soil, air, and water.
- Two water saturations (20±0.5% and 80±0.5%), five soil bulk densities (1.2–1.6 g/cm³), 3 replicates per bulk density.
- Each image is 512×512×512 voxels; voxel values encode soil, water, and air phases.

## Sample and preparation
- Soil origin: sandy loam from Bullion field, James Hutton Institute, Invergowrie, Scotland (2011 sample).
- Composition (1–2 mm fraction): sand 55.7%, silt 31.0%, clay 13.3%; organic matter 5.5%; C/N 17.1.
- Processing: air-dried, sieved to 1–2 mm; sterilized by autoclaving twice (121 °C, 100 kPa, 30 min, 24 h apart).
- Microcosms: packed in polyethylene rings (inner diameter 17.0 mm, height 15.0 mm) at five bulk densities (1.2–1.6 g/cm³).
- Water content adjusted so air-filled pore space was consistent across treatments (gravimetric water contents: 0.13, 0.11, 0.09, 0.07, 0.06).

## Imaging and data processing
- CT imaging: Metris X-Tek HMX CT scanner; voxel resolution 24 μm; 105 keV, 96 μA, 2000 projections; 3D reconstruction with CT Pro; volume processing with VGStudio MAX.
- Pre-processing: thresholding via in-house indicator kriging; removal of unconnected solids with ImageJ 3D Fill Holes.
- Data encoding: soil=255, water=127, air=0 in each voxel.

## Numerical modelling of air–water distribution
- Modelling approach: lattice-Boltzmann method (two-phase, single-component, two-relaxation times; TRT-LBM).
- Saturation targets: S_w = 0.8 and S_w = 0.2 (corresponding to 80% and 20% water saturation).
- Governing parameters: independent parameter λ = 1/3; ν = 1/6; Λ = 3/16; other specifics set to match incompressible Stokes flow.
- Wettability settings: W = 0.15 for S_w = 0.8 (fully wetting), W = 0.13 for S_w = 0.2 (mostly non-wetting); one image used 0.125.
- Boundary conditions: bounce-back at solid; hydrophobic (W=0) at boundary voxels containing air to reflect edge effects; hydrophilic (W>0) elsewhere.
- Initialization: water density P_I calculated from mass balance; initial water density distributed in two steps, then refined with an iterative procedure (double loop, main loop up to 10,000 time units; tolerance 0.005).
- Computation: run on high-performance computing nodes (two Intel E5-2620 v4 CPUs; Red Hat Linux 7.2).
- Thresholding: simulated densities thresholded at mean ρ = 1.225.

## Data specifications and file structure
- File naming: BDXX_R_SW.tif, where BD is bulk density (1.2, 1.3, 1.4, 1.5, 1.6 g/cm³), R is replicate (1–3), SW is saturation (20±0.5% or 80±0.5%).
- Image content: 512 z-slices per image; each voxel labeled as soil (255), water (127), or air (0).
- Data volume: 30 microstructures total, each with 512³ voxels.

## Data provenance and usage notes
- Soil source and preparation details cited from related work (Juyal et al., 2018; Bullion field site).
- Modelling framework and parameter choices referenced to Ginzburg (2005) and Genty & Pot (2013); validation or methodological details available in cited literature.
- Deposit reference: EIDCHELP-33383.