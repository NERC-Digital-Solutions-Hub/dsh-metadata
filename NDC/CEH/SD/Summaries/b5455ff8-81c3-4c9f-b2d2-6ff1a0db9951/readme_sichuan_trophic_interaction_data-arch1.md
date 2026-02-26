# ReadMe_ Sichuan_trophic_interaction_data.doc

- The dataset documents quantitative surveys of three trophic levels in Sichuan, China: Fagaceae tree species, morphospecies of herbivorous Cynipid gallwasps, and morphospecies of Hymenopteran parasitoids reared from the galls.
- Collected from two sites (Emeishan and Mianning) between November 2017 and June 2022; methods and taxonomy detailed in Fang et al. 2024.
- Aimed at enabling analyses of network structure and taxonomic composition of tritrophic communities.

## Purpose and scope

- Provide pairwise interaction counts across trophic levels to support network analyses and predictive modeling of tri-trophic interactions.
- Datasets define taxa as in Fang et al. 2024; suitable for examining correlations, patterns, and potential predictions about network structure and dynamics.

## Data collected and quality control

- Sampling followed standardized protocols; all field work conducted by a single field team.
- Taxonomic identifications of trees, gall morphotypes, and parasitoids validated by the field team; parasitoid identifications further validated by an external expert from the Natural History Museum in London.
- Gall morphotypes validated using DNA barcoding (as described in Fang et al. 2024).
- Datasets are carefully checked for errors and are represented as counts of interactions between trophic levels.

## Data structure and files

- Data are stored as pairwise matrices of counts, linking higher trophic levels to lower ones. Taxa definitions follow Fang et al. 2024.
- File groupings (by site and AllAreas) and their contents:
  - galltypes_by_parasitoid_morphospecies_AllAreas.csv
    - Rows: gall morphotypes; Columns: parasitoid morphospecies; counts across both sites combined.
  - galltypes_by_parasitoid_morphospecies_Emeishan.csv
    - Rows: gall morphotypes; Columns: parasitoid morphospecies; counts for Emeishan site.
  - galltypes_by_parasitoid_morphospecies_Mianning.csv
    - Rows: gall morphotypes; Columns: parasitoid morphospecies; counts for Mianning site.
  - trees_by_galltype_AllAreas.csv
    - Rows: tree species; Columns: gall morphotypes; counts across both sites combined.
  - trees_by_galltype_Emeishan.csv
    - Rows: tree species; Columns: gall morphotypes; counts for Emeishan site.
  - trees_by_galltype_Mianning.csv
    - Rows: tree species; Columns: gall morphotypes; counts for Mianning site.
  - trees_by_parasitoid_morphotype_AllAreas.csv
    - Rows: tree species; Columns: parasitoid morphospecies; counts across both sites combined.
  - trees_by_parasitoid_morphotype_Emeishan.csv
    - Rows: tree species; Columns: parasitoid morphospecies; counts for Emeishan site.
  - trees_by_parasitoid_morphotype_Mianning.csv
    - Rows: tree species; Columns: parasitoid morphospecies; counts for Mianning site.

## Reference

- Fang, Z.; Tang, C.-T.; Sinclair, F.; Csóka, G.; Hearn, J.; McCormack, K.; Melika, G.; Mikolajczak, K.M.; Nicholls, J.A.; Nieves-Aldrey, J.-L.; Notton, D.G.; Radosevic, S.; Bailey, R.I.; Reiss, A.; Zhang, Y.M.; Zhu, Y.; Fang, S.; Schönrogge, K.; Stone, G.N. (2023). Network structure and taxonomic composition of tritrophic communities of Fagaceae, cynipid gallwasps and parasitoids in Sichuan, China. Insect Conservation and Diversity, 2024:1-26. DOI: 10.1111/icad.12768