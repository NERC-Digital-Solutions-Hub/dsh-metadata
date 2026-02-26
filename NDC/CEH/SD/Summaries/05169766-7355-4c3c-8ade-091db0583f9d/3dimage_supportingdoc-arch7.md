# OVERVIEW

- The dataset comprises 3D colour images from scanned insect specimens and modified intermediate images prepared for 3D printing.
- Raw reconstructions are provided as 3D meshes with textures; modified intermediate images are provided as printable 3D meshes.
- 3D images were produced via photogrammetry from specimens collected in England between June 2020 and August 2021.

## Data Content

- Raw reconstructions
  - 39 reconstructions at the specimen level
  - Each consists of: .obj (shape), _map0.jpg (texture), .mtl (materials)
  - Filenames follow a genus/species convention (e.g., Amellifera7)
- Modified intermediate images (suitable for 3D printing)
  - 130 .ply files
  - Each file name encodes contributions from two specimens and trait mappings
  - Trajectory and trait combinations described in transect_details.csv
- Associated metadata
  - reconstructed_specimens.csv: 39 rows of specimen-level data
  - transect_details.csv: 130 rows detailing file_name and specimen contributions

## Collection and Production Methods

- Collection
  - Field collection in England (June 2020 – August 2021) using hand nets
  - Specimens euthanized by freezing at -18°C for ~30 minutes, pinned, and dried
- Photogrammetry workflow
  - Specimens suspended on a motorized turntable with white background and indirect lighting
  - DSLR: Canon EOS 600D with macro lens; 36 photographs per specimen from multiple angles
  - Wings removed during imaging; legs and antennae removed digitally for processing and re-added later
- 3D reconstruction and texture
  - 3DSOM used to generate raw 3D shapes from photographs
  - Colour texture projected onto the 3D shape
  - Blender used for editing; Deformetrica used for shape morphing via large deformation mapping
  - Pattern manipulation performed with custom R scripts; colour segmentation via K-means (K=2)
  - Intermediate/shape processing: base meshes standardized for printing; wings rendered as flat shapes with grey colour; legs/antennae simplified to printable forms
- Printing and assembly considerations
  - 0.6 mm diameter legs, 0.8 mm antennae; wings 0.4 mm thick
  - Antennal extensions may be added for strength and trimmed after printing
  - Final assembly combines body, legs, antennae, wings, and base

## Data Formats, Naming, and Structure

- File formats
  - Raw: .obj (shape), _map0.jpg (texture), .mtl
  - Modified: .ply (printable meshes)
- Naming conventions
  - Raw reconstructions: genus initial + species name + specimen number (e.g., Amellifera7)
  - Modified intermediates: [specimen1]_[specimen1 contrib]_[specimen2]_[specimen2 contrib].ply
  - Contributions expressed as percentages or trait letters (S, P, C, Z) with possible 50 indicating halfway
  - Some files labeled with _v2 or _v3 for alternate base designs
- Metadata files
  - reconstructed_specimens.csv: 39 rows, 15 columns (including specimen_id, taxonomic info, collection details, and quality indicators)
  - transect_details.csv: 130 rows, 6 columns (file_name, category, specimen1, s1_prop, specimen2, s2_prop)

## Quality Control and Provenance

- Manual quality checks performed on all raw scans
  - Review for artefacts such as holes, missing appendages, misaligned textures
  - Quality notes recorded in reconstructed_specimens.csv (specimen_quality, shape_quality, texture_quality)
- Integrity checks performed on all modified intermediate images

## Units and Coordinates

- 3D coordinates are in millimetres
  - .obj and .ply files follow standard XYZ millimetre conventions

## Relevance for GIS Specialists

- Metadata includes collection location details (location description and six-figure grid references), enabling spatial context for distribution studies.
- Data products provide 3D spatial representations of biological morphology that can complement geo-spatial analyses or visualization in GIS environments, particularly for educational or policy-facing map-based demonstrations of biodiversity morphology.
- The dataset highlights data provenance, normalization, and transformation workflows—useful for mapping data lineage and reproducibility in GIS data pipelines.