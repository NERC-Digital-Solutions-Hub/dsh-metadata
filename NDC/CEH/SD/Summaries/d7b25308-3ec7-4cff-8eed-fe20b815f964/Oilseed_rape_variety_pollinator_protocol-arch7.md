# Supporting documentation for the dataset: Pollinator visitation data on oilseed rape varieties

## Overview
- A 2012 dataset from UK national trial sites aimed at identifying key pollinators of oilseed rape (OSR) and potential feeding preferences by variety.
- Four sites: Fulbourn (Cambridge), Orford (Suffolk), Horncastle (Lincs), Benson (Oxford).
- OSR varieties coded (commercial sensitivity); breeding system indicated for different varieties.
- Data suitable for GIS-driven analysis of pollinator activity by site, plot, and variety.

## Experimental Design and Sampling Regime
- Sites: each with 20 varieties replicated in three blocks; observations conducted on two blocks per site (40 plots per site).
- Plot size: each experimental plot 12 m × 12 m.
- Observation period: two visits per site during mid- to late-flowering; observations between 10:00 and 16:00 hours.
- Flowering threshold: only plots with ~30% or more OSR plants flowering were observed.
- Observation method: six-minute observation per plot, walking within a 2 m edge strip; plots can be revisited multiple times.
- Replication: each variety observed in two separate six-minute periods on each of the two sampling days per site (one per replicate block).

## Pollinator Observations and Taxonomic Resolution
- Data captured per plot per site, including:
  - Percentage of OSR plants in flower within a 1 × 1 m area.
  - Pollinator counts by taxonomic groups:
    - Honey bees: Apis mellifera
    - Bumblebees: Bombus species (multiple specified taxa)
    - Solitary bees: grouped to functional forms (Lasiglossum, Osmia by color/form, Andrena by body form)
    - Hoverflies: large (>12 mm) and small (<11 mm)
    - Bibionidae: primarily Bibio marci
- Aims include identifying key pollinator taxa and any variety-specific visitation patterns.

## Quality Assurance
- Field identifications overseen by bee taxonomy experts; consistency checked by an overall expert.
- Field recorders were bees/field ecologists; each data sheet recorded who collected the sample.
- Data entry used standardized sheets, consistent species abbreviations, and uniform nomenclature to avoid taxonomic duplicates.
- Data entry double-checked; outliers flagged via graphical inspection of raw values.

## Data Structure and Access
- Primary data file: Oilseed_rape_variety_pollinator_data.csv
- Metadata file: Oilseed_rape_variety_pollinator_data_metadata.csv (describes each column)
- Reference framework: Pollard, E & Yates, T.J. 1993 (Monitoring Butterflies for Ecology and Conservation)
- Visual aid: Figure 1 depicts the 12 m × 12 m plots with a 2 m transect inside the plots.

## GIS-Relevant Details and Potential Uses
- Spatially keyed by site and plot, enabling mapping of pollinator abundance and diversity across OSR varieties and trial locations.
- Data granularity at the plot level supports choropleth or point-based mapping of pollinator activity and flowering percentage.
- Variety codes and flowering data allow integration with spatial layers of OSR fields and trial blocks.
- Limitations: exact geographic coordinates of plots and full trait data (beyond breeding system) may require additional metadata or field notes for precise geospatial integration.

## References
- Pollard, E. & Yates, T.J. (1993). Monitoring Butterflies for Ecology and Conservation. Chapman and Hall, London.