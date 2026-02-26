# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Purpose and scope
- Presents three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019.
- All maps use 21 UKCEH Land Cover Classes derived from UK Biodiversity Action Plan (BAP) Broad Habitats, aligned with LCM2015 for consistency.
- Production is automatic (Bootstrap Training + Random Forest) to enable rapid, annual updates.
- Aims to help users classify land cover and understand changes over time; includes production decisions, validation, and future plans.

## Data products and structure
- Datasets included for each year (GB and NI): 20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, plus 1km products.
- 1km products: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), and Dominant Aggregate Cover (1 band).
- Total datasets: 42 (GB and NI duplicates across years and product types).
- Core datasets:
  - 20m Classified Pixels: a new layer per year with per-pixel class and a per-pixel confidence score (0–100).
  - Land Parcels: vector framework tying 20m pixels to land parcels with attributes such as hist, mode, purity, conf, stdev, and n.
  - 25m Rasterised Land Parcels: rasterized summary with 3 bands (mode, conf, purity).
  - 1km Raster products: aggregated metrics per 1km grid (percent cover, percent aggregate cover, dominant/dominant aggregate).
- Spatial framework and extents:
  - Great Britain and Northern Ireland, with GB using British National Grid (EPSG:27700) and NI using Irish Transverse Mercator (TM75, EPSG:29903).
  - Land Parcels have a minimum mapped unit of ~0.5 hectares; designed to represent discrete real-world units (fields, parks, urban areas, etc.).
- Data governance and terminology:
  - Updated attribute naming in line with production software; preserved core information such as gid for longitudinal comparisons within the LCM2017–2019 series.
  - Visual guidance and color mappings provided to support interpretation (RGB recipe in Appendix 3).

## Production methodology
- Bootstrap Training:
  - Fully automatic training process that reuses historic maps as training data to avoid new field collection.
  - Bootstrap samples come from UKCEH LCM2015, which was itself bootstrap-derived from historic data (1990–2007) with manual observations.
  - For each year, land parcels with ≥99% purity from LCM2015 were used to generate training samples.
  - Future Bootstraps planned to use majority signals across multiple years (e.g., 2017–2019 for 2020; 2018–2020 for 2021).
- Random Forest (RF) classification:
  - RF classifier trained with 10,000 samples per class per tile, using balanced sampling to avoid dominance by common classes.
  - 36-band spectral data per Classification Scene plus 10 Context Layers (e.g., terrain, proximity to features) for GB; 7 additional context layers used in NI.
- Data inputs:
  - Seasonal Composite Images: Sentinel-2 TOA reflectance, median per season, produced from Google Earth Engine.
  - Seasonal Classification Scenes: 46-band GB scenes (spectral bands + context layers); about 74 overlapping scenes classified to produce full GB coverage; NI used a single 43-band scene per year.
  - Context rasters help resolve spectral confusion (e.g., distance to coast, roads, buildings; terrain features).
- Classification approach and validation:
  - Each Classification Scene is trained and classified independently; overlaps resolved by visual inspection to choose best results (manual judgement limited).
  - No manual corrections applied this round to maintain annual production speed.
- Land Parcel Spatial Framework:
  - Parcels derived from a generalised national framework, aligned with previous LCMs; parcel identifiers (gid) do not match LCM2015 but can be compared via spatial overlap.
  - Land Parcels provide a structured way to summarize 20m pixel classifications.

## Validation and results
- Validation dataset: GB countryside survey 2019 data, open-source National Forest Inventory, IACS, plus bespoke LCM validation points (22,325 points).
- Accuracy outcomes (UK scale, 21 classes):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Notes:
  - Validation used the same points across all three products; references to sources with some class-definition differences require conversions to UKCEH classes.
  - Overall accuracy around 80% is considered strong for an automatic, nationwide product; authors anticipate improvements as methods mature.

## Metadata, openness, and governance
- Comprehensive accompanying text (appendices) detailing class relationships, telemetry, and metadata considerations.
- The 20m Classified Pixels include per-pixel confidence (probability of membership) to support uncertainty analyses.
- The LCM framework is designed to be repeatable and comparable over time, with explicit notes about changes in data structures and parcel identifiers to aid users in longitudinal analyses.

## Spatial scales and data structure for monitoring
- Multi-scale outputs suitable for policy and environmental health monitoring:
  - Fine-grained 20m pixel data preserves landscape details and micro-habitats.
  - 25m Land Parcels and 1km raster products enable broader-scale trend analyses and integration with other regional datasets.
- Consistent 21-class structure across years facilitates change detection and trend assessment for environmental health indicators.
- Availability of both GB-wide and NI-specific products supports regional monitoring and governance.

## Use for monitoring environmental health and policy
- Enables rapid assessment of land cover change and spatial distribution of habitats and anthropogenic features over time.
- Bootstrap Training minimizes reliance on field campaigns, supporting timely policy evaluation and scenario testing.
- Error characteristics are acknowledged (class-specific confusions; some peatland and upland habitats challenging to separate), informing interpretation and uncertainty assessments.
- The 1km products provide a scalable basis for integration with climate, hydrology, and biodiversity monitoring frameworks.

## Appendices and technical details (highlights)
- Appendix 1–2: Detailed notes on UKCEH Land Cover Classes and their relationship to UK BAP Broad Habitats; guidance on how spectral detection aligns with habitat concepts.
- Appendix 3: Recommended RGB color mapping for displaying Land Cover Classes.
- Appendix 5: Full list of datasets by year and product type, including GB and NI versions and the naming conventions used.

## Future plans and limitations
- Annual release ongoing (LCMs planned for subsequent years); exploration of expanding satellite inputs (e.g., Sentinel-1 radar) and additional data sources to fill seasonal gaps.
- Potential to increase resolution of contextual and thematic classes; consideration of refining upland peatland classifications with new training data.
- Acknowledges limitations in data availability, metadata depth, and cross-year parcel identifiers; continues to refine validation resources and data sharing practices.
- Continues to balance automated production speed with validation and user needs for transparency and reproducibility.