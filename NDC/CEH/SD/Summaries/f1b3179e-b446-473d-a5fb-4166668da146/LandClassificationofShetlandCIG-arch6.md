# Land Classification of Shetland (1974)

## Aim and scope
- Document describes a terrestrial habitat survey of the Shetland Isles (1974) that used a stratified sampling approach to classify land based on environmental characteristics.
- Part of a broader project to assess the status and value of Shetland’s plant and animal species and communities.
- Generated a framework to sample efficiently across Shetland and to support later analyses of habitat types and vegetation.

## Geography and timeframe
- Geographic coverage: Shetland Islands, Scotland.
- Timeframe: 1974 field survey; part of ongoing work described in later references.
- Data format: ESRI Shapefile with 1 km sampling units; projection OSGB 1936.

## Stratification and data structure
- Stratification approach: initial stratification using maps and aerial photographs to classify landforms, followed by stratified random sampling within strata.
- Ground sampling unit: fixed 1 km square grid (2046 squares covering land in Shetland).
- Final product: distribution into 16 environmental strata, described as four hierarchical groups with distinct geographic/biophysical characteristics.
  - Strata 1–4: Coastal, minimal rivers, relatively gentle terrain.
  - Strata 5–8: Coastal with more sea influence, steeper slopes, more headlands and cliffs.
  - Strata 9–12: High-altitude inland with 600–900 ft hills, limited water bodies, major rock type often gneiss.
  - Strata 13–16: Lower, undulating with peat and many freshwater lochs; hills around ~300 ft; rock types more varied (e.g., Old Red Sandstone).
- Data attributes:
  - Physical/geographic attributes: continuous (e.g., altitude, slope) and presence/absence features (e.g., cliffs, hill-tops).
  - 150 attributes used for map analysis (plus 18 geological attributes derived from a quarter-inch Geological map).
  - Attribute data were analyzed using indicator species analysis methods to support classification.

## Data collection and products
- Field data: nearly 1000 vegetation plots (each ~200 m²) collected using standardized methods; supplemented by specialist surveys for bryophytes and lichens, and for key habitats (cliffs, salt-marshes, shingle banks).
- Data integration: maps and later aerial photographs used to validate and refine stratification; aerials later used to produce detailed vegetation maps and to check map-derived predictions.
- Outputs:
  - A map showing the final 16 strata (for landscape-scale interpretation and sampling guidance).
  - Dataset schema includes fields such as OBJECTID, STRATA, Shape (geometry), with STRATA indicating the 1–16 strata.
  - Related datasets: Shetland Freshwater Survey (1974), Shetland Coastal Survey (1974), Shetland Vegetation Survey (1974), and later ITE Land Classification of Great Britain (2007).

## Methodological and analytical context
- Core aim was to confirm the dominance of the sea in shaping Shetland’s geography and to explore how geology relates to geography and vegetation.
- Map-based stratification was complemented by field observations to produce habitat classifications that could be cross-referenced with vegetation and geology.

## Origin and references
- Originator: R.G.H. Bunce (Institute of Terrestrial Ecology, Merlewood) with collaborators.
- Key publications and related works include:
  - Bunce & Shaw (1973): Standardized ecological survey procedure.
  - Bunce (1974, 1975): Shetland vegetation survey methods and monitoring reports.
  - Milner (1975): Shetland project monitoring report.
  - Hill (1973) and Hill, Bunce & Shaw (1975): Indicator species analysis and ordination methods.
  - Metzger et al. (2005) and Bunce et al. (2007): Later developments in European climatic stratification and the ITE Land Classification of Great Britain.
- References for further reading include project reports and subsequent land-classification frameworks.