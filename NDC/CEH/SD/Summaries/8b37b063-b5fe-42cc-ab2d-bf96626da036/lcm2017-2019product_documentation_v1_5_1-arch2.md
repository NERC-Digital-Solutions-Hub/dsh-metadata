# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- UKCEH released three new national land cover maps (LCMs): LCM2017, LCM2018 and LCM2019, each representing a range of geospatial datasets built on 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
- Production is automatic, employing Bootstrap Training and Random Forest (RF) classification to enable rapid UK-wide mapping with annual updates.
- Visual checks and formal validation were performed; maps are of similar quality to LCM2015, with validation indicating around 78–80% overall accuracy at the 21-class level.

## Purpose and scope
- Provide consistent, analysable land cover data for monitoring environmental health and policy performance over time.
- Align classes with UKCEH Land Cover Classes (tied to BAP Broad Habitats) while noting distinctions between BAP Broad Habitats and UKCEH classes.
- Deliver a UK-wide, annually updated LCM series suitable for change detection and environmental monitoring.

## What is included (data products and structure)

- 20m Classified Pixels: new RF classification results for each year; per-pixel class with a second band indicating classification confidence (0–100).
- Land Parcels: derived parcel-level attributes by intersecting 20m classified pixels with a UKCEH Land Parcel Spatial Framework (~0.5 ha MMU); provides per-parcel histograms, mode, purity, confidence, and counts.
- 25m Rasterised Land Parcels: three-band rasters (dominant class, confidence, purity) for each parcel.
- 1km Raster datasets:
  - 1km Percent Cover (21-band)
  - 1km Percent Aggregate Cover (10-band)
  - 1km Dominant Cover (single-band)
  - 1km Dominant Aggregate Cover
- Datasets are generated for Great Britain (GB) in EPSG:27700 (GB National Grid) and Northern Ireland (NI) in EPSG:29903 (Irish Grid), with a total of 42 datasets (GB and NI for each year).

## How the data were produced

- Seasonal Composite Images: Sentinel-2 based, four-season TOA reflectance images (winter, spring, summer, autumn) at 20m resolution; nine bands used to form Classification Scenes; some seasons may have cloud gaps.
- Context Rasters: 20m context layers to reduce spectral confusion (e.g., height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, urban/woodland masks).
- Classification Scenes: GB classified in 100x100 km tiles (74 overlapping scenes); NI classified in a single 43-band scene per year; each scene trained independently using bootstrap training data.
- Bootstrap Training: automatic, uses historic maps to sample current satellite images; initial bootstrap for 2017–2019 constructed from LCM2015 with high-purity parcels (≥99% purity). Future bootstraps aim to use majority signals across multiple years.
- Random Forest: balanced sampling (10,000 samples per class) across training bags to produce the 20m Classified Pixels product.
- Validation: UK-wide validation against GB Countryside Survey 2019 data, National Forest Inventory, IACS, and bespoke LCM validation points (22,325 points); results:
  - LCM2017: ~78.6% overall accuracy
  - LCM2018: ~79.6% overall accuracy
  - LCM2019: ~79.4% overall accuracy
- Production approach emphasizes speed and automation; no manual region-specific corrections were applied in these releases.

## Dataset details and metadata

- 21 UKCEH Land Cover Classes (aligned with LCM2015; near match to earlier LCMs)
- Relationship notes: UK BAP Broad Habitats underpin classes; some refinements exist to balance detection via remote sensing. In several cases, sub-divisions (e.g., Heather vs Heather Grassland) reflect detection considerations and MMU constraints.
- Dataset descriptions and attributes include per-parcel histograms, modal class, purity, confidence, and pixel counts; 25m parcels retain a third band (purity) for improved confidence representation.
- See Appendix-style notes in the guide for class derivations and interpretation considerations, including upland peatland mapping limitations and coastal habitat distinctions.

## Production decisions and limitations

- Fully automatic classification: no manual corrections were applied to preserve annual timeliness; recognized that this may introduce localized misclassifications, though they are expected to be randomly distributed across years.
- TOA reflectance was preferred over surface reflectance (SR) for these products; potential future enhancements may incorporate additional optical/sensor data.
- LCM2017–2019 land parcel identifiers (gid) differ from LCM2015; cross-year parcel comparisons require spatial overlap rather than parcel-id matching.
- 0.5 ha minimum mapping unit (MMU) governs parcel delineation; some small features may be underrepresented in parcel-based outputs but preserved in 20m classified pixels.

## Spatial framework and time-series considerations

- UKCEH Land Parcel Spatial Framework provides a consistent structure for Change Detection, though parcel IDs change between releases; comparisons across years should rely on spatial overlap rather than gid matching.
- The framework is designed to support fixed real-world units (e.g., fields, parks, urban areas) to ease change detection, while allowing users to apply their own parcel structures if desired.
- Annual releases enable monitoring of land cover change, with the bootstrap training progressively leveraging the majority signal across recent years.

## Practical notes for analysts

- Use the 20m Classified Pixels for high-detail, fine-scale analysis and to preserve landscape features that may be lost in coarser summaries.
- Use Land Parcels or 1km rasters for aggregated summaries and time-series analyses at administrative or watershed scales.
- When comparing across years, prefer spatial overlap methods (parcel-based or pixel-based with alignment) due to changing parcel identifiers.
- Be mindful of BAP-based terminology vs. UKCEH Land Cover Classes terminology; consult Appendix notes for nuances in class definitions and detection caveats.
- Expect ongoing improvements: future LCM updates aim to enhance training data, incorporate additional data sources, and refine upland and coastal vegetation mappings.

## Accessibility and update cadence

- Annual update plan: UKCEH intends to release a new LCM each year (with ongoing refinement of Bootstrap Training and RF processes).
- All years for GB and NI are provided at 20m, 25m parcel, and 1km raster scales, with documentation and metadata to support reproducibility and auditing.