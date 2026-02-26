# Metadata for EIDC

- Purpose and scope
  - Global concern about declining health of oak trees (Quercus petraea and Q. robur) and uncertain impact on associated biodiversity.
  - Assembles a UK-focused database (OakEcol) of species that use oak trees across six taxon groups: birds, bryophytes, fungi, invertebrates, lichens, and mammals.
  - Contains data on 2300 species with a defined level of association to oak (obligate to cosmopolitan) and detailed ecological use of the tree.
  - Includes data on use of oak by 30 alternative tree species for comparison, plus data on conservation status and risk to oak decline.

- What the data capture
  - For each species: level of association with oak, ecology of use (how the species uses the tree), parts of the tree used, age of tree, woodland type, tree form (coppice, pollard, natural), and season of use.
  - Data on whether each species also uses 30 alternative tree species; assessment of the strength of that association.
  - Conservation status indicators: UK/IUCN status, UK Red Data Book status, BAP/priority species designations, and Birds of Conservation Concern where applicable.
  - A composite “at risk to oak decline” index combining association with oak and conservation status (coded RED to GREEN).

- Experimental design, materials, and methods
  - Literature review conducted in 2016–2017, incorporating published and grey literature as well as unpublished information.
  - Focused on six taxon groups; excluded algae, bacteria, and other micro-organisms.
  - Data organized under a predefined structure in a relational database (OakEcol); six taxon-specific association criteria defined in OakEcol_Definitions_Association and related files.
  - Association levels defined per taxon using records count or literature-based judgments; data quality and provenance recorded (peer-reviewed status, UK relevance, etc.).
  - All sources and data quality controls documented (OakEcol_References.csv and related metadata files).

- Data structure and contents
  - OakEcol relational database, stored as CSV files in multiple interconnected tables.
  - Core tables and data relationships (illustrated in Figure 1) include:
    - Species: main species list with Latin/English names, association level, conservation status, native status, geography, and reference linkage.
    - Only_oak_tree_species: subset of species that specifically use oak trees.
    - Age, Use, Tree_part, Tree_form, Season, Woodland: ecological attributes describing how species interact with oak.
    - Ecology_notes: notes on species ecology.
    - Invert_fungi: fungal relationships for invertebrates (fungivore status, fungi carried, etc.).
    - Alternative_Trees and  Alternative_Tree_names: details on the 30 alternative tree species and each species’ association with them.
    - References: full bibliographic details for data sources.
    - Plus 13 definitions and status tables (Definitions_Age, Definitions_Association, Definitions_Conservation_status, Definitions_Part, Definitions_Season, Definitions_Species_Group, Definitions_Use, Definitions_Woodland, and related) that define categorisations used across the dataset.
  - 25 CSV table files in total, each described by the accompanying metadata documents (e.g., Table 3: Species, Table 4: Age, Table 5: Alternative_Trees, Table 6: Other, etc.).
  - Data columns and relationships are designed to allow reconstruction of the OakEcol database from CSVs (as summarized in Table 2 and Figure 1).

- Data quality, provenance, and access
  - Data quality captured via association confidence definitions and data-type provenance (UK vs non-UK, peer-reviewed vs other).
  - All data sources for assessments are recorded (OakEcol_References.csv).
  - Acknowledges funding and programmatic support; data hosted under the OakEcol schema for reuse and re-analysis.

- Acknowledgments and funding
  - Funded by Defra through the BBSRC PuRpOsE project (Protecting Oak Ecosystems; BB/N022831/1).
  - Additional funding for RJM from the Scottish Government’s Rural and Environment Research and Analysis Directorate (2016–2021).

- How this resource supports data use
  - Enables users to explore oak-associated biodiversity and potential risks to oak ecosystems.
  - Facilitates self-service analysis through a structured data model (oak associations, ecological uses, and conservation concerns) and clear definitions.
  - Provides a platform for comparing oak-associated species with a broad set of alternative tree species, informing conservation and management decisions.

- References and related work
  - Includes comprehensive references across birds, bryophytes, invertebrates, fungi, lichens, and mammals, with cross-links to the OakEcol database structure.
  - Related foundational work cited for methodology and conservation context (e.g., Mitchell et al. 2014; Mitchell et al. in press; UK conservation status documents).

- Endnotes and data access pointers
  - The OakEcol database is documented through a set of CSV files, with detailed table descriptions and column headings provided in the accompanying metadata.
  - Users can reconstruct the relational model from the CSVs using the table relationships described (Table 2 and Figure 1).