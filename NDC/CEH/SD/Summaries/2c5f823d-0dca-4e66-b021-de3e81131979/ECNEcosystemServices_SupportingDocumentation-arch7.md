# Ecosystem services variables from the UK Environmental Change Network (ECN)

## Overview
- Describes a dataset of ecosystem services variables derived from the UK Environmental Change Network (ECN), using the Millennium Ecosystem Assessment (MA) framework as a theoretical basis.
- Aims to support GIS-based exploration and mapping of ecosystem services across multiple long-term monitoring sites.

## Data scope and boundary definition
- 11 ECN sites selected to assess boundary definition for ecosystem services, considering biogeophysical features and social discontinuities (land management and ownership boundaries).
- Boundary choices largely reflect land ownership and decision-making scales; ECN site boundaries often align with internal management units (e.g., whole farms) or, at some sites, correspond to complete water basins.
- Site codes and areas:
  - ALI (Alice Holt) – 850 ha
  - CAI (Cairngorm) – 1000 ha
  - DRA (Drayton) – 200 ha
  - GLE (Glensaugh) – 1125 ha
  - MOO (Moor House) – 3500 ha
  - NOR (North Wyke) – 248 ha
  - POR (Porton Down) – 1564 ha
  - ROT (Rothamsted) – 341 ha
  - SNO (Snowdon) – 544 ha
  - SOU (Sourhope) – 1120 ha
  - WYT (Wytham) – 770 ha
- Total area across sites: 11,262 ha; forested areas present at several sites.

## Data sources and collection
- Three data source types for each site:
  - ECN-collected data following standard ECN protocols.
  - Site managers’ data from additional sources.
  - Expert knowledge from site managers.
- Variables are standardized for a single year (commonly 2009) or annual averages to reduce temporal variability; area-dependent variables are scaled by site area.

## Variables and structure
- 73 ecosystem services variables organized across multiple service categories.
- Key categories (with representative examples):
  - Food: meat (tonnes per ha), vegetables, fruit, cereals, eggs, mushrooms, number of provisioning categories.
  - Fibre: wool (sheep/goats) per ha, wood, etc.
  - Fuel: wood for fuel, hydropower output.
  - Genetic resources: animal and plant species held as genetic stock, national collections.
  - Biochemicals and pharmaceuticals, Ornamental resources.
  - Environmental regulation: Air quality (N and S flux), Climate regulation (net CO2e flux), Water regulation (dam presence, flood events), Erosion.
  - Health and pest regulation: Human diseases risk, Biological control (pest regulation), Pollination (butterflies).
  - Natural hazards and hazards management: Fire frequency, other hazards (noise regulation).
  - Cultural and social values: Cultural diversity, Spiritual and religious values, Educational values, Aesthetic values, Social relations, Heritage, Ecotourism.
- Variables include specific units (e.g., tonnes ha-1, yes/no, numbers per site, log10 scales) and variable numbers/IDs for cross-site consistency.
- Data are intended for spatial analysis and comparison across sites and themes.

## Data format and structure
- Original dataset: Excel 2007; converted to comma-separated values (CSV) for long-term storage.
- Core columns (Table structure):
  - Service type
  - Definition
  - Indicator variable (units)
  - Variable_ID (short name)
  - Variable_Number (the variable’s order)
  - Per-site columns: ALI, CAI, DRA, GLE, MOO, NOR, POR, ROT, SNO, SOU, WYT
- Site-specific data are aligned with Table 1 (site details) and Table 3 (site code mappings).

## Methodology and implementation notes
- Variable selection conducted via a site managers’ workshop in January 2010 to standardize definitions.
- Focus on consistent environmental and biodiversity measurements over time and space; uses 2009 data or year averages for consistency.
- Area-based variables are scaled by site area to enable fair comparisons across sites.
- Data provenance and definitions are detailed in the accompanying tables (Table 2 for variable definitions; Table 3 for site coding; Table 1 for site characteristics).

## References and related work
- Millennium Ecosystem Assessment (2005). Ecosystems and human well-being.
- Dick et al. (2011). A comparison of ecosystem services delivered by 11 long-term monitoring sites in the UK Environmental Change Network. Environmetrics 22(5), 639-648. DOI: 10.1002/env.1069
- Data availability and citation: Dick et al. 2011, ECN Ecosystem services variables; NERC Environmental Information Data Centre. DOI: 10.5285/2c5f823d-0dca-4e66b021-de3e81131979

## Practical implications for GIS Specialists
- Enables cross-site spatial visualization of diverse ecosystem services using standardized, area-adjusted variables.
- Boundary definitions (ownership/management) are integral for accurate mapping and downstream analyses.
- Year-specific snapshots (or averages) support temporal comparisons and trend analyses when combined with other ECN data.
- CSV format with consistent site coding facilitates integration into GIS workflows and spatial joins.