# ReadMe_ Sichuan_trophic_interaction_data.doc

## Overview
- Dataset linked to analyses in Fang et al. (2024), available freely online.
- Contains quantitative survey records across three trophic levels: Fagaceae tree species, morphospecies of Cynipid gallwasps, and morphospecies of parasitoids reared from galls.
- Collected from two sites in Sichuan Province, China (Emeishan and Mianning) between November 2017 and June 2022.
- Detailed sampling methods and taxonomy are described in Fang et al. (2024).

## Data Collection and Provenance
- Field work conducted by a single team; identifications validated by the same team.
- Parasitoid identifications validated by an external expert from the Natural History Museum, London.
- Gall morphotype identifications validated using DNA barcoding.
- Data collection followed standardized protocols as described in Fang et al. (2024).
- Taxa definitions for all three trophic levels are provided in Fang et al. (2024).

## Data Quality and Validation
- Consistent field methodology and validation across all samples.
- Quality checks performed to minimize errors in counts and identifications.
- External validation for parasitoids enhances reliability of the third trophic level data.

## Data Structure and Content
- Data are pairwise matrices of counts showing interactions between trophic levels.
- Datasets are organized by site and also include a combined AllAreas file.
- Files included:
  - galltypes_by_parasitoid_morphospecies_AllAreas.csv (gall morphotypes by parasitoid morphospecies, All Areas)
  - galltypes_by_parasitoid_morphospecies_Emeishan.csv (Emeishan site)
  - galltypes_by_parasitoid_morphospecies_Mianning.csv (Mianning site)
  - trees_by_galltype_AllAreas.csv (tree species by gall morphotypes, All Areas)
  - trees_by_galltype_Emeishan.csv (Emeishan site)
  - trees_by_galltype_Mianning.csv (Mianning site)
  - trees_by_parasitoid_morphotype_AllAreas.csv (tree species by parasitoid morphospecies, All Areas)
  - trees_by_parasitoid_morphotype_Emeishan.csv (Emeishan site)
  - trees_by_parasitoid_morphotype_Mianning.csv (Mianning site)
- File contents: counts of recorded interactions with rows representing higher-trophic-level taxa and columns representing lower-trophic-level taxa.
- Taxa definitions and the scope of taxa are described in Fang et al. (2024).

## Metadata, Taxonomy, and Provenance
- Taxa definitions for all three trophic levels defined in Fang et al. (2024).
- Gall morphotype identifications validated with DNA barcoding.
- Parasitoid identifications validated by an external taxonomic expert.

## Access, Usage, and Reference
- Data are freely accessible online.
- Primary reference for the data and its interpretation:
  - Fang, Z.; Tang, C.-T.; Sinclair, F.; Csóka, G.; Hearn, J.; McCormack, K.; Melika, G.; Mikolajczak, K.M.; Nicholls, J.A.; Nieves-Aldrey, J.-L.; Notton, D.G.; Radosevic, S.; Bailey, R.I.; Reiss, A.; Zhang, Y.M.; Zhu, Y.; Fang, S.; Schönrogge, K.; Stone, G.N. (2023). Network structure and taxonomic composition of tritrophic communities of Fagaceae, cynipid gallwasps and parasitoids in Sichuan, China. Insect Conservation and Diversity, 2024;1-26. DOI: 10.1111/icad.12768

## Relevance for Data Leaders
- Demonstrates end-to-end data governance: standardized collection, multi-level validation, and cross-site data integration.
- Illustrates management of complex, multi-trophic networks with clearly defined metadata, taxonomic references, and data provenance.
- Provides a model for organizing large-scale ecological interaction data into site-specific and aggregated matrices for analysis and dissemination.