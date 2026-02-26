# Scan and Segmentation Details

- Overview
  - A comprehensive listing of CT scan and segmentation details for a large set of avian specimens housed primarily at NHMUK (The Natural History Museum, UK) and NMS (National Museums Scotland), among others.
  - Scans were down-sampled from 16-bit depth to 8-bit, cropped to regions of interest, and voxel sizes reduced where necessary to manage large file sizes.
  - Endocranial casts and flocculus removals are repeatedly referenced as the primary segmentation tasks, performed by Stig Walsh (and collaborators) across many specimens.
  - Original data produced as 16-bit VGStudio Max VOL files, then output to 8-bit BMP stacks or 8-bit MCS stacks; some datasets remained as 16-bit DCM stacks before down-sampling.
  - Institutions noted with abbreviations NHMUK, NMS; specimen entries span multiple taxa and catalog numbers.

- Data Generation and Processing per specimen
  - For each specimen: species name, catalog/inventory numbers, and institution (e.g., NHMUK S/1966.51.209; NMS Z.2000.08.105; NHMUK S/2007.139.12, etc.).
  - Scanning details:
    - Instrument: Nikon Metrology HMX ST CT.
    - Scanned along the axial axis as part of various grants (e.g., NERC Small Grant NE/H012176/1; NE/E008380/1) and fellowships (e.g., Intra-European Marie Curie Fellowship 255039).
    - Original reconstruction: 16-bit VGStudio Max VOL file; output as 8-bit BMP stack; some datasets converted to 8-bit MCS or 16-bit DCM stacks before downsampling.
  - Processing parameters:
    - Final image stack resolutions ranging from 10 µm to 88 µm, with typical fields of view in the 13–71 mm range.
    - Final slices per specimen commonly in the few hundred to ~1,100 range.
    - Field of view and grid dimensions provided per specimen (e.g., 1506 x 1211 grid at 10 µm; 764 x 940 grid at 30 µm; others similar).
  - Segmentation and post-processing:
    - Endocranial cast segmentation performed; flocculus cast removal performed by Stig Walsh (and others).
    - Recurrent notations of “Endocranial cast segmention” and “flocculus cast removal” across entries.
  - Output formats:
    - 8-bit BMP stacks; 8-bit MCS stacks; some datasets originally as 16-bit DCM stacks and later downsampled.
    - Emphasis on making data more manageable for analysis while preserving provenance.

- Data Structure, Metadata, and Provenance
  - Each entry documents:
    - Species, specimen/catalog number, and current collection (institutional abbreviation).
    - Scanner type, axis of scanning, grant or fellowship context.
    - Original and final data formats (VOL -> BMP/MCS; some DCM stacks).
    - Resolution, slice count, grid dimensions, and field of view (per specimen).
    - Segmentation details (endocranial cast, flocculus removal) and responsible personnel.
  - Provenance notes emphasize consistent attribution to researchers (e.g., Stig Walsh; Monja Knoll; Estelle Bourdon) and collaborating institutions.
  - Data lineage is explicit: 16-bit VGStudio Max origins, conversion to 8-bit formats, and associated metadata about voxel size and ROI cropping.

- Data Accessibility and Reuse Considerations
  - Data is described in detail for reproducibility and potential reuse in comparative anatomy, imaging workflows, and data-system planning.
  - Formats chosen (BMP, MCS, DCM) reflect a balance between accessibility and file size, highlighting a common challenge for data leaders: maintaining discoverability and interoperability across formats.
  - The document documents extensive collaboration across institutions and funding sources, illustrating cross-organizational data stewardship and governance implications.

- Relevance to Data Leaders (Aims and Challenges)
  - Supports thinking about a whole data system by documenting acquisition, processing, and segmentation workflows across many specimens.
  - Demonstrates the importance of metadata completeness (instrument, axis, resolution, slices, field of view, formats, segmentation actions) for discoverability and reusability.
  - Highlights data quality and standardization considerations (consistent segmentation terms, uniform down-sampling, and ROI cropping) across a heterogeneous collection.
  - Reflects collaboration and provenance as foundational to trust and future integration within a broader data ecosystem.
  - Illustrates a practical pathway to improve data assets: adopt standardized metadata schemas, maintain clear data lineage, and define preferred formats to balance reuse and storage efficiency.

- Key Takeaways for Actionable Data Leadership
  - Establish a standardized metadata schema capturing specimen identifiers, institution, scanner details, acquisition parameters, processing steps, segmentation actions, and data formats.
  - Preserve full provenance: retain original 16-bit VOL files and document every transformation, including down-sampling and format conversion.
  - Create a centralized repository or catalog that links each specimen’s raw data, processed stacks, and segmentation outputs with clear, searchable metadata.
  - Harmonize data formats and provide conversion pipelines to common, widely supported formats to enhance discoverability and long-term accessibility.
  - Document roles, contributors, and funding sources to support traceability and credit in collaborative projects.