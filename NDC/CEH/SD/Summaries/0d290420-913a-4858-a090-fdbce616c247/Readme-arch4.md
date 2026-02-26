# Solid, air and water phase distributions of a UK sandy loam soil packed at five bulk densities, 2018

## Data scope and purpose
- 30 Computed Tomography (CT) based soil microstructures showing distributions of soil, air, and water.
- Two water saturations: 20±0.5% and 80±0.5% (volume fraction of visible pore space).
- Five soil bulk densities: 1.2, 1.3, 1.4, 1.5, 1.6 g cm^-3.
- Three replicates per bulk density per saturation (total 15 microcosms per saturation; 30 images overall).
- Each image: 512x512x512 voxels, voxel size 24 μm.
- Voxel values encode soil, water, and air as 255, 127, and 0 respectively.

## Data content and structure
- Filenames follow the pattern BDXX_R_SW.tif, where XX = bulk density (1.2–1.6), R = repetition (1–3), SW = water saturation (20 or 80).
- Each image comprises 512 slices in the z-direction and is stored as a TIFF stack.
- Domain size per image: 512×512×512 voxels.
- Voxel encoding explicitly assigns soil, water, or air per the specified grayscale values.

## Data provenance and preparation
- Soil origin: sandy loam from Bullion field, James Hutton Institute, Invergowrie, Scotland (collected 2011).
- Physicochemical composition: ~55.7% sand, 31.0% silt, 13.3% clay; organic matter ~5.5%; C/N ~17.1.
- Pretreatment: air-dried, aggregates sieved to 1–2 mm; sterilized by autoclaving (twice at 121°C, 100 kPa, 30 min, 24 h apart).
- Microcosm setup: polyethene rings (inner diameter 17.0 mm, height 15.0 mm) packed at five bulk densities; gravimetric water contents adjusted to equalize air-filled pore space across treatments (0.13, 0.11, 0.09, 0.07, 0.06 correspondingly).

## CT imaging parameters
- Instrument: Metris X-Tek HMX CT scanner.
- Voxel resolution: 24 μm.
- X-ray settings: 105 keV, 96 μA; 2000 projections.
- Reconstruction: Metris X-Tek CT Pro v2.1; visualization and export: VGStudio MAX V2.2.
- Output used for downstream processing and modelling.

## Image pre-processing and segmentation
- Thresholding: in-house indicator kriging method (Houston et al., 2013).
- Post-processing: removal of unconnected solid particles with ImageJ 3D Fill holes plugin.

## Air-water distribution modelling
- Modelling approach: two-phase single-component, two-relaxation-times lattice-Boltzmann model.
- Saturations simulated: Sw = 0.8 (fully wet) and Sw = 0.2.
- Key parameters: TRT-LBM, specific values linked to viscosity and boundary conditions; hydrophobic boundary treatment at pores intersecting image edges; bounce-back at solid boundaries.
- Initialization: water density set based on mass balance; remainder distributed near solid voxels adjacent to pore space.
- Iterative solution: two-loop solver with a warm-up (2,000 time units) and main loop (10,000 time units); tolerance 0.005 (±0.5%).
- Computation: runs on compute nodes with two Intel E5-2620 v4 CPUs under Red Hat Enterprise Linux 7.2.

## Data encoding and outputs
- Voxel values: soil = 255, water = 127, air = 0.
- Outputs are 3D TIFF stacks corresponding to each microstructure, with 512 slices along z.

## Data governance, quality, and reproducibility notes
- provenance and preparation are documented (field origin, sieving, sterilization, replication).
- Modelling methodology is described with software and parameters, enabling reproducibility.
- Potential caveats include thresholding method specifics, edge effects from image boundaries, and assumptions in boundary conditions for the lattice-Boltzmann simulations.