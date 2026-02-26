# ReadMe_ Sichuan_trophic_interaction_data.doc

- This document describes a dataset of quantitative trophic interactions among Fagaceae trees, Cynipid gallwasps, and parasitoids from Sichuan Province, China, linked to Fang et al. (2024).

## Purpose and scope
- Records counts of interactions across three trophic levels:
  - Higher level: tree species (Fagaceae)
  - Middle level: gall morphotypes (Cynipid gallwasps)
  - Lower level: parasitoid morphospecies reared from the galls
- Data focus on two field sites, Emeishan and Mianning, collected between November 2017 and June 2022.
- Taxa and morphospecies definitions follow Fang et al. (2024).

## Collection and data generation
- Data consist of quantitative survey records:
  - Tree species associated with gall morphotypes
  - Gall morphotypes associated with parasitoid morphospecies
- Sampling performed by a single field team; standardised protocols described in Fang et al. (2024).
- Identifications:
  - Parasitoid identifications validated by an external expert from Natural History Museum, London.
  - Gall morphotype identifications validated using DNA barcoding (per Fang et al. 2024).
- Full sampling details, including sample sizes per site and taxon, are provided in Fang et al. (2024).

## Data quality and structure
- Quality control:
  - Standardised data collection methods
  - Consistent team validation for tree, gall, and parasitoid identifications
  - External taxonomic validation for parasitoids; DNA-based validation for gall morphotypes
  - Careful error checking documented
- Data structure:
  - Pairwise matrices of counts linking higher to lower trophic levels
  - Taxa definitions and structure referenced to Fang et al. (2024)
  - Files are organized by site and by all-sites combined (AllAreas)

## Files and contents
- galltypes_by_parasitoid_morphospecies_AllAreas.csv
  - Counts of recorded interactions between gall morphotypes (rows) and parasitoid morphospecies (columns) across both sites combined.
- galltypes_by_parasitoid_morphospecies_Emeishan.csv
  - Same structure as above for the Emeishan site.
- galltypes_by_parasitoid_morphospecies_Mianning.csv
  - Same structure as above for the Mianning site.
- trees_by_galltype_AllAreas.csv
  - Counts of interactions between tree species (rows) and gall morphotypes (columns) across both sites combined.
- trees_by_galltype_Emeishan.csv
  - Counts of interactions between tree species (rows) and gall morphotypes (columns) at Emeishan.
- trees_by_galltype_Mianning.csv
  - Counts of interactions between tree species (rows) and gall morphotypes (columns) at Mianning.
- trees_by_parasitoid_morphotype_AllAreas.csv
  - Counts of interactions between tree species (rows) and parasitoid morphospecies (columns) across both sites combined.
- trees_by_parasitoid_morphotype_Emeishan.csv
  - Counts of interactions between tree species (rows) and parasitoid morphospecies (columns) at Emeishan.
- trees_by_parasitoid_morphotype_Mianning.csv
  - Counts of interactions between tree species (rows) and parasitoid morphospecies (columns) at Mianning.

## Units and taxonomy
- Recorded values are counts of individual interactions (not presence/absence or rates).
- Gall morphotypes, parasitoid morphospecies, and tree species follow taxonomic definitions as outlined in Fang et al. (2024).

## Temporal and geographic coverage
- Locations: Emeishan and Mianning, Sichuan Province, China
- Sampling period: November 2017 – June 2022

## Access and references
- Data are presented in conjunction with Fang et al. (2024) and are available freely online.
- Primary reference:
  - Fang, Z., Tang, C.-T., Sinclair, F., Csóka, G., Hearn, J., McCormack, K., Melika, G., Mikolajczak, K., Nicholls, J.A., Nieves-Aldrey, J.-L., Notton, D.G., Radosevic, S., Bailey, R.I., Reiss, A., Zhang, Y.M., Zhu, Y., Fang, S., Schönrogge, K., and Stone, G.N. (2023). Network structure and taxonomic composition of tritrophic communities of Fagaceae, cynipid gallwasps and parasitoids in Sichuan, China. Insect Conservation and Diversity, 2024;1-26. DOI: 10.1111/icad.12768

## Relevance for environmental monitoring
- Provides standardized, cross-site datasets suitable for monitoring changes in:
  - Tritrophic network structure (trees → galls → parasitoids)
  - Taxonomic composition and interaction frequencies over time
- Supports analyses of network metrics, biodiversity patterns, and potential policy-relevant indicators of ecosystem health in Fagaceae-dominated habitats.