# This dataset consists of three complete sets of tiff images representing microCT scans of adult little skate ( Leucoraja erinacea ) axial columns.

## Overview
- Three complete TIFF image sets representing microCT scans of adult little skate vertebral columns.
- Collected in summer 2019 off Massachusetts coast; stored at University of Cambridge Museum of Zoology (UMZC 2021.50.1, 2021.50.2, 2021.50.3).
- Data designed for visualization in CT software and for vertebral morphometric analyses.

## Data assets and structure
- Skate 1: 1997 TIFF images
- Skate 2: 1998 TIFF images
- Skate 3: 3761 TIFF images
- Supporting data:
  - CT scanning parameter documents: Skate1scanparameters.txt, Skate2scanparameters.txt, Skate3scanparameters.txt
  - Vertebral landmark coordinates (3D Cartesian): Skate1_vert_landmarks.nts, Skate2_vert_landmarks.nts, Skate3_vert_landmarks.nts
  - Landmark coordinate files used for morphometrics: skate1_landmarks.txt, skate2_landmarks.txt, skate3_landmarks.txt
  - 3D reconstruction image: Skate_CT_skeleton.tif
  - R script for analyses: skate_regions.R (requires a landmark file)
- Vertebral data notes: vertebrae up to 70; landmark coordinates plotted on each vertebra (13 landmarks per vertebra)

## Provenance, methods, and repeatability
- Project focus: vertebral morphology and development in cartilaginous fishes.
- Collection details: specimens collected in 2019; scans performed Jan 2020 (Skate 1 & 3) and Dec 2020 (Skate 2) at Cambridge Biotomography Centre using Nikon XTEK H 225 ST MicroCT.
- Operators: Keturah Smithson.
- Repeatability aids: comprehensive scanning parameter files; clearly defined vertebral landmarks and numbering (first 25–26 vertebrae fused as synarcual).

## Metadata, standards, and documentation
- File-level documentation included to enable replication and reuse:
  - Scanning parameters per skate
  - Landmark coordinates per skate
  - Landmark coordinate lists aligned with vertebra numbering
- Data are described in a way that supports insertion into CT software and downstream morphometric workflows (R script provided for region/vertebral analyses).

## Accessibility, storage, and governance
- Stored under UMZC accession numbers, ensuring persistent visibility within a museum data governance framework.
- Dataset designed to be openly usable in standard CT software; supports discoverability through explicit file names and accompanying parameter/landmark files.
- No explicit licensing information provided; stewardship note: ensure appropriate data sharing terms with the museum and maintain linkage to accession identifiers for discoverability.

## Reuse, potential impact, and stewardship considerations
- Usability: TIFF image sets are importable into CT software; accompanying parameters and landmark files enable replication of analyses.
- Analysis readiness: R script ( skate_regions.R ) supports vertebral morphometrics; requires a vertebral landmark file.
- Stewardship considerations:
  - Maintain dataset integrity and provenance by preserving accession numbers and file naming conventions.
  - Consider adding formal metadata (e.g., licensing, data quality flags, methods DOI) to improve interoperability.
  - Monitor transfer and storage of large TIFF sets; consider scalable hosting or cataloging to support long-term accessibility.
  - Ensure updates to parameter files and landmark references remain synchronized with image data.