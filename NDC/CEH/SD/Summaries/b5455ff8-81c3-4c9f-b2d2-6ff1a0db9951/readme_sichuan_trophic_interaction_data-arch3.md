# ReadMe_ Sichuan_trophic_interaction_data.doc

## Overview
- This dataset contains quantitative survey records related to tritrophic interactions among Fagaceae trees, Cynipid gallwasps, and their parasitoids from Sichuan, China.
- It supports analyses presented in Fang et al. (2024) and is freely accessible online.
- Sampling covers two sites (Emeishan and Mianning) from November 2017 to June 2022; full sampling details are in Fang et al. 2024.

## Study design and taxa
- Three trophic levels:
  - Higher level: Linnean tree species from Fagaceae
  - Mid level: morphospecies of herbivorous Cynipid gallwasps
  - Lower level: morphospecies of parasitoids reared from Cynipid galls
- Data collected as counts of interactions between trophic levels.
- Data files are organized by site and combined (AllAreas).

## Data structure and content
- Pairwise matrices of counts:
  - Gall morphotypes (rows) vs. parasitoid morphospecies (columns)
  - Tree species (rows) vs. gall morphotypes (columns)
  - Tree species (rows) vs. parasitoid morphospecies (columns)
- Files (9 total):
  - galltypes_by_parasitoid_morphospecies_AllAreas.csv
  - galltypes_by_parasitoid_morphospecies_Emeishan.csv
  - galltypes_by_parasitoid_morphospecies_Mianning.csv
  - trees_by_galltype_AllAreas.csv
  - trees_by_galltype_Emeishan.csv
  - trees_by_galltype_Mianning.csv
  - trees_by_parasitoid_morphotype_AllAreas.csv
  - trees_by_parasitoid_morphotype_Emeishan.csv
  - trees_by_parasitoid_morphotype_Mianning.csv
- Taxa definitions and exact mappings are detailed in Fang et al. (2024).

## Data quality and validation
- Standardised data collection protocols followed (described in Fang et al. 2024).
- Fieldwork conducted by a single team; identifications validated by the team.
- Parasitoid identifications validated by an external expert from the Natural History Museum, London.
- Gall morphotypes validated using DNA barcoding.
- Data checked for errors and quality assured prior to release.

## Metadata, accessibility, and governance
- Detailed methodology, site-specific sampling, and taxonomy are described in Fang et al. (2024).
- Data are intended to support transparent sharing, replication, and integration with monitoring frameworks.
- The dataset emphasizes openness, data provenance, and the need for clear metadata to enable re-use and verification.

## Relevance for monitoring frameworks
- Provides a concrete example of a structured, multi-trophic monitoring dataset across multiple sites.
- Demonstrates how to:
  - organize data into site-specific and aggregated matrices
  - validate taxonomic identifications and interactions
  - maintain data quality through standardized protocols and external validation
  - share underlying data to support network analyses and policy evaluation
- Supports development of indicators based on network structure and taxonomic composition of complex ecological communities.

## Reference
- Fang, Z.; Tang, C.-T.; Sinclair, F.; Csóka, G.; Hearn, J.; McCormack, K.; Melika, G.; Mikolajczak, K.M.; Nicholls, J.A.; Nieves-Aldrey, J.-L.; Notton, D.G.; Radosevic, S.; Bailey, R.I.; Reiss, A.; Zhang, Y.M.; Zhu, Y.; Fang, S.; Schönrogge, K.; Stone, G.N. (2023). Network structure and taxonomic composition of tritrophic communities of Fagaceae, cynipid gallwasps and parasitoids in Sichuan, China. Insect Conservation and Diversity, 2024;1-26. DOI: 10.1111/icad.12768