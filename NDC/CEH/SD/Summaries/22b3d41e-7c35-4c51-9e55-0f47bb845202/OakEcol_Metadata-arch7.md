# Metadata for EIDC

- Global context and purpose
  - Addresses decline in oak health and unknown impacts on associated biodiversity.
  - Compiles a UK-wide database (OakEcol) of all known oak-associated species across six taxa to support understanding and visualization of spatial relationships with oak ecosystems.

- Scope and contents
  - Taxa covered: birds, bryophytes, fungi, invertebrates, lichens, and mammals.
  - Approximately 2300 species included, each with:
    - Level of association with oak (obligate to cosmopolitan or uses).
    - Ecology and use of the tree (part used, feeding/roosting/breeding, age of tree, woodland type, tree form, season of use).
    - Use or potential use of 30 alternative tree species.
    - Data quality, provenance, and confidence indicators.
    - Conservation status (IUCN, UK Red Data Book, national/BAP/priority lists, Birds of Conservation Concern).

- Experimental design and methodology
  - Literature review conducted in 2016/17 (published and grey literature, plus unpublished sources).
  - Focus on six taxon groups; excluded algae/bacteria/micro-organisms.
  - Pre-defined data structure; relational database (OakEcol) with data quality controls.
  - Association categories defined per taxon (e.g., based on records on Quercus petraea/robur vs. other trees) and documented in metadata files.
  - Consolidation of conservation status and risk to oak decline into an at-risk index.

- Data architecture and content
  - OakEcol relational database stored as separate CSV tables.
  - Core tables and data files (examples):
    - Table 3: Species – main species data, Latin/English names, association level, conservation status, native status, and references.
    - Tables for ecological details: Woodland, Use, Age, Tree_part, Tree_form, Season, and Ecology_Notes.
    - Table 18: Invert_Fungi – whether invertebrates eat or carry fungi.
    - Table 19: Only_Woodland – species associated with oak woodlands but not directly using the oak.
    - Table 20: References – full details for all sources.
    - Tables 4–25: Detailed data structures (Age, Alternative_Trees, Definitions for ages, associations, confidence, conservation, parts, seasons, woodland types, etc.).
  - Table 1 describes methods to assess association by taxon; Table 2 lists all OakEcol tables and their relationships.
  - Figure 1 (not reproduced here) shows the relational diagram linking tables; Table 3–25 describe column headings and metadata.

- Data quality, confidence, and provenance
  - Association levels: obligate, high, partial, cosmopolitan, uses.
  - Confidence indicators detail whether data are peer-reviewed, quality-controlled, and UK vs non-UK sources.
  - All data sources and references are recorded (References table).

- Potential GIS applications
  - Enables map-based visualization of oak-associated biodiversity across the UK.
  - Supports analyses by tree age, form, woodland type, season of use, and relationship to alternative tree species.
  - Provides a structured, exportable dataset suitable for spatial mapping and risk assessment (e.g., at_risk_to_oak_decline index).

- Access and contact
  - Authors and affiliations: The James Hutton Institute et al.
  - Contact: ruth.mitchell@hutton.ac.uk
  - Funding and acknowledgments: Defra/ BBSRC PuRpOsE; Scottish Government STRATEgic programme.
  - References include key literature and the Mitchell et al. (2014) framework for assessing risk to oak ecosystems.