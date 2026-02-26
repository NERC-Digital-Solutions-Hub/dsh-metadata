# LAND COVER MAP 2007 DATASET DOCUMENTATION

- A parcel-based UK land cover classification (LCM2007) using 23 Broad Habitat-based classes, derived from summer–winter satellite composites at ~20–30 m pixels.
- Product family supports diverse applications: vector (polygons with rich metadata) and raster (25 m and 1 km resolutions), for Great Britain and Northern Ireland separately.
- LCM2007 maps land cover (not land use) and uses a minimum mappable unit of >0.5 ha; parcels smaller than 0.5 ha or lines <20 m are dissolved into surrounding areas.
- Validation shows average thematic accuracy around 83% against 9127 ground reference polygons; local discrepancies may occur.

## Introduction and Background Highlights

- LCM2007 updates LCM2000 with a framework aligned to OS digital cartography (OSMM for GB; L&S Large-scale Vector for NI), yielding polygons tied to real-world objects (fields, woodland blocks).
- Designed to be compatible with other GIS datasets; focus on land cover rather than precise land-use inference.
- Change mapping across LCM1990/2000/2007 is complex due to class and spatial structure differences; overall change detection is not recommended with this dataset.

## Product Overview

- Delivered as a range of data products (vector and raster) at multiple thematic/spatial resolutions to suit different applications.
- Vector dataset: 8.6 million GB polygons and 0.9 million NI polygons; 10 attributes per polygon; includes Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE, Knowledge-based enhancements (KBE), ProbList, CorePixels, Construct, TotPixels.
- Raster datasets: 25 m and 1 km products (GB and NI separate); 1 km products provide Dominant cover, Percentage cover for both 23 classes and Aggregate classes.

## Vector Data Set (Key Details)

- Parcel_ID: unique ID for each parcel (e.g., 11853977:c20); BH: dominant Broad Habitat; BHSub: sub-class; FieldCode: short descriptor; INTCODE: 1–23 class for display/QA; KBE: processing history; ProbList: top 5 spectral matches; CorePixels/TotPixels: pixel counts.
- Sub-classes (BHSub) provide additional information but are not part of the QA for the 23-class scheme; recommended user validation if using sub-classes for analysis.
- Rich metadata accompanying polygons supports traceability of data sources, processing steps, and classification history.

## Raster Data Sets (Key Details)

- 25 m rasters: 23 LCM2007 classes; GB and NI provided separately with appropriate projections.
- 1 km rasters: Aggregate classes (merged 23 classes) and 1 km dominant/percentage products; suitable for national-scale modelling and integration with other large-scale datasets.
- Metadata in Tables 2 and 3 describe the relationship between classes, extents, pixel counts, and coordinate systems.

## Map Projection and Spatial Referencing

- GB: British National Grid; NI: Irish National Grid.
- Northern Ireland is transitioning toward Ireland Transverse Mercator (ITM); GIS software should reproject NI data if needed.

## File Size and Data Access

- Vector (GB shapefile, 100 km × 100 km): ~4.13 GB; NI vector ~433 MB.
- Raster 25 m: GB ~1.36 GB; NI ~46 MB.
- Raster 1 km: GB products range from ~21 MB to ~49 KB; NI products vary similarly.
- Data access:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster products available under licence on request from CEH; licensing and fees may apply.

## Applications and Guidance for Analysts (Aimed at Data-driven Decision Makers)

- Use 23-class vector data when detailed land-cover delineation is needed; prefer 1 km rasters for national-scale analyses and when integrating with other large datasets.
- Retain Parcel_ID and KBE history for reproducibility and traceability; apply user-led validation if using Broad Habitat sub-classes.
- Be mindful of QA limitations at finer scales; the 83% average accuracy indicates local misclassifications are possible.
- For change detection, do not rely on LCM2007 alone due to methodological differences across versions; consider using the Final Report and cross-referencing with ground-truth data.

## Appendices (Important for Technical Reference)

- Appendix 1: LCM2007 Classes – definitions and Broad Habitat descriptions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Various Grassland types, Fen/Marsh/Swamp, Bog, Montane/Inland Rock, Saltwater/Freshwater, Littoral/Coastal types, Built-up Areas and Gardens including Urban and Suburban).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (field codes and mappings to 1–23 class numbers, with notes on interpretation and caution for sub-classes).
- Appendix 3: LCM2007 colour mapping (class numbers to RGB values) used in the Final Report; ArcGIS .lyr availability.
- Appendix 4: Updates to Products (Version 1.2, May 2014) – additions include OS Tiles for Fair Isle and Stranraer; water class updates for 1 km products; NI updates.