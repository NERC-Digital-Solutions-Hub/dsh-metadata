# MicroCT 3D scans from Passer sparrows - house ( Passer domesticus) , Spanish ( Passer hispaniolensis) , and Italian ( Passer italiae) sparrows and F1 hybrids generated during a crossing experiment at the University of Oslo, Norway in 2014/2015.

## Overview
- 3D skull scans (MicroCT) of Passer domesticus, P. hispaniolensis, P. italiae, and F1 hybrids from a crossing experiment (Oslo, 2014/2015).
- Data intended for morphometric analysis and cross-study comparability.

## Source and data generation
- Samples drawn from Natural History Museum of Oslo via material transfer agreement.
- Scanning performed with Waygate Technologies v|tome|x M 240kV CT at 26 μA, Hounsfield Facility, Sutton Bonington Campus, University of Nottingham, UK.
- Rotation-based acquisition; ring artefacts observed (not significantly affecting scan quality).
- TIFF images reconstructed into 3D skull models; .VOL files created for analysis with Avizo 9.1.0.

## Landmarking and morphometrics
- 20 landmarks in 3D coordinates digitized three times per individual; mean used for analysis.
- Landmarks taken on the right side only in the sagittal plane to reduce redundancies (skulls largely symmetric).
- Data organized in a 3D array in R; Partial Generalized Procrustes Analysis (GPA) via geomorph (gpapgen) to align shapes.
- Procedures:
  - Translate to common centroid
  - Scale to centroid size = 1
  - Rotate to minimize Procrustes distance
  - Superimpose in tangent space
- Shape defined as geometric features excluding scale, location, rotation; size defined separately by centroid size (square root of the sum of squared landmark distances from the centroid).

## Data format and structure
- Outputs stored as STL files (triangulated 3D surfaces) representing skull scans with landmarks.
- Each STL file corresponds to a single individual.

## Metadata and naming
- Metadata tracked: species, sex, location of capture for each individual.
- Filenames correspond to STL files and encode information (e.g., species combinations, sex, location).
- Examples include various P. domesticus x P. hispaniolensis crosses, P. hispaniolensis, P. domesticus, and P. italiae each with multiple sample IDs and locations (e.g., badajoz_spain; oslo_norway; puglia_italy).

## Quality control
- Verification of landmark coordinates across scans; manual corrections applied where needed.

## Provenance and references
- Gower, J.C. (1975) Generalized Procrustes Analysis.
- Baken, Collyer, Kaliontzopoulou & Adams (2021) geomorph v.4.0 and gmShiny.

## Reuse and data accessibility
- Data are prepared for integration with other datasets and standardised analyses (environmental/morphometric context).
- Metadata and standardized file formats (STL) facilitate storage, sharing, and potential upload to appropriate data portals.
- Clear documentation of methods enables replication and cross-study comparisons, supporting long-term environmental and phenotypic monitoring.