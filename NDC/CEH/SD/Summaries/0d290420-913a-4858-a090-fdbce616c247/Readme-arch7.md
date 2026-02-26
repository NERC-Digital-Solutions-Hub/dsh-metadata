# Solid, air and water phase distributions of a UK sandy loam soil packed at five bulk densities, 2018

- Purpose and scope
  - 30 CT-based soil microstructure images showing distributions of soil, air, and water.
  - Two water saturation levels (20±0.5% and 80±0.5%) across five bulk densities, with three replicates each (total 30 images).
  - Each image is a 512x512x512 voxel volume representing a soil microstructure.

- Data structure and formats
  - Image files named in the format BDXX_R_SW.tif, where:
    - BDXX: bulk density values (1.2, 1.3, 1.4, 1.5, 1.6 g cm^-3)
    - R: replication (1, 2, or 3)
    - SW: water saturation (20±0.5% or 80±0.5%)
  - Voxel values: soil = 255, water = 127, air = 0

- Source material and preparation
  - Soil origin: sandy loam from Bullion field, James Hutton Institute, Invergowrie, Scotland (2011 collection).
  - Soil fraction: 1–2 mm aggregates; composition 55.7% sand, 31.0% silt, 13.3% clay; organic matter ~5.5%.
  - Soil sterilization by autoclaving (two cycles).
  - Microcosm setup: polyethene rings packed at five bulk densities (1.2–1.6 g cm^-3); adjusted gravimetric water contents to ensure equal air-filled pore spaces across treatments; three replicates per treatment (15 microcosms in total).

- CT imaging and reconstruction
  - Instrument: Metris X-Tek HMX CT scanner.
  - Resolution: 24 μm voxel size; 105 keV, 96 μA; 2000 projections.
  - Reconstruction: CT Pro v2.1; volume processing and export to image stacks with VGStudio MAX V2.2.

- Image pre-processing
  - Thresholding of X-ray CT data using an in-house indicator kriging method.
  - Removal of unconnected solids with ImageJ 3D Fill Holes plugin.

- Air–water distribution modelling (for saturation targets)
  - Lattice-Boltzmann method (two-phase, single-component, TRT) to obtain distributions at S_w = 0.8 and S_w = 0.2.
  - Model parameters and boundary conditions:
    - Independent parameter ξ = 1/3; velocity field defined with ν = 1/6 and Λ = 3/16.
    - Interaction parameters: W = 0.15 for S_w = 0.8 (fully wetting), W = 0.13 (except one case with 0.125) for S_w = 0.2.
    - Hydrophobic boundary conditions (W = 0) at boundary voxels containing air; hydrophilic otherwise.
    - Bounce-back at solid boundaries; density initialization for water based on mass balance.
  - Computational details:
    - Iterative solver with an initial approximation and a main loop; warm-up of 2,000 time units and main iterations of 10,000 time units; tolerance 0.005 (±0.5%).
    - Simulations run on HPC nodes (Intel E5-2620 v4 CPUs) under Red Hat Linux 7.2.

- Practical considerations for GIS use
  - Data are 3D voxel volumes suitable for volumetric analysis, potentially convertable to 3D rasters or slices for GIS workflows.
  - Clear semantic mapping in voxels: soil (255), water (127), air (0).
  - Large data volumes (30 full 512^3 volumes) and 24 μm resolution imply substantial storage and processing needs.

- Metadata, provenance, and references
  - Data deposit reference: EIDCHELP-33383.
  - Background methods and preparation details referenced to Juyal et al. (2018) Frontiers in Environmental Science, 6:73.
  - The dataset includes both the CT-derived microstructures and the modeled liquid distributions under defined saturations.