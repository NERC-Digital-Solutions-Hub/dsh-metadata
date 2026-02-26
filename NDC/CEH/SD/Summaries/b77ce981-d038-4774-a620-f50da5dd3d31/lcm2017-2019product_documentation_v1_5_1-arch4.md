# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- The document is a user guide accompanying the release of three UKCEH Land Cover Maps (LCMs) for 2017, 2018 and 2019, describing their content, production, validation and planned use.
- LCMs produce 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats and are intended to enable rapid, annual mapping of land cover across the UK with quality controls and clear metadata.
- Production uses an automated Bootstrap Training approach with Random Forest classification, designed to remove the need for labor-intensive manual data gathering while enabling yearly updates.
- The release emphasizes informing users how to apply the data, understand production decisions, and anticipate limitations and future improvements.

## Purpose and Content

- Extends the UKCEH LCM series with LCM2017, LCM2018 and LCM2019, each mapping 21 UKCEH Land Cover Classes (close to the 2015 scheme) derived from BAP Broad Habitats definitions.
- Aim to release a new LCM annually, balancing rapid production with validation to maintain comparable quality.

## Data Products and Structure

- Total datasets: 42 datasets across three years, with a set of 14 datasets per year (GB and NI counterparts for each product).
- For each year:
  - 20m Classified Pixels (GB and NI)
  - Land Parcels (GB and NI)
  - 25m Rasterised Land Parcels (GB and NI)
  - 1km Dominant Cover (GB and NI)
  - 1km Dominant Aggregate Cover (GB and NI)
  - 1km Percent Cover (GB and NI)
  - 1km Percent Aggregate Cover (GB and NI)
- 20m Classified Pixels:
  - New addition: 2-band 8-bit rasters. Band 1 = most likely UKCEH Land Cover Class; Band 2 = classifier confidence (0–100).
  - Preserves fine landscape features; not generalized by the Land Parcel Spatial Framework.
- Land Parcels:
  - Attributes include gid, _hist (histogram of class frequencies within the parcel), _mode (dominant class), _purity, _conf (mean class membership probability), _stdev, _n (number of 20m pixels).
  - Attribute names have been updated to align with production software; some history attributes were simplified.
- 25m Rasterised Land Parcels:
  - 3-band raster: band1 = _mode, band2 = _conf, band3 = _purity.
- 1km Raster Datasets (aggregations by 1km grid):
  - 1km Percent Cover: 21-band raster (percent cover per class).
  - 1km Percent Aggregate Cover: 10-band raster (percent cover per UKCEH Aggregate Class).
  - 1km Dominant Cover: 1-band raster (dominant class per 1km cell).
  - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class per 1km cell).
- Seasonal Composite Images and Classification Scenes:
  - Seasonal composites derived from Sentinel-2 imagery (TOA reflectance, resampled to 20m) for winter, spring, summer, autumn.
  - 9 Sentinel-2 bands used; some seasons may have gaps due to cloud;-treated with RF tolerance to incomplete data.
  - GB Classification Scenes: 100x100 km tiles, total of 74 overlapping scenes; NI: single 43-band scene per year.
- Context Rasters:
  - 20m context layers to help disambiguate spectrally similar classes (GB and NI have different context sets, including terrain, proximity to buildings/roads/coast, water, urban/foreshore masks, etc.).
- UKCEH Land Parcel Spatial Framework:
  - Uses to summarise 20m Classified Pixels by land parcels; minimum mapping unit ~0.5 ha.
  - Parcel gid values differ from LCM2015 due to data organisation; comparisons across years should use gid (LCM2017–2019) rather than LCM2015 parcel identifiers.
- Display and classification outputs:
  - Appendix 3 provides an RGB recipe for display of the 21 Land Cover Classes.
  - Datasets are 8-bit rasters with explicit extents and grid alignments (GB: British National Grid; NI: Irish Grid).

## Production, Methodology and Validation

