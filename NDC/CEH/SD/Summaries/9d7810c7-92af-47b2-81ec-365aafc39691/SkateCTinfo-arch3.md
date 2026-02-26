# This dataset consists of three complete sets of tiff images representing microCT scans of adult little skate ( Leucoraja erinacea ) axial columns

## Overview
- A dataset of microCT scans from adult little skate vertebral columns collected off the Massachusetts coast in summer 2019.
- Scans performed at the Cambridge Biotomography Centre using a Nikon XTEK H 225 ST MicroCT scanner.
- Skates 1 and 3 scanned Jan 2020; Skate 2 scanned Dec 2020.
- Specimens housed at the University of Cambridge Museum of Zoology with accession numbers UMZC 2021.50.1, 2021.50.2, and 2021.50.3.
- Project aims to investigate vertebral morphology and development in cartilaginous fishes.

## Data content
- Three complete TIFF image sets representing CT scans:
  - Skate 1: 1997 TIFF images
  - Skate 2: 1998 TIFF images
  - Skate 3: 3761 TIFF images
- 3D vertebral landmark data:
  - skate1_vert_landmarks.nts
  - skate2_vert_landmarks.nts
  - skate3_vert_landmarks.nts
  - Landmarks begin at vertebra 26 for Skates 1 and 3, and vertebra 27 for Skate 2 (first 25–26 vertebrae fused to form a synarcual).
- CT reconstruction visualization:
  - Skate_CT_skeleton.tif
- Data files enabling analysis:
  - Comprehensive CT scanning parameter documents for repeatability:
    - Skate1scanparameters.txt
    - Skate2scanparameters.txt
    - Skate3scanparameters.txt
  - R script for ventrebral morphometric and regionalisation analyses:
    - skate_regions.R

## Supporting documents and tools
- Verterbral landmark coordinates provided in three text/landmark files (as above).
- 3D reconstruction image (Skate_CT_skeleton.tif) illustrating the vertebral column.
- R-based analytical workflow (skate_regions.R) requires a corresponding landmark file to run analyses.

## Methods and reproducibility
- Scans were designed to be importable into any CT software for visualization.
- Landmark-based morphometric analysis prepared to quantify vertebral shape and regionalisation.
- The inclusion of scanning parameters and landmark coordinates supports replication and independent verification of results.

## Access, sharing, and governance considerations
- Supporting documentation accompanies the dataset to facilitate replication and reuse.
- The dataset provides raw imagery, landmark coordinates, and a reproducible analysis script, supporting openness and transparency.
- Metadata completeness (e.g., scan parameters, vertebral numbering) is essential for accurate interpretation and reuse.

## Relevance to monitoring frameworks
- Demonstrates a structured approach to assembling a monitoring-quality dataset: raw imaging data, clearly defined anatomical landmarks, and a reproducible analysis pipeline.
- Highlights critical aspects for monitoring datasets:
  - Thorough metadata (scanning parameters, vertebral numbering, anatomical regions)
  - Open access to data and analysis scripts to enable independent validation
  - Documentation of data processing steps and analytical workflows
- Provides a model for linking image-based phenotypic data to morphometric analyses that could inform environmental health indicators in fish populations.

## Key considerations for policymakers and data stewards
- The importance of including detailed scanning and measurement protocols to ensure comparability across studies.
- The value of publishing supporting landmark files and analysis scripts to support reproducibility in monitoring efforts.
- Attention to data governance and metadata quality to reduce barriers to data integration and long-term usability.