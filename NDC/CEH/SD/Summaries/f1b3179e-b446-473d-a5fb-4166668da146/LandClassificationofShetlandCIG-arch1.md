# Land Classification of Shetland (1974)

- A stratified sampling framework for assessing Shetland’s terrestrial habitats and vegetation, based on environmental characteristics to support ecological surveying and status/value assessments of plant and animal communities.
- Geographic Coverage: Shetland Islands, Scotland; Time period: 1974.
- Data Format/Projection/Resolution: ESRI Shapefile; OSGB 1936; 1 km grid cells.
- Core output: 16 environmental strata used to guide sampling across the land area; later used as a basis for vegetation and habitat analysis.

## Stratification and Sampling Methodology

- Approach: Initial stratification into areas with similar environmental characteristics (Land Classification), followed by random sampling within strata; supplemented by specialist surveys for bryophytes and lichens and key vegetation/habitat types.
- Basis: Maps and aerial photographs used to classify landform and habitat; aerials were not initially available, so stratification relied on map-derived types and later used aerials for validation and detailed vegetation mapping.
- Sampling Units: 1 km grid squares chosen as fixed, referenceable units across scales.
- Data Collected: Approximately 1000 plots of 200 m² surveyed for plant species, soils, habitat types, and major biota; 150 attributes used for stratification; 18 geological attributes recorded from the quarter-inch Geological map.
- Analytical Methods: Indicator species analysis to relate map attributes to vegetation patterns; methods described by Hill et al. (1973, 1975).

## Strata (Overview)

- Strata 1-4: Coastal, few rivers, >80% land, relatively gentle terrain.
- Strata 5-8: Coastal with more sea and steeper slopes; more headlands and sea cliffs; more rivers entering the sea.
- Strata 9-12: High-altitude inland group with 600–900 ft hills; few small water bodies; major rock likely gneiss.
- Strata 13-16: Lower, undulating inland with extensive peat and many freshwater lochans; hills around ~300 ft; rock more commonly Old Red Sandstone.

## Dataset Structure

- Core Columns: 
  - OBJECTID: Unique row identifier
  - STRATA: Strata number (1–16)
- Geometry: Shape (default geometry)
- Coverage Details: 2046 1 km squares in Shetland containing land

## Related Datasets and Publications

- Related datasets (1974): 
  - Shetland Freshwater Survey 1974
  - Shetland Coastal Survey 1974
  - Shetland Vegetation Survey 1974
  - ITE Land Classification of Great Britain (2007)
- Key References:
  - Bunce R.G.H. & Shaw M.W. (1973). A Standardized Procedure for Ecological Survey.
  - Bunce R.G.H. (1974). Shetland Vegetation Survey: Handbook of Field Methods.
  - Bunce R.G.H. (1975). The Terrestrial Survey of Shetland.
  - Milner C. (1975). Shetland project monitoring report.
  - Hill M.O. (1973). Reciprocal averaging: eigenvector ordination.
  - Hill M.O., Bunce R.G.H. & Shaw M.W. (1975). Indicator species analysis.
  - Metzger M.J. et al. (2005). Climatic stratification of Europe.
  - Bunce R.G.H. et al. (1996). Land classification for strategic ecological survey.
  - Bunce R.G.H. et al. (2007). ITE Land Classification of Great Britain.

## Origin and Context

- Originator: R.G.H. Bunce, Institute of Terrestrial Ecology, Merlewood Research Station, Grange over Sands, Cumbria.
- Background: A comprehensive survey of Shetland’s terrestrial habitats and vegetation conducted in 1974 to support status/value assessments and broader ecological research.

## Notable Insights and Implications

- Main finding: The sea dominates Shetland’s geography, with complex interactions between land and sea affecting vegetation; shelter and exposure influence habitat types (e.g., maritime grassland vs. blanket bog) in ways not easily inferred from maps alone.
- Utility: The 16-strata framework provides a robust basis for stratified ecological sampling, cross-dataset comparisons, and landscape-level habitat modelling, linking geology and geography to ecological patterns.