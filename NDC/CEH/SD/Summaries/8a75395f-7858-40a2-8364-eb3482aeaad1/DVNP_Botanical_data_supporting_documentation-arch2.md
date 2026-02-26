# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component botanical data

## Overview
- Documents the field component botanical dataset for the Dorset Valuing Nature Project (DVNP).
- Uses a historic baseline from Professor Ronald Good’s 1931–1939 Dorset botanical survey to select sites and study changes in ecosystem services with habitat condition.
- Aims to provide comparable, monitorable data to assess environmental health and policy performance over time.

## Experimental design
- Target habitats: calcareous grassland, heathland, and woodland identified by Good (1930s) and resampled to reflect a degradation gradient.
- Site selection: 13 calcareous grassland, 13 heathland, and 12 woodland sites chosen to represent a range of gradient categories.
- Subsampling and data sources: current habitat types inferred using multiple sources (UK Land Cover Map 2007, Natural England Priority Habitat Inventory 2015, SSSIs 2014, Horsfall 1981, Dorset Heathland survey 2000, Higher Level Stewardship schemes).
- Gradient categorisation: habitats classified along degradation/restoration pathways (e.g., calcareous grassland moving toward improved or restored states, heathland toward coniferous plantation or high gorse/SSSI-quality states, woodland toward coniferous/broadleaf/ancient woodland states).

## Collection methods
- Plot design: 50 m × 50 m sample squares randomly assigned within the Good survey area (via ArcGIS).
- Heathland and calcareous grassland: five 1 m quadrats per site to record percent cover of plants (species or genus when necessary) plus bare ground and litter; sward height measured directly (five points per quadrat).
- Woodland: a more complex layout with five 10 m × 10 m quadrats in a cross pattern to capture canopy and understory structure; central 5 m × 5 m quadrat for understory and shrubs; nested 2 m × 2 m quadrats for ground-layer and saplings/trunk data; records include canopy cover, species presence, and growth forms.
- Documentation: detailed figure 1 illustrating the woodland quadrat arrangement and recording protocols.

## Quality control
- Fieldwork performed by experienced ecologists; the same team conducted all surveys to ensure consistency.
- Data capture and entry: data logged directly into field spreadsheets and checked for anomalies.
- Data schemas provided for botanical data (groundcover and woodland canopy) with explicit column definitions and units to standardise subsequent analysis.

## Data structure and fields (key elements)
- DVNP_Botanical_Data_Groundcover: capture of site, survey date, surveyor, habitat, grid reference, quadrat number/size, sward height, species name (species or genus), percent cover, vegetation layer (ground vs canopy-specific notes for heathland).
- DVNP_Botanical_Data_WoodlandCanopy: captures woodland-specific canopy/understory data across multiple nested quadrats, including tree type, cover type, measurement units, abundance, and values.
- Lookup table: Habitat_1940 to Habitat_2017 mappings used to define gradient categories (e.g., Calcareous -> Calcareous grassland (SSSI quality), Improved grassland, Restoring calcareous grassland; Heathland -> Coniferous plantation, Gorse high heathland, Heathland (SSSI quality); Woodland -> Broadleaf/Coniferous/Ancient woodland (SSSI quality)).
- Metadata conventions: site numbers, date formats, surveyor initials, grid references at 10 km resolution, quadrat identifiers, and explicit notes on species identification when only genus-level determination was possible.

## Gradient habitat mapping (lookup)
- A comprehensive mapping from 1940 habitat categories to 2017 gradient categories to assess condition change over time.
- Examples:
  - Calcareous (1940) → Calcareous grassland (SSSI quality), Improved grassland, or Restoring calcareous grassland (depending on 2017 data).
  - Heathland (1940) → Coniferous plantation on heathland, Gorse high heathland, or Heathland (SSSI quality).
  - Woodland (1940) → Broadleaf woodland, Coniferous plantation, or Ancient woodland (SSSI quality).
- Purpose: standardise comparison of historical habitat condition with contemporary survey results.

## Data sources and references
- Good, R. (1937). An account of a botanical survey of Dorset.
- Horsfall, A. (1981). Observations on plant habitat change in North-East Dorset since 1931.
- Natural England (2014, 2015). SSSIs and Priority Habitats Inventory.
- Rose, R.J., Webb, N.R., Clarke, R.T., Traynor, C.H. (2000). Changes on the heathlands in Dorset between 1987 and 1996.
- These sources underpin site selection, habitat identification, and gradient categorisation for longitudinal analysis.

## Potential uses for analysts monitoring environmental health
- Baseline establishment and longitudinal comparison of habitat condition and ecosystem services.
- Standardised data processing and QA to enable reproducible monitoring across time and datasets.
- Integration with additional environmental datasets to enhance the value and accessibility of the DVNP botanical data.