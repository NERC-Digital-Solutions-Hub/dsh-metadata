# Supporting documentation for the dataset: Pollinator visitation data on oilseed rape varieties

## Overview
- Purpose: dataset from 2012 to identify key pollinators for oilseed rape (OSR) and assess potential variety-specific feeding preferences.
- Scope: field observations across four UK national trial sites owned by Syngenta; varieties are coded due to commercial sensitivity.
- Content: structured observations of pollinator visitation linked to OSR flowering in defined plots and varieties; metadata and QA processes documented to support data discovery, reuse, and governance.

## Experimental design and sampling regime
- Sites: Fulbourn (Cambridge), Orford (Suffolk), Horncastle (Lincolnshire), Benson (Oxford).
- Trial structure: 20 OSR varieties replicated in three blocks per farm; plots are 12 × 12 m; varieties represented by codes (breeding system indicated).
- Sampling framework: two visits during mid- to late-flowering; only two replicate blocks used per site for observations; 40 plots per site (20 plots per block across two blocks).
- Plot layout: each plot 12 × 12 m; within-plot flowering estimated in a 1 × 1 m area.
- Observation timing: transects from 10:00 to 16:00, with sampling commencing no later than 15:00; to maximize bee activity.
- Observation protocol: for each plot, a six-minute observation period walking within a 2 m edge strip; plots could be revisited as needed.
- Replication: each OSR variety observed in two separate six-minute periods on each of the two sampling days per site (one per replicate block).

## Data collected per plot per observation
- Flowering status: percentage of OSR plants in flower within the 1 × 1 m area (only recorded if ~30% or more flowering).
- Pollinator counts by taxonomic groups and resolution:
  - Honey bees: Apis mellifera
  - Bumblebees: multiple Bombus species (e.g., B. lapidarius, B. terrestris, B. lucorum, B. pascuorum, B. pratorum, B. hortorum, B. hypnorum, B. vestalis, B. rupestris)
  - Solitary bees: grouped by body forms and representative OSR pollinators (e.g., Lasiglossum, Osmia, Andrena groupings)
  - Hoverflies: large (>12 mm) and small (<11 mm) categories
  - Bibionidae: primarily Bibio marci
- Notes on data: detailed taxonomic resolution as described; records only when flowers ≥ ~30%.

## Quality assurance and data management
- Field QA: data collection overseen by a recognized bee ID expert (Bee/Ant/Wasp Recording Society member); consistency checks by an overarching expert.
- Recorder accountability: field sheets identify who collected each sample.
- Data entry: standardized entry sheets; common abbreviations; consistent species nomenclature to avoid taxonomic duplication from revisions.
- Data integrity: single data-entry person; post-entry double-checks to correct typing errors; outlier detection via graphing of raw values.

## Data structure and accessibility
- Primary data file: Oilseed_rape_variety_pollinator_data.csv
- Metadata file: Oilseed_rape_variety_pollinator_data_metadata.csv
- Methodology reference: Pollard, E. & Yates, T.J. 1993. Monitoring Butterflies for Ecology and Conservation.
- Figure reference: Figure 1 describes the plot layout and 2 m transect within each 12 × 12 m plot.

## Metadata, governance, and sharing considerations
- Commercial sensitivity: OSR varieties are expressed as coded identifiers; breeding system information is retained; data sharing should preserve coding to protect sensitive information.
- Data discoverability and reuse: standardized data structure and accompanying metadata to enable interpretation and integration with other datasets.
- Update and maintenance: dataset documented with clear data handling and QA steps to support future updates and consistency across systems.
- Potential challenges for data stewardship: ensuring timely data receipt from multiple field teams; maintaining consistent metadata across updates; handling large, multi-site datasets and ensuring interoperability across platforms.