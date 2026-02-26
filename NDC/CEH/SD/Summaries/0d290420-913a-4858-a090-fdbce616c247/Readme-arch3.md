# Solid, air and water phase distributions of a UK sandy loam soil packed at five bulk densities, 2018

- Overview
  - Provides 30 Computed Tomography (CT) based soil microstructures showing distributions of soil, air, and water.
  - Two water saturations (20 ± 0.5% and 80 ± 0.5%), five soil bulk densities, three replicates per density (total 30 images).
  - Each image is 512 × 512 × 512 voxels; grayscale encoding: soil = 255, water = 127, air = 0.

- Dataset composition and variables
  - Images named as BDXX_R_SW.tif, where XX = bulk density (1.2, 1.3, 1.4, 1.5, 1.6 g cm^-3), R = repetition (1, 2, or 3), SW = water saturation (20±0.5% or 80±0.5%).
  - Each volume element (voxel) is categorized as soil, water, or air with the specified grayscale values.
  - 30 microstructures correspond to all combinations of the five bulk densities, two saturations, and three replicates.

- Soil preparation and microcosm preparation
  - Soil source: sandy loam from Bullion field (James Hutton Institute, Invergowrie, Scotland; collected 2011).
  - Composition (1–2 mm fraction): ~55.7% sand, ~31.0% silt, ~13.3% clay, ~5.5% organic matter; C/N ~17.1.
  - Soil sterilized by autoclaving (two cycles, 121 °C, 100 kPa, 30 min, 24 h interval).
  - Microcosms: polyethene rings (inner diameter 17.0 mm, height 15.0 mm) packed at five bulk densities (1.2–1.6 g cm^-3).
  - Matched air-filled pore space across treatments via gravimetric water contents (0.13, 0.11, 0.09, 0.07, 0.06 for densities).

- Computed Tomography imaging
  - Scanner: Metris X-Tek HMX CT (NIKON Metrology, UK).
  - Resolution: 24 μm voxel size; energy 105 keV; current 96 μA; 2000 projections.
  - Reconstruction via Metris X-Tek CT Pro v2.1; volume processing with VGStudio MAX V2.2; exported image stacks to BMP for processing.

- Image pre-processing
  - Thresholding with an in-house indicator kriging method.
  - Removal of unconnected solid particles using ImageJ 3D Fill Holes plugin.

- Air-water distribution modelling
  - Two-phase single-component, two-relaxation-times lattice-Boltzmann model (TRT-LBM) to reach target saturations (S_w = 0.2 and 0.8).
  - Model parameters and boundary conditions:
    - Independent parameter set to 1/3; kinematic viscosity chosen to enforce incompressible Stokes flow.
    - Specific W values chosen to represent hydrophobic/hydrophilic boundaries; bounce-back at solid boundaries.
    - Hydrophobic boundary voxels (air present at boundary) set W = 0; other regions use W > 0.
  - Initial water particle density (Ρ) computed from a mass-balance equation using densities of gas and liquid phases, saturation, porosity, and image size.
  - Iterative solver with two-stage initialization, main loop up to 10,000 LB time units; tolerance 0.005 (±0.5%).
  - Computations performed on nodes with dual Intel E5-2620 v4 CPUs (Red Hat Linux).

- Data outputs and accessibility
  - Each microstructure contains 512 z-slices saved as .tif; voxel assignments as described.
  - For reference, original processing produced intermediate image stacks in .bmp after reconstruction; final dataset stores 512-slice volumes per image.
  - File naming convention (BDXX_R_SW.tif) enables traceability of density, replicate, and saturation.

- Reproducibility, provenance, and metadata considerations
  - Detailed methodological lineage: soil source and preparation, CT imaging parameters, pre-processing steps, and LBM modelling setup.
  - Explicit mapping of voxel values to phases enhances interoperability and reuse in monitoring frameworks.
  - Some constraints relevant to monitoring use:
    - Autoclaved, laboratory-prepared soil may differ from in-field conditions.
    - Saturation states are fixed at two discrete levels; dynamic field conditions are not represented.
    - Boundary condition choices and hydrophobic/hydrophilic assumptions influence pore-scale distributions.

- Relevance for monitoring frameworks
  - Provides baseline, high-resolution pore-scale distributions of soil, water, and air across multiple densities and saturations, enabling:
    - Calibration and validation of pore-scale moisture transport and gas diffusion models.
    - Assessment of how bulk density and saturation influence pore connectivity and phase distributions.
    - Support for reporting on soil health indicators related to pore structure and water–air partitioning.
  - The dataset emphasizes data quality, metadata richness, and clear data provenance—key considerations for monitoring-related data governance and sharing.

- Limitations and caveats for interpretation
  - Laboratory-controlled conditions and sterilization may limit direct field applicability.
  - Finite sample size (five densities, two saturations, three replicates) may not cover all field scenarios.
  - Modelling assumptions (LBM parameters, boundary conditions) influence exact phase distributions; use with awareness of these assumptions.