# UK Environmental Change Network (http://www.ecn.ac.uk) Vegetation: Fine Grain (VF)

- Overview
  - Long-running ECN dataset focusing on fine-grained vegetation data across multiple UK sites.
  - Aims to monitor environmental change using standardized, comparable outputs for environmental health and policy assessment over time.
  - Outputs include presence/absence data, plots, maps, and charts; designed for broad monitoring use.

- Data provenance and access
  - Originator: ECN Data Centre, Centre for Ecology and Hydrology.
  - Owners: UK government departments and agencies funding monitoring and network coordination.
  - Citation/acknowledgement: ECN requests acknowledgment of data use and submission of one reprint for any publication citing the data.

- Protocol and sampling cadence
  - Plot design: at least two randomly selected 10m x 10m plots per site within each NVC type; species presence recorded in 40cm x 40cm cells.
  - Temporal cadence: surveys every three years; some sites conduct annual surveys on a subset of plots for finer temporal resolution.
  - Data quality: accompany outputs with quality information; verification and QA are performed prior to outputs.

- Data structure and schema
  - Storage and schema: core data stored in Oracle in site-specific tables organized as D1VF_xxx, D2VF_xxx, D3VF_xxx (xxx = site code).
  - Core data examples:
    - D1VF_xxx: plot-level vegetation data (SITECODE, SYEAR, PLOTPID, CELLID, FIELDNAME, VALUE).
    - D2VF_xxx: site/plot environmental descriptors (PEDATE, LANDUSE, SLOPE, ASPECT, SLOPEFORM, NVCCLASS).
    - D3VF_xxx: cell-level features (SITECODE, SYEAR, PLOTPID, CELLID, FEATURE).
  - Metadata: core metadata tables and documentation provide definitions; data are verified, quality assured, cleaned, and transformed for standardized outputs.

- Site codes and landscape context data
  - 12 UK sites (e.g., T01 Drayton, T02 Glensaugh, T03 Hillsborough, …, T12 Cairngorms) with documented coordinates and survey periods (e.g., 1994–2012, 1996–2012, etc.).
  - Landscape descriptors:
    - Land Use (Hodgson codes 1–22; e.g., Ley grassland, permanent grassland, cereals, woodland types, heath/moor, etc.).
    - Slope Form (Hodgson codes 1–3: convex, straight, concave).
    - Features (codes for paths, walls, streams, hedges, ditches, fences, banks, boundaries, etc.).
    - NVCCLASS: National Vegetation Classification class per site.

- Landscape and site context data
  - Site-level descriptors accompany vegetation data to enable contextual analyses and cross-site comparisons.
  - Large, cross-referenced species dictionary supports linking codes to Latin/common names and taxonomic databases.

- Species and taxonomy coding
  - Extensive species coding system linking numeric codes to:
    - Latin names, common names, and database identifiers (e.g., BRC concepts) to enable longitudinal analyses and integration with other datasets.
  - Examples include numerous Salix species and related taxa, with many cross-references to synonyms and taxonomic concepts to support consistent identification across time.

- Data usage, quality, and storage
  - Data handling: verified, quality assured, cleaned, and transformed to standardized outputs.
  - Outputs: reports, maps, and charts suitable for monitoring environmental health and policy performance.
  - Storage and accessibility: datasets stored and uploaded to appropriate portals to facilitate reuse.

- Quality assurance and quality codes
  - ECN quality codes: standard list assigned by site managers to indicate factors affecting data quality.
  - Codes cover a wide range of issues (e.g., missing information, sampling or equipment problems, sample contamination, environmental interferences, etc.).
  - 999: unusual event requiring accompanying text for context.
  - A comprehensive set of quality codes is provided and accompanying quality text explains non-standard circumstances.

- Key considerations for Analysts Monitoring the Environment
  - Consistency: standardized data collection and schema enable cross-site, multi-year comparisons.
  - Reuse and integration: aim to increase dataset value by combining vegetation data with environmental descriptors and other datasets; maintain provenance and rich metadata.
  - Accessibility: facilitate access to underlying data used to generate outputs.
  - Policy relevance: outputs designed to inform environmental change indicators and policy performance over time.