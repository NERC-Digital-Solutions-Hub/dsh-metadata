# Scan and Segmentation Details

- Purpose and scope
  - Documentation of CT-scanned cranial specimens across a wide range of bird species (and a few other taxa) from NHMUK (The Natural History Museum) and NMS (National Museums Scotland).
  - Emphasis on creating endocasts and performing flocculus cast removal as part of neuroanatomical studies.
  - Scans were down-sampled and cropped to manage processing requirements; voxel size reductions applied where stacks remained large.

- Data processing workflow
  - Original data: 16-bit VGStudio Max volumes reconstructed and output as 8-bit stacks (BMP, MCS) or DCM stacks for various specimens.
  - Down-sampling: 16-bit → 8-bit; cropping to region of interest; voxel size reductions to ease manipulation.
  - Scanning axis: All specimens scanned along the axial axis using Nikon Metrology HMX ST CT.
  - Endocranial segmentation: Performed by Stig Walsh (primarily).
  - Flocculus cast removal: Performed by Stig Walsh (with some instances by Monja Knoll); some entries note endocast segmentation separately.
  - File formats for final data: BMP stacks, MCS, and DCM stacks; VGStudio Max VOL files referenced in provenance.

- Technical details and ranges
  - Final image stack resolutions commonly range from about 12 µm to 149 µm per voxel, varying by specimen.
  - Number of slices per specimen typically ranges from roughly 424 to nearly 2,000 slices.
  - Field of view (FOV) generally between ~14 mm and ~82 mm.
  - Original resolutions often around 10–150 µm, with final processing reducing detail to accommodate data handling.
  - Common final stack formats encountered: BMP (8-bit), MCS, and DCM stacks.

- Specimen and dataset characteristics
  - Taxa: Broad sampling of avian species (e.g., Acanthorhynchus superciliosus, Alca torda, Amazona aestiva, Falco spp., Gallus gallus, Struthio camelus, etc.) and several non-bird taxa (e.g., Casuarius casuarius, Dromaius novaehollandiae, Rheas, etc.).
  - Institutions: The Natural History Museum (NHMUK) and National Museums Scotland (NMS) are the primary scanning sites.
  - Cataloging: Specimens identified by diverse catalog numbers; some entries marked as unregistered or with non-standard identifiers.
  - Personnel and provenance: Scans conducted and curated by Stig Walsh and collaborators (e.g., Estelle Bourdon, Richard Abel); segmentation and flocculus work primarily by Walsh; some segmentation credited to Monja Knoll.
  - Funding and projects: NE/H012176/1 (NERC Small Grant) and NE/E008380/1 (NERC Small Grant) acknowledged; some scans linked to Intra-European Marie Curie Fellowship programs (255039).

- Data provenance and metadata
  - Documentation tracks original VGStudio Max 16-bit VOL files, subsequent 8-bit conversions, cropping, and down-sampling steps.
  - Metadata notes per specimen include original resolution, final stack resolution, slice count, field of view, and processing actions (endocranial segmentation, flocculus removal).
  - Abbreviations used: NHMUK (The Natural History Museum, UK) and NMS (National Museums Scotland).

- Practical implications for analysis
  - Numerous specimens provide a large, multi-specimen dataset suitable for comparative neuroanatomy or endocranial studies.
  - Data consistency considerations: varying final voxel sizes, formats, and slice counts across specimens; ensure uniform voxel calibration when comparing measurements.
  - Reproducibility: segmentation and flocculus removal largely tied to specific researchers (Stig Walsh); detailed methodology per specimen is documented but may require replication settings for exact reproducibility.
  - Accessibility: final formats include BMP/MCS/DCM stacks; provenance references to VGStudio Max files indicate upstream data may be stored in original project formats; portal-based discoverability is not specified in this document.