# Supporting documentation

- Overview
  - Dataset of 3D LiDAR (TLS) scans representing 0.5 ha permanent sample plots in Caatinga, NE Brazil.
  - Plots: PET-01 (Petrolina, Pernambuco) and SDA-01, SDA-02 (Serra das Almas Reserve, Ceará).
  - Collected as part of the Nordeste project to study Caatinga biodiversity, plant-soil-climate relationships, biomass, and ecosystem function.
  - Scans conducted between July 2017 and May 2019 using terrestrial laser scanning.

- Data content and formats
  - 32 files in total, comprising:
    - 20 xyz files for individual trees from PET (representative Caatinga-native trees), including outside (OUT) and indoor (IN) scans; multiple species scanned.
    - 10 m^2 processed point clouds for PET subplots (multiple scans per subplot) in xyz format with six columns: X, Y, Z, and RGB intensities.
    - 3D scans for SDA subplots (and related data) exported as ply or xyz formats.
  - File structure includes entries such as PET-01, SDA-01, SDA-02 with associated coordinates.
  - Data acquired with a Faro Focus TLS and processed/registered with Faro Scene; final outputs exported as xyz (and ply in some cases) with metric and radiometric capabilities.

- Location and timeframe
  - PET-01: Petrolina, Pernambuco, Brazil (Latitude -9.04803, Longitude -40.3198).
  - SDA-01: Serra das Almas, Crateus, Ceará, Brazil (Latitude -5.1468, Longitude -40.9282).
  - SDA-02: Serra das Almas, Crateus, Ceará, Brazil (Latitude -5.1414, Longitude -40.9149).
  - Scans collected across multiple years within July 2017 – May 2019.

- Scanning methodology
  - Target: representative trees and subplots within Caatinga; species scanned include Manihot pseudoglaziovii, Commiphora leptophloeos, Sapium glandulosum, and Cnidoscolus quercifolius.
  - Protocol:
    - Tag trees and/or mark subplot corners.
    - Capture multiple viewpoints (photos suggested; typical workflow includes ~4 photos per tree).
    - Record a low-resolution whole-tree/whole-subplot scan for reference.
    - For portions of trees, perform indoor scans with numerous angles/heights.
    - Use Faro Scene for processing and registration, export to xyz/ply.

- Processing workflow
  - Steps in Faro Scene:
    - Load scans; remove dark points; smooth scans.
    - Apply stray point and edge artifact filters.
    - Register scans manually ( Targets marked; optimization cloud-to-cloud).
    - Create a final point cloud; isolate the target with a clipping box; manually clean noise.
    - Wipe project history to free disk space; export the point cloud (xyz) or ply as needed.
  - For SDA plots, integrate approximately 10x10 m scans from multiple raw scans to generate a single, cohesive model.

- Plot/species details
  - Individual-tree scans represent multiple species native to Caatinga; indoor and outdoor sessions documented for PET trees.
  - Subplot scans (SDA) provide multi-view datasets for canopy or understory structure within the Serra das Almas plots.

- Data availability and structure
  - The dataset comprises multiple files describing tree- and subplot-level point clouds, with explicit representation in xyz (and ply) formats.
  - Each file contains six-column coordinates (X, Y, Z) with associated RGB intensities, enabling integration with GIS and 3D analysis workflows.

- Applications for GIS analysis
  - 3D point clouds support analyses of tree architecture, biomass estimation, carbon stock modeling, and canopy structure.
  - Can be integrated with other spatial datasets for habitat mapping and ecosystem functioning studies in GIS environments.
  - Useful for validating remote sensing products and for conservation planning in Caatinga and similar dry tropical biomes.

- Notes and caveats
  - Data require processing to consolidate multiple scans into single models (manual registration is used).
  - Formats include xyz (and ply) with radiometric information; coordinate references rely on TLS-derived locations and plot coordinates.
  - The documentation outlines detailed processing parameters and workflow, which may be necessary to reproduce or adapt for GIS-based analyses.