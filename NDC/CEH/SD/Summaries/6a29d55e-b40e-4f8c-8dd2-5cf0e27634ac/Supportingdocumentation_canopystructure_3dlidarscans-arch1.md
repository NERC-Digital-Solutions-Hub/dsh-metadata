# Supporting documentation

- Overview
  - Dataset of 3D LiDAR (TLS) scans representing 0.5 ha permanent sample plots in Caatinga, northeast Brazil, collected under the Nordeste project to study relationships among trees, soil, climate, and biodiversity; aims to support understanding of growth, carbon allocation, stocks, and ecosystem function.

- Geographic and temporal scope
  - Plots: PET-01 (Petrolina, Pernambuco) and SDA-01, SDA-02 (Serra das Almas, Crateús, Ceará), Brazil.
  - Timeframe: scans conducted between July 2017 and May 2019.
  - Coordinates provided for each plot (latitude, longitude) and place names.

- Dataset contents
  - 32 files total describing TLS data and processing.
  - Individual-tree scans: 20 files in xyz format representing processed point clouds for representative Caatinga trees (species include Manihot pseudoglaziovii, Commiphora leptophloeos, Sapium glandulosum, Cnidoscolus quercifolius).
  - Subplot scans: 10 files in ply/xyz formats representing representative subplots (Petrolina and Serra das Almas), captured across multiple dates.
  - Data include both outdoor (in nature) and indoor (lab) scans using the same protocol.
  - Scans collected with a Faro Focus TLS; registration and export performed via Faro Scene software.

- Species and plots
  - Species scanned across plots include Manihot pseudoglaziovii, Commiphora leptophloeos, Sapium glandulosum, and Cnidoscolus quercifolius.
  - SDA plots include multiple subplots within Serra das Almas; PET plot is a Petrolina subplot.

- Data formats and processing status
  - Raw scans originally in .fls and other Faro formats; converted to ply/xyz for distribution.
  - For PET: 10 m scale subplots with processed point clouds; for SDA: 10 m scale subplots with multiple raw scans per subplot required for integration into a single model.
  - Final outputs include crop/clip operations to isolate trees or subplots and manual noise cleaning.

- TLS data collection and processing workflow
  - Field protocol:
    - Tag a representative tree/subplot with species/date labels.
    - Take multiple photos from different viewpoints.
    - Perform an initial low-resolution 3D scan of the whole tree/subplot.
    - Scan a portion of the tree indoors with numerous angles/heights.
  - Processing steps (Faro Scene):
    - Load scans; remove dark points; smooth scans.
    - Apply stray point and edge artifact filters.
    - Manual registration of scans (cloud-to-cloud) to align scans.
    - Create a consolidated point cloud; clip to isolate target tree/subplot; clean noise.
    - Export final point cloud to xyz; wipe project history to free space.
  - Note: A consistent, documented workflow is provided to reproduce the 3D models and ensure comparability across scans.

- Data availability and access considerations
  - Documentation references the Faro Scene workflow and provides guidance for processing; raw data include all scans and formats related to the project.
  - Data management notes emphasize preserving provenance, but final delivery involves converted formats (ply/xyz) suitable for analysis and modelling.
  - Users may need substantial computing resources due to large 3D datasets and multi-scan registration requirements.

- Potential uses for data analysts
  - 3D modelling of tree architecture and subplot structure for biomass or carbon stock estimation.
  - Validation or calibration of remote sensing data and algorithms with ground-truth TLS measurements.
  - Exploration of species-specific architectural traits and how they relate to soil and climate variables.
  - Development and testing of data pipelines for integrating multi-source 3D data (trees and plots) with environmental datasets.