- Bootstrap Training:
  - Fully automatic training using historic LCM data (starting from LCM2015) to generate labeled training observations.
  - Bootstrap Training selects land parcels with high purity (≥99% from LCM2015) to train the RF classifier; aims to capture majority signal while tolerating smaller shifts over time.
  - Future plans suggest bootstrap sampling across multiple years (e.g., 2017–2019 majority) for subsequent maps.
- Random Forest Classification:
  - Training uses balanced sampling across classes (10,000 samples per class per training run) to avoid dominance by common classes.
  - Production software combines Weka with PostGIS and GDAL; open-source components.
- Validation and Accuracy:
  - UK-scale validation performed against 22,325 points from GB countryside survey data, National Forest Inventory, IACS and manual interpretation points.
  - Reported overall accuracy: LCM2017 = 78.6%, LCM2018 = 79.6%, LCM2019 = 79.4%.
  - Validation data are not perfect truth; currency and class mapping variations exist. Full validation details and confusion matrices are provided in Appendix 4.

## Production Details and Data Management

- Spatial Extent and Grids:
  - Great Britain: British National Grid (EPSG:27700); Northern Ireland: Irish Grid (EPSG:29903).
- Time-series and comparability:
  - gid values for Land Parcels are not aligned with LCM2015; cross-year parcel comparisons should use the gid present in LCM2017–2019.
- Manual Corrections:
  - The production notes state that there were no manual corrections this cycle; visual checks and formal validation were performed to ensure quality parity with LCM2015.
- Output Characteristics:
  - 20m Classified Pixels preserve detailed spatial features; subsequent layers (Land Parcels, 25m, and 1km rasters) are derived by summarising or aggregating from the 20m results.
  - 1km products illustrate how finer classifications generalize at coarser scales, with accompanying examples and figures to illustrate the generalisation effect.

## Appendices, Class Definitions and Display

- UKCEH Land Cover Classes and mapping to UK BAP Broad Habitats are described (Appendix 1) with notes on detection limits, spectral confusion, and habitat interpretations.
- Appendix 2 expands on the Biodiversity Action Plan Broad Habitats definitions.
- Appendix 3 provides recommended RGB color values for displaying each UKCEH Land Cover Class.
- Appendix 4 contains full validation tables and confusion matrices for LCM2017, LCM2018 and LCM2019, including producer’s and user’s accuracies by class.
- Appendix 5 lists the full dataset inventory and naming conventions for LCM2017, LCM2018 and LCM2019 (including GB and NI datasets for each year).

## Practical Implications for Data Leaders

- Data strategy and governance:
  - Clear, globally consistent 21-class framework with annual updates supports monitoring land-cover change and policy analysis.
  - Bootstrap Training and RF-based classification enable scalable, repeatable production with reduced manual intervention, aligning with rapid data-cycle goals.
- Data management and interoperability:
  - Multiple interoperable products (20m pixels, land parcels, 25m parcels, and 1km summaries) support diverse analyses and downstream integration.
  - Parcels-based summaries offer a structured basis for time-series comparison, though cross-year parcel IDs are not preserved for 2015 comparisons.
  - The 20m Classified Pixels layer preserves detail but requires careful handling when aggregating or dis aggregating to parcel-based products.
- Data quality and limitations:
  - Validation accuracy is approximately 79% across years, with known limitations due to spectral confusion, coarse class boundaries, and changes in data sources.
  - No manual corrections in this cycle; ongoing visual checks and formal validation are still part of the process.
  - Classification is inherently imperfect, and users should apply their own accuracy assessments for critical analyses.
- Future directions:
  - Potential expansion of input data sources (including SAR like Sentinel-1) to improve robustness, especially under cloud cover.
  - Exploration of gap-filling strategies for seasons with incomplete data and further improvements to training data through expanding Bootstrap Training datasets.

## Access and Reference

- The document provides full methodological detail, dataset descriptions, and validation results intended to inform data users, managers and analysts responsible for data governance, change detection, and longitudinal studies.
- Appendix 5 enumerates the complete dataset list per year and geography, enabling precise asset tracking and integration into organisational data catalogs.