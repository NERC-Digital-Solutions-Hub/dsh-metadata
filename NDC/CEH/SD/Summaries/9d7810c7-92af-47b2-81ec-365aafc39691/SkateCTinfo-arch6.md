# This dataset consists of three complete sets of tiff images representing microCT scans of adult little skate ( Leucoraja erinacea ) axial columns.

## Overview
- Three complete TIFF image sets of microCT scans of adult little skate axial columns.
- Collected by the Marine Biological Laboratory, Woods Hole, MA, USA, in summer 2019; housed at the University of Cambridge Museum of Zoology (UMZC 2021.50.1, 2021.50.2, 2021.50.3).
- Scans performed at Cambridge Biotomography Centre, Department of Zoology, University of Cambridge using a Nikon XTEK H 225 ST MicroCT scanner (Keturah Smithson).
- Skate 1 and Skate 3 scans obtained January 2020; Skate 2 in December 2020.
- Part of a project investigating vertebral morphology and development in cartilaginous fishes.
  
## Data contents
- Vertebral scope: vertebrae up to 70 extracted from each scan; 13 landmark coordinates plotted on each vertebra to quantify shape.
- Landmark files: skate1_landmarks.txt, skate2_landmarks.txt, skate3_landmarks.txt (begin at vertebra 26 for Skate 1 and 3, and at vertebra 27 for Skate 2 due to a fused synarcual that supports the pectoral fins).
- TIFF data files:
  - Skate 1: 1997 TIFF images
  - Skate 2: 1998 TIFF images
  - Skate 3: 3761 TIFF images
- Supporting documents include:
  - CT scanning parameters: Skate1scanparameters.txt, Skate2scanparameters.txt, Skate3scanparameters.txt
  - Vertebral landmarks in 3D Cartesian coordinates: Skate1_vert_landmarks.nts, Skate2_vert_landmarks.nts, Skate3_vert_landmarks.nts
  - 3D reconstruction image: Skate_CT_skeleton.tif (for Skate 1)
  - R script for analyses: skate_regions.R (ver­tebral morphometric and regionalisation analyses; requires a landmark file)

## Access, replication, and reuse
- TIFF images can be imported into any CT software to visualize skate anatomy.
- Provided scanning parameters and landmark coordinates enable replication of CT processing and morphometric analyses.
- The included R script offers a starting point for region-based vertebral analyses using the landmark data.
  
## Provenance and potential uses
- Clear collection and processing provenance supports data discovery and reuse in comparative anatomy, vertebral morphology research, and methodological development for morphometrics.
- Enables cross-sample comparison across the three individuals (Skate 1, Skate 2, Skate 3) and replication of vertebral morphometric workflows.