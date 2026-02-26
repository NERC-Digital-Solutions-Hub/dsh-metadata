# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Fine Grain (VF)

- Overview
  - Fine-grained vegetation dataset across 12 UK sites designed for map-based GIS analysis and change monitoring.
  - High-resolution sampling: 10m x 10m plots with species presence recorded in 40cm x 40cm cells within plots.
  - Cadence: every three years, with some sites collecting annual sub-samples to extend the temporal range.

- Data structure and storage
  - Data stored in site-specific Oracle tables with core metadata, enabling integrated GIS workflows:
    - D1VF_xxx: Plot-level data
    - D2VF_xxx: Environmental data
    - D3VF_xxx: Cell-level features
  - Metadata references (e.g., M_DESC, M_REFFIELD) guide data lineage and interpretation.

- Coding systems and vocabulary
  - Rich, cross-referenced vocabularies to support GIS joins and semantic queries:
    - Land Use (Hodgson codes 1–22), terrain-related codes (SLOPE, SLOPEFORM, NVCCLASS), and various feature indicators (Path, Wall, Stream, Hedge, etc.).
    - Extensive species codes with mappings among Latin names, common names, and cross-references to multiple taxonomic concepts.
  - The provided mappings allow robust attribute joins and reconciliation of synonyms in spatial analyses.

- Data quality, standards, and integration
  - Quality information is essential due to variability in timing and resolution across sites.
  - Data standards are not uniform; cleaning and transformation are typically required to produce consistent GIS layers.
  - Integration requires careful joining on SITECODE, SYEAR, PLOTPID, and CELLID, with accompanying quality metadata.

- Access, use, and citation
  - Protocols and coordination information are available on the ECN site; contact ecn@ceh.ac.uk.
  - ECN requests acknowledgement in publications and, when possible, the reprint of cited work.

- GIS-ready guidance
  - Spatial design: use 10m x 10m footprints as the primary unit; derive species presence within 40cm cells.
  - Data preparation: extract and join D1VF_xxx, D2VF_xxx, and D3VF_xxx by SITECODE, SYEAR, PLOTPID, and CELLID; align temporal ranges across sites.
  - Output: create map-ready layers for plots, cell-level species presence, and environmental covariates; develop legends around Hodgs codes, NVCCLASS, and key species groups.
  - Documentation: maintain metadata lineage linking to protocol documentation and site-specific code mappings.

- Appendix: Key vocabulary notes (from the provided text)
  - Species coding: contains numerous mappings between different scientific and common names (e.g., Salix aurita and related taxa) to standardized codes, enabling consistent GIS attribution despite taxonomic synonyms.
  - Quality codes: ECN quality codes (100–999) describe data collection issues; 999 denotes an unusual event with accompanying text in the quality metadata.

- Practical takeaway for GIS work
  - Plan for data harmonization due to site-specific differences.
  - Leverage the extensive vocabularies to ensure consistent attribute joins and semantic queries.
  - Always incorporate accompanying quality metadata when mapping and interpreting results.