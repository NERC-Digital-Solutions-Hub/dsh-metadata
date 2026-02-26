# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component botanical data.

## Experimental design
- Builds on Professor Ronald Good’s Dorset botanical survey (1931–1939); archive publicly available via Dorset Environmental Records Centre.
- Uses Good’s baseline to select survey sites and examine how ecosystem services change with habitat condition.
- Subsamples sites identified by Good as calcareous grassland, heathland, or woodland to create a survey set: 13 calcareous grassland, 13 heathland, and 12 woodland sites.
- Sites chosen to represent a gradient of degradation from the original habitat.
- Gradient classifications relate 1940 habitat categories to 2000s/2017 interpretations (e.g., calcareous → calcareous grassland (SSSI quality), improved grassland, restored grassland; heathland → coniferous plantation on heathland, gorse-high heathland, heathland (SSSI quality); woodland → broadleaf woodland, coniferous plantation, ancient woodland (SSSI quality)).
- Ancient woodland exclusions noted to ensure fidelity to initial landscape types.

## Collection methods
- Sample areas: 50m x 50m plots randomly allocated within the Good survey area using ArcGIS.
- Heathland and calcareous grassland: five 1m x 1m quadrats per site to record percentage cover of all plant species (identified to species or genus when needed), plus bare ground and litter; sward height measured directly (five points per quadrat, averaged).
- Woodland: five 10m x 10m quadrats (cross-shaped) to capture canopy and cover; a central 5m x 5m quadrat for understory and shrubs; a 2m x 2m quadrat for herbaceous species and ground-level measurements; data collected separately for canopy, understory, and ground flora, including saplings and tree seedlings.
- Data collected includes detailed field records for species names, coverage, vegetation layer, and height metrics (with specific field protocols per habitat type).

## Quality Control
- Surveys conducted by the same experienced field ecologists to ensure consistency.
- Data entered into field spreadsheets with predefined column headers and units; datasets include:
  - DVNP_Botanical_Data_Groundcover for ground-level vegetation in heathland/grassland.
  - DVNP_Botanical_Data_WoodlandCanopy for woodland canopy and multi-layered structure.
- Data checked for anomalies; documentation includes explicit definitions and coding for fields (site numbers, dates, habitat, grid references, quadrat numbers, species, cover percentages, vegetation layers, etc.).
- A lookup table exists to map 1940 habitat classifications to 2017 gradient categories (habitat 1940 ↔ habitat 2017).

## Data structure and metadata
- Detailed field definitions and units provided to ensure consistency and reusability of the botanical data.
- Gradient mapping table links historical habitat categories to current habitat interpretations, enabling comparisons across time.
- Data sources and supporting datasets underpinning site selection and gradient assignment include:
  - UK Land Cover Map 2007
  - Natural England Priority Habitat Inventory (2015)
  - Natural England Sites of Special Scientific Interest (SSSI) data (2014)
  - Horsfall (1981) plant habitat change observations
  - Dorset Heathland Survey (Rose et al., 2000)
  - Higher Level Stewardship schemes

## References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments. https://www.gov.uk/sites-of-special-scientific-interest-and-historical-monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1. http://www.gis.naturalengland.org.uk/pubs/gis/gis_register.asp
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125