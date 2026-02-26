# Supporting documentation for the dataset: Pollinator visitation data on oilseed rape varieties

- Aim and scope
  - Purpose: identify key pollinators for oilseed rape (OSR) and whether there are feeding preferences for individual OSR varieties.
  - Context: data collected in 2012 across UK national trial sites managed by Syngenta to compare pollinator visitation among OSR varieties.

- Experimental design and sampling regime
  - Sites and materials
    - Four national trial sites: Fulbourn (Cambridge), Orford (Suffolk), Horncastle (Lincolnshire), Benson (Oxford).
    - Each site contains 20 OSR varieties replicated in three blocks; varieties are represented as codes for commercial sensitivity.
    - Plots: 12 m × 12 m each.
  - Observation framework
    - Only two replicate blocks per site were used for pollinator observations, comprising 40 plots per site (20 plots per block).
    - Two visits per site during mid- to late-flowering period.
    - Flowering threshold: observations conducted where approximately 30% or more OSR plants were in flower.
  - Observation protocol
    - Time window: observations between 10:00 and 16:00 (start times not after 15:00) to capture high bee activity.
    - Each plot observation: six-minute period walking within a 2 m edge band of the plot.
    - Each variety observed in two separate six-minute periods per site, on two sampling days (one per replicate block).
  - Data recorded per plot per six-minute interval
    - Percentage of OSR plants flowering within a 1 m × 1 m area.
    - Pollinator counts by taxonomic group with specified resolutions (see below).
  - Flowering threshold requirement
    - If flowering was less than ~30%, pollinator observations were not recorded for that plot.

- Pollinator data and taxonomic resolution
  - Honey bees: Apis mellifera.
  - Bumblebees: Bombus spp with species-level resolution for several taxa (e.g., B. lapidarius, B. terrestris, B. lucorum, etc.).
  - Solitary bees: grouped by functional forms; includes Lasiglossum (genus), Osmia (bicolour & rufa), Andrena with body-form classifications corresponding to multiple species.
  - Hoverflies: divided into large (>12 mm) and small (<11 mm) groups.
  - Bibionidae: primary focus on Bibio marci.
  - Taxonomic granularity reflects practical identification limitations in field conditions and the study’s design.

- Quality assurance and data integrity
  - Field data collection overseen by an expert in bee identification from the Bees, Ants & Wasps Recording Society; other recorders were recognized bee experts or experienced ecologists.
  - Consistency checks performed by a senior expert; identifiable recorders on data sheets to enable traceability.
  - Standardised data entry sheets with a shared nomenclature to ensure consistency across species names and avoid duplications due to taxonomic updates.
  - A single person conducted data entry; post-entry checks included double-entry verification and graphing raw values to detect outliers and errors.

- Data structure and accessibility
  - Primary data file: Oilseed_rape_variety_pollinator_data.csv.
  - Metadata file: Oilseed_rape_variety_pollinator_data_metadata.csv, describing the meanings of columns and data fields.
  - Reference framework for observational methods: Pollard, E. & Yates, T.J. (1993) Monitoring Butterflies for Ecology and Conservation.
  - Visual aid: Figure 1 illustrates the plot layout and the 2 m band used for pollinator observations.

- Considerations for analysis and interpretation
  - Commercial sensitivity limits access to actual variety names; analyses will rely on coded variety identifiers.
  - Observations are restricted to specific blocks/sites and limited to two visits per site, which may influence temporal and spatial generalizability.
  - Taxonomic resolution varies by group, which may affect fine-grained correlation analyses between pollinator groups and specific varieties.
  - Data quality measures (expert QA, standardized entry, and outlier checks) support reliability but users should account for potential weather-related variability and flowering thresholds when modeling relationships.

- References
  - Pollard, E. & Yates, T.J. (1993). Monitoring Butterflies for Ecology and Conservation. Chapman and Hall, London.