# The UKCEH Land Cover Map for 2023

## Purpose and scope
- User guide for LCM2023, detailing seven geospatial data holdings: three regional datasets for Great Britain and Northern Ireland (10 m classified pixels, land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster product covering both regions.
- Explains data production, validation, and data accuracy to help users assess suitability and limitations for current and future work.

## Data products (structure)
- 10 m Classified Pixel datasets (GB and NI)
  - Pixel-level land cover class (UKCEH Land Cover Class) plus a confidence/probability band.
  - 2-band product for GB and NI respectively.
- Land Parcel datasets (GB and NI)
  - Derived by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
  - Includes 25 m Rasterised Land Parcel products (GB and NI) and vector land parcels (GB and NI).
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Three-band rasters: mean parcel mode, confidence, and purity.
- 1 km summary rasters (GB and NI)
  - Dominant class, aggregate classes, and percentage cover products with specific rounding rules near coastlines.
- Dataset metadata and DOIs are provided for citation.

## Production methodology
- UKCEH Land Cover Classes
  - 21 classes derived from Biodiversity Action Plan (BAP) Broad Habitats; mappings between UKCEH classes and BAP habitats described in Appendices.
- Seasonal Composite and context layers
  - Seasonal Composite Images created from Sentinel-2 data (four seasons) with spectral bands listed in Table 4.
  - Context Rasters (10 m) include terrain (height, aspect, slope) and proximity masks (building, road, tidal water, freshwater, foreshore, woodland, saltmarsh).
- Bootstrap Training and Random Forest classification
  - Bootstrap Training uses historic LCMs (LCMs from 2020–2022) to automatically generate training data without fresh field collection.
  - 10 m classification scenes are classified with a Random Forest classifier; class with the highest probability becomes the map classification; a second band provides the associated probability/confidence.
  - GB is tiled into 32 Classification Scenes; NI uses a single 49-band scene (10 m+ context) due to smaller extent.
- UK Land Parcel Spatial Framework
  - Parcels have a minimum area of ~0.5 ha (MMU); parcels are generalised from national cartography to form discrete units for stability and change detection.
- Validation and accuracy
  - Validation performed with 33,107 reference points across 21 classes; overall accuracy of 83%.
- Production timeline and updates
  - Annual production with ongoing methodological evolution; significant improvements may lead to full catalogue re-application to maximise temporal comparability.

## Data quality, limitations, and governance
- Accuracy
  - Overall accuracy: 83% (LCM2023 full thematic detail).
  - Appendices provide detailed correspondence matrices, user’s and producer’s accuracies by class (Appendix 4).
- Known issues
  - Some polygons missing from vector land parcel products (negligible effect on 1 km outputs; 10 m pixels unaffected).
  - Minor classification confusions among certain UKCEH/BAP classes (notably in mixed or spectrally similar categories); coastal and intertidal areas may show some misclassification (Saltwater vs Freshwater near tidal zones).
  - GID/parcel identifiers have changed since LCM2015; time-series comparisons should rely on spatial overlap rather than ID matching.
- Data compatibility
  - Methodology changes over time can cause differences between successive maps beyond actual land-cover changes.
  - 1 km summary rasters help with cross-cohort comparability; coastlines near 100% area mapping can diverge due to percentage rounding.
- Spatial reference and extent
  - GB: British National Grid (EPSG:27700); NI: Irish Grid (TM75, EPSG:29903).
  - MMU of 0.5 ha for land parcels; 10 m and 25 m pixel resolutions; broad geographic coverage for UK.
- Provisions for reuse
  - DOIs provided for all datasets; formal citations recommended (Table 5).
  - Recommended color schemes provided (Appendices 5 and 6) with QGIS symbol files to support consistent visualization.

## Usage guidance for data stewards
- Data governance
  - Treat LCM2023 as a yearly update with clear lineage from Bootstrap Training and Sentinel-2 seasonal composites.
  - Record and cite the specific dataset DOIs when using results; reference the accompanying Marston et al. papers for production methods.
- Time-series considerations
  - Use spatial overlap rather than parcel IDs when comparing across years due to changes in the Land Parcel Spatial Framework identifiers.
  - Be aware of method evolution; document any method-specific caveats when aggregating across years.
- Data interpretation
  - Understand the 21 UKCEH Land Cover Classes and their relationship to BAP Broad Habitats (Appendices 1–2) to interpret classifications in environmental reporting.
  - When detailed habitat discrimination is critical, consult Appendix 1 for class-specific notes and potential confusions.
- Visualization and metadata
  - Utilize the provided color schemes (Appendix 5–6) and the accompanying QGIS files (lcm_raster.qml, lcm_raster_cb_friendly.qml) for consistent mapping and color-blind accessibility.
- Validation and quality control
  - Leverage the 1 km summary rasters for higher-level summaries and cross-check 10 m pixel classifications against known site-level information.
  - Note the 83% accuracy baseline and use validation datasets as a benchmark for quality assurance in new analyses.

## Appendices at a glance
- Appendix 1: Notes on UKCEH Land Cover Classes and cross-references to UK BAP Broad Habitats (definitions, training data caveats, and class-specific notes).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions (detailed descriptions of each habitat type).
- Appendix 3: Full list of UKCEH LCM2023 datasets with DOIs and citations.
- Appendix 4: Correspondence matrices (confusion matrices) for LCM2023 by class, including user’s and producer’s accuracies.
- Appendix 5/6: Color recipes for displaying UKCEH Land Cover Classes (standard and color-blind friendly) and corresponding QGIS symbol files.