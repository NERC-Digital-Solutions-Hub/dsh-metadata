# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Overview
  - User guide accompanying the release of LCM2017, LCM2018 and LCM2019.
  - Maps represent 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) and match the LCM2015 framework.
  - Automatic production using Bootstrap Training plus Random Forest; aims to enable annual UK-wide land cover maps.
  - Validation and visual checks indicate maps are of similar quality to LCM2015, with no manual corrections this cycle.

- Data products and structure
  - 20m Classified Pixels
    - New in this release; RF classification results from Sentinel-2 seasonal composites (TOA reflectance).
    - 2-band, 8-bit rasters: band 1 = most likely class, band 2 = confidence (0–100).
    - Preserves fine detail (no generalisation by Land Parcel Framework).
  - Land Parcels
    - Attributes derived by intersecting 20m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Key fields: gid (parcel ID), _hist (class frequencies within parcel as tuples), _mode (dominant class), _purity, _conf (mean per-pixel membership probability), _stdev, _n (number of 20m pixels in parcel).
    - Note: new products use different gid values than LCM2015; parcel comparison across years uses gid only.
  - 25m Rasterised Land Parcels
    - Rasterised version of Land Parcels (25m pixels) with 3 bands: _mode, _conf, _purity.
  - 1km Raster Products
    - 1km Percent Cover: 21-band raster (per class percentages in each 1km cell).
    - 1km Percent Aggregate Cover: 10-band raster (per UKCEH Aggregate Class).
    - 1km Dominant Cover: single-band raster (dominant class per 1km cell).
    - 1km Dominant Aggregate Cover: single-band raster (dominant Aggregate Class per 1km cell).

- Datasets and extents
  - For each year (2017–2019) and region (Great Britain, Northern Ireland), 42 datasets in total (GB and NI, multiple products).
  - GB extent: Great Britain coordinate system is British National Grid (EPSG:27700).
  - NI extent: Northern Ireland grid (TM75 Irish Grid, EPSG:29903).
  - Pixel and grid specifics:
    - Classified Pixels: 20m resolution.
    - Land Parcels: derived from 20m pixels using the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
    - 25m Rasterised Parcels: 25m grid aligned to GB/N.I. origins.
    - 1km rasters: aggregated from 25m parcels to 1km cells.

- Classification methodology
  - Bootstrap Training: uses historic LCM2015 as the training base; selects parcels with ≥99% purity to bootstrap training data.
  - Random Forest: trained on balanced samples (10,000 per class) across 36-band seasonal composites plus 10 context rasters; outputs 21-class classification.
  - Seasonal composites: Sentinel-2 TOA reflectance, median per season (winter, spring, summer, autumn), 20m resolution.
  - Context rasters (GB 20m): terrain (Height, Aspect, Slope), proximity masks (buildings, roads, sea, freshwater, foreshore, tidal water, woodland).
  - Seasonal composites generated via Google Earth Engine (GEE). SR (surface reflectance) data were considered but TOA was chosen for this release due to lack of observed improvement.
  - Classification Scenes: GB used overlapping 100x100 km tiles; NI used a single 43-band scene per year. Each scene trained and classified independently; some regions receive multiple classifications due to overlaps.

- UKCEH Land Parcel Spatial Framework
  - Maintains ~0.5 ha MMU; parcel data are reused with reordering and new indices for faster processing.
  - gid values differ from LCM2015; parcel comparisons across 2017–2019 rely on gid.
  - Spatial framework enables change detection over time and provides a fixed structure for summarising 20m pixels.

- Class definitions and relationships
  - 21 UKCEH Land Cover Classes aligned with UK BAP Broad Habitats (not identical to BAP; some refinements applied for detectability via remote sensing).
  - Appendix 1/2 provide detailed class notes and BAP definitions; Table 1 maps UKCEH classes to BAP Broad Habitats and assigns internal identifiers.
  - Appendix 3 provides a recommended RGB color recipe for displaying the classes.

- Validation and quality
  - UK-scale validation used 22,325 points from GB countryside survey, National Forest Inventory, IACS, and expert interpretation.
  - Overall accuracy (approx.): LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
  - Validation points were sourced from datasets with different purposes; some class mappings required subjective conversions.
  - No manual accuracy corrections were applied in this release; visual checks and formal validation were performed.

- Changes and considerations since LCM2015
  - Introduction of 20m Classified Pixels (new in 2017–2019) to preserve landscape detail.
  - Removal of the Composite attribute (no longer relevant with seamless GEE composites).
  - Land Parcel identifiers (gid) changed due to framework adjustments; cross-year parcel matching uses gid only for LCM2017–2019 comparisons.
  - Some attributes were redefined or renamed to align with production software conventions (e.g., _hist format, _conf scaling).

- Appendices and further information
  - Appendix 1–2: UKCEH Land Cover Class notes and detailed BAP Broad Habitat definitions.
  - Appendix 5: Full list of datasets by year and product.
  - The document notes ongoing development and future plans, including exploring higher-resolution or additional optical/SAR data to fill gaps and improve accuracy.

- Practical guidance for GIS specialists
  - Choose product granularity based on need:
    - 20m Classified Pixels: highest detail, suitable for fine-scale mapping and change detection.
    - 25m Land Parcels: parcel-based summaries with rich per-parcel attributes.
    - 1km Percent/Dominant products: efficient for regional analyses and coarser-scale mapping.
  - Be aware of parcel identifier changes when comparing with LCM2015; use gid for cross-year comparisons.
  - Use the 20m pixel confidence band (_conf) to assess per-pixel classification certainty; leverage _purity and _hist for parcel-level interpretation.
  - Leverage context rasters to reduce spectral confusion between spectrally similar classes (e.g., arable vs. grassland, freshwater vs. saltwater in coastal zones).
  - For change detection and time-series analyses, rely on Bootstrap Training’s majority signal across years to maintain consistency while tolerating year-to-year classification noise.

- Notable limitations
  - Some inter-class confusion remains (as shown in confusion matrices); accuracy varies by class (e.g., higher for common classes like Urban, lower for fine-grained upland vegetation).
  - Tidal and coastal water classes (Saltwater, Freshwater, Saltmarsh) can exhibit confusion in coastal contexts; coastal context rasters mitigate but do not eliminate errors.
  - Some high-detail classes (e.g., Heather vs. Heather Grassland or Bog) show variable producer’s/user’s accuracy; further training data could improve separability.

- Access and further reading
  - Primary methodologies and datasets are described across the document, with Appendices detailing class relations, color schemes, and validation results.
  - For more information, refer to the datasets and appendices listed in Appendix 5 and the project references cited within the guide.