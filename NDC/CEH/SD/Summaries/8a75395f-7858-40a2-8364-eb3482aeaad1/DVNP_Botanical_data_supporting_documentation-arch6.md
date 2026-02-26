# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component botanical data

- Overview
  - Publicly available dataset documenting field botany for the Dorset Valuing Nature Project, using a historical baseline (1931–1939) by Professor Ronald Good to assess changes in ecosystem services with habitat condition.
  - Combines multiple data sources to classify current habitat types and degradation gradients across three original habitat types: calcareous grassland, heathland, and woodland.
  - Aims to enable comparisons of habitat condition with ecosystem service potential and to support data-driven insights and products for end users.

## Experimental design
- Baseline and sampling
  - Good (1937) survey used as baseline habitat reference; 1930s calcareous grassland, heathland, and woodland were identified for follow-up.
  - Sites were selected to represent a gradient of degradation from the original habitat.
- Site selection and gradient categorisation
  - Calcareous: 13 sites; Heathland: 13 sites; Woodland: 12 sites.
  - Gradient definitions include combinations such as “Improved grassland,” “Restoring calcareous grassland,” “Calcareous grassland (SSSI quality),” “Coniferous plantation on heathland,” “Gorse high heathland,” “Heathland (SSSI quality),” “Coniferous plantation,” “Broadleaf woodland,” and “Ancient woodland (SSSI quality).”
  - Gradient categories were defined by integrating 1940 Good survey data with 2000s/2017 data from multiple sources.
- Data sources and integration
  - UK Land Cover Map 2007; Natural England Priority Habitat Inventory (2015); Sites of Special Scientific Interest (SSSI) data (2014); Horsfall (1981); Dorset Heathland survey (Rose et al., 2000); Higher Level Stewardship schemes.
  - A lookup table maps 1940 habitat designations to 2017 habitat/gradient categories.

- Special notes
  - Ancient woodland plantations were screened out to avoid confounding results.
  - Some sites represent restoration or maintenance categories aligned with habitat policy classifications.

## Collection methods
- Plot design and placement
  - Randomly assigned 50m x 50m sample squares within the original Good survey area (via ArcGIS) prior to fieldwork.
- Heathland and calcareous grassland methods
  - Five 1m x 1m quadrats per sample, placed at random within the 50m square.
  - Record plant species (to species level where possible, else genus), percent cover per species, bare ground, and litter.
  - Sward height measured directly with a ruler at five points per quadrat; average used as sward height.
- Woodland methods
  - Five 10m x 10m quadrats arranged in a cross across the 50m square to capture canopy structure.
  - Within the center 5m x 5m quadrat: record understory species and canopy/shrub presence; within a 2x2 m nested quadrat: record ground-level vegetation and saplings.
  - Data capture includes canopy cover by tree type, understory, saplings, and ground-cover components; distinct protocols for canopy vs. ground-level measurements between Heathland/Grassland and Woodland plots.

## Quality control
- Personnel and consistency
  - All data collected by experienced field ecologists; the same ecologists conducted all surveys for consistency.
- Data recording and verification
  - Field-recorded data entered directly into DVNP_Botanical_Data_Groundcover (groundcover data) and DVNP_Botanical_Data_WoodlandCanopy (woodland canopy data).
  - Data checked for anomalies and harmonised to defined column headings and units.
- Data structure and documentation
  - Detailed data dictionaries accompany the files, describing site numbers, dates, surveyors, habitats, grid references, quadrat details, species names (with notes when only genus-level ID possible), percent cover, vegetation layer, and measurement units.

## Data files and lookup resources
- DVNP_Botanical_Data_Groundcover
  - Ground-level and subplot botanical data for heathland and calcareous grassland plots.
- DVNP_Botanical_Data_WoodlandCanopy
  - Woodland canopy and associated subplots, including tree/shrub layers, saplings, and ground-cover measurements.
- Habitat gradient lookup (2017)
  - Crosswalk mapping historical 1940 habitats to 2017 habitat categories and their corresponding gradient classifications (e.g., Calcareous grassland (SSSI quality), Restoring calcareous grassland, Ancient woodland (SSSI quality), etc.).
- Data provenance and structure
  - Clear column definitions for site, date, surveyor, habitat, grid references, quadrat numbers/sizes, species, cover percentages, vegetation layers, and measurement values.

## Data provenance and references
- Primary sources
  - Good, R. (1937) on Dorset botanical survey; Horsfall (1981) pattern of habitat change; Natural England sources on SSSIs and Priority Habitats Inventory (2014–2015); Dorset Heathland survey (Rose et al., 2000).
- Public accessibility
  - Archive publicly available via Dorset Environmental Records Centre (DERC).

## Practical considerations for data use
- Potential outputs
  - Baseline vs. current habitat condition comparisons; gradient-based analyses of ecosystem service changes; ability to create self-serve dashboards or reports showing habitat condition, species composition, and canopy/ground-layer structure across sites.
- Data compatibility and integration
  - Uses multi-source, historical-to-modern harmonization; gradient categories enable comparability across time.
- Limitations and cautions
  - Despite rigorous QC, data integrate diverse sources and habitat types; ensure consistent interpretation of gradient labels across sites (e.g., distinguishing SSSI quality vs. restoration states).
  - Ancient woodland filtering applied; some species identifications limited to genus where necessary.