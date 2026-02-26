# The UKCEH Land Cover Map for 2021

- The ninth UKCEH land cover map (LCM2021) produced by UKCEH. It maps land cover across Great Britain and Northern Ireland using 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats. Annual production aims to improve temporal consistency, support change detection, and aid environmental decision-making. Formal validation reports an overall accuracy of 82.6% (95% CI: 82.19%–82.99%).

## Data products and structure

- Datasets (GB and Northern Ireland; six in total)
  - 10 m Classified Pixel datasets: per-pixel land cover class with a second band giving the classifier’s confidence. High spatial detail preserved (not generalised by the Land Parcel Spatial Framework).
  - Land Parcel datasets: land parcels derived from generalised framework; provide parcel-level attributes (e.g., hist, mode, conf, purity, n) and support change detection.
  - 25 m Rasterised Land Parcel datasets: rasterised version of parcels with three bands (dominant land cover, conf, purity).
- 1 km raster products (derived summaries)
  - Dominant cover at 1 km for LCM2021 classes and aggregates (1-band).
  - Percentage cover at 1 km for classes and aggregates (21 and 10 bands respectively); values are integer-rounded; coastal areas may sum to slightly below 100 due to mapping proportions.
- Dataset metadata and references
  - Official dataset names and extents are provided in Appendix 3; GB uses British National Grid (EPSG 27700); NI uses Irish Grid TM75 (EPSG 29903).
  - GB extent: 0–700,000 m Easting, 0–1,300,000 m Northing; NI extent is truncated to suitable bounding box.

## How the maps are made (methodology)

- Seasonal and contextual imagery
  - Classification Scenes built from four-season Sentinel-2 Seasonal Composite Images (10 bands) plus 10 Context Rasters to reduce spectral confusion.
  - Seasonal composites are derived via Google Earth Engine; occasional cloud gaps are handled so no manual gap filling is required.
- Context rasters
  - GB: Terrain (Height, Aspect, Slope), distances to buildings/roads/sea/freshwater, foreshore and tidal masks, and a woodland mask.
  - NI: Terrain plus urban mask and distances to coast, freshwater, and roads, plus foreshore and tidal masks.
- Classification approach
  - Bootstrap Training: uses historic LCM data (LCM2018–LCM2020) filtered to parcels with >80% purity and consistent class across years to form training data.
  - Random Forest (RF) classifier
    - Training uses 10,000 samples per bootstrap bag; sampling is balanced to give equal weight to all classes.
    - Implemented with a bespoke pipeline combining Weka, PostGIS, and GDAL (open-source tools).
- Classification outputs
  - 10 m Classified Pixels: the primary 10 m product; includes class ID and confidence, suitable for specialist analyses.
  - Land Parcel Spatial Framework: parcels used to aggregate 10 m pixels, reducing noise and enabling stable change detection.
- Validation
  - 35,182 validation points across all 21 classes; validation data drawn from GB countryside survey, open data inventories, Rural Payments data, and bespoke imagery/field points.
  - Overall accuracy: 82.6% (95% CI 82.19%–82.99%).

## The UKCEH Land Cover Classes and relationships

- 21 UKCEH Land Cover Classes are aligned with BAP Broad Habitats but are not a one-to-one mapping; some distinctions exist due to the satellite-based methodology.
- Appendices outline how UKCEH Classes relate to BAP Broad Habitats and provide guidance on when terms should be italicised (BAP) vs. standard capitalised class names.
- In some cases, BAP Broad Habitats are split or merged to better reflect spectral separation (e.g., Heather vs. Heather Grassland; Urban vs. Suburban).

## Technical details and notes for analysts

- Dataset descriptions (Table 2 and Table 3 references)
  - 10 m Classified Pixels: two-band raster (class id, confidence); not generalised by the Land Parcel Framework.
  - Land Parcels: parcel-level attributes including a frequency history (_hist), modal class (_mode), mean confidence (_conf), standard deviation (_stdev), aggregate class (_agg), and count of pixels (_n).
  - 25 m Rasterised Land Parcels: three-band raster (dominant class, conf, purity) aligned to parcel geometry.
  - 1 km Products: summarize 25 m data to 1 km scale (dominant class, percentage cover per class/aggregate).
- Training data and modelling notes
  - Bootstrap Training relies on large, wall-to-wall historic data to generate robust training observations for the RF model.
  - The pipeline balances class representation to avoid bias toward more common classes.
- Limitations and considerations
  - Some spectral confusions persist between certain land cover types; context rasters help reduce confusion but are not perfect.
  - The 1 km percentage products are rounded integers; the sum of percentages may not be exactly 100% due to rounding.
  - The UK Land Parcel Spatial Framework uses a minimum parcel size (~0.5 ha); classification is parcel-based to reduce noise, but some fine-scale features fall below the MMU.
  - Comparability with LCM2015 is affected by re-ordered parcel identifiers; cross-year comparisons should use spatial overlap rather than parcel IDs.

## Practical interpretation and usage guidance

- Annual maps enable better separation of random classification errors from real land-cover change over time.
- The 10 m Classified Pixels provide a rich, high-resolution view for detailed analyses, while the Land Parcel and 1 km products support consistent change detection and broad-scale assessments.
- The Appendix color recipes (Appendix 5 and 6) offer suggested color schemes, including color-blind friendly options, for map visualization.

## Appendices and supplementary material

- Appendix 1: Notes on UKCEH Land Cover Classes (interpretation guidance for each class and common confusions)
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and relationships to UKCEH classes)
- Appendix 3: Full list of UKCEH LCM2021 datasets (GB and NI)
- Appendix 4: Correspondence matrices and per-class accuracy/producer’s accuracy data (confusion analysis)
- Appendix 5–6: Recommended color recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly)
- References: foundational sources for RF, training, and habitat classifications