# Land Cover Map of Great Britain

- Purpose and scope
  - Digital dataset classifying land cover into 25 target classes at 25m resolution, plus 1km summary data with 17 key classes.
  - Derived from Landsat 5 Thematic Mapper imagery using supervised maximum likelihood classification; combines summer and winter data to improve accuracy.
  - Widely used for planning, management, and monitoring across agriculture, ecology, conservation, forestry, water, urban growth, transport, and more.
  - Notable milestone: first complete digital, satellite-derived land cover map for Great Britain since the 1960s.

- Data structure and classification scheme
  - 25 target classes (A–Q, plus UNCLASSIFIED) mapped on a 25m grid.
  - 1km summary data provides for 17 key classes (A–Q) as the proportion of each 1km cell occupied by each key class.
  - Descriptions cover a broad range of land cover types, including sea/inland water, bare ground, arable land, pastures, various grasslands, heath/moor, bracken, different woodlands, bogs, urban/suburban development, and inland bare ground.
  - UNCLASSIFIED (0) accounts for about 2% of Britain due to cloud cover, data gaps, or unusual cover types.

- Methodology and accuracy
  - Classification method: supervised maximum likelihood using Landsat TM data; accuracy improved by using both summer and winter images.
  - Reported overall accuracy around 80–85% when accounting for definitional differences, boundary pixels, and temporal changes; mis-registration and mixed pixels are main error sources.
  - Accuracy comparisons are complex due to differing definitions and reference data; the document emphasizes that results are average error rates and may vary locally.
  - Ground-truth data are limited; exact validation is challenging, and accuracy should be interpreted in the context of data model, scale, and class definitions.

- Data availability, licensing, and access
  - Stand-alone datasets available for specific geographic areas; data can be provided at 25m resolution or 1km resolution (percentage or dominant value).
  - Licensing offered under a range of agreements (from single-user to corporate multi-site); pricing bands follow NERC Data Policy (commercial, non-commercial, research); UK academics may receive reductions.
  - Data can be re-aggregated or customized (e.g., presenting 25m data as 17 key classes).
  - 2000 update: Land Cover Map 2000 is available with further information and sample data online; downloadable via the Countryside Information System.

- How to use and interpret the data
  - Landscape vs. land use: data represent cover types observed at imaging times, not necessarily current land use.
  - Spatial and temporal considerations: accuracy reflects dominant cover at the time of imaging; users should consider temporal change when comparing surveys.
  - 1km summary data enable broad-scale analyses using proportional cover per key class within each 1km cell.
  - Aggregation and customization: users may aggregate 25 classes into fewer categories in GIS if needed, depending on accuracy requirements.
  - Color and classification mapping: Appendix 2 provides a color recipe to visualize classes consistently.

- Practical applications and examples
  - Change detection and landscape management.
  - Environmental assessments (e.g., motorway impact, bracken distribution related to health studies).
  - Planning telecom networks, forestry management, water resources, urban development monitoring.

- Usage notes and governance
  - Data should be considered in context of metadata and data provenance; recommended to use a Data Assessment Report (DAR) for feedback and quality notes.
  - The dataset acknowledges potential limitations in class definitions, generalization effects, and cross-survey differences.

- Appendix and technical details
  - Appendix 2: Colour mapping (RGB values) for each target and key class to support consistent visualization.

- Availability of Land Cover Map 2000
  - The Land Cover Map 2000 (updated product) is now available with additional information and sample data online; downloadable via the Countryside Information System.

- Example applications and current relevance
  - Used for detecting changing land cover, supporting ecological and environmental assessments, and informing spatial planning and infrastructure development.