# ReadMe_ Sichuan_trophic_interaction_data.doc

- Overview
  - Dataset relates to data and analyses in Fang et al. (2024) and is available freely online.
  - Focused on a tri-trophic network involving Fagaceae trees, Cynipid gallwasps, and parasitoids in Sichuan, China.

- Collection and scope
  - Quantitative survey records for:
    - Linnean tree species from the family Fagaceae
    - Morphospecies of herbivorous Cynipid gallwasps (Cynipidae: Cynipini) on those trees
    - Morphospecies of Hymenopteran parasitoids reared from the Cynipid galls
  - Sites: Emeishan and Mianning, Sichuan Province, China
  - Timeframe: November 2017 – June 2022
  - Full sampling methods and taxonomic details described in Fang et al. (2024)

- Taxa and measurements
  - Nature of data: counts of gall morphotypes associated with tree species, and counts of parasitoid morphospecies associated with gall morphotypes
  - Taxa definitions and hierarchical structure are described in Fang et al. (2024)

- Quality control and provenance
  - Standardised data collection protocols (detailed in Fang et al. 2024)
  - All field samples collected by the same field team
  - Identifications for trees, galls, and parasitoids validated by the same team
  - Parasitoid identifications validated by an external expert from the Natural History Museum, London
  - Gall morphotype identifications validated using DNA barcoding
  - Data thoroughly checked for errors

- Data structure and contents
  - Form: pairwise matrices of counts linking higher trophic levels to lower trophic levels
  - Datasets are split by site (Emeishan, Mianning) and for AllAreas (both sites combined)
  - Included files (CSV) and their contents:
    - galltypes_by_parasitoid_morphospecies_AllAreas.csv: interactions between gall morphotypes (rows) and parasitoid morphospecies (columns) across both sites
    - galltypes_by_parasitoid_morphospecies_Emeishan.csv: interactions at the Emeishan site
    - galltypes_by_parasitoid_morphospecies_Mianning.csv: interactions at the Mianning site
    - trees_by_galltype_AllAreas.csv: interactions between tree species (rows) and gall morphotypes (columns) across both sites
    - trees_by_galltype_Emeishan.csv: interactions at the Emeishan site
    - trees_by_galltype_Mianning.csv: interactions at the Mianning site
    - trees_by_parasitoid_morphotype_AllAreas.csv: interactions between tree species (rows) and parasitoid morphospecies (columns) across both sites
    - trees_by_parasitoid_morphotype_Emeishan.csv: interactions at the Emeishan site
    - trees_by_parasitoid_morphotype_Mianning.csv: interactions at the Mianning site

- Documentation and references
  - Detailed sampling methods and taxonomy are described in Fang et al. (2024)
  - Related publication: Fang, Z.; Tang, C.-T.; Sinclair, F.; Csóka, G.; Hearn, J.; McCormack, K.; Melika, G.; Mikolajczak, K.M.; Nicholls, J.A.; Nieves-Aldrey, J.-L.; Notton, D.G.; Radosevic, S.; Bailey, R.I.; Reiss, A.; Zhang, Y.M.; Zhu, Y.; Fang, S.; Schönrogge, K.; Stone, G.N. (2024). Network structure and taxonomic composition of tritrophic communities of Fagaceae, cynipid gallwasps and parasitoids in Sichuan, China. Insect Conservation and Diversity, 2024;1-26. DOI: 10.1111/icad.12768

- Data stewardship notes for reuse
  - Open-access dataset; ensure citation of Fang et al. (2024) for taxonomy and methods
  - Follow metadata standards implied by related publication for discoverability
  - Be aware of site- and taxon-level structure when integrating across files
  - Consider data licensing and attribution when sharing analyses derived from these matrices