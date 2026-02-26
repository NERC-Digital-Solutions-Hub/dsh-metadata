# Countryside Survey 2007

## Purpose and structure
- Two main components: 
  - Field Survey (habitats, vegetation, soils 0–15 cm, and freshwater)
  - Land Cover Map (satellite-based digital map to be published in 2009)
- Provides national and regional estimates of Broad Habitats and Priority Habitats, vegetation condition, soils, and freshwater features.
- 30-year data series (1978–2007) enabling analysis of long-term change; UK-wide summaries combine GB data with Northern Ireland Countryside Survey (NICS).

## Sampling design and geographic scope
- 591 sample squares of 1 km x 1 km across England, Scotland, and Wales; Northern Ireland uses 0.5 km x 0.5 km squares (NICS, 288 squares in 2007 for NI).
- Sampling stratified by Land Classes to reflect environmental gradients; some years include more squares to improve reliability.
- Acknowledges that CS results are estimates, not absolute counts; data integration across years allows change detection through statistical modeling (bootstrapping).

## Data collected and habitat classification
- Broad Habitats: 27 Broad Habitats (UK Biodiversity Action Plan framework) used for area estimation and change detection.
- Priority Habitats: 65 sub-classifications; some national estimates provided (e.g., Hedgerows, Ponds, Arable Field Margins) and backed to UK BAP definitions.
- Field Survey outputs include:
  - Extent and change of habitats
  - Vegetation condition within habitats
  - Landscape features (hedges, walls, ponds, trees)
- Land Cover and habitats are mapped as polygons within each 1 km square; linear features are recorded with a defined hierarchy.

## Vegetation sampling and condition metrics
- Vegetation plots: up to about 67 plots per square, recording presence and percent cover of vascular plants.
- Aggregate Classes (ACs) used to summarize vegetation condition (AC1–AC8), enabling cross-year comparison and linking plots to Broad Habitats.
- Measures of vegetation condition include depth and diversity indicators (e.g., species richness, grass-forb ratios, competitor/stress-tolerator/ruderal scores, Ellenberg-based light, fertility, pH, and moisture scores).

## Soils and freshwater sampling
- Soils (0–15 cm): pH, carbon concentration, bulk density; five soil plots per square (sample points relocated across years to avoid disturbance).
- Freshwater: headwater streams assessed for biology (macroinvertebrates, plant communities) and physical habitat (RHS) along 500 m reaches; pond surveys include plant-based condition and PSYM pond-quality metric (plant-focused in 2007).
- Pond and stream data provide baseline and change information for aquatic habitats, with a 1990–1998–2007 comparison for streams and 1996–2007 for pond-related measures.

## Data collection, management, and GIS integration
- 2007 introduced electronic data capture in the field (GIS-based mapping, GPS-enabled plotting, laptop data entry) with built-in validation and completeness checks.
- Custom GIS software developed with CEH and ESRI UK; data stored in a single geographically referenced database linking habitat polygons, vegetation plots, soils, and freshwater data.
- Field teams trained to ensure consistency; plots relocated using GPS, photographs, and notes to enable cross-year follow-up.
- Northern Ireland: NI-specific masks and land classifications used to derive Broad Habitat estimates; data integrated with GB totals for UK reporting.

## Reporting framework and interpretation
- Results reported at UK, Great Britain, and country levels; country-specific reports published separately.
- Conversion flows between Broad Habitats (1984–1998–2007) are described to show direction of change, recognizing potential mapping errors.
- Significance testing: 0.05 level as a standard, with arrows indicating direction and stars indicating level of significance; ecological importance discussed in accompanying text.
- Thresholds and masks (e.g., SNH, JNCC, Natural England, Welsh upland) used to delineate Priority Habitats and derive national estimates.

## How this maps to GIS work and data exploration
- Rich, long-running geospatial dataset: habitat polygons, vegetation plots, soils, streams, and ponds all tied in a single GIS database.
- Enables map-based visualization of habitat extent and change over time, conversion flows between habitat types, and evaluation of habitat condition across scales (plot-level to national).
- Land Cover Map (2009 release) complements ground-truth data with satellite-derived information for integrated spatial analysis and visual storytelling.
- Suitable for policy support, environmental planning, and public-facing spatial dashboards showing trends in biodiversity, landscape structure, and environmental health.