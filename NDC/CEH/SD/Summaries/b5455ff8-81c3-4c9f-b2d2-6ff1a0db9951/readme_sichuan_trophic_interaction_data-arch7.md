# ReadMe_ Sichuan_trophic_interaction_data.doc

## Overview
- Dataset related to Fang et al. (2024) and describes data and analyses on a tritrophic network from Sichuan, China.
- Focuses on interactions among three trophic levels: Fagaceae tree species, morphospecies of herbivorous Cynipid gallwasps, and morphospecies of parasitoids reared from the galls.
- Data collected at two sites, Emeishan and Mianning, between November 2017 and June 2022; data are counts of interactions (records of gall morphotypes with parasitoids and with trees).

## Data collection and quality control
- Field work conducted by the same team; identifications validated by the same team members.
- Parasitoid identifications validated by an external expert from the Natural History Museum, London.
- Gall morphotype identifications validated using DNA barcoding (as described in Fang et al. 2024).
- Standardised data collection protocols followed; datasets checked for errors.

## Data structure and content
- Datasets are pairwise matrices of counts, linking higher trophic levels to lower ones.
- Three trophic levels defined as per Fang et al. 2024; taxonomy and morphospecies definitions aligned with that work.
- Files are organized by site and by AllAreas (both sites combined), each containing a matrix of counts:
  - galltypes_by_parasitoid_morphospecies_AllAreas.csv
  - galltypes_by_parasitoid_morphospecies_Emeishan.csv
  - galltypes_by_parasitoid_morphospecies_Mianning.csv
  - trees_by_galltype_AllAreas.csv
  - trees_by_galltype_Emeishan.csv
  - trees_by_galltype_Mianning.csv
  - trees_by_parasitoid_morphotype_AllAreas.csv
  - trees_by_parasitoid_morphotype_Emeishan.csv
  - trees_by_parasitoid_morphotype_Mianning.csv
- Each file structure:
  - Rows represent the higher-level taxon (e.g., gall morphotypes or tree species).
  - Columns represent the associated lower-level morphospecies (e.g., parasitoid morphospecies or gall morphotypes), with counts indicating recorded interactions.
  - Units are counts of interactions; datasets describe counts of recorded interactions between the specified taxa.

## Spatial/contextual notes for GIS use
- The data are designed as interaction matrices at two locations (Emeishan and Mianning) and combined AllAreas, suitable for integration with spatial data if site coordinates are added.
- To map or visualise spatial patterns, users would typically join these matrices to spatially explicit species distribution data or site shapefiles; the current files do not include coordinates themselves.
- Potential GIS outputs include interaction heatmaps by site, network visualization by geography, and spatially informed analyses of tripartite interactions when combined with occurrence/abundance data.

## Limitations and considerations
- Data cover two sites with potential resolution limitations for some applications; site-level matrices may not capture microhabitat variation without additional spatial data.
- Data correspond to counts within specified sampling periods; temporal resolution is not provided beyond the overall collection window.
- Taxonomic concepts are defined in Fang et al. 2024; users should refer to that work for detailed taxon definitions.

## Reference
- Fang, Z., Tang, C.-T., Sinclair, F., Csóka, G., Hearn, J., McCormack, K., Melika, G., Mikolajczak, K.M., Nicholls, J.A., Nieves-Aldrey, J.-L., Notton, D.G., Radosevic, S., Bailey, R.I., Reiss, A., Zhang, Y.M., Zhu, Y., Fang, S., Schönrogge, K., and Stone, G.N. (2023). Network structure and taxonomic composition of tritrophic communities of Fagaceae, cynipid gallwasps and parasitoids in Sichuan, China. Insect Conservation and Diversity, 2024;1-26. DOI: 10.1111/icad.12768

## Availability
- Datasets are linked to freely available online analyses and supplementary material accompanying Fang et al. 2024.