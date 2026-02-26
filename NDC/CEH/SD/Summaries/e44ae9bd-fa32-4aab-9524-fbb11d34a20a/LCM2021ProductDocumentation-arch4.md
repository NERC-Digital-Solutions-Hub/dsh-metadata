# The UKCEH Land Cover Map for 2021

- Purpose and scope
  - LCM2021 is the ninth UK land cover map produced by UKCEH, intended to help users understand land cover and support decision-making.
  - Dataset suite comprises six datasets across Great Britain and Northern Ireland: three per region – a 10 m Classified Pixel dataset, a Classified Land Parcel dataset, and a 25 m Rasterised Land Parcel dataset.
  - Additional derived outputs include 1 km raster products (dominant and percentage cover) summarising the 25 m data.
  - Formal validation reports an overall accuracy of 82.6%.

- Product suite and data structure
  - 10 m Classified Pixel dataset: per-pixel land cover class with a second band indicating classification probability/confidence; not generalised by the UKCEH Land Parcel Spatial Framework to preserve fine features; intended for specialist users.
  - Land Parcel dataset: links 10 m pixels to land parcels; includes attributes such as hist, mode, conf, purity, stdev, agg, n; designed to support change detection and parcel-level analysis.
  - 25 m Rasterised Land Parcel dataset: 3-band raster (dominant land cover, conf, purity) derived by rasterising parcel-level data.
  - 1 km products: derived by aggregating 25 m rasters; include Dominant cover at 1 km (class and aggregate), and Percentage cover at 1 km (21-class and 10-aggregate bands); rounding may cause sums to deviate from 100%.
  - Geographic coverage and references: GB uses British National Grid (EPSG:27700), NI uses Irish Grid (TM75, EPSG:29903); GB parcels approx. 6,741,288; NI parcels approx. 902,248.

- Data production: methodology and inputs
  - Core classes: 21 UKCEH Land Cover Classes, aligned loosely with Biodiversity Action Plan (BAP) Broad Habitats for consistency with earlier products.
  - Classification approach: automatic, using Bootstrap Training combined with Random Forest (RF) classifier.
  - Bootstrap Training: training data are generated from historic LCMs (LCM2018–LCM2020) by selecting parcels with >80% purity and consistent class across three years; used to train RF and bootstrap the next map.
  - Seasonal and contextual inputs: Classification Scenes comprise Sentinel-2 Seasonal Composite Images (four seasons) plus 10 Context Rasters to reduce spectral confusion; total of up to 50 bands per Scene (GB) or 49 bands (NI).
  - Seasonal composites: Sentinel-2 bands 2,3,4,5,6,7,8,8A,11,12 at respective resolutions; four seasonal periods (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec); cloud gaps are handled by the classifier.
  - Context rasters: GB uses terrain-related layers (Height, Aspect, Slope), proximity masks (distance to buildings, roads, sea, freshwater), foreshore and tidal masks, and a woodland mask; NI uses similar terrain layers plus urban mask and proximity layers.
  - Classification scenes and tiling: GB uses a grid of tiles (~100 x 100 km) resulting in 32 Classification Scenes for full GB coverage; NI uses a single Classification Scene for the landmass extent.

- The UKCEH Land Parcel Spatial Framework
  - Parcels have a minimum area of ~0.5 ha (MMU) and were derived by generalising national cartography to provide discrete, mappable units (e.g., fields, parks, woodlands).
  - Parcel identifiers (gid) differ from LCM2015; primarily impacts longitudinal comparisons by parcel ID rather than spatial overlap.
  - Parcel data structure supports aggregation of 10 m pixels into coherent land parcels, aiding change detection and data usability.

- Validation and accuracy
  - Validation dataset: 35,182 reference points covering all 21 classes, drawn from GB countryside surveys, National Forest Inventory, Rural Payments data, and bespoke validation points.
  - Reported accuracy: overall 82.6% with 95% confidence interval 82.19–82.99%.
  - Appendix 4 contains detailed confusion matrices; class-wise producer’s and user’s accuracies are reported to inform reliability of each class.

- UKCEH Land Cover Classes and BAP relationship
  - The 21 UKCEH Land Cover Classes map to, but are not identical to, UK BAP Broad Habitats; some BAP classes are split or combined for remote-sensing practicality.
  - Appendices describe class-to-BAP relationships, including notes on how certain habitats (e.g., Bracken, Bog, Neutral Grassland) are represented and potential spectral confusions.
  - Descriptive notes help users interpret classes and align historical or regulatory datasets with LCM2021 outputs.

- Practical considerations for data leaders (usage, governance, and uptake)
  - Annual production supports monitoring state and change and helps distinguish real change from random classification noise.
  - Provides high-resolution data suitable for policy colleagues and partners; supports co-ownership and iterative improvement of data products through user feedback.
  - Emphasizes metadata, discoverability, data quality, and appropriate use of the 10 m pixel dataset (not validated against parcel data) for nuanced analyses.
  - Encourages integration with wider data communities and ongoing method improvements; plans exist to re-apply methods if new techniques yield substantial accuracy gains.

- Limitations and caveats
  - 10 m Classified Pixel data are not validated against the Land Parcel dataset; users should be aware of differences when combining products.
  - Land Parcel identifiers changed since LCM2015, limiting direct parcel-ID-based historical comparisons.
  - Spectral similarity and boundary issues (e.g., Saltwater vs Freshwater, Neutral Grassland vs other grasslands) remain sources of confusion; context rasters and training data mitigate some issues but residual misclassification can occur.
  - Some very small patches remain below the 0.5 ha parcel minimum and may be underrepresented.

- Access, standards, and future directions
  - Outputs are provided in standard GIS-ready formats; the methodology supports improvements and potential re-application across the catalog if accuracy gains are achieved.
  - The project uses open-source tools (Weka, PostGIS, GDAL) and Google Earth Engine for processing.
  - The documentation includes detailed appendices (definitions, class mappings, and color palettes) to support map display and interpretation.

- Appendices: key references and guidance
  - Appendix 1–2 provide detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats terminology and mappings.
  - Appendix 3 lists official dataset names and metadata considerations for the LCM2021 products.
  - Appendix 4 presents full correspondence matrices (confusion matrices) for class-level accuracy assessment.
  - Appendix 5–6 offer recommended color palettes and color-blind-friendly alternatives for displaying the classes.