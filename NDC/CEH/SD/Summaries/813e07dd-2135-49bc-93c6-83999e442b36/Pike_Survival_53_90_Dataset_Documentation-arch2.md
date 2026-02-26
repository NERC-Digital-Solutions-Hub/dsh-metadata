# Pike Survival Data 1953-1990

## Overview
- Dataset used in Vindenes et al. (2013) American Naturalist on climate change effects in freshwater predator dynamics.
- Derived from capture-mark-recapture data of Pike (Esox lucius) in Windermere Lake, UK.
- Covers survival data (binary) for individuals over time; includes both sexes and unknown-sex individuals.

## Content and Format
- Format: CSV
- Size: 68 KB
- Core columns:
  - YEAR: Year of first capture of an individual
  - LENGTH: Fork length at capture (cm)
  - SURVIVAL: 1 if the individual was recaptured/sighted again (survived the first period after capture), 0 otherwise
- Location: Windermere Lake, Cumbria, Great Britain (grid references provided)
- Species: Esox lucius (Pike)

## Sampling regime and data collection
- Sampling site: Windermere Lake, with data from north and south basins
- Temporal space: Data collection began in 1944; this dataset spans 1953–1990 for survival
- Collection methods (historical to standardised):
  - Gill netting (since 1982 standardised): 64 mm bar mesh, multifilament nets, 40 m x 3 m
  - Sampling schedule: Oct–Dec, at about 10 sites per basin; five nets deployed per site
  - Protocol: nets set on the bottom, checked biweekly; sites rotated to cover entire lake
  - Post-1989/1990 changes: total annual sampling ~240 net days, distributed between basins
- Tagging and sightings:
  - Mark-and-release with individually numbered tags
  - Catch-and-release anglers contributed sightings of tagged fish

## Measurements and data processing
- In-lab measurements: fork length (to 1 mm), weight (to 100 g); sex determined from dissection
- Aging: opercular bone (ageing method by Frost & Kipling, 1959)
- Birth date used for age structure: 1 April
- Data linkage: combined morphometric and age data with tag sightings to compute SURVIVAL (per Haugen et al., 2007)

## Quality control
- Measurements are checked by permutations involving three individuals to ensure accuracy

## Analytical framework and outputs
- Survival derived from recapture/sighting data (SURVIVAL column)
- Related analyses and context:
  - Used in studies of density dependence and population dynamics (e.g., Haugen et al., 2007)
  - Linked to climate-related trait dynamics in freshwater ecosystems (Vindenes et al., 2013)
  - Related physiological and ecological insights through complementing datasets (growth, fecundity, temperature)

## Related datasets and metadata
- Metadata record: Pike 1944-2002
- Related datasets provided by CEH/FBA:
  - Pike - Fecundity Data 1963-2002
  - Pike - Growth Data 1944-1995
  - Windermere Lake Temperature 1944-2002

## Practical notes for environmental monitoring analysts
- Data provenance: collected from a long-running, standardized monitoring program with mark-recapture elements
- Standardised methodology since 1982 enhances comparability over time
- Outputs suitable for monitoring survival trends, age-structured dynamics, and potential climate/density effects
- Data accessibility: CSV format with clear field definitions; linked to broader metadata and related datasets for extended analyses
- Considerations and caveats:
  - Presence of unknown-sex individuals
  - Survival interpreted as first-period survival post-capture; longitudinal follow-up depends on recapture/sighting effort
  - Sampling effort shifted over time (notably around 1990) which may influence trend interpretation

## Data usage in monitoring and policy evaluation
- Enables temporal comparisons of survival linked to environmental drivers (e.g., prey availability, temperature)
- Supports integration with other windermere datasets (growth, fecundity, temperature) for holistic ecosystem assessments
- Formats suitable for dashboards, maps, and charts illustrating survival dynamics and spatial basins
- Promotes data reuse and transparency by providing metadata and cross-referenced publications