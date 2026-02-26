# Cumbria_Land_Classification file details

- Dataset documents a 16-class land classification for Cumbria, Great Britain, stratified by environmental characteristics (climate, altitude, slope) and “land class” (stratum).
- Format: ESRI Shapefile
- Resolution: 1 km
- Coordinate system: British National Grid (OSGB36), Projection: Transverse Mercator
- Extent: Great Britain
- Descriptions and analysis derive from historical ecological surveys and map-based attributes.

## Data content and structure

- Land Classes: 16 hierarchical land classes (1–16) representing upland and lowland areas with distinct geology and land-use characteristics.
- Basis for classification:
  - Map characteristics from one-inch scale Ordnance Survey maps
  - Inclusion of human artefacts (e.g., roads, buildings) as potentially informative features
  - Exclusion of drift due to unavailable data
- Analytical approach:
  - Sampling: central square from 3x3 km blocks, approximately 11% sample
  - Classification methods: Indicator Species Analysis (ISA) and Reciprocal Averaging Ordination (RA) to allocate squares to land classes
  - Output interpretation relies on a hierarchical key and ordination trends; not strictly numeric order
- Data provenance:
  - Grounded in Bunce et al. (1975) work and subsequent ecological surveys
  - References to related field methods and analytic techniques

## Land Classes at a glance

- Land Class 1: Lowland characteristics; Solway Plain, western coastal plain; medium-quality agricultural land with varied soils.
- Land Class 2: Slightly higher elevation; Eden Valley/Solway Plain; undulating land with good-quality pasture; deep brown earth soils.
- Land Class 3: Lowland traits at higher elevation (152–229 m); western Eden Valley; limestone geology; mixed pasture with stony brown soils.
- Land Class 4: Mixed lowland-upland features; margins of central fells; variable soils; mixed conifer/deciduous woodlands.
- Land Class 5: Predominantly lowland alluvial plains; Intensive farming; deep brown earth soils.
- Land Class 6: Lowland with significant human artefacts and communications influence; intensive grazing.
- Land Class 7: Coastal estuarine sand and mud.
- Land Class 8: Coastal with bare sand/mud; improved pasture; livestock-oriented farming; deep soils.
- Land Class 9: Markedly upland; foothills of Lake District and Pennines; conifer-dominated forestry; poor moorland soils.
- Land Class 10: Upland with valley bottoms and mountainsides; varied woodland and moorland; poor shallow soils.
- Land Class 11: Complex middle fells; broadleaved woods; poor upland grazing and variable soils.
- Land Class 12: Featureless low fells; extensive conifer plantations; poor soils with peat presence.
- Land Class 13: Steep Pennine/Skiddaw margins; open moorland; deep peats/peaty gleys.
- Land Class 14: High altitude summits and plateaux; little or no trees; open-range sheep/grouse moors; deep peats.
- Land Class 15: Upper slopes of central Lake District fells; rugged, open moorland; peat soils.
- Land Class 16: Summits and highest slopes; very mountainous; peat-rich soils, little grassland.

## Data quality, limitations, and considerations

- Temporal context: Historical dataset; derived from ecological surveys and archival map data (S papers from 1975–1978).
- Data limitations:
  - Drift was excluded due to lack of adequate maps
  - Attributes rely on map-based indicators; field verification may be required for current applicability
  - Some textual descriptions in the documentation include typographical inconsistencies
- Data quality implications for Data Leaders:
  - Provides a structured baseline for regional land-characterization and initial data discovery
  - Suitable for historical trend analysis, regional planning, and cross-domain data integration with caution regarding currency
  - Emphasizes the importance of metadata, data provenance, and explicit classification methodology (ISA/RA) for governance and reuse

## Usage, applications, and governance notes

- Use cases:
  - Baseline land-class distribution and regional segmentation for planning, conservation, and land-use policy
  - Cross-reference with geological and soils data to inform ecosystem assessments
  - Support for historical land-use analyses and methodological replication in similar regions
- Discoverability and metadata:
  - Clear classification hierarchy and methodology (ISA and RA) facilitate traceability and reproducibility
  - Requires awareness of the 1 km resolution and the OSGB36 coordinate system for alignment with other datasets
- Data stewardship considerations:
  - Document lineage, sampling design, and analysis steps to support reuse
  - Assess currency and perform updates or recalibration if applying to contemporary analyses

## Summary conclusions

- The dataset reveals a dominant upland/lowland split in Cumbria, with 16 distinct land classes capturing variations in altitude, geology, land use, and vegetation.
- Approximately two-thirds of Cumbria are classified as lowland, with upland classes forming the remainder; coastal classes form a notable subset at the extremes.
- The hierarchy and class descriptions provide a comprehensive framework for regional land characterization, emphasizing the role of altitude and geology in shaping landscape patterns.
- For Data Leaders, the document offers a well-documented, provenance-rich dataset suitable as a historical baseline, with clear methods and structured classification that supports governance, discovery, and potential integration with other data sources.