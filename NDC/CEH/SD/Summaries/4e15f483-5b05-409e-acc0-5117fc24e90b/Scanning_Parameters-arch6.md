# Scan and Segmentation Details

- The document compiles imaging and segmentation metadata for numerous specimens from The Natural History Museum, UK (NHMUK) and National Museums Scotland (NMS).

- Preparation steps common to all entries:
  - Image stacks were down-sampled from 16-bit depth to 8-bit and cropped to a region of interest to reduce processing requirements.
  - Voxel size reductions were applied when stacks remained too large after cropping and bit-depth reduction.
  - Scans were performed along the axial axis; endocranial casts were segmented and flocculus casts removed as part of the workflow.

- Institutional context and provenance:
  - Abbreviations used: NHMUK (The Natural History Museum) and NMS (National Museums Scotland).
  - Many scans were conducted under NERC Small Grant NE/H012176/1 and related projects; several entries note involvement of Intra-European Marie Curie Fellowship 255039.
  - Key personnel involved in segmentation and processing include Stig Walsh (endocranial segmentation and flocculus removal) and Monja Knoll (flocculus removal).

- Data acquisition details:
  - Imaging platform: Nikon Metrology HMX ST CT scanner used across entries.
  - Scanning orientation: axial axis for each specimen.

- Data products and formats:
  - Original data described as 16-bit VGStudio Max VOL files, later reconstructed and output as 8-bit BMP stacks.
  - Final outputs commonly include 8-bit BMP stacks or 8-bit MCS files; some entries also reference 16-bit DCM stacks.
  - Examples of final stack parameters include varying resolutions and slice counts (e.g., final resolutions around 10–149 µm per voxel, with slices ranging from several hundred to around two thousand, depending on specimen).

- Segmentation and metadata details:
  - Segmentation tasks include endocranial cast segmentation and, where applicable, flocculus cast removal.
  - Metadata provided for each specimen includes taxon, specimen accession, institution, scanner details, voxel/stack resolution, slice count, field of view, and the individuals responsible for segmentation/removal tasks.

- Scope:
  - The document covers a broad range of species, primarily avian and other vertebrates, across numerous NHMUK and NMS specimens, each with its own scan and segmentation record.