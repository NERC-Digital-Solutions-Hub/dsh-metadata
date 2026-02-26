# Metadata for EIDC

## Overview
- Global concern about oak health and unknown impacts on associated biodiversity; this work assembles a UK-focused database of oak-associated species (Quercus petraea and Q. robur).
- Contains 2300 species across six taxon groups: birds, bryophytes, fungi, invertebrates, lichens, and mammals.
- For each species, records level of association with oak (obligate to cosmopolitan) and ecological details such as part of tree used, how it uses the tree (feeding, roosting, breeding), tree age, woodland type, tree form, and season.
- Also captures use or presence on 30 other tree species and provides an overall "at risk to oak decline" categorization.

## Data Architecture and Model
- Relational database named OakEcol; data stored as separate CSV files with defined table relationships.
- Core data structure is delivered through 25 interlinked tables (e.g., Species, Woodland, Use, Age, Tree_part, Tree_form, Season, References, Ecology_notes, Alternative_Trees, Invert_Fungi, etc.).
- Figure 1 illustrates the relational layout; Table 3 describes the primary Species table and its links to other tables.
- Designed so the entire dataset can be rebuilt from the CSV files (Tables 1 and 2 describe data sources and table descriptions).

## Data Content and Definitions
- Species-level data include: Latin and English names, conservation status (UK-specific, IUCN, Red Data Book, BAP, Birds of Conservation Concern), native/introduced status, and an explicit level of association with oak.
- Association levels defined per taxon with standardized categories (e.g., obligate, high, partial, cosmopolitan; and “uses” for ambiguous cases); association confidence indicates data type (peer-reviewed, UK vs non-UK, etc.).
- Ecology fields per species cover:
  - Use of the tree (feeding directly, feeding indirectly, living space, nesting, roosting)
  - Part of the tree used
  - Age of tree used
  - Tree form (natural growth, coppice, pollard)
  - Woodland type used
  - Season of oak usage
- Consolidated conservation risk: combines association level with conservation status to produce an “at risk to oak decline” index (RED to GREEN).
- 30 alternative tree species: data determine whether each oak-associated species uses these other trees, including whether use is of the genus or species, regular vs. rare usage, and data confidence.
- Data quality and provenance definitions are captured in dedicated definitional tables (e.g., Definitions_Association, Definitions_Conservation_status, Definitions_Age, Definitions_Woodland, etc.).

## Provenance, Sources, and Quality
- Data curated from a 2016/17 literature review of published, grey, and unpublished sources; six taxon groups; restricted to oak associations (no algae, bacteria, or other microorganisms in scope for fungi assessments).
- Taxon-specific primary data sources:
  - Birds: online peer-reviewed literature plus unpublished reviews
  - Bryophytes: British Bryological Society records and key literature
  - Fungi: FRDBI-based assessments with strict criteria for obligate/high associations
  - Invertebrates: multiple key references (e.g., Alexander 2002; Emmet 1992; Stork & Hammond 2013; etc.)
  - Mammals:British Mammals handbook and targeted literature
  - Lichens: British Lichen Society records and related literature
- All data sources, along with bibliographic details, are stored in the References table.
- Data sources and quality controls are documented across the OakEcol_Definitions and related metadata files.

## Access, Governance, and Reuse
- OakEcol dataset provided as CSV files, with explicit guidance on rebuilding the relational structure (via Table 1 and Table 2 references) and the Figure 1 schema.
- Primary publication: Mitchell et al. (in press); accompanying acknowledgments note Defra funding under PuRpOsE and Scottish Government support.
- Contact for data and metadata: ruth.mitchell@hutton.ac.uk
- Designed to support data-driven decisions, co-ownership of data products, and broader ecosystem and conservation planning around oak decline and associated biodiversity.

## Practical Implications for Data Leaders
- Enables a system-wide view of oak-associated biodiversity and risk assessment (via the at-risk-to-oak-decline index).
- Provides a richly documented data asset with clear metadata, data provenance, and quality levels to inform governance, stewardship, and policy discussions.
- Supports transparency and discoverability through standardized definitions, explicit associations, and linked ecology data, facilitating cross-institution collaboration and data-sharing across networks.

## Limitations and Notes
- UK-focused dataset reliant on historical literature and available records; some associations involve subjective or literature-based judgments.
- Data quality depends on source reliability and the predefined association definitions; ongoing updates may be needed as new evidence emerges.