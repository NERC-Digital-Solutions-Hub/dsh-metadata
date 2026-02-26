# The UKCEH Land Cover Map for 2021

- LCM2021 is the ninth UK land cover map produced by UKCEH, created from automatic classification of Classification Scenes that combine Sentinel-2 Seasonal Composite Images with 10 Context Layers to reduce spectral confusion.
- Product consists of six datasets across Great Britain and Northern Ireland: three for GB and NI each (a 10 m classified pixel dataset, a dataset of classified land parcels, and a 25 m pixel dataset or rasterised land parcels).
- Annual production aims to improve temporal consistency, comparability, and change detection, while enabling easier monitoring of UK countryside state and change.
- Formal validation reports an overall accuracy of 82.6% at full 21-class thematic detail.

## Purpose and scope

- Provide a user guide for LCM2021 including production, validation, data accuracy, and guidance on application for current and future work.
- Present the data structure, methods, and validation to help users make informed decisions about applying LCM data.

## Data structure and datasets

- Three geospatial datasets (GB and NI; six in total):
  - 10 m Classified Pixel datasets: mosaic of Classification Scenes; RF classifier yields most probable UKCEH Land Cover Class; band 1 = class identifier, band 2 = class probability.
  - Land Parcel datasets: results of intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework to generate parcel attributes.
  - 25 m Rasterised Land Parcel datasets: rasterised 25 m representation with 3 bands per parcel (dominant class, confidence, purity).
  - 1 km raster products: summarised from 25 m rasters to provide dominant class and percentage cover (21 class bands and 10 aggregate bands); rounding may cause minor sums-off-100 near coastlines.
  - 10 m Context Rasters: GB includes height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, and a woodland mask; NI includes height, aspect, slope, urban mask, distance to coast/roads/freshwater, foreshore and tidal masks.
  - Seasonal Composite Images: four-season Sentinel-2-based images (January–March, April–June, July–September, October–December) at 10 m resolution; occasional cloud-related gaps mitigated by classifier tolerance.
  - Classification Scenes: GB classified using 32 tiles (roughly 100 x 100 km tiles) to yield 50-band Seasonal Composite Images plus 10 Context Layers; NI uses a single 49-band classification scene combining 40-band Sentinel-2 Seasonal Composite with NI Context Rasters.
- Datasets are described with coordinate systems and extents:
  - GB: British National Grid (EPSG: 27700).
  - NI: Irish Grid TM75 (EPSG: 29903).
- Dataset naming and extent notes provided in Appendix 3.

## Methodology

- Bootstrap Training: Automatic, repeated sampling from historic land cover maps (LCM2018–LCM2020) to generate training observations without fresh field data. Training parcels must have >80% purity and be consistently classified across three years.
- Random Forest (RF) classification: Pixels are sampled into labeled bags; 10,000 samples per bag with replacement to balance class representation; RF classifier outputs the most probable class per pixel.
- Data inputs: Classification Scenes composed of Seasonal Composite Images plus 10 Context Rasters to reduce spectral confusion.
- Software stack: Bespoke UKCEH workflow integrating Weka, PostGIS, and GDAL (all open source).

## UKCEH Land Parcel Spatial Framework

- Land Parcels represent discrete real-world units (approx. 0.5 ha MMU) derived by generalising national cartography; parcels help reduce classification noise and enable consistent, change-detection-ready comparisons over time.
- Parcel identifiers (gid) may not match LCM2015 due to framework reordering; most users are unaffected.

## Validation and accuracy

- Validation dataset: 35,182 reference points across all 21 classes, drawn from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Overall accuracy: 82.6% (95% CI 82.19%–82.99%); class-specific accuracies vary (details in Appendix 4: Correspondence matrices).
- Validation targets primarily the 25 m rasterised land parcel product; 10 m pixels are not validated against the parcel framework.

## UKCEH Land Cover Classes and BAP Broad Habitats

- LCM2021 uses 21 UKCEH Land Cover Classes, closely related to UK BAP Broad Habitats but not identical.
- Relationships are described and clarified with appendices; some BAP Broad Habitats are split or merged to better reflect remote-sensing capabilities and training data.
- When referring to BAP Broad Habitats, italics are used; UKCEH class names are capitalised.

## Data interpretation and guidance for analysts

- 10 m Classified Pixel dataset: high detail, preserves narrow features; not generalised by the Land Parcel Framework; suitable for specialist users aware of the implications for validation and accuracy assessment.
- 25 m Rasterised Land Parcel dataset: more stable for change detection and parcel-level analyses; derived by intersecting 10 m pixels with the Land Parcel Spatial Framework.
- 1 km products: suitable for regional summaries and broad-scale monitoring; percentage values are integer-rounded and may not sum exactly to 100 due to edge effects, especially near coastlines.
- Seasonal composites and context rasters enhance phenological discrimination and reduce misclassification for certain habitat types.
- Annual production enables distinguishing persistent real change from random classification noise; random errors tend to flicker over time.

## Practical considerations for monitoring the environment

- Use time-series capability to differentiate real land cover change from random misclassification.
- Exercise caution with classes that are spectrally confounded (e.g., certain grassland, bog, fen, and coastal classes); model-based context rasters help but some ambiguity remains.
- For coastal and aquatic features, Saltwater and Freshwater distinctions are improved with coastal/foreshore context but still exhibit some misclassification in tidal zones.

## Limitations and future directions

- Bootstrap Training relies on historic maps; accuracy improvements depend on availability and consistency of past maps.
- Some inter-class confusions persist due to spectral similarity and dynamic habitat mosaics; ongoing enhancements may include new training data and updated methods.
- If new methods yield significant improvements, UKCEH may re-apply updates across the entire catalogue to maximise temporal consistency and change-detection potential.

## Appendices and supporting material

- Appendix 1 & 2: Notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats (definitions and distinctions).
- Appendix 3: Full list of LCM2021 datasets by region and product type.
- Appendix 4: Correspondence matrices (class-by-class accuracy and producer/user accuracies; detailed breakdown).
- Appendices 5 & 6: Recommended colour schemes for displaying UKCEH Land Cover Classes, including color-blind friendly versions.
- Introduction emphasizes that land cover types are capitalised and that BAP terms are italicised when referenced for clarity.