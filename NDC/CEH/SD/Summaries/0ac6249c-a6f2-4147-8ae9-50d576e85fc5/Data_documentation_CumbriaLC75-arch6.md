# Dataset Documentation

- Overview
  - Cumbria_Land_Classification file details describing a 16-class land classification for Cumbria, Great Britain.
  - File format: ESRI Shapefile; Resolution: 1 km.
  - Coordinate system: British National Grid; Projection: Transverse Mercator; Extent: Great Britain; OSGB36.
  - Purpose: hierarchical land classification to interpret geomorphology, land use, and related features; used as a dichotomous key to classify the remaining area.

- Data Content and Structure
  - 16 land classes derived from environmental characteristics (climate, altitude, slope) and human artefacts.
  - Classification hierarchy (Fig. 2) used to classify samples and interpret affinities between classes (Fig. 3 as an example).
  - Major division: upland vs lowland, with altitude and geology guiding subsequent splits.
  - Descriptions for each land class provided, combining map-characteristics and field survey insights.

- Data Collection and Analysis
  - Sampling method: grid of county squares created from 3x3 km blocks; central square selected to form an approximately 11% sample.
  - Map characteristics recorded from 1-inch scale Ordnance Survey maps; included attributes like roads, buildings, water features, geology, elevation, and other relevant features.
  - Drift was excluded due to inadequate available maps.
  - Analytical methods:
    - Indicator Species Analysis (ISA) to identify discriminating characteristics for classes.
    - Reciprocal Averaging (RA) ordination to assess relationships and test correlations between analyses.
  - Output: a hierarchical land-class framework and a classification key for assigning remaining squares.

- Land Classes: Descriptions and Characteristics
  - Land Class 1–6: generally lowland with varying distance from coastal plains and human artefacts; differing soil types and agricultural qualities.
  - Land Class 7–8: coastal estuarine and bare sand/mud characteristics with mixed agricultural use.
  - Land Class 9–12: upland or middle fells with moorland, coniferous forestry, variable soils, generally poorer agricultural quality.
  - Land Class 13–16: high elevation, Pennine/Lake District margins, steep slopes or summits, extensive peat soils, little to no tree cover, predominantly open-range sheep grazing.

- Distribution and Patterns
  - Approximately two-thirds of Cumbria classified as lowland.
  - Variation in frequency across classes; coastal and upland extremes are relatively infrequent.
  - Large-block occurrence tendencies for some classes (e.g., 1 and 2); smaller, more fragmented patterns for others (e.g., 4 and 11).
  - Upland classes tend to form cohesive patterns between themselves; lowland classes form larger, more dispersed blocks.

- Outputs, Usage, and References
  - Tables and figures referenced:
    - Table 2: Frequency of land classes.
    - Table 3: Associations between land classes.
    - Figure 4: Distribution of land classes.
    - Figure 2: Hierarchy of the land classification.
    - Figure 3: Example usage of the land classification key.
  - Descriptions of each land class are provided, enabling interpretation and application to regional planning, geomorphology, and land-use analyses.
  - References:
    - Bunce, Morrell, & Stel (1975); Hill (1973); Hill, Bunce, & Shaw (1975).

- Practical Considerations and Limitations
  - Sampling represents roughly 11% of the county, with minor differences between sample and full enumeration.
  - Attributes rely on readily recordable map characteristics from 1:1 inch OS maps; some environmental or geological details not captured.
  - Drift and certain geological attributes were excluded due to data availability, which may influence class delineations.

- Summary
  - The dataset provides a structured 16-class land classification for Cumbria, derived from altitude, geology, and human artefacts, using ISA and RA analyses. It offers a reproducible classification framework, detailed class descriptions, and a practical key for classifying remaining areas, with clear implications for understanding regional geomorphology, land use, and planning potentials.