# The UKCEH Land Cover Map for 2023

- UKCEH LCM2023 is the eleventh UK land cover map produced, offering a multi-resolution dataset suite for Great Britain and Northern Ireland (GB: 10 m classified pixels, 25 m land parcels raster, and 1 km summary rasters; NI similarly) plus a GB+NI 1 km summary raster.
- Purpose: provide environmental health measures to monitor and evaluate policy and inform future decisions; supports change detection and state monitoring with annual updates.
- 21 UKCEH Land Cover Classes (based on Biodiversity Action Plan Broad Habitats) are mapped and linked to BAP habitats, with careful cross-walking notes to avoid ambiguity.
- Validation shows overall accuracy of 83% for full thematic detail across 21 classes.

## Data products and datasets

- 10 m Classified Pixel datasets
  - One mosaic per region (GB and NI) from multiple Classification Scenes.
  - Each pixel yields: the most likely UKCEH Land Cover Class (as an integer) and a second band with the associated class probability (confidence).
  - 10 m pixels are not generalized to the UKCEH Land Parcel Spatial Framework to preserve fine features; validated separately from the 25 m dataset.
- Land Parcel datasets (based on the UKCEH Land Parcel Spatial Framework)
  - Land Parcel Product (vector/parcels) and rasterised 25 m Land Parcel Product (three bands: dominant class mode, confidence, and purity).
  - Land parcels have a minimum area of ~0.5 ha (MMU); parcels represent discrete real-world units and are used for change detection.
  - The 25 m raster aligns with the parcel framework; some parcel IDs differ from LCM2015, affecting direct cross-year parcel ID comparisons.
- 1 km raster products (GB and NI)
  - Summary rasters derived from 25 m data: dominant class at 1 km (21-class and 10-aggregate variants) and percentage cover per class (and per aggregate).
  - Integer rounding means 1 km class percentages may sum to slightly above/below 100; coastal pixels may sum to less than 100 due to mapping extents.
- Seasonal Composite Images and Context Rasters
  - Seasonal Composite Images derived from Sentinel-2 at 10 m, providing four seasonal medians (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) across 10–12 bands.
  - Context Rasters (GB: height, aspect, slope, distances to buildings/roads/tidal water/freshwater, foreshore mask, woodland mask, saltmarsh mask); NI: urban mask and distances to coast, freshwater, roads, plus coastal masks.
- Classification Scenes
  - GB classified in 32 tiles roughly 100 x 100 km each; NI uses one Scene (minimum bounding rectangle).
  - Each Scene trained and classified independently to manage regional variation and data volume.
- Coordinate systems and extents
  - GB: British National Grid (EPSG: 27700); NI: Irish grid (TM75, EPSG: 29903).
  - GB/N1 data extents and parcel counts provided; detailed in Table 2 and Table 3 of the document.

## Production methodology

- Bootstrap Training
  - Automatic, data-driven training that uses historic LCM maps (LCM2020–LCM2022) to generate training observations when >80% probability and consistent class across three years are available.
  - Enables wall-to-wall training data without field-gathered data; supports continual improvement through successive maps.
  - Limitations: areas with crop rotations between arable and improved grassland over the update window may rely on alternative training data (e.g., UKCEH Land Cover plus: Crops data for 2023).
- Random Forest classification
  - Balanced training via sampling with replacement; 10,000 samples per class per bag; majority signal determines class membership per pixel.
  - Software stack includes bespoke UKCEH tools integrating WEKA, PostGIS, and GDAL (all open source).
- Seasonal and contextual information
  - Classification Scenes combine Sentinel-2 Seasonal Composite Images with Context Rasters to reduce spectral confusion and improve discrimination among similar habitats.

## Data governance, validation, and quality

- Validation
  - 33,107 validation points across 21 classes; sources include GB countryside survey, open National Forest Inventory data, Rural Payments data, and bespoke validation points.
  - Overall accuracy reported at 83% for full thematic detail.
- Validation caveats
  - Validation focuses on 25 m Rasterised Land Parcel dataset; 10 m Classified Pixels are not part of the validation dataset in the same way.
- Known issues
  - A small number of polygons are missing from the vector Land Parcel products, producing nodata in the 25 m rasterised Land Parcels; minimal impact on 1 km products.
- Data availability and citation
  - Each dataset has a DOI; formal citations provided (e.g., Marston et al. 2024a–g); DOIs and references cover 10 m classified pixels (GB and NI), 25 m rasterised parcels (GB and NI), land parcels (GB and NI), and 1 km summary rasters.
- Usage guidance and updates
  - Acknowledges that slight methodological changes between years can produce differences between maps; annual updates enhance temporal consistency and change detection.

## UKCEH Land Cover Class definitions and BAP alignment

- The 21 UKCEH Land Cover Classes are closely related to UK BAP Broad Habitats but not identical; explicit cross-walks and notes are provided (Appendices 1–2) to reduce ambiguity.
- Some BAP Broad Habitats are split or combined to maintain mapping performance with remote sensing constraints (e.g., Heather vs. Heather grassland; Urban vs. Suburban; Saltwater vs. Freshwater handling).
- Detailed class descriptions and habitat-related considerations are documented to assist users in interpreting outputs.

## Data provision, formats, and color representation

- Output formats
  - 10 m Classified Pixels: two-band rasters (class ID, confidence)
  - 25 m Rasterised Land Parcels: three-band rasters (mode, conf, purity)
  - 1 km rasters: multiple bands for dominant and percentage covers
  - Vector Land Parcels: parcel-level attributes and cross-tabulations
- Color mapping
  - Appendix 5 provides a recommended color recipe for displaying UKCEH Land Cover Classes
  - Appendix 6 provides a color-blind friendly version
  - QGIS symbology files are provided to aid immediate use
- Data accessibility and documentation
  - Appendices and Tables provide metadata mappings, dataset names, and official dataset names to support reproducibility and policy monitoring

## Practical implications for monitoring policies

- Timeliness and change detection
  - Annual LCM updates allow monitoring of land cover changes and differentiation of random classification noise from real change.
- Data quality and governance
  - Emphasis on data provenance, metadata clarity, and data sharing; use of Bootstrap Training supports scalable, repeatable monitoring workflows while acknowledging potential class-specific training limitations.
- Policy relevance
  - 21 UKCEH Land Cover Classes aligned with BAP concepts enable policy-relevant interpretation of habitat and land-cover dynamics.
- Limitations to consider in monitoring
  - 0.5 ha MMU for land parcels may omit smaller features; 10 m pixel detail is preserved in pixels but not parcel-level generalisation.
  - Differences in parcel identifiers between LCM2015 and LCM2023 may affect cross-year parcel-based trend analyses.
  - Methodological updates can introduce non-change-related differences; users should consider methodological context when interpreting year-to-year results.