# The Sampling Strategy for Countryside Survey (up to 2007)

- An historical record of how the ITE Land Classification and Countryside Survey sampling framework evolved from 1978 to 2007, linking field surveys to map-based classifications and to country-specific outputs.

## Core concepts and aims for GIS-focused work

- Use stratified, random sampling to ensure representative spatial coverage across Britain.
- Employ the ITE Land Classification as the stratification framework to group land into homogeneous ecological units.
- Link field survey data to land classes for national and, later, country-specific estimates.
- Provide a basis for map- and GIS-ready visualisations of habitat areas and changes over time.

## Evolution of the ITE Land Classification (why and how)

- Origin (early 1970s): Grounded in Quadrat-based vegetation classification scaled to 1 km squares; developed to classify land by environmental attributes (altitude, geology, climate, etc.) using Indicator Species Analysis.
- 1978 (first Countryside Survey): Created a gridded, stratified, random sampling framework from 32 Land Classes derived from a core set of classified squares; eight samples per class were selected, yielding 256 squares, plus surrounding squares for classification context.
- 1984: Sampling expanded to 12 squares per class (384 total); eight original squares retained; refinement focused on land-use and landscape features.
- 1990: All GB 1 km squares incorporated into a revised Land Classification; 508 squares surveyed; introduction of the first Land Cover Map linkage; data included repeat vegetation quadrats.
- 1998: Land Classification extended to cover all GB squares with surrogate environmental factors; classification expanded to 40 classes to improve regional applicability; sampling framework adapted for regional/local estimates.
- 2000: CS2000 introduced separate country estimates (England with Wales, Scotland); Land Classes were subdivided to create country-unit versions; 40 strata were maintained but redistributed to reflect country boundaries; additional upland habitat module added for England and Wales to improve upland estimates.
- 2007: Wales-focused reporting led to Welsh-specific class subdivisions (creating five new Welsh classes: 5w, 6w, 7w, 15w, 18w) and an increase to 45 strata. Wales received 43 additional squares; some English classes (5e, 15e) were reduced to 4 squares per class. An upland module remained, with additional squares for Wales. Figures illustrate the revised England-Wales-Scotland classifications and sample distributions.

## Sampling framework by survey year (key changes and numbers)

- 1978 Countryside Survey (CS1978)
  - Land Classification: 32 classes
  - Sampling: 8 samples per class (256 total squares)
  - Coverage: Center squares of a 15 x 15 km grid; 4 surrounding squares allocated to classes
  - Purpose: National habitat area estimates based on mean per-square habitat area within each class

- 1984 Countryside Survey (CS1984)
  - Sampling: 12 squares per land class (384 total)
  - Previous 8 squares re-visited; larger emphasis on land use and landscape features

- 1990 Countryside Survey (CS1990)
  - Land Classification updated to include data for all GB 1 km squares
  - Sampling: 508 squares surveyed
  - Output: Land Cover Map linked results; continued field observations with repeat quadrats

- 2000 Countryside Survey (CS2000)
  - New Land Classification to support country-unit estimates (England with Wales, Scotland)
  - Stratification expanded from 32 to 40 strata (with subdivisions and aggregations to fit country units)
  - Adjustments to ensure adequate representation: 19 additional squares to England & Wales, plus 11 more to balance England and Wales sampling rates; Isle of Man samples removed and replaced
  - Upland module: an additional 30 squares placed in uplands and marginal uplands to boost upland habitat estimates

- 2007 Countryside Survey (CS2007)
  - Welsh-only reporting needs drive changes: five Welsh country-unit sub-classes created (5w, 6w, 7w, 15w, 18w)
  - Total strata increased to 45; 43 Welsh additional squares added to ensure representation
  - Some English classes (5e, 15e) reduced to 4 squares per class
  - Wales becomes most intensively sampled country; England and Scotland distributions adjusted accordingly
  - Wales-specific revised class maps (England with Wales and Scotland) and sample square maps provided
  - Table 3 (summary) details numbers of squares per class for CS2007

## How national estimates are derived (for GIS analysts)

- Core method: For each Land Class, multiply the mean habitat area per square by the total area of that class, then aggregate across classes to obtain national estimates.
- Country-unit approach (CS2000 onward): Classify GB squares into country-specific units (England with Wales; Scotland) to produce country-level estimates; sub-divide and, where necessary, aggregate classes within each country to maintain adequate representation.
- Upland module: Adds targeted sampling in upland classes to improve precision of upland habitat estimates in England and Wales.
- Consistency note: Changing the Land Classification across surveys affects the comparability of national stock estimates; two approaches exist:
  - Use the latest classification for within-survey national estimates (preferred for consistency of within-survey outputs)
  - Use the original classification for cross-survey consistency (more uniform across different surveys)

## Additional notes important for GIS work

- The Land Classification evolution affects how map data are attributed; practitioners must account for reclassification when aligning historical maps with current outputs.
- The 1 km square framework underpins spatial aggregation; understanding the strata and their geographic distribution is essential for accurate mapping of habitat areas and changes over time.
- Wales-specific and upland modules emphasize the need for country- and habitat-specific maps and change detection, important for policy-relevant GIS applications.
- Figures and tables (e.g., land class maps, sample distribution maps, and Table 3) document the spatial and numerical layout of samples, aiding reproducibility and GIS data layering.

## Acknowledgements and references

- Acknowledges statistical guidance and contributions from multiple collaborators across the DETR, CEH, and ITE communities.
- Includes a detailed bibliography and appendices that outline the historical development and methodological decisions behind the ITE Land Classification and Countryside Survey sampling strategy.