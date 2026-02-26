# ReadMe_ Sichuan_trophic_interaction_data.doc

- The dataset documents quantitative survey records across three trophic levels: Linnean tree species in the Fagaceae family, morphospecies of herbivorous Cynipid gallwasps (Cynipidae: Cynipini) collected from those trees, and morphospecies of Hymenopteran parasitoids reared from the Cynipid galls.
- Data originate from two sites in Sichuan Province, China (Emeishan and Mianning) collected between November 2017 and June 2022. Full sampling details and taxonomy are described in Fang et al. (2024).

## Data Collection and Quality Control

- Data collection followed standardised protocols described in Fang et al. (2024); all field work conducted by the same field team.
- Taxonomic identifications:
  - Gall morphotypes validated using DNA barcoding.
  - Parasitoid identifications validated by an external expert taxonomist from the Natural History Museum, London.
  - Tree and gall identifications validated by the field team members.
- Data were carefully checked for errors to ensure quality.

## Taxa and Taxonomic References

- Three trophic levels defined as:
  - Higher level: tree (Fagaceae) species.
  - Middle level: gall morphotypes of Cynipid gallwasps.
  - Lower level: parasitoid morphospecies reared from the galls.
- Taxa definitions align with Fang et al. (2024); taxonomic details referenced there.

## Data Structure and Files

- Data are presented as pairwise count matrices (counts of interactions) linking higher trophic level taxa to lower trophic level taxa.
- Files are split by site and for all areas combined (AllAreas):
  - galltypes_by_parasitoid_morphospecies_AllAreas.csv: gall morphotypes (rows) × parasitoid morphospecies (columns) across both sites.
  - galltypes_by_parasitoid_morphospecies_Emeishan.csv: gall morphotypes × parasitoid morphospecies at Emeishan.
  - galltypes_by_parasitoid_morphospecies_Mianning.csv: gall morphotypes × parasitoid morphospecies at Mianning.
  - trees_by_galltype_AllAreas.csv: tree species (rows) × gall morphotypes (columns) across both sites.
  - trees_by_galltype_Emeishan.csv: tree species × gall morphotypes at Emeishan.
  - trees_by_galltype_Mianning.csv: tree species × gall morphotypes at Mianning.
  - trees_by_parasitoid_morphotype_AllAreas.csv: tree species (rows) × parasitoid morphospecies (columns) across both sites.
  - trees_by_parasitoid_morphotype_Emeishan.csv: tree species × parasitoid morphospecies at Emeishan.
  - trees_by_parasitoid_morphotype_Mianning.csv: tree species × parasitoid morphospecies at Mianning.

## Usage and Citation

- The dataset supports analysis of tritrophic network structure and taxonomic composition in Sichuan, China, with analyses described in Fang et al. (2024) (Insect Conservation and Diversity; freely available online) and the associated reference:
  - Fang, Z.; Tang, C.-T.; Sinclair, F.; Csóka, G.; Hearn, J.; McCormack, K.; Melika, G.; Mikolajczak, K.M.; Nicholls, J.A.; Nieves-Aldrey, J.-L.; Notton, D.G.; Radosevic, S.; Bailey, R.I.; Reiss, A.; Zhang, Y.M.; Zhu, Y.; Fang, S.; Schönrogge, K.; Stone, G.N. (2023). Network structure and taxonomic composition of tritrophic communities of Fagaceae, cynipid gallwasps and parasitoids in Sichuan, China. Insect Conservation and Diversity, 2024;1-26. DOI: 10.1111/icad.12768.