# Final Report for LCM2007 - the new UK land cover map

- The LCM2007 project delivers the first continuous UK land cover map at parcel level, enabling cross-country comparisons and integration with other national datasets. The report focuses on how LCM2007 compares with Countryside Survey (CS) 2007 results, highlighting agreements, differences, and implications for analysis and policy support.

## Very similar area estimates
- Definition: Class areas falling within the CS upper and lower 95% confidence limits in every country.
- Examples of very similar classes across the UK:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland

## Similar area estimates
- Definition: Class areas falling within the CS upper and lower 95% confidence limits for the UK.
- Examples of similar classes:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

## Dissimilar area estimates
- Definition: Classes falling beyond the CS upper and lower 95% confidence limits for the UK.
- Notably dissimilar classes include:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key points on Arable and Horticulture: CS UK estimate around 46,574 km2; CS upper limit ~51,276 km2; LCM2007 estimate ~63,005 km2. Differences attributed to:
  - What each product classifies as “Arable and Horticulture”
  - Spectral confusion and inclusion of boundary/linear features in LCM2007
  - Temporal mismatch and multi-year image requirements in LCM2007
  - Boundary and linear features from Countryside Survey being below LCM MMU, causing boundary-related allocation differences
- Other notable dissimilarities and causes:
  - Improved Grassland vs Neutral Grassland: likely due to how each product distinguishes species composition on soils; spectral signatures vs field observations
  - Dwarf Shrub Heath vs Bog: allocation differences between the two habitats
  - Montane Habitats and coastal habitats: poorer representation in CS data, larger differences in estimates
  - Fen, Marsh and Swamp: CS 2007 vs LCM2007 differ by an order of magnitude due to mosaic nature of fen and small patch sizes; many CS fen areas map as Rough Grassland or Acid Grassland in LCM2007
- Other factors contributing to dissimilarities:
  - Differences in spatial structure (field-squarish CS vs parcel-based LCM)
  - Temporal differences and the need for multi-year imagery in LCM2007
  - Spectral variability and signature representation for certain land covers
  - Classification boundaries and MMU-related aggregation

## Discussion: interpretation of comparisons
- The Countryside Survey estimates are scaled-up field observations, while LCM2007 uses satellite imagery and a parcel-based approach; this yields different strengths and limitations.
- Grassland categories pose notable challenges due to one-to-many relationships with Broad Habitats; this motivated the use of Broad Habitat Associations (BHAs) to improve cross-product correspondences.
- LCM2007 shows high correspondence with CS 2007 for the Arable and Horticulture area in 1 km squares, but overall Broad Habitat extents differ, partly due to classification philosophy and boundary treatment.
- Fen, Marsh and Swamp estimates show substantial divergence, reflecting the complexity of mosaics and the small patch sizes typical of fen landscapes.
- The analysis suggests the value of developing Knowledge-Based Enhancements (KBEs) and potentially reclassifying certain grassland and fen components to improve alignment with field surveys.

## Implications for analysts and practical guidance
- Use KBEs to refine classifications of grassland types and montane habitats; consider aggregating grassland into a single class when comparing with field surveys to improve correspondence.
- Leverage Broad Habitat Associations to interpret CS-LCM2007 correspondences where one-to-many habitat relationships exist.
- Be cautious when using CS-based area estimates to validate or calibrate LCM2007, especially for heterogeneous or mosaic habitats like fen and montane zones.
- Recognize that different data structures (parcel-based vs field-square-based) influence area estimates and boundary delineations; spatial scale and MMU choices will affect comparability.

## Data products and access
- Vector product: parcel-based land cover with 10 processing attributes, including Construct history and KBEs.
- Raster products:
  - 25 m resolution raster with 23 LCM2007 classes
  - 1 km resolution rasters with either:
    - Percentage cover per class (UK-wide and country subsets)
    - Dominant class per pixel
- Access:
  - 1 km raster data via CEH Information Gateway
  - Full vector and 25 m raster data available on request under licence from CEH (licence fees may apply)
  - Additional details and licensing information available on CEH websites

## Broader context and validation
- LCM2007 provides coast-to-coast coverage and integrates with national cartography, enabling consistent national monitoring and change detection.
- The report emphasizes that LCM2007 and CS complement each other: CS provides ground-truth, high-detail field observations; LCM2007 offers scalable, consistent national coverage and supports policy-relevant analyses across sectors.
- The Bespoke validation approach highlights the value of parcel-level metadata (KBEs applied, ProbList of top spectral variants) to assess the quality and suitability of classifications for specific study areas.