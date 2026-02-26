# OVERVIEW

- The dataset comprises 3D color images from scanned insect specimens and modified intermediate images that are suitable for 3D printing.
- Outputs include raw 3D reconstructions (.obj with textures) and modified intermediate meshes (.ply), designed to explore and print morphologically varied specimens.

## What is included

- 39 raw reconstructions
  - Each consists of: .obj (shape), _map0.jpg (texture), .mtl (materials)
  - Named using the genus/species to allow unique identification
- 130 modified intermediate images for printing
  - .ply format
  - Filenames encode contributions from two source specimens and trait combinations
- Metadata and supporting files
  - reconstructed_specimens.csv: 39 rows of specimen-level data
  - transect_details.csv: 130 rows detailing how each intermediate image combines two specimens and which traits are used

## Collection and generation methods

- Collection
  - Location: England
  - Period: June 2020 – August 2021
  - Method: hand net; specimens euthanized by freezing at -18°C, pinned, dried 6–24 h
- Photogrammetry
  - Setup: suspended on motorized turntable with white background and indirect LED lighting
  - Angles: 36 photos per specimen (3 vertical positions × 12 turntable orientations)
  - Wings removed and photographed separately to capture abdominal patterns
- 3D reconstruction
  - Software: 3DSOM used to build meshes from outlines and project color textures onto 3D shapes
  - Output: raw reconstructions (.obj) with textures
- Digital editing and morphing
  - Blender used to create transects of similarity in 3D morph space
  - Four axes of variation: shape, colour, pattern, size
  - Shape deformations: Deformetrica (control-points-based large deformation mapping)
  - Pattern manipulation: custom R scripts; K-means clustering for color segments; distance maps used for interpolation
- Practical adjustments for printing
  - Legs and antennae simplified to standardized shapes (cylindrical) due to printing limits
  - Wings created as flat shapes with uniform 0.4 mm thickness and grey color
  - Wings removed from the body during photogrammetry, then re-attached conceptually in the final meshes
  - Base added for attachment and structural stability

## Data formats and units

- .obj files: 3D shapes in millimetres (XYZ)
- .ply files: 3D shapes in millimetres (XYZ)

## Metadata and quality control

- reconstructed_specimens.csv (39 rows; 15 columns) includes:
  - specimen_id, genus, species, sex, order, family, collection date and location, photo date, and quality assessments
  - quality fields: specimen_quality, shape_quality, texture_quality
- Quality review performed manually to check for artefacts, missing parts, extraneous features, and texture misalignments

## File naming and mapping

- Raw reconstructions: named after species with a trailing number (e.g., Amellifera7)
- Modified intermediates: filenames encode specimen contributions and trait mix (e.g., Ca1_025_Vv12_075.ply)
- transect_details.csv provides, for each intermediate:
  - file_name, category (experiment), specimen1, s1_prop, specimen2, s2_prop
- specimen details and trait combinations can be cross-referenced via reconstructed_specimens.csv and transect_details.csv

## How this can support analysis

- Enables study of morphological variation across four axes (shape, colour, pattern, size) and their combinations
- Provides both real-endpoint specimens and interpolated intermediates for modeling correlations and predictive morphology
- Useful for evaluating how composite phenotypes might be achieved or for validating 3D-printed physical analogs of insect morphology
- Metadata supports reproducibility, provenance tracking, and potential replication or extension of the transects with new specimen pairs

## Limitations and notes

- Wings and leg details are simplified in the final printed-ready meshes due to printing constraints
- Some specimens were not scanned; thus, not all possible combinations exist
- Colour in printed wings is uniform due to printing limitations
- Intermediates include v2 and v3 variants to reflect small design changes; see transect_details.csv for specifics