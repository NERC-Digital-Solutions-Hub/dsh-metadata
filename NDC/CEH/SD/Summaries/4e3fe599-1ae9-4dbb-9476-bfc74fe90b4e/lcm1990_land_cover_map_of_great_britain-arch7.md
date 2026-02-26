# Land Cover Map of Great Britain (1990)

- Digital dataset classifying land cover into 25 classes at 25m resolution, derived from Landsat 5 Thematic Mapper imagery.
- Provides a nationwide, first digital map of land cover with accuracy checked against ground surveys; supports planning, ecology, conservation, forestry, environmental assessment, urban planning, transport, and telecommunications.

## What the data contains and how it can be used

- 25 target classes include sea/inland water, bare ground, arable land, pastures and meadows, rough grass, grass heath, bracken, shrubs, deciduous and coniferous woodlands, bogs, urban and suburban development, and inland bare ground.
- Applications examples: detect land cover change, landscape management, bracken mapping for health studies, motorway environmental assessments, telecommunication planning, and various environmental and planning analyses.
- Data can be licensed for any area and supplied under different licensing forms to fit user needs.

## Classification approach and accuracy

- Method: supervised maximum likelihood classification of Landsat TM data, with a 25m grid and 25 target classes (plus an unclassified category). Combined summer and winter imagery significantly improved accuracy over single-date analyses.
- Reported results:
  - Approximately 88% of Britain classified; 12% from single-date data; minimal cloud cover (0.4% of Britain obscured on both dates).
  - Registration accuracy: Landsat-derived maps aligned with vector field maps with average displacement ~0.8 pixels (20 m); most squares needed no shift or only 1–2 pixel shifts.
- Accuracy discussion:
  - Ground-truth data are limited; class definitions vary, which affects comparisons.
  - Between field surveys and Landsat classification, average correspondence around 67% when accounting for definitional differences.
  - Boundary/mixed pixels contribute substantial error (about 40% of pixels), reducing to ~71% when boundary pixels are excluded.
  - Time-based changes (e.g., pasture ploughed) can affect accuracy; allowing for such changes, overall correspondence rises to about 76–82%.
  - A realistic, general accuracy is considered to be in the 80–85% range, acknowledging regional and class-definition variations.

## Spatial resolution, registration, and map limits

- Resolution: 25 m; features are detectable down to about 1 ha in practice, with smaller elements possible if spectral signatures are strong.
- Spatial accuracy: good overall, with some spatial displacement possible; mixed boundary pixels are a major source of error.
- Minimum map-able area: effectively around 1 ha in practice; some as small as 0.125 ha (2 pixels) can be detected depending on spectral contrast.

## Stand-alone datasets and data structure

- Stand-alone datasets are available:
  - 25 m resolution dataset: single layer with values 0–25 for each 25 m cell (0 = unclassified in 25 m data).
  - 1 km resolution dataset: 17 key-class layers, each cell containing the percentage (0–100) of that key class within the 1 km cell.
- 1 km data organization: each of the 17 layers corresponds to a key class (A, B, …, Q); percentages are integers.
- 25 m vs 1 km: 25 m data provides full 25-class detail; 1 km data provides summarized, proportion-based information for 17 key classes.
- If a subset of key classes is requested, the corresponding bands are provided (e.g., B, G, M, Q as bands 1, 2, 3, 4).

## Class descriptions (high-level)

- A Sea/Estuary; B Inland Water; C Coastal Bare Ground; D Saltmarsh; E Rough Pasture / Dune Grass / Grass Moor; F Pasture / Meadow / Amenity Grass; G Marsh / Rough Grass; H Grass / Shrub Heath (aggregated in 17-class output); I Shrub Heath; J Bracken; K Deciduous / Mixed Wood; L Coniferous / Evergreen Wood; M Bog (Herbaceous); N Tilled Land (Arable); O Suburban / Rural Development; P Urban Development; Q Inland Bare Ground; UNCLASSIFIED (0 in 25 m data).
- Additional nuance: regional upland vs. lowland distinctions; grassland classifications reflect management intensity and spectral separability; some classes may be aggregated in certain outputs (e.g., 17-class 1 km data).

## Data usage notes and limitations

- The product maps land cover (not necessarily land use); viewing depends on dominant cover at imaging time.
- Accuracy figures are approximate and depend on class definitions, data resolution, and temporal differences; local discrepancies may occur.
- A quality assessment process (Data Assessment Report) is provided to capture user feedback and best practices.

## Licensing, access, and data delivery

- Licensing options range from single-user research licences to corporate multi-user, multi-site licences.
- Data charges are divided into commercial, non-commercial, and research bands; UK academics may receive reductions.
- Licences can be tailored; data can be provided for a specified geographic area, with 25 m or 1 km resolution.
- Contact: CEH Wallingford, Land Cover Map Sales; tel: +44 (0)1491 692315; email: spatialdata@ceh.ac.uk.

## Related information and updates

- Land Cover Map 2000 is available as an updated product with sample data and download options via the Countryside Information System.
- Appendix highlights include color mappings (Appendix 2) to ensure consistent display across platforms.

## Practical considerations for GIS workflows

- Use 25 m data for detailed, category-specific mapping (A–Q) and for custom aggregations within GIS.
- Use 1 km data to analyze broad land-cover proportions within grid cells and to compare across large extents.
- Account for potential mis-registration and mixed boundary pixels; consider applying boundary-exclusion approaches when computing accuracy metrics.
- When integrating with other datasets, be aware of possible time lags between imagery dates and ground-truth references.