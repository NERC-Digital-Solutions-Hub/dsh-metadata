# Three complete sets of tiff images representing microCT scans of adult little skate (Leucoraja erinacea) axial columns

## Overview
- Dataset of three complete sets of TIFF images from microCT scans of adult little skate axial columns.
- Collected in 2019 off the Massachusetts coast; currently housed at the University of Cambridge Museum of Zoology (UMZC 2021.50.1, 2021.50.2, 2021.50.3).
- Scans conducted at the Cambridge Biotomography Centre using a Nikon XTEK H 225 ST MicroCT scanner.
- Skate 1 and 3 scanned in January 2020; Skate 2 scanned in December 2020.
- Aimed at investigating vertebral morphology and development in cartilaginous fishes; vertebrae up to 70 were analyzed with 13 landmark coordinates per vertebra.

## Data contents
- Skate 1: 1997 TIFF images forming the CT scan.
- Skate 2: 1998 TIFF images forming the CT scan.
- Skate 3: 3761 TIFF images forming the CT scan.
- A 3D reconstruction image: Skate_CT_skeleton.tif.

## Supporting documentation and data products
- Comprehensive CT scanning parameters for replication:
  - Skate1scanparameters.txt
  - Skate2scanparameters.txt
  - Skate3scanparameters.txt
- Vertebral landmarks (3D Cartesian coordinates, 13 landmarks per vertebra), exported for each skate:
  - Skate1_vert_landmarks.nts
  - Skate2_vert_landmarks.nts
  - Skate3_vert_landmarks.nts
- Analysis script and regionalisation tool:
  - skate_regions.R (R script for vertebral morphometric and regionalisation analyses; requires a landmark file)
- Data visualization asset:
  - Skate_CT_skeleton.tif (image of a 3D vertebral reconstruction)

## Methods and repeatability
- Vertebrae up to number 70 were extracted; 13 landmarks annotated on each vertebra to quantify shape.
- Landmark coordinates deliberately start at vertebra 26 (skates 1 and 3) and vertebra 27 (skate 2) due to an initial synarcual fusion forming part of the pectoral fin support.
- The dataset is organized to be imported into standard CT software and analyzed with the provided R script, enabling reproduction and further morphometric analyses.

## Reuse, accessibility, and value
- Data are accompanied by full parametric details to enable replication of scanning conditions.
- Landmark data and morphometric scripts facilitate reuse in comparative morphology, vertebral development studies, and potential integration with other environmental or biodiversity datasets.
- Housed in a stable institutional repository (UMZC) with explicit file-level documentation to support transparency, verification, and long-term accessibility.