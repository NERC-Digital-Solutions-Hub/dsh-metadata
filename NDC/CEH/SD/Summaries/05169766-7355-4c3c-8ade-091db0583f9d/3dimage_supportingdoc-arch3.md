# OVERVIEW:

- A dataset comprising 3D colour images from scanned insect specimens and modified intermediate images suited for 3D printing.
- Modified intermediates are constructed to combine traits from two specimens, enabling creation of novel phenotypes in 3D space.

## COLLECTION AND GENERATION METHODS:

- Collection window: June 2020 to August 2021, from various locations in England using a hand net.
- Specimens euthanized by freezing (-18 C, ~30 minutes), pinned, posture stabilized, then dried (6–24 h).
- Photogrammetry protocol (adapted from Nguyen et al. 2014):
  - Specimens suspended on a motorized turntable against a white background; indirect lighting from two LED panels.
  - DSLR photography (Canon EOS 600D, macro lens) from 36 angles (3 vertical positions × 12 turntable orientations).
  - Wings removed for imaging and photographed separately to capture abdomen patterns.
- 3D reconstruction:
  - 3DSOM used to create raw meshes by carving shapes from outlines; textures mapped from photos.
  - Blender used for editing; creation of transects along axes of shape, colour, pattern, and size to generate intermediate phenotypes.
  - Digital removal of legs/antennae and wings due to processing/printing constraints; simplified reattachment later.
  - Shape deformations performed with Deformetrica; intermediate shapes derived along endpoints.
  - Pattern manipulation via custom R scripts; colour segments defined by K-means on RGB values; distance maps used to interpolate patterns.
  - Wings created as flat shapes with uniform 0.4 mm thickness and 50% grey colour due to printing limitations.
- Final assembly:
  - All body parts combined into a full mesh, scaled to endpoint body length, with a base for attachment and enhanced structural integrity.

## DATA PRODUCTS AND FILE STRUCTURE:

- Raw reconstructions:
  - 39 specimens with three files each: .obj (shape), _map0.jpg (texture), .mtl (materials).
  - File naming: genus initial + species name, e.g., Amellifera7.
  - Metadata on specimens stored in reconstructed_specimens.csv.
- Modified intermediate images (for 3D printing):
  - 130 .ply files, named to reflect contributions from two original specimens (e.g., Ca1_025_Vv12_075.ply).
  - transect_details.csv documents exact specimen contributions and trait selections (specimen1, specimen2, s1_prop, s2_prop; trait letters S/P/C/Z with possible 50% intermediates).
- Supporting metadata:
  - reconstructed_specimens.csv: 39 rows, 15 columns including specimen_id, genus, species, sex, date_collect, location, grid_ref, microhabitat, date_photo, and quality descriptors (specimen_quality, shape_quality, texture_quality).
  - transect_details.csv: 130 rows, 6 columns detailing file_name, category, specimen1, s1_prop, specimen2, s2_prop.

## QUALITY CONTROL AND DATA QUALITY:

- Raw scans reviewed for artefacts (holes, missing parts, misaligned textures, extra features); notes recorded in reconstructed_specimens.csv (shape_quality, texture_quality, specimen_quality).
- All modified intermediate images checked for integrity of shapes.

## METADATA, PROVENANCE, AND DATA FORMATS:

- Data formats and units:
  - Raw shapes: .obj with XYZ coordinates (millimetres); textures: .jpg; materials: .mtl.
  - Intermediates: .ply (millimetres).
- Provenance and documentation:
  - Detailed specimen metadata in reconstructed_specimens.csv (collection date, location, microhabitat, etc.).
  - Detailed file-level contributions and trait combinations in transect_details.csv.
  - Naming conventions and versioning evident in file names (including _v2, _v3 where applicable).

## ACCESS, SHARING, AND GOVERNANCE:

- Data organization emphasizes traceability, reproducibility, and clear data lineage (end-to-end from collection to intermediate outputs).
- Some general barriers noted for monitoring datasets (data availability, metadata quality, and data sharing) though this dataset provides extensive metadata and clearly documented transformations to support transparency and reuse.

## IMPLICATIONS FOR MONITORING FRAMEWORKS:

- Demonstrates robust metadata groundwork (reconstructed_specimens.csv, transect_details.csv) enabling traceability of data provenance and trait combinations.
- Highlights the necessity of documenting data transformations and processing steps (from raw photogrammetry to intermediate, print-ready models) to ensure replicability.
- Illustrates handling of methodological constraints (e.g., removal and later reattachment of delicate structures) and explicit recording of such limitations.
- Underscores the importance of standardized file naming, version control, and clear communication of data quality metrics to facilitate governance and reuse.