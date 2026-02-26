# This dataset consists of three complete sets of tiff images representing microCT scans of adult little skate ( Leucoraja erinacea ) axial columns.

## Overview
- Three complete microCT datasets of adult little skate axial columns collected off the Massachusetts coast in summer 2019.
- Housed at the University of Cambridge Museum of Zoology (UMZC 2021.50.1, 2021.50.2, 2021.50.3).
- Scans performed at Cambridge Biotomography Centre using a Nikon XTEK H 225 ST MicroCT scanner.
- Skate1 and Skate3 scans acquired January 2020; Skate2 scan acquired December 2020.
- TIFF image stacks can be imported into any CT software for visualization.
- Supporting documentation provided to enable repeatability and verification of methods.

## Data Content
- Data sets:
  - Skate1: 1997 TIFF images
  - Skate2: 1998 TIFF images
  - Skate3: 3761 TIFF images
- Vertebral focus: vertebrae up to number 70 extracted; 13 landmark coordinates plotted on each vertebra to quantify shape.
- Landmark data:
  - Skate1_landmarks.txt
  - Skate2_landmarks.txt
  - Skate3_landmarks.txt
  - Landmark files begin at vertebra 26 for Skates 1 and 3; vertebra 27 for Skate 2 (first 25-26 vertebrae fused as a synarcual supporting the pectoral fins).
- Supporting parameter documentation (repeatability):
  - Skate1scanparameters.txt
  - Skate2scanparameters.txt
  - Skate3scanparameters.txt
- Landmark coordinates in 3D:
  - Skate1_vert_landmarks.nts
  - Skate2_vert_landmarks.nts
  - Skate3_vert_landmarks.nts
- Visualisation:
  - Skate_CT_skeleton.tif (3D reconstruction image of Skate 1)
- Analysis:
  - R script skate_regions.R for vertebral morphometric and regionalisation analyses (requires a vertebral landmark file)

## Access, Provenance and Documentation
- Provenance: scans conducted at Cambridge Biotomography Centre; specimens curated by UMZC.
- Comprehensive documentation included to enable replication of scans and analyses (parameter files, landmark files, and the analysis script).
- Clear association between raw imaging data, landmark data, and analytic tooling.

## Usage and Reuse
- Primary use: vertebral morphology and regionalisation analyses in cartilaginous fishes.
- Reuse potential: cross-study comparisons, method development in morphometrics, educational demonstrations, and reproducible research workflows.
- Analytical workflow: import TIFF stacks into CT software; use landmark files for morphometric analyses; run skate_regions.R to perform regionalisation analyses.

## Discoverability and Metadata
- File naming and structured documentation enhance discoverability and reuse.
- Metadata includes species (Leucoraja erinacea), specimen origin (Massachusetts coast), collection date (summer 2019), and institutional housing (UMZC) with accession numbers.
- Supports replication through explicit scanning parameters and landmark data.

## Data Stewardship and Future Work
- Demonstrates robust data stewardship with preserved imaging data, corresponding landmarks, reconstruction imagery, and analysis scripts.
- Data are prepared for reuse; future updates not indicated, but documentation supports ongoing interpretation and replication.