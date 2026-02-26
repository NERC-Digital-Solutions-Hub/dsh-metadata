# The UKCEH Land Cover Map for 2023

- UKCEH’s eleventh land cover map (LCM2023) delivering 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats, derived from Sentinel-2 Seasonal Composite Images plus Context Rasters.
- Aim is to provide map-based data products that support monitoring, change detection and informed decision-making, with validation and data accuracy described for informed use.

## Product suite (datasets)

- Seven geospatial datasets for Great Britain and Northern Ireland (GB & NI):
  - 10 m Classified Pixel datasets (GB and NI): pixels classified to UKCEH Land Cover Classes with a second band for class membership probability.
  - Land Parcel datasets (GB and NI): land parcel geometry and attributes created by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised parcel data with three bands per parcel (dominant land cover class, mean confidence, and polygon purity).
  - 1 km summary raster product (GB and NI): four products summarising 25 m data into 1 km pixels (dominant class, dominant aggregate class, and percentage cover for classes/aggregates).
- Official dataset names and DOIs are provided; each dataset has its own citation.

## Geographic scope and coordinate systems

- GB: British National Grid (EPSG: 27700) for GB datasets.
- NI: Irish Grid TM75 (EPSG: 29903) for NI datasets.
- Land parcels: MMU ~0.5 ha; designed around discrete real-world units (fields, parks, urban areas, etc.) and intended for change detection.

## Data content and structure

- 10 m Classified Pixel dataset
  - Two bands: (1) most likely UKCEH Land Cover Class; (2) probability/confidence for the classification.
  - Preserves detailed landscape features (no generalisation to Land Parcel Spatial Framework) to retain narrow features.
- 25 m Rasterised Land Parcel dataset
  - 3 bands: band 1 (mode class per parcel), band 2 (conf), band 3 (purity).
- Land Parcel Spatial Framework
  - Provides a standardized framework to group 10 m pixels into meaningful parcels.
  - Some IDs differ from LCM2015 due to reorganisation of database storage; spatial overlap comparisons with 2015 not straightforward.
- 1 km summary rasters
  - Provide dominant class per 1 km pixel and percentage cover per class/aggregate.
  - Coalescing notes: percentages are integer values and may not sum exactly to 100 due to rounding; coastal areas may sum to less than 100.

## Seasonal and contextual data inputs

- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2: four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - Spectral bands include 2, 3, 4, 5, 6, 7, 8, 8A, 11, 12.
  - Occasionally seasonal gaps due to cloud; classifier tolerates partial spectral information.
- Context Rasters (10 m)
  - GB: height, aspect, slope; distance to buildings, roads, tidal water, freshwater; foreshore mask; woodland mask; saltmarsh mask.
  - NI: height, aspect, slope; urban mask; distance to coast, distance to freshwater, distance to roads; foreshore mask; tidal water mask.
  - Used to reduce spectral confusion in classification.

## Classification methodology

- Bootstrap Training
  - Automatic training dataset creation without new field data.
  - Uses historic LCM data (LCM2020–LCM2022) to sample current satellite imagery for training.
  - Pixels selected if >80% probability and consistently classified in all three years.
  - Addresses data scarcity and helps weather rare-class sampling.
- Random Forest classification
  - Ensemble RF classifier with 10,000 samples per class for training; balanced sampling to avoid dominance by common classes.
  - Implemented with bespoke UKCEH software integrating Weka, PostGIS and GDAL (open source).
- Validation and QA
  - Validation with 33,107 reference points across all 21 classes.
  - Overall accuracy: 83% for the 25 m rasterised land parcel dataset (and related products), with detailed class-level metrics provided in Appendix 4.

## Data quality, known issues, and caveats

- Known issues
  - A small number of polygons missing from vector land parcel products, causing nodata in derived 25 m parcel rasters; negligible effect on 1 km products; 10 m classified pixels datasets are unaffected.
- Interpretation notes
  - Some inter-class confusion remains (e.g., bog vs. acid grassland vs. fen/marsh) due to the nature of broad habitat definitions and spectral similarity.
  - Coastal Saltwater vs. Freshwater distinctions rely on context rasters and may have reduced accuracy in some coastal/estuarine settings.
  - Annual map changes reflect real change and/or methodological differences; validation is performed against a high-quality reference dataset.

## Usage guidance and presentation

- Data presentation
  - Appendix 5 provides recommended color schemes for display of UKCEH Land Cover Classes; Appendix 6 provides color-blind-friendly alternatives; QGIS symbology files accompany products.
- Data access and citation
  - Each LCM2023 dataset has a DOI; users should cite the appropriate dataset(s) per product (and consult Marston et al. 2023/2024 for production methods overview).
- Temporal context
  - The project emphasises annual production to distinguish true land cover change from classification error and to enhance change detection and temporal comparability.

## Production approach and future directions

- Annual production with continuous improvement
  - Methods are evolving; significant accuracy improvements may lead to re-application across the catalog to maximise temporal consistency and change-detection capabilities.
- Validation and accuracy goals
  - Formal validation shows 83% overall accuracy; ongoing improvements are expected to enhance class discrimination and reduce confusion in key habitat categories.

## Appendices (high-level highlights)

- Appendix 1 and 2
  - Notes on UKCEH Land Cover Classes and their relationship to Biodiversity Action Plan (BAP) Broad Habitats, with mapping nuances and class-specific considerations.
- Appendix 3
  - Full list of LCM2023 datasets and their DOIs.
- Appendix 4
  - Correspondence matrices (confusion matrices) for class-level performance, including user’s and producer’s accuracies.
- Appendix 5 and 6
  - Display color recipes (standard and color-blind friendly) and associated QGIS symbol files.