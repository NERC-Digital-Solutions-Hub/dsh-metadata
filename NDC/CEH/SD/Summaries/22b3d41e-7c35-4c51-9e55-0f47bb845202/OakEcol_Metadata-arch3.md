# Metadata for EIDC

## Overview
- Global concern over oak decline (Quercus petraea and Q. robur) and unknown impacts on associated biodiversity.
- A UK-focused database (OakEcol) collates oak-associated species across six taxon groups to understand dependence on oak and inform conservation and management.
- Dataset supports monitoring of oak ecosystem health and informs policy decisions.

## Scope and Taxa
- Taxon groups included: birds, bryophytes, invertebrates, fungi, lichens, and mammals.
- Data cover species that use oak trees and, for some records, species that use oak woodland habitat but not the tree itself.
- Final database lists 2300 species with an explicit level of association to oak (obligate, high, partial, cosmopolitan, uses).

## Data Collected
- For each oak-associated species: level of association with oak, and ecology of use (how species use the tree and in which part of the tree).
- Tree-related ecology fields include:
  - Part of tree used
  - Type of use (feeding, roosting, nesting, living space, etc.)
  - Age of tree used
  - Tree form (pollard, coppice, natural growth)
  - Woodland type used
- Data also include use or association with 30 alternative tree species for comparative context.
- Conservation status integrated (UK/Global): IUCN status, UK Red Data Book, Biodiversity Action Plans, Birds of Conservation Concern, and country-specific priority species lists.
- An “at risk to oak decline” index is derived by combining association level with conservation status (RED to GREEN).

## Methods and Data Collection
- Literature review conducted in 2016/17, drawing from published and grey literature and unpublished information.
- Six taxon groups defined; excluded algae, bacteria, and other micro-organisms.
- Pre-defined data structure used; all data entered into a relational database (OakEcol).
- Association levels defined per taxon with specific criteria (e.g., proportion of records on oak vs. other trees; for some groups, more subjective assessments based on literature).
- Data quality assessments captured via association confidence and data type indicators, plus whether data are UK-based or international.

## Data Organization and Database Structure
- OakEcol is a relational database stored as CSV files in multiple tables.
- Figure 1 (in the document) describes relationships and rebuild workflow for OakEcol from CSVs.
- Core tables and themes:
  - Species: main list of oak-associated species, Latin/English names, conservation status, native status, UK priority status, and association level.
  - Use, Age, Tree_part, Tree_form, Season, Woodland: ecological context fields linked to Species.
  - Alternative_Trees and Related tables: assessment of 30 alternative tree species and their association with oak-associated species.
  - References: full details for all data sources.
  - Additional tables: Ecology_notes, Invert_fungi, Only_Woodland, and metadata definitions (e.g., Definitions_Age, Definitions_Association, Definitions_Woodland, etc.).
- Data model comprehensively documented with cross-references between tables (e.g., Species_Latin links to many tables; table-specific definitions and confidence levels provided).

## Key Variables and How They Are Used
- Level_of_association: obligate, high, partial, cosmopolitan, uses (defined per taxon).
- Conservation_status: UK/BAP status, Red Data Book categories, IUCN category; used to derive “at risk to oak decline” codes (RED to GREEN).
- Ecology fields: how/where species use oak (feeding, roosting, nesting, living space), part of tree used, age of tree, tree form, and woodland type.
- Data quality indicators: association_confidence, data_type (UK vs non-UK, peer-reviewed vs other), and metadata quality notes.
- References: every assessment is traceable to a reference, enabling auditability and data governance.

## Data Sources and References
- Data sources span peer-reviewed literature, sectoral reports, checklists, and species-specific databases (with explicit citations per taxon).
- Tables detail the sources used for each taxon (birds, bryophytes, invertebrates, fungi, lichens, mammals) and how association levels were determined.
- Comprehensive reference table lists authors, year, publication type, titles, DOIs, and other bibliographic details.

## Access, Sharing, and Data Governance
- Data governance implied by the need to record confidence, data type, and reference provenance; underlying data and metadata are intended to be transparent and shareable.
- The dataset is designed to support transparency and reproducibility, with explicit metadata files (e.g., OakEcol_Definitions_*, References).

## Funding and Acknowledgments
- Funded by Defra through the BBSRC PuRpOsE grant (BB/N022831/1).
- Additional support from the Scottish Government’s Rural and Environment Research and Analysis Directorate (2016-2021).
- Acknowledges a broad range of data sources and contributors.

## Relevance for Monitoring Frameworks
- Provides a structured, auditable dataset to monitor oak ecosystem health and associated biodiversity.
- Facilitates evidence-based policy decisions by linking species associations with oak to conservation status and habitat use.
- Addresses common monitoring challenges: data gaps, data access, data quality, metadata completeness, and governance through a well-documented, centralized data model.