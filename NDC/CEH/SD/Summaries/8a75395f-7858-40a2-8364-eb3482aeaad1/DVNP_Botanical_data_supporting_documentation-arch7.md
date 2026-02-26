# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component botanical data

## Overview
- Documents the experimental design, collection methods, quality control, and data schemas for the field component botanical dataset of the Dorset Valuing Nature Project (DVNP).
- Aims to create a baseline of habitat condition and assess how ecosystem services change with habitat condition across calcareous grassland, heathland, and woodland in Dorset.
- Archive is publicly available via the Dorset Environmental Records Centre.

## Experimental design
- Based on Ronald Good's 1931–1939 Dorset botanical survey; Good’s site information forms the baseline.
- Subsampled sites identified by Good as calcareous grassland, heathland, or woodland to survey current habitat types.
- Data sources for site selection include:
  - UK Land Cover Map 2007
  - Natural England Priority Habitat Inventory (2015)
  - Sites of Special Scientific Interest (SSSIs) data (Natural England, 2014)
  - Horsfall (1981) plant habitat change data
  - Dorset Heathland survey (Rose et al., 2000)
  - Higher Level Stewardship schemes
- Final sampling: 13 calcareous grassland sites, 13 heathland sites, and 12 woodland sites, representing a gradient of degradation from the 1930s baseline.
- Gradient categories established for each habitat type (e.g., calcareous: improved grassland, restoring grassland, calcareous grassland (SSSI quality); heathland: coniferous plantation, high-gorse heath, heathland (SSSI quality); woodland: coniferous, broadleaf, ancient woodland (SSSI quality)) with index terms reflecting 1940 vs. 2017 classifications.

## Collection methods
- Sampling frame: 50 m x 50 m sample squares randomly assigned within the original Good survey area using ArcGIS.
- Heathland and calcareous grassland:
  - Five 1 m quadrats per site; record percentage cover of all plant species within each quadrat.
  - Species identified to species level where possible (genus when not).
  - Record bare ground and litter.
  - Sward height measured directly at five points per quadrat; average to produce a single height value.
- Woodland:
  - Five 10 m x 10 m quadrats arranged in a cross within the 50 m x 50 m area to sample canopy and understory.
  - Within the center 5 m x 5 m quadrat: record canopy cover and presence of shrubs, understory trees, and tree saplings.
  - Within the center of each 5 m x 5 m quadrat, a 2 m x 2 m quadrat is used to record herbaceous species, ground-level cover, and sapling data.
  - Documentation includes a figure illustrating the quadrat layout for woodland sampling.

## Quality control
- Field data collected by experienced ecologists; the same ecologists conducted all surveys for consistency.
- Data entered as recorded in the field; checks performed for anomalies.
- Two main data schemas with detailed column definitions:
  - DVNP_Botanical_Data_Groundcover
  - DVNP_Botanical_Data_WoodlandCanopy

## Data schema and fields (examples)
- DVNP_Botanical_Data_Groundcover:
  - Site_No, Date_of_Survey, Surveyor, Habitat, Grid_ref, Quad_No, Quad_Size, Sward_Ht, Species_name, %_cover, Vegetation_Layer
- DVNP_Botanical_Data_WoodlandCanopy:
  - Site_No, Date_of_Survey, Surveyor, Quad_No, Quadrat_size, Species_name, Tree_type, Cover_type, Measurement_unit, Value
- Lookup table for habitat 2017 vs 1940 to define a proposed gradient category (associates 39 entries with corresponding 2017 habitat labels, e.g., Calcareous grassland (SSSI quality), Improved grassland, Restoring calcareous grassland, Coniferous plantation on heathland, Ancient woodland (SSSI quality), Broadleaf woodland, etc.).

## Gradient classification and lookup
- A 2017 habitat gradient lookup table maps 1940 habitat categories to 2017 habitat categories, along with gradient qualifiers (e.g., Calcareous grassland (SSSI quality), Improved grassland, Restoring calcareous grassland, Ancient woodland (SSSI quality), Broadleaf woodland).
- Used to define the site-specific gradient category for analysis and mapping.

## Data sources and accessibility
- Core data sources referenced for site selection and baselining:
  - Good, R. (1937) Dorset botanical survey
  - Horsfall, A. (1981) plant habitat change in Dorset
  - Natural England datasets (SSSIs, Priority Habitats Inventory)
  - Dorset Heathland Survey (Rose et al., 2000)
  - UK Land Cover Map 2007
  - Higher Level Stewardship schemes
- Data and accompanying materials are publicly accessible via the Dorset Environmental Records Centre.

## References
- Good, R. (1937). An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981). A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014). Sites of Special Scientific Interest and historical monuments
- Natural England (2015). Priority Habitats' Inventory version 2.1
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000). Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125