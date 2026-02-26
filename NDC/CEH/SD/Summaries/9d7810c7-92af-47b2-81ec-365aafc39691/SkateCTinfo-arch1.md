This dataset consists of three complete sets of tiff images representing microCT scans of adult little skate ( Leucoraja erinacea ) axial columns.

## Overview
- Collected by the Marine Biological Laboratory in Woods Hole, MA, USA, in summer 2019; specimens housed at the University of Cambridge Museum of Zoology (UMZC 2021.50.1, 2021.50.2, 2021.50.3).
- Scans performed at the Cambridge Biotomography Centre using a Nikon XTEK H 225 ST MicroCT scanner.
- Skate 1 and Skate 3 scanned in January 2020; Skate 2 scanned in December 2020.
- Scientific aim: investigate vertebral morphology and development in cartilaginous fishes.
- Scans can be visualized in any CT software; comprehensive scanning parameters are provided to enable replication.

## Dataset contents
- Raw image sets:
  - Skate 1: 1997 TIFF images
  - Skate 2: 1998 TIFF images
  - Skate 3: 3761 TIFF images
- Supporting documentation:
  - CT scan parameters: Skate1scanparameters.txt, Skate2scanparameters.txt, Skate3scanparameters.txt
  - Vertebral landmarks (3D Cartesian coordinates): Skate1_vert_landmarks.nts, Skate2_vert_landmarks.nts, Skate3_vert_landmarks.nts
  - 3D reconstruction image: Skate_CT_skeleton.tif
  - Analysis script: skate_regions.R (R script for vertebral morphometric and regionalisation analyses)
  - Landmark collection origin: landmarks collected in Checkpoint by Stratovan
- Landmark and vertebrae details:
  - Vertebrae extracted up to number 70 per skate
  - Landmark files include 13 landmarks per vertebra
  - Landmark files start at vertebra 26 for Skate 1 and Skate 3, and vertebra 27 for Skate 2 (first 25–26 vertebrae fused to form a synarcual supporting the pectoral fins)

## Data and landmark specifics
- Landmark coordinates are provided as text files with Cartesian coordinates for each vertebra mapped onto the CT-derived models.
- The included vertebral region image (Skate_CT_skeleton.tif) provides a visual reference of the vertebral column.

## How to use and reproduce analyses
- Visualization: import TIFFs into any CT software to view anatomy.
- Morphometric analysis: use skate_regions.R in conjunction with a corresponding vertebral landmark file to perform regionalisation analyses.
- Reproducibility: CT scanning parameters files enable replication of imaging setup; landmark files and the analysis script support replicating the morphometric workflow.

## Provenance and accessibility
- Data and supporting materials are organized with explicit file names to track provenance.
- All components needed to replicate the vertebral morphometric workflow are provided (raw images, landmarks, parameters, 3D reconstruction, and analysis script).