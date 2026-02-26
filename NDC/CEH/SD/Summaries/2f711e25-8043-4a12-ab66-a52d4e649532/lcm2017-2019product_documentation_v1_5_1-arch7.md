# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

## Overview
- Release of three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map presents 21 UKCEH Land Cover Classes (based on BAP Broad Habitats) with an approximate one-to-one mapping to previous UKCEH class schemes.
- Production is automatic via Bootstrap Training and Random Forest, using Sentinel-2 Seasonal Composite Images and 20m Context Rasters.
- No manual corrections were applied to these maps; visual checks and formal validation were performed.
- Aims to enable rapid, annual updates to monitor land cover change; validation indicates quality comparable to the latest prior map (LCM2015).

## Data Content and Classification Framework
- 21 UKCEH Land Cover Classes; relationship to UK BAP Broad Habitats detailed in Appendices 1–2.
- Datasets available in two national gridding systems: Great Britain (EPSG:27700) and Northern Ireland (EPSG:29903).
- The product suite includes 42 datasets (for 3 years × multiple dataset types), duplicated for GB and NI.
- Ground-truth validation against GB countryside survey data, National Forest Inventory, IACS, and bespoke validation points (22,325 points in total).

## Production Methodology
- Bootstrap Training: automatic sampling of historic land cover maps (from LCM2015) to create training data for current classification; uses majority signal across time for evolving maps.
- Random Forest: supervised classifier trained on bootstrap samples; balanced sampling across classes to avoid dominance by common classes.
- Classification Scenes: GB produced as 74 overlapping 100x100 km tiles (each year, independently trained and classified); NI uses a single 43-band scene per year.
- Context Rasters: 20m layers providing terrain and proximity context to reduce spectral confusion (e.g., height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore, coastal/urban masks).
- Seasonal Composite Images: Sentinel-2 TOA reflectance; four seasons (winter, spring, summer, autumn) at 20m; Cloud-related gaps handled by classifier; future work may add SR or radar inputs.
- Land Parcel Spatial Framework: fixed GB NI parcel framework (~0.5 ha MMU) to summarize 20m classified pixels; parcel identifiers (gid) do not match LCM2015 but can be used for cross-year comparisons via gid.

## Data Products and Dataset Structure
- 20m Classified Pixels: new 2-band 8-bit rasters per year (class id, confidence 0–100); preserves fine detail and narrow features not aggregated into parcels.
- Land Parcels: 20m Classified Pixels intersected with the Land Parcel Spatial Framework; parcel-level attributes include hist, mode, purity, conf, stdev, n; gid is stable within LCM2017–2019 but not with LCM2015.
- 25m Rasterised Land Parcels: 3-band rasters for each parcel (mode, conf, purity); provides a summarized, parcel-averaged view.
- 1km Rasters (per year):
  - 1km Percent Cover: 21-band raster (percentage cover per class).
  - 1km Percent Aggregate Cover: 10-band raster (aggregate classes).
  - 1km Dominant Cover: single-band raster (dominant class per 1km cell).
  - 1km Dominant Aggregate Cover: 1-band raster (dominant aggregate class per 1km cell).

## Dataset Details and Extents
- GB extents: British National Grid (EPSG:27700); 0–700,000 East; 0–1,300,000 North.
- NI extents: Irish Grid (TM75) (EPSG:29903); defined NI extents.
- Pixel sizes: Classified Pixels 20 m; Land Parcels 25 m; Percent Cover / Dominant rasters for 1 km resolution ( aggregates up to 1 km).
- Number of classes: 21 (UKCEH Land Cover Classes) and 21 for Land Parcels datasets; additional metadata provided in Tables and Appendices.

## UKCEH Land Parcel Spatial Framework
- Based on LCM2007 framework with minor updates; identical parcel geometries to LCM2015 but with reordering/indices for faster processing.
- gid remains the stable parcel identifier within LCM2017–LCM2019, but not identical to LCM2015 parcel IDs.
- MMU approx. 0.5 ha; designed to represent discrete real-world units (fields, parks, urban areas, etc.).
- Users can summarise 20m Classified Pixels with their own parcel delineations if desired.

## Bootstrap Training and Validation
- Bootstrap Training derives training data from UKCEH LCM2015 to classify 2017–2019 scenes; aims to exploit majority signal for robustness against modest land-cover changes.
- Validation involved 22,325 points across GB NI datasets, yielding:
  - LCM2017: ~78.6% overall accuracy
  - LCM2018: ~79.6% overall accuracy
  - LCM2019: ~79.4% overall accuracy
- Validation data come from multiple sources and required class-conversion; results are indicative, not absolute truth, and currency varies by dataset.

## Practical Considerations for GIS Specialists
- Annual updates enable monitoring of land-cover change with a consistent 21-class framework aligned with historic UK maps.
- The 20m Classified Pixels dataset retains detailed landscape features that are often lost in parcel-generalized products.
- The 25m Land Parcels and 1km rasters support scalable analyses, from fine-scale parcel-level studies to broad regional assessments.
- Cross-year comparisons are facilitated by gid within 2017–2019, but gid across 2015–2019 differ; year-to-year change should be interpreted with caution where parcel IDs differ.
- Context rasters and seasonal composites improve classification reliability in spectrally similar classes (e.g., various grasslands, wetlands).
- Future data products may incorporate additional input sources (e.g., Sentinel-1 radar) to address cloud gaps and expand thematic detail.

## Appendix and Classification Context (highlights)
- Appendix 1–2 provide detailed notes on UKCEH Land Cover Classes vs. UK BAP Broad Habitats and their practical detection limitations from remote sensing.
- Appendix 3 offers RGB color recipes for displaying classes.
- Appendix 4 contains full confusion matrices and accuracy assessments for 2017–2019, including producer’s and user’s accuracy per class and cross-class confusion notes.
- Appendix 5 lists full datasets per year and dataset naming conventions.

## References and Tools
- Underlying methods and tools include Random Forest (Breiman, 2001), WEKA, PostGIS, and GDAL.
- Supporting literature provides context for Sentinel-2 band usage, bootstrapping, and landscape mapping considerations.