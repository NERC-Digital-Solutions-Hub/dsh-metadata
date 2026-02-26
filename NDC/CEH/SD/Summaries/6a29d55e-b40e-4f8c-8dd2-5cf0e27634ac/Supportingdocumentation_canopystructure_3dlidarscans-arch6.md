# Supporting documentation

- Purpose and context
  - Provides 3D LiDAR (TLS) scan data from Caatinga, Brazil, as part of the Nordeste project.
  - Aim: support conservation-relevant biodiversity and ecosystem-function research in a seasonally dry Caatinga biome; improve understanding of tree architecture, carbon, biodiversity, and remote sensing relationships.
  - Study area includes 0.5 ha permanent plots: SDA (Serra das Almas) in Crateus, Ceara and PET (Petrolina) in Pernambuco; scans collected between July 2017 and May 2019.

- Data content and scope
  - Dataset contains 32 files representing TLS data from trees and subplots.
  - PET plots ( Petrolina)
    - 20 files in xyz format: point clouds for 10 individual representative Caatinga trees scanned both outdoors (OUT) and indoors (lab, IN) using the same protocol.
    - Species scanned include Manihot pseudoglaziovii, Commiphora leptophloeos, Sapium glandulosum, and Cnidoscolus quercifolius.
    - 10 m2 representative subplots also scanned; multiple dates used for the same subplot.
  - SDA plots ( Serra das Almas)
    - 3 files in xyz/ply format: 10 m2 subplots scanned across multiple sessions; raw scans exist (.fls and other Faro formats) and were converted to ply.
  - Data formats
    - xyz files for tree point clouds (with X, Y, Z coordinates and RGB intensities).
    - ply files for processed/combined subplots.
  - Plot metadata
    - PTA coordinates and locations listed (GPS latitude/longitude, city, state, country) for PET and SDA plots.

- Data collection and provenance
  - Scanning performed with a TLS Faro Focus scanner; data registered and exported using Faro Scene software.
  - Protocol emphasizes: selecting representative tree/subplot, tagging, multi-view photos, initial low-res scans, indoors detailed scans, and comprehensive registration.

- Data processing workflow (reproducible pipeline)
  - Processing steps in Faro Scene:
    - Load scans; filter dark points; smooth scans.
    - Apply stray point and edge artifact filters.
    - Manual registration (cloud-to-cloud) using targets.
    - Create final point cloud; isolate the target with a clipping box; manual cleaning of noise.
    - Export final products as xyz; wipe project history to free space.
  - Model generation
    - For SDA, raw scans are available for user-defined registration and model generation (with emphasis on homogenization across scans).
    - Final outputs support metric and radiometric capabilities.

- Data quality, limitations, and usage notes
  - Raw and processed data enable flexible reprocessing and parameter selection by end users.
  - The dataset provides both outdoor and indoor scans (PET) and multiple temporal scans (subplots across dates) to support comparisons and model robustness.
  - Some sections note the need to homogenize scans and manually adjust registration to ensure accurate integration.

- Access, documentation, and potential outputs
  - Original raw scans (.fls and related formats) are available for reprocessing; converted ply files are provided for SDA subplots.
  - Processed xyz point clouds (and ply where applicable) support analysis of tree structure, volume, and canopy/subplot characteristics.
  - Documentation describes the end-to-end workflow, enabling researchers to reproduce or extend the dataset for related biodiversity, ecosystem function, and remote sensing studies.