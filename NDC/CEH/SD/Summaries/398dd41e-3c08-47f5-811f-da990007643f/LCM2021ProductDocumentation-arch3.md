# The UKCEH Land Cover Map for 2021

- Purpose: User guide for the UKCEH Land Cover Map 2021 (LCM2021). Describes data production, validation, data accuracy, and guidance to help users apply LCM2021 in current and future work. Aims to support informed monitoring, decision-making, and change detection.

- What LCM2021 is
  - Ninth UK land cover map produced by UKCEH, with annual production to support monitoring of state and change in the countryside.
  - Six geospatial datasets (three per region) covering Great Britain and Northern Ireland:
    - 10 m Classified Pixel datasets (GB and NI)
    - Land Parcel Spatial Framework datasets (GB and NI)
    - 25 m Rasterised Land Parcel datasets (GB and NI)
  - Additional outputs include 1 km raster products summarising 25 m data (dominant cover and percentage cover) and related seasonal/context layers used for classification.
  - Land cover is defined as 21 UKCEH Land Cover Classes linked to Biodiversity Action Plan (BAP) Broad Habitats descriptions; general mappings and caveats to preserve comparability with earlier products.

- Data production components
  - Seasonal Composite Images: Sentinel-2 data (four seasonal periods) processed in Google Earth Engine to create multi-band seasonal rasters (10 bands used after selection).
  - Context Rasters: 10 m layers to reduce spectral confusion (height, aspect, slope, distances to buildings, roads, sea, freshwater, foreshore, tidal water, woodland) for GB; similar but NI-focused layers for Northern Ireland.
  - Classification Scenes: GB classified using a grid of tiles (approx. 100 x 100 km), each built from 50-band Seasonal Composite Images plus Context Rasters; NI uses a single 49-band Classification Scene.
  - Bootstrap Training: Automatic training dataset built from historic LCMs (LCM2018–LCM2020) with >80% purity, for sampling current pixels to train the classifier. This “Bootstrap Training” enables near-wall-to-wall training data without new field collection.
  - Random Forest Classification: Balanced training with 10,000 samples per class per bag; uses RF to assign the most likely class to each pixel. The classification software combines Weka with PostGIS and GDAL (open-source tools).
  - UK Land Parcel Spatial Framework: Generalised parcel framework with a 0.5 ha minimum mapping unit (MMU). Serves as the fixed structure for parcel-based attributes and change detection; parcel identifiers (gid) differ from LCM2015 if users compare across years.

- Datasets and data structure
  - 10 m Classified Pixel datasets (GB and NI): Pixel-level classifications with two-band output per pixel:
    - Band 1: Most likely UKCEH Land Cover Class (integer)
    - Band 2: Classification confidence (probability)
  - Land Parcel datasets (GB and NI): Derived by intersecting 10 m classified pixels with the Land Parcel Spatial Framework to create parcel attributes (Table 3 metadata fields include _hist, _mode, _purity, _conf, _stdev, _agg, _n).
  - 25 m Rasterised Land Parcel datasets (GB and NI): Rasterised version of parcels with three attributes per parcel:
    - Band 1: Dominant land cover class (_mode)
    - Band 2: Mean confidence (_conf)
    - Band 3: Parcel purity (_purity)
  - 1 km raster products: Summary at 1 km resolution providing dominant class and percentage coverage for both 21 UKCEH classes and 10 UKCEH aggregates (rounded values; coastal areas may sum to slightly less or more than 100 due to rounding and resolution).
  - Spatial reference: Great Britain uses British National Grid (EPSG: 27700); Northern Ireland uses Irish Grid TM75 (EPSG: 29903).

- Validation and accuracy
  - Validation dataset: 35,182 reference points spanning all 21 classes, drawn from GB countryside surveys, National Forest Inventory data, Rural Payments Agency data, and bespoke validation points.
  - Overall accuracy: 82.6% with a 95% confidence interval of 82.19%–82.99%.
  - Validation approach links reference data to the 25 m rasterised parcel products to assess correspondence.

- Data governance, openness, and metadata considerations
  - Data are produced to enable open sharing and reuse, but some barriers can arise from metadata gaps, the need to share underlying data, and the complexity of coordinating data governance across organisations.
  - The UKCEH Land Parcel Spatial Framework and changes to parcel identifiers mean users comparing across years should be aware that gid values may not match LCM2015 for direct spatial overlap comparisons.
  - Some data (e.g., 10 m pixel-level outputs) are highly detailed and not formally validated against every pixel-level output; users should understand the distinction between pixel-level versus parcel-level validation.

- Practical guidance for users and monitoring frameworks
  - Annual cadence: Annual LCMs enhance change detection by distinguishing random classification errors (which flicker over time) from persistent real-world change.
  - Use cases: Monitoring state and change of land cover, informing environmental objectives, and supporting decision-making with 21 land cover classes aligned to BAP Broad Habitats (with caveats on exact equivalence).
  - Interpretation notes: Spectral confusion between certain classes can occur; context rasters significantly improve discrimination for some habitat types (e.g., various grassland types, bog, fen).
  - Coastal and water classes: Saltwater and Freshwater distinguished using coastal/near-shore context rasters and seasonal information; some confusion can occur in tidal rivers.
  - Data usage considerations: 10 m pixel data retains fine landscape detail but the validation is anchored to the 25 m Land Parcel framework; 1 km summaries are suitable for broad-scale monitoring and trend analysis.

- Appendices and supplementary guidance
  - Appendix 1 and 2: Notes on UKCEH Land Cover Classes and BAP Broad Habitats, including implications for mapping and potential spectral confusion.
  - Appendix 3: Full list of LCM2021 datasets by region.
  - Appendix 4: Correspondence matrices illustrating misclassification patterns and user/producer accuracy for representative classes.
  - Appendix 5 and 6: Recommended color recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options, to support consistent visualization in reports and dashboards.

- Limitations and considerations for monitoring frameworks
  - Spectral similarity between classes leads to inter-class confusion in some regions; ongoing improvements and training data updates are anticipated.
  - Some features may fall below the MMU and will not appear in parcel-based outputs; coastal and ephemeral features (temporary water bodies) may be underrepresented.
  - The linkage between UKCEH Land Cover Classes and UK BAP Broad Habitats is close but not exact; appendices provide clarifications to reduce ambiguity in reporting and interpretation.

- Key takeaway for monitoring and policy use
  - LCM2021 provides a rigorously produced, annually updated, 21-class land cover map for Great Britain and Northern Ireland, with rich metadata and parcel-based attributes to support robust environmental monitoring, state-and-change analysis, and decision-making, while acknowledging data governance, validation limitations, and classification uncertainties.