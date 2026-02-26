# Supporting documentation

## Dataset scope
- 3D LiDAR (TLS) scans representing 0.5 ha permanent sample plots in Caatinga, Brazil.
- Plots: two in Serra das Almas Reserve (SDA) and one in Petrolina (PET).
- Collected 2017–2019 as part of the Nordeste project.

## Nordeste project context
- Northeast Brazil Caatinga is dry with irregular rainfall; conservation and biodiversity work is limited.
- Nordeste project is a Brazilian–UK collaboration to study plant, soil, climate relationships and ecosystem function to inform conservation and modelling (growth, carbon, biodiversity, remote sensing).

## Data content and formats
- Total files: 32.
- PET plots (Petrolina):
  - 20 processed point clouds for 10 individual trees (xyz format). Species represented: Manihot pseudoglaziovii, Commiphora leptophloeos, Sapium glandulosum, Cnidoscolus quercifolius.
  - 3D point clouds for subplots (10 m × 10 m), scanned at multiple dates; format xyz with six columns (X, Y, Z, and RGB intensities).
  - Scans recorded both outdoors (nature) and indoors (lab) using the same protocol.
- SDA plots (Serra das Almas):
  - 10 m × 10 m subplots scanned with multiple raw scans; processed to a single model with metric and radiometric capabilities.
  - Original raw Faro scans (.fls and other formats) were converted to ply format for export.
- Data formats present: xyz (trees and subplots) and ply (subplots), with references to raw Faro Scene workflow for registration and processing.

## Location metadata
- PET-01 (Petrolina): latitude -9.04803, longitude -40.3198; city Petrolina; state Pernambuco; country Brazil.
- SDA-01 (Serra das Almas): latitude -5.1468, longitude -40.9282; Crateus; Ceara; Brazil.
- SDA-02 (Serra das Almas): latitude -5.1414, longitude -40.9149; Crateus; Ceara; Brazil.

## Scanning and processing workflow
- Equipment: Faro Focus TLS scanner; Faro Scene software for registration and export.
- Field procedure (illustrative): select representative tree/subplot, tag species/date, take multiple views/photos, perform initial low-res whole-tree scan, indoors scans of parts, then register scans, create a point cloud, clean noise with clipping, and export (xyz); project history wiped post-export to save space.
- Processing steps (as applied): load scans, remove dark points, smooth, apply stray point and edge artifact filters, manual registration (cloud-to-cloud), create point cloud, cleaning with a clipping box, delete noise, export to xyz (and ply for some SDA data).
- Consistency note: for SDA, raw data are available for fine registration using user-specified parameters.

## Data management, provenance, and sharing
- Data are documented with collection dates, locations, species, and site protocols; exports are available in standardized 3D point formats (xyz/ply) with explicit processing steps.
- Provenance includes the field collection protocol and the Faro Scene processing workflow (registration, filtering, and export) to ensure traceability from raw scans to final datasets.
- Suggested governance actions (for data stewards):
  - Attach a dataset-level license and data usage terms.
  - Include file-level metadata: tree/subplot IDs, plot IDs, species, date ranges, scanner model, software version, and processing parameters.
  - Maintain a clear record of provenance, including whether data are raw vs. processed, and any transformations applied.
  - Ensure clear naming conventions and documentation to support reuse across projects.

## Governance considerations and recommended actions for Data Stewards
- Align metadata with community standards for LiDAR/biodiversity datasets (plot id, tree id, subplot id, coordinates, date, species, sensor, processing steps).
- Provide metadata for file formats (xyz, ply) and for the processing pipeline (Faro Scene version, filters used, registration method).
- Document licensing, access rights, and any embargoes or restrictions (especially for ongoing conservation work or sensitive locations).
- Flag large data volumes and consider hosting or chunking strategies to facilitate discovery and download.
- Encourage updates to reflect any reprocessing or additional scans to maintain currentness.

## Potential challenges and considerations
- Large and multi-format dataset spanning multiple plots and years; require robust metadata and cataloging.
- Varied data formats (xyz, ply, possible raw formats) requiring standardization for interoperability.
- Need for clear user needs mapping to ensure discoverability and usability (e.g., who will use tree-level vs. subplot-level data, and for what analyses).
- Ensuring data are discoverable and usable by both ecosystem researchers and data managers across institutions.