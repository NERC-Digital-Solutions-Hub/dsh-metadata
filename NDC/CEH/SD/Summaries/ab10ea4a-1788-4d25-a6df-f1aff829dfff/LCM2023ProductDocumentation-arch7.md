# The UKCEH Land Cover Map 2023

- UKCEH’s annual land cover map (LCM2023) comprises 21 UKCEH Land Cover Classes derived from satellite data, designed for map-based data products and change monitoring.
- Classification approach: Sentinel-2 Seasonal Composite Images combined with Context Rasters; uses Bootstrap Training with a Random Forest classifier to produce classifications automatically.
- Purpose: describe data production, validation, and accuracy to help users apply LCM2023 data confidently for current and future work.

## Data Product Suite (structure and formats)

- Three geospatial datasets per region (Great Britain and Northern Ireland) plus a 1 km summary raster:
  - 10 m Classified Pixel dataset (GB and NI): per-pixel land cover class with a second band giving classification confidence. Keeps full 10 m detail (not generalised by the Land Parcel Spatial Framework).
  - 25 m Rasterised Land Parcel dataset (GB and NI): rasterised land parcels derived from the 10 m classifications, carrying parcel-level attributes; used for reduced-detail analyses and change detection at parcel scale.
  - Land Parcel Vector datasets (GB and NI): vector land parcel products linked to the UKCEH Land Parcel Spatial Framework.
  - 1 km Summary rasters (GB and NI): aggregated products summarising 25 m data to 1 km resolution (dominant class and percentage cover per class/aggregate class).
- Appendix 3 lists official dataset names and DOIs; all datasets are citable.

## Spatial reference and extents

- Great Britain: British National Grid, EPSG 27700.
- Northern Ireland: Irish Grid (TM75), EPSG 29903.
- Pixel resolutions: 10 m (pixels); 25 m (land parcel rasters); 1 km summary rasters summarize the 25 m data.
- Land parcel counts and extents vary by region (e.g., thousands of parcels per region; MMU ~ 0.5 ha for land parcels).

## UKCEH Land Cover Classes and BAP Broad Habitats

- LCM2023 uses 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats; relationships are described and sometimes diverge from BAP definitions.
- Appendices explain class definitions and how they map to BAP Broad Habitats; notes on potential spectral confusion and training data considerations.

## Data production: Seasonal imagery, context rasters, and classification scenes

- Seasonal Composite Images:
  - Derived from Google Earth Engine using Sentinel-2 data; four seasons: Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec.
  - 10 spectral bands used; occasional data gaps due to cloud are handled; still ensures full UK coverage.
  - Four-season spectra enable temporal differentiation of vegetation types.
- Context Rasters (10 m for GB; a separate set for NI):
  - Elevation (height), slope, aspect, distances to features (buildings, roads, tidal water, freshwater), foreshore, woodlands, saltmarsh; tailored to GB and NI data sources.
- Classification Scenes:
  - GB classified in 32 tiles (approx. 100 x 100 km) to manage regional phenology variation; NI uses a single scene covering the landmass.
  - Each classification scene is trained and classified independently.

## Bootstrap Training and Random Forest classification

- Bootstrap Training:
  - Automatically derives training observations from historic LCM maps (2020–2022) with >80% probability and consistency across years.
  - Large training sets reduce impact of small changes; two example figures illustrate the process.
- Random Forest classifier:
  - 10,000 samples per tree bag, balanced across classes to avoid domination by common classes.
  - Produces the 10 m Classified Pixel dataset (class band + confidence band).
- Software stack: bespoke UKCEH toolchain integrating Weka (machine learning), PostGIS, and GDAL; all open-source components.

## Validation, accuracy, and known issues

- Validation:
  - 33,107 validation points across all 21 classes; derived from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
  - Overall accuracy for LCM2023: 83%.
- Known issues:
  - A small subset of polygons missing from vector land parcel products, causing nodata areas in the 25 m rasterised land parcels dataset; effect on 1 km products is negligible; 10 m classified pixels are unaffected.
- Note on method changes: ongoing methodological refinements may cause minor differences between successive annual maps.

## Use and interpretation guidance (for GIS work)

- 10 m Classified Pixels:
  - High detail; used where fine-scale features matter (e.g., narrow patches, edges); not generalised by the Land Parcel Spatial Framework to preserve detail.
  - Validation against 25 m rasterised parcels; some classification uncertainty exists (see Appendix 4 confusion matrices).
- 25 m Rasterised Land Parcels:
  - Generalised parcel-level products; suitable for change detection and aggregation at coarser scales.
  0.5 ha MMU applied to parcel delineation; parcels often dominated by a single land cover type.
- 1 km Summary rasters:
  - Useful for broad-scale analyses and compatibility with regional datasets; rounding for percentage cover may cause sums to deviate from exactly 100%.
- Seasonal and Context data:
  - Seasonal composites and context rasters are designed to reduce spectral confusion and improve classification performance.

## Color standards and accessibility

- Appendix 5: Recommended color recipes for displaying UKCEH Land Cover Classes (distinct color sets for standard viewing).
- Appendix 6: Color-blind-friendly alternatives for the same class set.
- QGIS symbology files are provided to enable immediate map production.

## Data access, citations, and further reading

- Each LCM2023 dataset has a DOI and citation; cited works include Marston et al. (2024) and related production method references.
- DOIs are provided for 10 m classified pixels (GB and NI), 25 m rasterised land parcels (GB and NI), land parcel vector data (GB and NI), and 1 km summary rasters.
- Disclaimer: ongoing development means some annual map differences reflect methodological changes in addition to real land-cover change.

## Appendix highlights (key references)

- Appendix 1–2: Notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats.
- Appendix 3: Full list of LCM2023 datasets and citations.
- Appendix 4: Detailed correspondence matrices (confusion matrices) for class accuracy and producers’/users’ accuracy.
- Appendices 5–6: Color recipes (standard and color-blind friendly) and associated QGIS files.