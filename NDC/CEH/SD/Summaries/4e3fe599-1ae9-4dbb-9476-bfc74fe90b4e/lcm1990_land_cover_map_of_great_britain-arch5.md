# Land Cover Map of Great Britain (1990)

## Overview
- Digital dataset classifying land cover into 25 classes at 25 m resolution, derived from Landsat Thematic Mapper data.
- Produced by CEH Wallingford; intended for government, business, and research applications including agriculture, ecology, conservation, forestry, water resources, urban planning, transport, recreation, and mineral extraction.
- Provides the first complete, satellite-based digital map of Great Britain’s land cover since the 1960s.
- Available for any area under a Licence; supports various licensing models from single-user to corporate multi-site.

## Data structure and classification
- Products:
  - 25m resolution full dataset with 25 target cover-types (plus UNCLASSIFIED).
  - 1 km resolution summary dataset aggregating into 17 key cover-types, with each 1 km cell containing the proportion (as an integer percentage) of the cell attributed to each key class.
- Classification scheme:
  - 25 target classes cover categories such as Sea/Estuary, Inland Water, Beach/Coastal Bare Ground, Saltmarsh, Grass Heath, Pasture/Meadow/Amenity Grass, Moorland Grass, Bracken, Deciduous/Mixed Woods, Coniferous/Evergreen Woodlands, Bogs (Upland/Lowland), Tilled Land, Suburban/Rural Development, Urban Development, Inland Bare Ground, Ruderal Weed, Felled Forest, among others, plus Unclassified.
  - Class definitions reflect ecological meaning and are designed for consistency across Britain; accommodates upland vs. lowland distinctions and regional variations in management and landscape.
- Mapping details:
  - Features mapped only if above minimum map-able size (approx. 0.125 ha or larger in practice), with a typical practical minimum around 1 ha.
  - Accuracy and interpretation depend on spectral signatures, time of year, and boundary clarity; mixed boundary pixels are a major source of error.
  - The 1 km data provide per-class proportions within each grid cell, enabling flexible aggregation and custom outputs.

## Data access, licensing, and distribution
- Stand-alone datasets can be ordered for specific geographic areas; available in 25 m and 1 km formats (25 m labels 1–25; 1 km provides 17 key-class layers with percentage cover per class per cell).
- Licensing:
  - Offered under Licence with formats ranging from single-user to corporate multi-site licenses; licensing can be tailored.
  - Data charges are in three bands: commercial, non-commercial, and research use; UK academics may receive reductions under NERC arrangements.
- Data provisioning:
  - Requires coordinates or vector shapefiles for the area of interest.
  - Contact CEH Wallingford for licensing and data delivery (phone: +44 (0)1491 692315; email: spatialdata@ceh.ac.uk).
- Additional notes:
  - Land Cover Map 2000 is also available; information and samples via the Countryside 2000 web resources.
  - Data can be used with custom aggregations or mappings in GIS; non-standard outputs are also possible.

## Data quality, accuracy, and limitations
- Accuracy assessment:
  - Ground-truth data are used for validation, but ground-truth itself varies by method and objectives; broad comparisons yield 67–82% correspondence depending on class definitions and treatment of boundaries and time differences.
  Boundary effects:
  - Approximately 40% of pixels lie on or near a boundary between classes; excluding boundary pixels raises correspondence to about 71%.
  Geometric considerations:
  - Minor spatial displacement can occur due to registration; typical average displacement relative to vector references is around 20 m (0.8 pixels on a 25 m grid).
  Temporal considerations:
  - Land cover can change between summer and winter imaging dates, affecting classifications (e.g., pasture ploughed between dates).
- Overall, a realistic error range is ~80–85% when accounting for interpretation, class definitions, and temporal changes; users should apply metadata and consider the Data Assessment Report (DAR) feedback mechanism for ongoing quality assessment.
- Unclassified areas:
  - About 2% of Britain remains unclassified in the 25 m data; in the 1 km summary, unclassified portions are represented by residual 0% or by the difference from 100% across the 17 key classes.
- Practical implications:
  - The dataset is suitable for landscape-scale analysis and monitoring but should not be treated as exact land-use; use with appropriate caveats, especially for time-sensitive applications.

## Governance, metadata, and good practice
- Documentation emphasizes the distinction between land cover (map) and land use; cover type does not always equate to use.
- Data notes highlight the importance of scale, resolution, class definitions, and the need to reference the DAR for user feedback, analysis guidance, and best practices.
- Classes can be re-aggregated or customized in GIS to meet specific objectives, with the understanding that some distinctions may not be consistently separable across imagery dates.

## Appendices and related notes
- Appendix 2 provides the colour recipe for LCMGB1990 mapping to facilitate consistent visualization.
- The document references ongoing methodological work and related studies, including links to 1994–1990 technical papers and related countryside land cover mapping efforts.

## Contact and further information
- Land Cover Map Sales, CEH Wallingford, Wallingford, Oxon OX10 8BB, England
  - Telephone: +44 (0)1491 692315
  - Email: spatialdata@ceh.ac.uk
- For broader context and updates, see Countryside 2000 resources and the CEH GIS data distribution channels.