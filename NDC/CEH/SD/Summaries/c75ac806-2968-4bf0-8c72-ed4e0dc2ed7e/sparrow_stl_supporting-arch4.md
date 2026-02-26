# MicroCT 3D scans from Passer sparrows - house ( Passer domesticus) , Spanish ( Passer hispaniolensis) , and Italian ( Passer italiae) sparrows and F1 hybrids generated during a crossing experiment at the University of Oslo, Norway in 2014/2015.

## Overview
- Dataset consists of MicroCT 3D skull scans across three Passer species and F1 hybrids from a crossing experiment conducted in 2014/2015 at the University of Oslo.
- Source materials come from the Natural History Museum of Oslo under a material transfer agreement.
- Scans were acquired with a high-resolution X-ray CT system (Waygate Technologies v|tome|x M 240kV) at the University of Nottingham, UK.
- Outputs include 3D reconstructions, landmark data, and processed shape/size analyses.

## Data provenance and access
- Sample provenance: Natural History Museum of Oslo; material transfer agreement in place.
- Scanning facility and instrument details: high-resolution CT at Hounsfield Facility, Sutton Bonington Campus, University of Nottingham.
- Artefacts: ring artefacts present in dorsal braincase area due to continuous skull rotation; artefacts deemed not to significantly affect scan quality.
- Data processing lineage: from raw projections to .TIF reconstructions, then to .VOL files for visualization/analysis in Avizo 9.1.0.

## Data contents and structure
- Data format:
  - STL files describing triangulated 3D surfaces for each individual skull.
  - Coordinates include 20 landmarks in 3D space, recorded (triplicated) and averaged for analysis.
- Landmarking approach:
  - Landmarks placed on the right side (sagittal plane) to reduce redundancy and because skulls are largely symmetrical.
  - 3D coordinates organized in a single 3D array; repeated digitization followed by mean calculation.
- Individual records:
  - Each STL file corresponds to one skull/individual.

## Data processing and analysis
- Landmark processing:
  - 20 landmarks digitized three times per individual; mean coordinates used.
  - Partial Generalized Procrustes Analysis (GPA) conducted to remove position, scale, and rotation effects, aligning configurations in tangent space.
- Shape vs. size:
  - Size defined by centroid size (square root of the sum of squared distances of landmarks to the centroid) and mathematically separated from shape.

## Metadata and identifiers
- Metadata scope includes species, sex, and location of capture for each individual.
- Filenames encode metadata (e.g., STL files like 2019-1.stl, E19-214.stl, HTE-01.stl, HYB-10.stl, etc.).
- Metadata table links each STL to species, sex, and capture location (e.g., badajoz_spain; oslo_norway).

## Quality control and validation
- Manual placement of landmarks checked by examining average coordinates; identified issues corrected on scans.

## Technical references
- Gower, JC (1975) Generalized Procrustes analysis.
- Baken, Collyer, Kaliontzopoulou, Adams (2021) geomorph v4.0 and related tools.

## Reuse considerations for data leaders
- Data formats and standards:
  - Use of standardized 3D surface format (STL) and clearly defined landmark conventions.
  - Provenance captured through MTAs and traceable scan/processing steps.
- Documentation and reproducibility:
  - Detailed workflow (from CT scanning to landmarking to GPA in R) enables reproducibility.
  - Software tools specified: Avizo 9.1.0 for visualization/analysis; R with geomorph for Procrustes analysis.
- Discoverability and metadata richness:
  - Rich metadata mapping filenames to species, sex, and capture location improves discoverability and cross-study interoperability.
- Data governance considerations:
  - Provenance and access controlled via MTAs; cross-institution collaboration evident (museum, university facilities).
- Potential applications for data leaders:
  - Basis for morphometric analyses across species and hybrids; scalable workflow for similarly structured datasets.
  - Clear data lineage supports performance of meta-analyses and cross-network data sharing under appropriate governance.