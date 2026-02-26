# Land Cover Map of Great Britain (1990)

- Purpose and scope
  - Digital dataset classifying land cover into 25 target classes at 25 m resolution, derived from Landsat 5 Thematic Mapper data.
  - First complete, national land cover map for Great Britain mapped from satellite data, and first digital national land cover map.
  - Used across government, business, and research for planning, ecology, conservation, forestry, water, urban spread, transport, recreation, and mineral extraction.

- Production and accuracy
  - Created with supervised maximum likelihood classifications using combined summer and winter Landsat imagery to improve accuracy.
  - Approximately 88% of Britain was classified from combined imagery; about 0.4% obscured by cloud on both dates.
  - Realistic overall accuracy likely 80–85%; misclassifications mainly due to mixed boundary pixels and differences in definition between surveys.
  - Some discrepancies arise from temporal changes (e.g., pasture ploughed) and differences in class definitions (botanical vs hydrological criteria for bogs, etc.).
  - Ground-truth data are limited; accuracy assessments compare satellite results with field surveys, acknowledging generalization and classification boundaries.

- Data details and formats
  - 25 target classes (A–Q) plus UNCLASSIFIED; 25 m grid cell data available, plus 1 km summary products.
  - 1 km data provide 17 “key” classes, with each 1 km cell showing the proportion (as an integer percentage) of that cell covered by each key class.
  - Stand-alone datasets can be produced for specific geographic areas; licensing options include various user licenses (single-user to corporate multi-site) and three data-charge bands (commercial, non-commercial, research).
  - Data is supplied under a Licence agreement; licensing can be tailored; contact CEH Wallingford for arrangements.
  - Appendix notes include guidance on data use, accuracy interpretations, and a colour mapping recipe for LCM1990.

- Data access, governance, and licensing
  - Access via Lands Cover Map Sales; licensing designed to support easy access and accommodate different user needs.
  - UK academics may receive reductions under applicable arrangements.
  - Data can be delivered in 25 m resolution (single 25 m layer) or 1 km resolution (summary bands), and tailored to user requirements.
  - Clear distinctions between land cover (map) and land use (functional interpretation); practical limitations in inferring use from cover.

- Class descriptions (selected overview)
  - A Sea/Estuary; B Inland Water; C Coastal Bare Ground; D Saltmarsh; E Rough Pasture / Dune Grass / Grass Moor; F Pasture / Meadow / Amenity Grass; G Marsh / Rough Grass; H Grass / Shrub Heath; I Shrub Heath; J Bracken; K Deciduous / Mixed Wood; L Coniferous / Evergreen Wood; M Bog (Herbaceous); N Tilled Land (Arable Crops); O Suburban / Rural Development; P Urban Development; Q Inland Bare Ground; UNCLASSIFIED.
  - Each class includes specific mapping rules, typical spectral and ecological characteristics, and notes on regional or management-related ambiguities.

- Related updates and further information
  - Land Cover Map 2000 and further information available via the Countryside 2000 website and data download sites.
  - References provided for methodology, accuracy assessments, and historical context.

- Practical considerations for data users
  - Data are best used for assessment of cover patterns, landscape management, environmental impact studies, and broad-scale planning.
  - Be cautious interpreting accuracy at local scales due to boundary effects, time-lag between imagery dates, and definitional differences.
  - For detailed thematic needs, consider aggregating 25 m classes into 17 key classes or customizing aggregations in GIS.