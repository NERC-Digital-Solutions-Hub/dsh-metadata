# This dataset consists of three complete sets of tiff images representing microCT scans of adult little skate ( Leucoraja erinacea ) axial columns.

## Overview
- Three complete TIFF image sets representing microCT scans of adult little skate axial columns.
- Specimens collected off the Massachusetts coast, USA, in 2019; currently housed at the University of Cambridge Museum of Zoology (UMZC 2021.50.1, 2021.50.2, 2021.50.3).
- Scans performed at the Cambridge Biotomography Centre using a Nikon XTEK H 225 ST MicroCT scanner.
- Skate1 and Skate3 scans collected in Jan 2020; Skate2 scan collected in Dec 2020.
- TIFFs can be imported into CT software to visualize skate anatomy.
- Supporting documents include comprehensive CT scanning parameters to enable replication.

## Data contents
- Image data
  - Skate 1: 1997 TIFF images
  - Skate 2: 1998 TIFF images
  - Skate 3: 3761 TIFF images
- Vertebral morphometrics
  - 13 landmark coordinates plotted on each vertebra
  - Landmarks extracted for vertebrae 26–70 (Skate 1 and Skate 3) and vertebrae 27–70 (Skate 2)
  - Landmark files: Skate1_vert_landmarks.nts, Skate2_vert_landmarks.nts, Skate3_vert_landmarks.nts
- Supporting documentation
  - CT scanning parameters: Skate1scanparameters.txt, Skate2scanparameters.txt, Skate3scanparameters.txt
  - 3D Cartesian landmark coordinates metadata produced with Checkpoint by Stratovan
- Visual reference
  - Skate_CT_skeleton.tif (image of a 3D vertebral reconstruction)
- Analysis script
  - skate_regions.R (R script for vertebral morphometric and regionalisation analyses; requires a landmark file)

## Data provenance and collection
- Collected in summer 2019 near Woods Hole, MA, as part of vertebral morphology and development research in cartilaginous fishes.
- Scans conducted at the Cambridge Biotomography Centre; specimens scanned with a Nikon XTEK H 225 ST MicroCT scanner.
- Vertebrae selection excludes the fused anterior region (first 25–26 vertebrae form a synarcual); landmarks begin at vertebra 26 (Skates 1 and 3) or vertebra 27 (Skate 2).
- Landmark coordinates generated in Checkpoint (Stratovan) and provided as .nts files.

## Data formats and accessibility
- TIFF image stacks for microCT volumes; 3D landmark coordinates in .nts text format; auxiliary image and R script provided.
- Documentation included to enable reproducibility of scanning and analyses.
- Designed to be importable into standard CT analysis software; parameters enable replication of the scan conditions.

## GIS- and spatial-analyst-oriented implications
- Provides 3D spatial representations of vertebral anatomy that can be translated into GIS-friendly formats (point clouds, 3D meshes, or voxel models).
- Landmark coordinates enable spatial analyses of vertebral morphology; compatible with 3D GIS workflows and spatial statistics.
- R script supports region-based analyses that can be mapped or visualized in spatial contexts; data can be integrated with other anatomical or comparative spatial datasets.

## Limitations and considerations for GIS use
- Small sample size (three specimens) and a single species; caution in broad generalization.
- Vertebrae 26–70 (or 27–70) are analyzed due to synarcual fusion; not all vertebrae are represented for landmarking.
- Data are anatomical rather than georeferenced; coordinates are local 3D Cartesian values tied to the vertebral frame of reference.
- Large data volumes (thousands of TIFFs) require appropriate data management and storage considerations.
- Access may depend on museum data policies and permissions for reuse.