# Earthworm diversity and the integration of physical, biochemical and microbiological functions.

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on understanding soil biota diversity and the functional roles of soil organisms.
- Located at Sourhope, Scottish Borders; Sweethope mesocosm dataset derived from controlled earthworm inoculation experiments.
- Aims to link earthworm community composition with soil microbial processes, organic matter transformations, and physical soil structure.
- Data provide final census data on earthworm abundance/biomass and botanical composition from the Sweethope site (2001).

## Study setting and design
- Experimental site: upland grassland at the Sourhope Research Station; soil types vary across the site.
- Sweethope mesocosms: 100 soil boxes removed from Sourhope and reburied 100 m away in an animal-proof enclosure.
- Experimental treatments:
  - No earthworm inoculation; inoculation with one epigeic species (A), one endogeic species (B), one anecic species (C), and all three functional groups (ABC).
  - Lime vs. control (limed plots applied to main Sourhope plots and mirrored in Sweethope).
- Earthworm inoculation: April 2000 with Lumbricus rubellus (20 per box, epigeic), Allolobophora chlorotica (15 per box, endogeic), Lumbricus terrestris (4 per box, anecic).
- Sampling: final census in October 2001; boxes were designed to prevent escape/invasion and to mirror the main plots’ layout.

## Data collected
- Earthworm census: hand-sorted to identify species; abundance and biomass per m^2; specimens killed in 40% ethanol prior to identification (Sims & Gerard key).
- Botanical composition: plant species presence and cover assessed at end of experiment using Braun-Blanquet scale.
- Data collected for each treatment and plot, enabling assessment of interactions between earthworm functional groups, lime treatment, soil biology, and plant communities.

## Datasets and structure
- Dataset 1009: Sweethope Endpoint Botanical Composition Data (2129_BOTANICAL_COMPOSITION.csv)
  - Key columns: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C=Control, L=Limed), SPECIES, BOTANICAL_COMPOSITION (Braun-Blanquet cover scale 0–6), plus metadata fields.
  - Purpose: botanical composition per experimental treatment at endpoint (16–17 Oct 2001).
- Dataset 1010: Sweethope Endpoint Earthworm Survey Data (P2129_EARTHWORM_SURVEY.csv)
  - Key columns: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C/L), SPECIES, ABUNDANCE (total per m^2), BIOMASS (per m^2).
  - Purpose: earthworm census per treatment at endpoint, including species-specific abundance and biomass.
- Both datasets include spatial coordinates (CELL_X, CELL_Y), plot identifiers (MAIN_PLOT, SUB_PLOT), and sampling metadata to enable spatial analyses and data integration.

## Data structure and access
- Data files are comma-separated CSVs with clearly defined columns, units, and data types.
- Documentation includes detailed column descriptions and data type definitions for reproducibility and reuse.
- Data storage and accessibility are oriented to enabling downstream analyses and portal uploads by monitoring organizations.

## Quality control and limitations
- Quality control steps included numeric range checks, formatting validation, and logical integrity checks.
- NERC provides no warranty on data accuracy or fitness for a particular use; liability for misuse or misinterpretation is disclaimed.
- Data are end-point snapshots within a controlled experimental framework; applicability to other sites or time periods requires careful consideration of context.

## Relevance for environment monitoring and analysis
- Provides standardized, well-documented datasets linking soil biota (earthworms) to plant communities under controlled treatments.
- Facilitates integration with other environmental data (soil chemistry, microbial processes, lime treatment effects) to evaluate ecosystem function and policy-relevant outcomes.
- Supports analyses of functional group effects on soil structure, carbon/nitrogen cycling, and vegetation dynamics, contributing to monitoring of soil biodiversity and ecosystem health over time.

## References and further reading
- Bishop, H. O., Grieve, I. C., Chudek, J. A., & Hopkins, D. W. (2008). Liming upland grassland: effects on earthworm communities and carbon characteristics in casts. European Journal of Soil Science, 59(3), 526-531.
- Scott, J., Bell, J., Kenny, C., Jeffers, J., Buckland, S., & Burt-Smith, G. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Supporting Information via EIDC catalogue.
- Sims, R. W., & Gerard, B. M. (1985). Earthworms: Keys and Notes for identification and study of species (Vol. 31). Brill Archive.
- Spring, C. A. (2003). The effects of earthworms on soil structure in upland grassland. PhD Thesis, University of Stirling.
- Usher, M. B., Sier, A. R., Hornung, M., & Millard, P. (2006). Understanding biological diversity in soil: UK Soil Biodiversity Research Programme. Applied Soil Ecology, 33(2), 101-113.