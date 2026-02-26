# Scan and Segmentation Details

- Processing and down-sampling
  - All image stacks are down-sampled from 16-bit depth to 8-bit.
  - Cropped to region of interest to reduce processing requirements.
  - Voxel size reductions applied where indicated to further reduce processing when stacks remained large.

- Data lineage and provenance
  - Institutions involved include The Natural History Museum (NHMUK) and National Museums Scotland (NMS), among others.
  - Specimens scanned by various teams (e.g., Richard Abel, Stig Walsh, Estelle Bourdon) using Nikon Metrology HMX ST CT scanners.
  - Scanning performed along the axial axis; data originally reconstructed as 16-bit VGStudio Max VOL files and output as 8-bit BMP stacks.
  - Some entries include 16-bit DCM stacks or 8-bit MCS files after processing in Mimics (14.11).

- Metadata and data formats
  - Original data formats: 16-bit VGStudio Max VOL files; 16-bit DCM stacks for some entries.
  - Final/processed formats: 8-bit BMP stacks; in some cases 8-bit MCS stacks.
  - Documentation notes specify equipment, scanning parameters, and field of view for each specimen.

- Specimen scope and documentation
  - A wide range of birds and related taxa (e.g., Acanthorhynchus superciliosus, Alca torda, Aquila chrysaetos, Corvus corax, Struthio camelus, etc.).
  - For each specimen, details typically include:
    - Taxon and catalog or registration numbers (e.g., NHMUK S/1966.51.209, NMS Z.2000.08.105, etc.)
    - Institution and collection information
    - Scanning resolution (µm), number of slices, grid dimensions
    - Field of view (mm)
    - Annotations: Endocranial cast segmentation performed by Stig Walsh; flocculus cast removal also credited to Stig Walsh

- Data governance and usability
  - Consistent emphasis on provenance, with explicit attribution of segmentation work and processing steps.
  - Metadata-rich approach supports discoverability and reproducibility across institutions.
  - Standardized workflow across many specimens, enabling cross-sample comparisons while acknowledging format conversions and down-sampling.

- Quality control and potential limitations
  - Down-sampling from 16-bit to 8-bit involves loss of some tonal/detail fidelity; cropping and voxel size reductions balance processing feasibility with data usability.
  - Varied file formats between stages (VOL, DCM, BMP, MCS) may require careful metadata mapping for proper re-use.