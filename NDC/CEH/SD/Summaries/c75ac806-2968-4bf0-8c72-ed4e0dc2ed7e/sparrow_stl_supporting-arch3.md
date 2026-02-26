# MicroCT 3D scans from Passer sparrows - house ( Passer domesticus) , Spanish ( Passer hispaniolensis) , and Italian ( Passer italiae) sparrows and F1 hybrids generated during a crossing experiment at the University of Oslo, Norway in 2014/2015.

## Overall purpose
- Document a dataset of high-resolution skull scans intended for shape and size analysis of sparrow cranial morphology.
- Create standardized 3D representations and morphometric coordinates to compare individuals across species and hybrids.

## Collection and generation methods
- Samples sourced from the Natural History Museum of Oslo under a material transfer agreement.
- Scanning performed with a high-resolution X-ray CT system (Waygate Technologies v|tome|x M 240kV) at the Hounsfield Facility, University of Nottingham.
- Procedure: skulls rotated on a mount during projection acquisition; ring artefacts observed (primarily dorsal braincase) but not mitigated as they did not significantly affect quality.
- Output: 3D reconstructions in STL format; visualized/analysed with Avizo 9.1.0.
- Landmarking: 20 landmarks in 3D per individual, measured three times and averaged; right-side sagittal plane used to avoid redundancy and simplify analyses due to general symmetry.

## Nature and units of record values
- Data stored as STL files describing triangulated skull surfaces with recorded landmarks.
- Landmarks and skull geometry represented in Cartesian coordinates.

## Data processing and analysis
- Landmark data organized into a 3D array in R.
- Generalized Procrustes Analysis (GPA) performed to remove effects of translation, rotation, and scale.
- Tangent-space analysis used to define shape independent of size.
- Centroid size used as size metric (square root of sum of squared distances of landmarks from centroid).
- Shape is defined as geometric features of landmarks excluding size, location, and orientation.

## Quality control
- Average landmark coordinates checked for placement errors and corrected on scans as needed.

## Data structure and metadata
- One file per individual; each STL file corresponds to a single skull.
- Metadata table includes species, sex, and capture location for each individual.
- Filenames encode metadata (e.g., species, sex, location) and map to corresponding STL files (e.g., 2019-1.stl, HYB-10.stl, etc.).

## Data governance and sharing considerations
- Metadata provided to support provenance and reproducibility.
- Data processing steps and software used (geomorph in R, GPA) are documented to enable replication.
- The text notes sharing and transparency expectations (e.g., underlying data sharing) in broader monitoring framework terms; specific public data access details are not provided, but the structure supports openness and verification.

## References
- Gower, JC (1975) Generalized Procrustes Analysis.
- Baken, E. et al. (2021) geomorph v.4.0 and gmShiny: enhanced analytics for morphometrics.