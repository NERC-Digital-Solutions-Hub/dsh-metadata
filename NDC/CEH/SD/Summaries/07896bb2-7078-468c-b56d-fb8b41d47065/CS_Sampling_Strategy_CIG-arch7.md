# The Sampling Strategy for Countryside Survey (up to 2007)

- A historical, map-based framework (ITE Land Classification) used to stratify field sampling across Great Britain for Countryside Survey, enabling robust, change-detecting habitat and land-use estimates.
- Core idea: stratified, random sampling of 1-km squares within land classes to ensure representative coverage and enable national/regional estimates.

## Key concepts and data products for GIS

- Land Classification as spatial stratification: groups of land with similar environmental attributes (e.g., altitude, geology, climate) used to allocate samples and estimate habitat areas.
- 1-km square sampling unit (with centre squares classified, plus surrounding squares for context) to balance survey efficiency and ecological detail.
- Land Classes mapped and described; successive surveys expanded classification detail and country-specific reporting.
- Outputs include class maps, sample-square locations, and national estimates of habitat areas by class and country.

## Evolution of the ITE Land Classification and sampling framework

- The beginning (early 1970s–1978)
  - ISA (Indicator Species Analysis) applied to vegetation data; environment-based classification extended to land areas.
  - 1-km squares used as sample units; 1228 centre squares classified, with 4 surrounding squares assigned by the ISA key (total 6039 km squares considered).
  - Eight samples per land class planned (total 256 squares) for the first GB survey.
- 1984 (second field survey)
  - Sampling increased to 12 squares per land class (total 384) to better capture variability; eight squares per class from CS1978 retained.
- 1990 (All Squares Land Classification; third field survey)
  - Land Classification extended to cover every square in GB (revised, more comprehensive framework); 508 squares surveyed.
  - Lands and habitat features recorded from the 1984 survey plus a repeat of 1978 quadrats.
  - First linking of Land Classification with a national land-cover product (land cover map from satellite data).
- 1998 (Revised Land Classification; fourth field survey)
  - A more detailed GB-wide classification introduced to enable separate Scottish reporting; number of Land Classes increased to 40.
  - National estimates still based on the revised GB-wide framework.
- 2007 (Revised Land Classification; fifth field survey)
  - Devolution-driven needs for Wales-only reporting led to further adjustments.
  - Wales sub-divided into country-unit versions of classes (creating 5 additional Welsh classes: 5w, 6w, 7w, 15w, 18w), increasing strata to 45.
  - Additional squares allocated in Wales to ensure adequate representation; some English classes (5e, 15e) reduced to 4 squares per class due to precision considerations.
  - England Wales Scotland maps updated to reflect the new sampling framework.

## Country-specific estimates and sampling adjustments

- Separate country estimates (England with Wales and Scotland) introduced to reflect policy and devolution needs.
- Class subdivisions and aggregations used to create 40 strata (and later 45 with Welsh subdivisions) to ensure representation within each country unit.
- Isle of Man: removed from Wales/England estimates; replaced with new squares in England.
- Wales uplands module (CS2000): added 30 squares in upland classes to improve habitat estimates in uplands and ensure robust Wales-based results.

## Sampling numbers and framework details (high-level)

- CS1978: 256 squares sampled (8 per class) across 32 Land Classes.
- CS1984: 384 squares sampled (12 per class for broader coverage).
- CS1990: 508 squares sampled; all GB squares classified; support for regional and local estimates.
- CS2000: expanded framework enabling England & Wales and Scotland estimates; 40 strata; additional squares added to correct class representation; upland module added.
- CS2007: Wales-specific refinements; 45 strata; 43 additional Welsh squares; updated class map for England/Wales/Scotland; maintained precision considerations in England for two smaller classes.

## Practical implications for GIS and data users

- Land Classification maps underpin sampling design and national estimates; changes in classification over time affect cross-survey comparability.
- Use of country-unit classifications enables policy-relevant reporting (England & Wales vs Scotland; later Wales-only reporting).
- Data interoperability considerations: alignment between original (1990) and revised classifications; some reclassification occurred between surveys, impacting direct comparisons unless aligned to a common framework.
- Upland and Wales-focused modules improve statistical accuracy where coverage would otherwise be sparse.

## Notes on national estimates and consistency

- The 2006 scoping study cautions that changing the basic classification used for national estimates affects consistency of stock estimates; two approaches exist:
  - Use the latest classification (country-specific classifications) for current surveys.
  - Use the original 1990 classification for cross-survey consistency.
- Table comparisons show differing sample sizes per class across surveys, reflecting evolving classifications and country-based reporting needs.

## Acknowledgements and references (high level)

- Acknowledged contributions from researchers, statisticians, and institutions (DETR, CEH, ITE) across the survey's evolution.
- Comprehensive bibliography accompanies the document, detailing methodological and applied works on land classification and Countryside Survey results.

## Summary takeaway for GIS specialists

- The Sampling Strategy for Countryside Survey (up to 2007) documents a long-running, GIS-centric approach to environmental stratification in Britain, built on the ITE Land Classification.
- It explains how land classes were defined, how samples were allocated within and across countries, and how classifications evolved to support Wales- and Scotland-specific reporting.
- The strategy provides the spatial basis for estimating habitat extent and change across GB, linking field surveys to map-based data products and enabling policy-relevant analyses at national and sub-national levels.