# Metadata for EIDC

- Global context: There is increasing concern about the decline of oak (Quercus petraea and Q. robur) health and the unknown biodiversity impacts of oak decline on associated species.
- Project aim: Compile and synthesise UK-specific data on species associated with oak trees to quantify associations, ecology, conservation status, and potential risks to oak ecosystems.

## Scope and dataset

- Taxa covered: Birds, bryophytes, fungi, invertebrates, lichens, and mammals (algae, bacteria, and other micro-organisms excluded).
- Species coverage: 2300 oak-associated species identified in the UK.
- Association levels with oak: obligate, high, partial, cosmopolitan, or uses.
- Comparative data: For each oak-associated species, data on use or non-use of 30 alternative tree species is captured.
- Conservation context: Conservation status across UK and international frameworks (IUCN, UK Red Data Book, Biodiversity Action Plans) and Birds of Conservation Concern are recorded; an “at risk to oak decline” index is calculated (RED to GREEN scale) based on association level and conservation status.

## Data collected and ecological detail

- Ecology data captured for each species:
  - How the species uses the tree (feeding directly/indirectly, living space, nesting, roosting)
  - Part of the tree used
  - Age of tree used
  - Woodland type
  - Tree form (coppice, pollard, natural growth)
  - Season of use
- Additional ecological data: Evidence on use of 30 alternative tree species, including whether the species uses the alternative tree, the degree of use (species vs. genus level), and frequency.
- Data quality and confidence: Data quality indicators reflect whether literature is peer-reviewed, whether data are UK-based, and the level of evidence underpinning association classifications.

## Data provenance and quality control

- Systematic literature review: Conducted in 2016/17 using published and grey literature plus unpublished information.
- Data structure standardisation: All data collected under a predefined common structure and stored in a relational database (OakEcol).
- Data sources and references: Full data sources are recorded; references are linked to each data entry.
- Confidence and data-type definitions: Separate definitions exist for association confidence and data types, with documented categories for each table.
- Data accessibility: OakEcol data are stored as separate CSV files per table; a diagram (Figure 1) describes relational links to enable reconstruction of the database from CSVs.

## OakEcol database: schema at a glance

- Central database: OakEcol (relational, CSV-based tables)
- Table overview (descriptions and purposes):
  - Species: Core list of oak-associated species with Latin/English names, association level, conservation status, native status, UK priority status, reference linkage, and related metadata.
  - Only_oak_tree_species: Subset of species that directly use oak (vs. broader woodland associations).
  - Age: Age of the oak tree used by species.
  - Alternative_Tree_names: Latin/English names for possible alternative tree species examined.
  - Alternative_Trees: Links between oak-associated species and their use of each alternative tree (association level, confidence, references).
  - Definitions_Age, Definitions_Alternative_Association, Definitions_Association, Definitions_Association_confidence, Definitions_Conservation_status, Definitions_Part, Definitions_Season, Definitions_Species_Group, Definitions_Use, Definitions_Woodland: Reference definitions and categorisations used across tables.
  - Ecology_notes: Notes on the ecology of each oak-associated species.
  - Invert_fungi: Data on fungal associations for invertebrates (fungivore status, fungus carried, notes).
  - Use: How the species uses the oak (feeding—direct, feeding—indirect, habitat—living space).
  - Woodland: Type of woodland where the species uses oak trees.
  - Season, Tree_form, Tree_part: Seasonal use, tree form used, and tree parts used by species.
  - References: Full bibliographic details for all sources.
- Table relationships: The database includes a diagram (Figure 1) showing relationships; Table 3 (Species) sits at the core and links to ecology, usage, age, and other attribute tables (Tables 4–25). Each table is saved as a separate CSV file.

## Data sources, definitions, and documentation

- Detailed methods by taxon group:
  - Birds: Primarily peer-reviewed literature plus unpublished habitat data.
  - Invertebrates: Key references include several avian and invertebrate checklists and habitat studies.
  - Bryophytes, Lichens, Fungi, Mammals: Sourced from specialist checklists, regional flora/fauna manuals, and curated databases; explicit criteria used to define association for each group.
- Documentation and definitions:
  - OakEcol_Definitions_Association.csv, OakEcol_Definitions_association_confidence.csv, OakEcol_Definitions_Conservation_status.csv, and related definition files describe categories and criteria used across tables.
  - References, age, use, woodland, season, tree_part, tree_form, and other tables include explicit column definitions and linkage rules to the Species table.

## Outputs and implications

- Purpose of the dataset: Quantify the breadth and strength of oak associations, map ecological uses, and assess risks to oak ecosystems by integrating association levels with conservation status.
- Risk indexing: The at-risk-to-oak-decline score integrates association strength with conservation threat to help prioritize management or further research.
- Practical end-products: A discoverable, well-documented dataset (OakEcol) intended to support conservation planning and ecological understanding of oak-dependent communities in the UK.

## Acknowledgments and funding

- Funded by Defra through the BBSRC PuRpOsE project (BB/N022831/1).
- Additional funding support from the Scottish Government's Rural and Environment Research and Analysis Directorate (2016–2021).

## References and further information

- Comprehensive reference list accompanying OakEcol, including sources for each taxon and methodological references (e.g., Mitchell et al. 2014; Mitchell et al. in press; various species checklists and conservation documents).
- Data availability note: The OakEcol database and its CSV table files are described with explicit data fields and metadata, enabling reconstruction and reuse by analysts.