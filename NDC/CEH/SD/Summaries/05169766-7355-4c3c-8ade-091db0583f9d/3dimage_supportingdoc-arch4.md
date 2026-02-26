# OVERVIEW:

- The dataset comprises 3D colour images from scanned insect specimens and modified intermediate images suitable for 3D printing.
- Modified intermediates combine traits from two specimens and are formatted for 3D printing.

## Data collection and generation methods

- Specimens collected June 2020 – August 2021 in England using a hand net; euthanized by freezing at -18 C for ~30 minutes; pinned and dried 6–24 hours.
- 3D images created via photogrammetry following a protocol adapted from Nguyen et al. 2014:
  - Specimens suspended on a motorized turntable against a white background; indirect lighting with LED panels.
  - Photographed from 36 angles per specimen (36 images per specimen: 3 vertical positions × 12 turntable orientations).
  - Wings removed and photographed separately to capture dorsal/ventral details; legs/antennae and wings later simplified in 3D.
  - 3D meshes built with 3DSOM; colour texture projected onto shapes to produce raw reconstructions (.obj with textures).
- Editing and morphing performed with Blender and Deformetrica:
  - Created transects in 3D morphological space along axes of shape, colour, pattern, and size.
  - Generated intermediate or extrapolated shapes along these axes.
  - Pattern manipulation used R scripts; colours assigned via median RGB values per pattern segment.
  - Printing limitations led to simplified legs/antennae shapes (cylindrical forms; uniform leg/antenna colour; grey wings).
  - Wings created as flat shapes with 0.4 mm thickness; printing could not reproduce transparency.
  - Final meshes combined, scaled to match endpoints, and attached to a base for stability.

## Data structure and formats

- Raw reconstructions (39 specimens):
  - .obj (3D shape)
  - _map0.jpg (texture)
  - .mtl (material)
  - Filenames derived from genus/species (e.g., Amellifera7).
- Modified intermediate images for printing (130 files):
  - .ply format
  - Filenames encode contributions from two specimens and trait composition (e.g., Ca1_025_Vv12_075.ply).
  - transect_details.csv documents the specimen contributions and trait combinations (S, P, C, Z) and their proportions.
- Supporting metadata:
  - reconstructed_specimens.csv: 39 rows, 15 columns (specimen_id, genus, species, sex, order, family, date_collect, time_collect, location, grid_ref, microhabitat, date_photo, specimen_quality, shape_quality, texture_quality).
  - transect_details.csv: 130 rows, 6 columns (file_name, category, specimen1, s1_prop, specimen2, s2_prop).

## Data quality and provenance

- Quality control involved human review of photogrammetry scans for artefacts (holes, extra features, misalignment) and integrity checks on modified intermediates.
- Quality indicators are recorded per specimen in reconstructed_specimens.csv (specimen_quality, shape_quality, texture_quality).
- All units are in millimeters; standard OBJ/PLY formats ensure cross-tool interoperability.
- Notes indicate not all specimens were scanned; only 39 raw reconstructions documented; 130 intermediates created.

## Metadata, documentation, and discoverability

- Detailed documentation of specimen metadata (collection date, location, microhabitat, grid reference) and quality descriptors.
- File naming conventions and trailable provenance provided (reconstructed_specimens.csv and transect_details.csv).
- Detailed descriptions of the transect construction, trait integration, and intermediate generation process included.

## Access, reuse, and potential applications

- Data suitable for morphometric analyses, 3D printing, and studies of phenotypic variation across insect specimens.
- The transect-based approach enables exploration of shape, colour, pattern, and size combinations between specimens.
- Useful for demonstrations of 3D data pipelines, from photogrammetry to printing, including quality control and documentation practices.
- Access considerations and potential barriers (not specified) may relate to file sizes, format needs, and the requirement to reference the transect_details.csv for trait composition.

## Data management considerations for Data Leaders

- Advantages:
  - Comprehensive provenance: specimen metadata, processing steps, and quality metrics are well-documented.
  - Clear data formats and naming conventions support discoverability and interoperability.
  - Versioned, modular structure (raw reconstructions vs. intermediates) enables reproducibility and re-use.
- Challenges and gaps:
  - Limited raw coverage (only 39 scanned specimens) relative to intermediate outputs (130 files); potential gaps in representativeness.
  - Printing-driven simplifications (legs/antennae/wings) may limit certain biological analyses and require careful interpretation.
  - Data standardization across multi-component 3D datasets (obj/ply, textures, morphometric endpoints) requires robust metadata pipelines.
- Recommendations:
  - Ensure long-term storage and version control for large 3D assets; maintain links between reconstructed_specimens.csv and corresponding .obj/.mtl/.jpg files.
  - Maintain clear documentation of the transect methodology and trait combination rules to support reuse across networks.
  - Consider expanding metadata to include software versions and processing parameters used in Blender, Deformetrica, and R scripts to enhance reproducibility.