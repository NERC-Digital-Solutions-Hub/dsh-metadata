# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

## Purpose and scope
- User guide accompanying the release of three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Maps present land cover across Great Britain and Northern Ireland using 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) with annual updates to enable rapid monitoring of land-cover change.
- Aims to help users assess environmental health measures, evaluate policy implications, and inform future decision-making.
- Acknowledges limitations: some thematic detail may be difficult to detect remotely; classification is automated with validation performed.

## Data products and structure
- Complete product suite includes multiple interconnected datasets, available for GB and NI:
  - 20m Classified Pixels: new per-pixel RF classification results with a second band indicating membership confidence (0–100). Preserves fine landscape detail by not generalising to parcels.
  - Land Parcels: parcel-based attributes derived from the 20m classified pixels, designed to reduce noise and support time-series comparisons.
  - 25m Rasterised Land Parcels: 25m rasters produced by rasterising Land Parcels; include bands for dominant class, confidence, and purity.
  - 1km Raster datasets: include 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (single band), and 1km Dominant Aggregate Cover (single band).
- Class count: 21 UKCEH Land Cover Classes (aligned with LCM2015, and broadly consistent with earlier maps); 10 UKCEH Aggregate Classes; classifications are linked to UK BAP Broad Habitats with careful note on mappings.
- Extents and formats: GB products use British National Grid; NI products use Irish Grid; datasets are provided per year (2017–2019) with a total of 42 datasets in the full release.

## Production approach and methodology
- Seasonal input: Sentinel-2 Seasonal Composite Images (TOA), one per season, created for each year and resampled to 20m resolution; includes four seasons to capture phenology.
- Contextual information: 20m Context Rasters (e.g., height, aspect, slope; distances to buildings, roads, coast, freshwater; foreshore and woodland masks) to reduce spectral confusion.
- Classification scenes and training:
  - GB: 100x100 km Classification Scenes, 36-band Seasonal Composite Images combined with 20m Context Rasters to form 46-band scenes; 74 overlapping GB scenes classified independently with an automated bootstrap approach.
  - NI: A single 43-band Classification Scene (36 spectral + 7 context layers) per year for the Northern Ireland land mass.
  - Bootstrap Training: automatic sampling from historic UKCEH maps (starting with LCM2015) to train a Random Forest classifier; forward-propagates the majority signal to subsequent maps.
- Validation and quality checks: visual checks and formal validation performed; no manual corrections were applied in these three releases to support annual updates; validation against countryside survey, National Forest Inventory, IACS, and bespoke points indicates comparable quality to previous maps.

## The UKCEH Land Parcel Spatial Framework
- Parcel-based structure: land parcels are ~0.5 ha minimum size; designed to represent discrete real-world units and reduce classification noise.
- Parcel identifiers: gid unique per framework; some changes mean LCM2017–2019 gid values do not match LCM2015; cross-comparison should use gid for linkage.
- Flexibility: framework is not mandatory; 20m Classified Pixels can be summarized with user-defined parcel structures if desired.
- Data governance and processing: minor attribute changes since LCM2015 to align with production software; attributes renamed for consistency (e.g., hist, mode, conf, purity, n-pix).

## Context, seasonal inputs, and classification details
- Seasonal Composite Details: four-season Sentinel-2 TOA reflectance, bands 2,3,4,5,6,7,8,11,12; some seasons may have cloud gaps; algorithm tolerates partial data; future work may include synthetic fills with alternative sources or SAR data.
- Context rasters (GB vs NI variations): GB uses 10 context rasters (terrain, proximity to buildings/roads/sea/freshwater, foreshore, tidal, woodland); NI uses a tailored set (terrain plus urban mask and proximity layers).
- Classification Scenes: GB uses 100x100 km tiles to form 36-band scenes; NI uses a single scene per year; overlap between scenes may yield minor differences where overlaps occur.

## Validation results and data quality
- UK-scale accuracy (compared with validation points, countryside survey, open data inventories):
  - LCM2017: about 78.6% overall correspondence
  - LCM2018: about 79.6%
  - LCM2019: about 79.4%
- Validation caveats: same validation data used across products, currency of points varies by product; conversions between historical maps and current classes introduce subjectivity.
- Overall: around 80% correspondence for the 21-class automatically produced maps; authors anticipate improvements as methods mature.

## Data product specifics and user guidance
- Dataset relationships and nomenclature: new products retain most of the LCM2015 framework but with updated attribute names and the removal of the Composite attribute (replaced by seamless Google Earth Engine composites).
- 20m Classified Pixels: provides per-pixel likelihood and class, preserving fine features; not generalised by the Land Parcel framework to retain narrow features.
- 25m Rasterised Land Parcels: provide a summary of parcel-level outputs, including mode, confidence, and purity statistics; designed to facilitate analysis at a coarser spatial scale.
- 1km products: provide area-weighted summaries (percent cover by class, dominant class, etc.) and across all 1km squares with potential rounding to 100%.
- Data accessibility: multiple datasets and formats (including 8-bit rasters for some products) designed for integration into dashboards, reports, and policy monitoring tools.

## Appendix highlights and caveats (context for policy monitoring)
- Biodiversity Action Plan (BAP) Broad Habitats: 21 classes with detailed definitions and notes on spectral detectability; highlights challenges such as upland peatland detection, linear feature mapping, and spectral confusion between similar habitats.
- Relationship mappings: Appendix explains how UKCEH Land Cover Classes relate to UK BAP Broad Habitats and to aggregate classes; some cases require careful interpretation to maintain consistency across time series.
- Color schemes and symbology: recommended color recipes and QGIS/CB-friendly files are provided for effective visualization of land-cover maps.

## Practical implications for monitoring and policy use
- Regular, annual updates enable timely tracking of land-cover change and habitat distributions to inform environmental health assessments and policy evaluation.
- The 20m Classified Pixels dataset offers high-detail inputs suitable for detection of small features and fine-scale change; 1km products facilitate broader, landscape-scale monitoring and reporting.
- Bootstrap Training and RF classification provide a scalable, automated workflow to produce national-scale land-cover maps with documented accuracy benchmarks.
- Users should be mindful of limitations due to spectral confusion, especially for certain habitat types (e.g., various grasslands, peatland-associated classes) and the need to interpret 21-class outputs in the context of BAP Broad Habitats.
- For time-series comparisons, use gid-based parcel comparisons when possible and note changes in parcel identifiers between releases.