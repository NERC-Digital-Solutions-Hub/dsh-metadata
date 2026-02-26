# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6

## Overview
- Three new UKCEH land cover maps: LCM2017, LCM2018, and LCM2019, each representing 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats.
- Maps produced automatically using Bootstrap Training with a Random Forest classifier; aim to deliver UK-wide maps annually.
- Validation indicates maps are of similar quality to the latest predecessor (LCM2015), with ~78.6–79.4% overall accuracy at UK scale.
- 21 classes are mapped, with careful handling to maintain consistency for change detection over time.

## Production Approach and Key Concepts
- Data inputs:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance, median per season) at 20 m resolution.
  - Ten Context Rasters (e.g., terrain, proximity to urban features, water bodies) to reduce spectral confusion.
- Seasonal and contextual framework:
  - Seasonal Composite Images cover winter, spring, summer, and autumn; context rasters provide location-based cues.
- Classification framework:
  - Bootstrap Training uses historic LCM2015 as the training base, sampling land parcels with high purity to generate robust spectral training data.
  - Random Forest classifier trained on balanced samples (10,000 per class) to ensure rarer classes are learned.
  - Processing uses a tile-based approach for Great Britain (100 km x 100 km tiles) and a single optimised approach for Northern Ireland.
- Land Parcel Spatial Framework:
  - UKCEH Land Parcel Spatial Framework enables summarising 20 m classified pixels into parcels (~0.5 ha MMU) for time-series comparison.
  - Framework is unchanged in geometry but reorganised for faster processing; gid identifiers differ from LCM2015 for NI/GB matching.
- Output datasets and structure (GB + NI; 42 datasets across years):
  - 20 m Classified Pixels (new 2-band rasters: dominant class and class confidence)
  - Land Parcels (parcel-level attributes; hist, mode, purity, confidence, etc.)
  - 25 m Rasterised Land Parcels (3 bands: mode, conf, purity)
  - 1 km Dominant Cover; 1 km Percent Cover (21 bands); 1 km Percent Aggregate Cover (10 bands)
- Software and workflow:
  - Custom production pipeline integrating Weka (machine learning), PostGIS, and GDAL; all open-source components.
- Additional production notes:
  - TOA reflectance used due to incomplete SR availability; potential for future refinement with additional input types.
  - No manual corrections were applied in this release; all classification is automatic, with visual checks and formal validation.

## Data Products and Metadata
- Coordinate systems and extents:
  - Great Britain: British National Grid (EPSG: 27700)
  - Northern Ireland: Irish Grid (TM75, EPSG: 29903)
- Land cover classes:
  - 21 UKCEH Land Cover Classes aligned with 2015 mappings; not a direct one-to-one with UK BAP Broad Habitats in all cases.
  - Tables describe class relationships to UK BAP Broad Habitats and aggregated classes.
- Dataset specifics:
  - 20 m Classified Pixels: new per-pixel 21-class classification with probability-based confidence (Band 2).
  - Land Parcels: attributes including gid, hist (frequency per class), _mode (dominant class), _purity, _conf (mean per-pixel probability), _stdev, _n (count of pixels).
  - 25 m Rasterised Land Parcels: three-band rasters (mode, conf, purity).
  - 1 km Raster products:
    - 1 km Percent Cover: 21-band raster of per-class percentages (sums may deviate from 100 due to rounding and coastlines).
    - 1 km Percent Aggregate Cover: 10-band raster for aggregate classes.
    - 1 km Dominant Cover: single-band raster for dominant class per 1 km cell.
    - 1 km Dominant Aggregate Cover: 1-band raster for dominant aggregate class per 1 km cell.
- Data volume and accessibility:
  - Total of 42 datasets across the three years; GB and NI versions provided for each dataset.
  - Datasets summarized in accompanying tables and appendices; full list in Appendix 6.
- Visualization and colour:
  - Appendix 3 and 4 provide recommended colour schemes (including colour-blind friendly options) for displaying Land Cover Classes.
- Validation and accuracy:
  - Independent validation against GB countryside survey (2019), National Forest Inventory, IACS, and bespoke LCM validation points (n ≈ 22,325).
  - UK-scale accuracy: LCM2017 78.6%, LCM2018 79.6%, LCM2019 79.4%.
  - Validation figures exclude exact truth status due to cross-walking between class schemes; provide useful performance indicators.

## Interpretation and Use Considerations
- Class definitions and mapping:
  - 21 UKCEH Land Cover Classes are designed for remote sensing detection and change analysis, with close alignment to BAP Broad Habitats but not identical to field-based BAP definitions.
  - Some upland, peatland, and coastal classes pose spectral and spatial detection challenges; context layers help mitigate misclassification.
- Temporal change and repeatability:
  - Bootstrap Training leverages historical maps to train classifiers, enabling rapid updates with short intervals between maps.
  - Individual classification scenes are trained independently; overlaps may show minor variation, but overall change is intended to reflect real land cover change.
- Spatial detail and summary products:
  - 20 m Classified Pixels preserve fine landscape details (e.g., narrow features) compared with higher-level parcel summaries.
  - 1 km and 25 m products provide scalable summaries suitable for regional analyses and integration with other geospatial datasets.
- Limitations and caveats:
  - No manual corrections in this release; some spectral confusions persist between similar habitats (e.g., various grasslands, bogs, peatlands).
  - Validation data use a mix of sources with potential class mapping differences; results should be treated as indicative rather than absolute truth.
  - Seasonal data gaps due to cloud coverage may occur; classification framework can tolerate partial seasonal information, but future work explores additional data sources (e.g., Sentinel-1) for gap filling.

## Appendices and Additional Resources
- Appendix 1–2: UK BAP Broad Habitat definitions and relationships to UKCEH classes.
- Appendix 3–4: Colour and colour-blind friendly display recipes; accompanying QGIS symbology files.
- Appendix 5: Confusion matrices and accuracy metrics by year (LCM2017, LCM2018, LCM2019) with producer’s and user’s accuracy details.
- Appendix 6: Full list of datasets by year and product type.
- References: Key sources for methods (Random Forest, bootstrapping, spectral/seasonal considerations) and background on BAP classifications.