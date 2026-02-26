# MicroCT 3D scans from Passer sparrows - house ( Passer domesticus) , Spanish ( Passer hispaniolensis) ,  and Italian ( Passer italiae) sparrows and F1 hybrids generated during a crossing experiment at the University of Oslo, Norway in 2014/2015.

## Overview
- A collection of high-resolution skull scans (MicroCT) from three Passer species and F1 hybrids resulting from a crossing experiment conducted in 2014/2015 at the University of Oslo.
- Data include 3D reconstructions and landmark-based morphometric analyses of each individual’s skull.

## Source and collection methods
- Samples derived from the Natural History Museum of Oslo under a material transfer agreement.
- Scanned with a high-resolution X-ray Waygate Technologies v|tome|x M 240kV CT system (26 μA) at the Hounsfield Facility, University of Nottingham, UK.
- 3D skull reconstructions created from projection data; scans exhibit ring artefacts mainly on the dorsal braincase but artefacts were not substantially affecting quality.
- Data are stored as .TIF images and reconstructed into 3D volumes; .VOL files analyzed with Avizo 9.1.0.

## Data processing and analysis
- 20 landmarks in 3D space were digitized three times per individual in Avizo; mean coordinates used for analysis.
- Landmarks placed on the right side and along the sagittal plane to avoid redundancy and because skulls are largely symmetrical; this reduces variables and degrees of freedom.
- Partial Generalized Procrustes Analysis (GPA) performed in R using geomorph (gpapgen) to translate, scale (centroid size normalized to 1.0), and rotate configurations for superimposition in tangent space.
- Shape defined as geometric features of the landmark configuration independent of size and orientation; size is represented by centroid size (square root of the sum of squared distances of landmarks from their centroid).

## Data nature and units
- Data are stored as STL files (stereolithography) describing triangulated 3D surfaces using Cartesian coordinates.
- STL files effectively represent skull wireframes with recorded landmarks.

## Quality control
- Average landmark coordinates checked for placement errors; any issues were corrected on the scans.

## Data structure
- Each file corresponds to the scan of a single individual.

## Metadata
- Metadata framework includes species, sex, and location of capture for each individual.
- Filenames correspond to individual STL files, with explicit fields embedded in the entries (e.g., species, sex, location).
- Examples of filename-to-metadata mappings:
  - 2019-1.stl: Species = P. domesticus × P. hispaniolensis; Sex = M; Location = badajoz, Spain
  - 2019-26.stl: Species = P. domesticus × P. hispaniolensis; Sex = F; Location = badajoz, Spain
  - E19-23.stl: Species = P. domesticus; Sex = F; Location = badajoz, Spain
  - HTE-01.stl: Species = P. domesticus; Sex = F; Location = oslo, Norway
  - HYB-10.stl: Species = P. domesticus × P. hispaniolensis; Sex = M; Location = badajoz, Spain
  - MAS_60.stl, MAS_62.stl, MAS_64.stl, MAS_66.stl, MAS-55.stl, MAS-56.stl, MAS52.stl, MAS53.stl, MAS54.stl, Mustazzo.stl, etc.: various combinations of P. italiae and locations in Italy
  - PD1.stl, PD2.stl, PD3.stl, PDxPH.stl, PH1.stl, PH2.stl, PH3.stl: additional hybrids and parental species with associated metadata in filenames
- Filenames encode key metadata fields to aid data discovery and association with the corresponding STL meshes.

## Software and references
- Software used: Avizo for 3D visualization/landmarking; R with geomorph package for Procrustes analysis.
- Methodological references:
  - Gower JC (1975) Generalized Procrustes analysis
  - Baken E, Collyer ML, Kaliontzopoulou A, Adams DC (2021) geomorph v.4.0 and gmShiny
- These references underpin the morphometric workflow and data analysis approach.

## Usage notes and potential applications
- Suitable for 3D shape analysis and cross-species/hybrid cranial morphology studies.
- Enables self-contained morphometric analyses by providing both raw STL surfaces and processed landmark coordinates (via mean values after GPA).
- Facilitates comparative studies across species and hybrids within the Passer sparrow complex, including assessment of size-shape relationships and symmetry assumptions.

## Provenance and access
- Specimens originate from the Natural History Museum of Oslo; scans conducted in the UK and processed with standard morphometrics workflows.
- Data organization emphasizes reproducibility: per-individual STL files, explicit metadata in filenames, and a documented analysis pipeline (GPA, tangent space, centroid size).