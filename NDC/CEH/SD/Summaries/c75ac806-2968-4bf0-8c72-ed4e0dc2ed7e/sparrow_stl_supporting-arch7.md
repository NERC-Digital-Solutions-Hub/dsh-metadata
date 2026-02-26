# MicroCT 3D scans from Passer sparrows - house ( Passer domesticus) , Spanish ( Passer hispaniolensis) ,  and Italian ( Passer italiae) sparrows and F1 hybrids generated during a crossing experiment at the University of Oslo, Norway in 2014/2015.

## Overview
- MicroCT 3D skull scans of sparrows and F1 hybrids from a crossing experiment (2014/2015) at the University of Oslo.
- Specimens originate from the Natural History Museum of Oslo; scanned at the University of Nottingham using a high-resolution CT system.
- 3D reconstructions produced from projections; analyses performed using landmark-based morphometrics (20 landmarks per skull, averaged across three digitizations).
- Data are stored as STL surface files with associated metadata and morphometric coordinates.

## Collection and generation methods
- Samples obtained from the Natural History Museum of Oslo under a material transfer agreement.
- Scanning performed with Waygate Technologies v|tome|x M 240kV CT system at 26 μA.
- Skull specimens rotated on a polystyrene mount; ring artefacts observed mainly dorsally near the braincase; artefacts not minimized as they did not significantly affect quality.
- Projections reconstructed into 3D skull models; .VOL files visualized/analysed in Avizo 9.1.0.
- Landmark data: 20 landmarks in 3D were digitized three times per individual in Avizo; mean coordinates used for analysis.
- Right-side landmarks were used on the sagittal plane to avoid redundancy due to symmetry; this reduces variables and degrees of freedom.

## Data format, structure, and processing
- Nature and units: Data recorded as STL files (stereolithography) describing triangulated 3D surfaces; landmarks captured as part of the surface geometry.
- Quality control: Average landmark coordinates checked for placement errors and corrected on scans.
- Data structure: Each STL file corresponds to a single individual.
- Landmark and morphometrics: Landmark configurations are translated, scaled to centroid size = 1, and rotated (Generalized Procrustes Analysis) to minimize distance; configurations are superimposed in tangent space to separate shape from size.
- Size definition: Centroid size is the square root of the sum of squared distances of landmarks from their centroid.
- Source and tools: Landmark coordinates sorted in a 3D array in R; Procrustes analysis performed with gpapgen() in geomorph (references provided).

## Metadata and file organization
- Metadata table includes species, sex, and capture location for each STL file.
- Filenames correspond to individual STL files (e.g., 2019-1.stl, 2019-26.stl, HYB-10.stl, MAS_60.stl, etc.).
- Examples of metadata entries: species (P. domesticus XP P. hispaniolensis; P. hispaniolensis; P. italiae), sex (M/F), location (e.g., badajoz_spain, oslo_norway, puglia_italy).

## Quality control and data quality
- Manual placement of landmarks validated by examining average coordinates; any identified issues corrected on the scans.
- Consistency maintained by using a single side (right) for symmetry considerations.

## GIS integration notes for spatial analyses
- 3D skull surfaces (STL) can be linked to capture locations (geographic context) in GIS workflows for spatial morphometric studies.
- Metadata includes location data that can be georeferenced for cross-site comparisons (e.g., oslo_norway, badajoz_spain, puglia_italy).
- Landmark and Procrustes-derived shape data enable quantitative comparisons of morphology across populations or sites within a geospatial framework.

## References
- Gower, JC (1975) Generalized Procrustes analysis, Psychometrika, 40, 33-51.
- Baken, E., Collyer, ML., Kaliontzopoulou, A., Adams, DC (2021) geomorph v.4.0 and gmShiny: Enhanced analytics and a new graphical interface for a comprehensive morphometric experience, Methods in Ecology & Evolution, 12, 2355-2363.