# Pollinators in oilseed rape fields in relation to local plant diversity and landscape characteristics

## Overview
- A dataset describing pollinators in winter-sown oilseed rape (Brassica napus) fields in relation to local plant diversity and landscape context.
- Collected as part of the Wessex BESS project (NERC Biodiversity and Ecosystem Service Sustainability program) across 2014–2015 in southern England.
- Aimed at linking pollinator presence and activity to local habitat diversity (in-crop and field margins) and landscape-scale features within 0.5–3 km buffers around collection points.
- Data designed for integration with other Wessex BESS WP4 datasets to support broader environmental monitoring and policy assessment.

## Study design and data collection
- Field sites: 12 fields surveyed each year (2014 and 2015) in the Wessex region, an area primarily arable and intensive grassland with remnant calcareous grassland.
- Local habitat assessment:
  - In-field margin and field-edge structure measured (field-edge length, hedge proportion, field-margin width/area).
  - Margin plant diversity estimated with five 1 m2 quadrats per sampling point.
- Pollinator sampling:
  - Flower visitors counted along three 58 m transects per field (perpendicular to field edge), focusing on Bombus spp. and Apis mellifera visiting flowers within 2 m of observers.
  - Pan traps (15 cm) used to sample solitary bees, hoverflies, and other visitors; pan traps deployed at 8 m, 32 m, and 58 m into the crop and left for 4 days.
  - Transect surveys conducted 10:00–16:00 under conditions: temperature > 12°C and wind speed < 6–8 m/s.
  - Bees identified to species and caste where possible; pan-trapped specimens identified to family level for some taxa.
- Temporal scope: data collected in 2014 and 2015 across the Wessex region (specific field coordinates provided for the NW and SE corners).

## Local habitat and plant diversity metrics
- Field-margin and edge characteristics:
  - Proportion of hedge, proportion of field margin, and width of field margin recorded near transects.
- Biodiversity within margins and crops:
  - Plant diversity measured with quadrats near transects and within crop areas; species identified using standard flora references.
- Data are designed to link local habitat structure with pollinator observations and landscape context.

## Landscape context and GIS methods
- Landscape variables calculated within buffers around transect midpoints (0.5–3 km, at 0.5 km intervals).
- Data sources and classifications:
  - CEH Land Cover Map 2007, Natural England Priority Habitats Inventory (PHI), and local National Vegetation Community (NVC) surveys.
  - Grassland types distinguished as species-rich, semi-improved, restored, intermediate, and improved based on NVC codes.
  - Restoring grassland categories derived from a combination of land-cover datasets and local knowledge of restoration projects.
- Metrics computed include:
  - Area of grassland types (species-rich, restoring, improved), semi-natural habitat, and arable habitat within each buffer.
  - Within-field and surrounding landscape composition expressed through SppRich (species-rich grassland), SN (semi-natural habitat), OSR (oilseed rape), IG (intensive grassland), RES (restored grassland), and related area and distance measures.
  - Additional landscape context metrics such as margins, hedge length/height, and proximity of different habitat patches.

## Data structure and metadata
- Core files:
  - NERCPollinatorSpeciesList.csv
  - NERCPanTrapData.csv
  - NERCPollTrans.csv
  - NERCPollLandscapeSurvey.csv
- Linking keys:
  - FarmID, FieldID, TransectID, PointCode, and SpeciesCode are common across WP4 datasets to enable data integration.
- Taxonomic and functional grouping:
  - Species identified to the highest possible taxonomic level; some taxa identified only to family or superfamily.
  - FunctionalGroupPollSwab and FunctionalGroupPollSwab link to pollinator function and, where possible, a related dataset on pollinator efficiency.
- Data quality notes:
  - Some missing data in pan trap records due to traps being knocked over.
  - Certain taxa identified only to higher taxonomic levels; some gender/caste data only available for Apoidea.
- Ethical and governance:
  - Field methods approved by the CLES Penryn Research Ethics Committee (application 2014/622).
  - Data entry and QA conducted with standardized protocols and training.

## Quality assurance and governance
- Standardized field and lab protocols followed; dedicated datasheets for each collection type.
- Data entered in MS Access with anomaly checks and training oversight.
- Ethics approval obtained and documented.

## Data accessibility and use for environmental monitoring
- Dataset is designed for use alongside other Wessex BESS WP4 datasets to enable integrated analysis of pollinators, plant diversity, and landscape context.
- Outputs supported by the dataset include clear formats such as maps, charts, and reports that illustrate environmental health and policy performance over time.
- Potential users include researchers, environmental monitor teams, and policy evaluators seeking standardized, linkable pollinator and habitat data.
- Key challenges highlighted for analysts:
  - Increasing the value of datasets by integrating with additional environmental data.
  - Enabling access to underlying data to support broader analyses and transparency.

## Applications and implications for policy and monitoring
- Enables assessment of how local plant diversity and landscape structure within 0.5–3 km affect pollinator communities in oilseed rape fields.
- Provides a standardized framework for monitoring pollinator activity in key agricultural landscapes over multiple years.
- Facilitates linkage to broader habitat quality indicators and biodiversity metrics used in policy evaluation and habitat management decisions.

## References
- Lancashire, P. D., et al. (1991). A uniform decimal code for growth stages of crops and weeds.
- Morton, D., et al. (2011). Final Report for LCM2007 - the new UK Land Cover Map.
- Rodwell, J. S. (1992). British Plant Communities. Cambridge University Press.
- Stace, C. (1997). New flora of the British Isles. Cambridge University Press.
- Toynton, P., & Ash, D. (2002). Salisbury Plain Training Area - The British steppes? British Wildlife.
- Walker, K., & Pywell, R. F. (2000). Grassland communities on Salisbury Plain Training Area. Wiltshire Botany.