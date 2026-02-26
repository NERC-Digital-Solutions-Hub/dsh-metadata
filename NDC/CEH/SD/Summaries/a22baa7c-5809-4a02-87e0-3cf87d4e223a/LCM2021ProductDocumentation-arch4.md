# The UKCEH Land Cover Map for 2021

- The document is a user guide for the UKCEH Land Cover Map for 2021 (LCM2021), detailing data production, validation, and how to use the six datasets across Great Britain and Northern Ireland.
- LCM2021 aims to provide annual, consistent land-cover information to support monitoring and decision-making, with formal validation and notes on accuracy and limitations.

## Data product suite (datasets and structure)

- Six datasets in total (for GB and NI):
  - 10 m Classified Pixel datasets (GB and NI): classified pixels from Classification Scenes; first band = UKCEH Land Cover Class, second band = class membership probability (confidence).
  - Land Parcel datasets (GB and NI): created by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework; provide parcel-level attributes.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised version of parcels; three-band rasters carrying dominant land cover (_mode), classification confidence (_conf), and parcel purity (_purity).
  - 1 km raster products: summaries of 25 m data to 1 km pixels; include dominant class and percentage cover (for both classes and aggregates).
  - Seasonal Composite Images: Sentinel-2 derived seasonal composites (January–March, April–June, July–September, October–December) used for classification; 10 m to 50-band configurations; occasional data gaps handled by the algorithm.
  - Context Rasters: 10 m GB context rasters (e.g., height, aspect, slope, distance to features, foreshore masks, etc.) and 9 NI context rasters (similar set plus urban mask and coast/freshwater/road layers) to reduce spectral confusion.
- For GB, 32 Classification Scenes were used; for NI, a single Classification Scene (49-band) was created to cover NI land mass.

## How the data were produced

- Bootstrap Training: An automatic, training-data approach that uses historical land-cover maps (2018–2020) to create training observations for the current classification, reducing the need for new field data.
- Random Forest classification: A supervised RF classifier trained on Bootstrap Training data; 10,000 samples per class are drawn with replacement to balance learning across classes.
- Classification Scenes and segmentation: GB divided into ~100 x 100 km tiles for processing; NI used a single scene based on the minimum bounding rectangle of NI land mass.
- Seasonal Composite Images: Derived from Google Earth Engine using Sentinel-2 data, resampled to 10 m; four seasonal periods provide phenological information for differentiation of vegetation types.
- Context Rasters: Added to help discriminate spectrally similar classes (e.g., rocks vs. vegetation, coastal features) by incorporating terrain, proximity, and land-cover context.

## The UKCEH Land Parcel Spatial Framework and MMU

- Land Parcel Spatial Framework: A fixed set of land parcels (~0.5 ha minimum mapping unit, MMU) designed to represent discrete real-world units (fields, parks, urban areas, etc.). Parcellation helps reduce noise and supports change detection.
- Framework changes: The gid identifiers differ from LCM2015 due to reordering and indexing updates; spatial overlap remains the core comparison method for time-series analysis.
- Purpose: Parcels provide a stable structure to compare land cover over time; the 10 m pixel data is not generalized by parcel framework to preserve fine detail (useful for specialist applications).

## Validation and accuracy

- Validation: 35,182 reference points across all 21 LCM classes; data derived from GB countryside surveys, National Forest Inventory, Rural Payments Agency data, and bespoke validation points.
- Overall accuracy: 82.6% with a 95% confidence interval of 82.19%–82.99% (full thematic detail).
- Validation against 25 m rasterized parcel data; context is used to explain certain misclassifications and to guide interpretation of accuracy in maps.

## Data relationships and classification detail

- UKCEH Land Cover Classes vs UK Biodiversity Action Plan (BAP) Broad Habitats: 21 UKCEH Land Cover Classes are aligned to BAP Broad Habitats (with some deviations) to preserve historical comparability. Appendices discuss the mappings and notes on potential ambiguities.
- Class terminology and notes: Appendices provide guidance on how specific classes (e.g., Broadleaved woodland, Coniferous woodland, Arable, Various grasslands, Bracken, Bog, Saltmarsh, Urban/Suburban, etc.) relate to BAP broad habitats, including known spectral or contextual ambiguities and how context rasters improve detection in some cases (e.g., Neutral Grassland, Fen, Marsh, Swamp).
- Colour recipes (color tables) and color-blind-friendly versions are provided for displaying the Land Cover Classes.

## Practical considerations, usage and limitations

- Temporal updates: LCM2021 is designed to be part of an annual series to differentiate errors from real-world change; random classification errors are expected to flicker over time, while real changes persist.
- Data granularity and MMU caveats:
  - The 10 m Classified Pixels retain fine landscape detail (e.g., narrow features) but are not generalized by the Land Parcel Spatial Framework for this product.
  - Some features, especially smaller patches and narrow linear features, may be below the 0.5 ha MMU and thus represented differently in parcel vs. pixel products.
- Access considerations:
  - The seed Bootstrap Training method uses historic maps (2018–2020) for training data, and new methods can be applied to the whole catalogue if accuracy improvements are significant.
  - Some data gaps may occur in seasonal composites due to cloud cover; the classification algorithm tolerates partial spectral information to complete UK coverage.
- Validation caveats: While overall accuracy is 82.6%, some classes show varying producer's/user's accuracy, and some inter-class confusion is noted (e.g., Bog vs. Heather/Heather Grassland, Saltwater vs. Freshwater, various grassland types). The Appendix 4 matrices provide detailed class-level validation metrics.

## Dataset metadata and access (high-level)

- Coordinate systems:
  - Great Britain: British National Grid, EPSG 27700
  - Northern Ireland: Irish Grid, EPSG 29903
- Pixel/parcel resolutions:
  - 10 m: Classified Pixels (GB and NI)
  - 25 m: Rasterised Land Parcels (GB and NI)
  - 1 km: Summary products (GB and NI)
- Official dataset naming and structure are documented in Appendix 3 and associated metadata tables.

- In sum, LCM2021 provides a multi-scale, well-documented land-cover product suite for GB and NI, built on automated, bootstrap-trained RF classification, enriched with context data and seasonal signals, with explicit validation and clear notes on use, limitations, and alignment with historical habitat classifications.