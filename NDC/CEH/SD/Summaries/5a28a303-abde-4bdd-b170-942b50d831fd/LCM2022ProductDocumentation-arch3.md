# The UKCEH Land Cover Map for 2022

- Purpose and scope
  - User guide for UKCEH Land Cover Map 2022 (LCM2022).
  - Product suite: seven geospatial datasets (three per region: Great Britain and Northern Ireland) plus a 1 km summary raster.
  - Aims to aid monitoring, policy scrutiny, and decision-making by providing detailed land cover information and data quality guidance.
  - Emphasises data production, validation, accuracy, and informed use of the data.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI): pixel-level land cover classification with two bands — the dominant UKCEH Land Cover Class and the associated class probability/confidence.
  - Land Parcel datasets (GB and NI): derived by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework to create parcel-level attributes.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised representation of land parcels with three bands — dominant land cover class (_mode), mean confidence (_conf), and parcel purity (_purity).
  - 1 km Raster products (GB and NI): summarize 25 m rasters to compute dominant class and percentage cover per 1 km pixel (both for classes and aggregates).
  - Seasonal composite images and context rasters underpin classification.

- Classification methodology
  - Classification Scenes: 10 m pixels are classified within 32 GB tiles (Great Britain) and a single NI scene, using a 49-band input (Sentinel-2 Seasonal Composite Images plus Context Rasters).
  - Seasonal composites: Sentinel-2 data resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) used to capture phenology.
  - Context rasters (GB): terrain height, aspect, slope, distances to buildings/roads/tidal water/freshwater, foreshore mask, woodland mask, and saltmarsh mask.
  - Context rasters (NI): height, aspect, slope, urban mask, distance to coast, freshwater, road, foreshore mask, tidal water mask.
  - Bootstrap Training: automatic training data derived from historical LCMs (LCM2019–2021) by selecting pixels with >80% probability consistently classified the same class across years; used to train a Random Forest classifier.
  - Random Forest: 10,000 samples per bag with replacement to balance class representation; classification yields the final 10 m pixel product.
  - Software: bespoke classifier integrating Weka, PostGIS, and GDAL (open source).

- Data quality, validation, and known issues
  - Validation: 33,107 validation points across the UK; overall accuracy 86.1% at full thematic detail (LCM2022).
  - Known issues: small numbers of missing polygons in the vector Land Parcel products, causing nodata areas in the 25 m rasterised parcels (negligible effect on 1 km products); 10 m classified pixels not used in formal validation (validation done on 25 m parcel data).
  - Users should expect some classification confusion among botanically similar habitats; the appendices discuss class-specific nuances and common misclassifications.
  - Disclaimer on year-to-year differences: small methodological changes can yield shifts; users should consider potential methodological changes when comparing across years.

- Relationship to biodiversity and class definitions
  - UKCEH Land Cover Classes (21 classes) are aligned with UK Biodiversity Action Plan (BAP) Broad Habitats, though not identical.
  - Descriptions and crosswalks provided to facilitate interpretation and comparability with BAP Broad Habitats.
  - Appendices detail class definitions, notes on potential spectral confusion, and guidance for interpreting distant or spectrally similar classes.

- Accessibility, citations, and data governance
  - Each LCM2022 dataset has a DOI; citations provided for all products (10 m classified pixels, land parcels, 25 m rasterised parcels, land parcels, and 1 km rasters).
  - Users are encouraged to cite the respective dataset DOIs and related Marston et al. publications where appropriate.
  - The guide discusses data governance considerations, including metadata and data sharing implications for frameworks that require open data.

- Practical guidance for monitoring framework authors
  - Supports policy monitoring and decision-making with annual, comparable land cover maps enabling change detection and trend analyses.
  - Provides detailed metadata, validation metrics, and known limitations to inform surveillance design and uncertainty assessment.
  - Offers crosswalks to BAP Broad Habitats to assist integration with regulatory and biodiversity reporting frameworks.
  - Includes resource for reproducibility: methodological descriptions, dataset lists, and DOIs to enable traceability and reuse.

- Appendices and additional resources
  - Appendix 1 and 2: UKCEH Land Cover Classes, BAP Broad Habitat relationships, and nuanced notes on individual classes.
  - Appendix 3: Full list of LCM2022 datasets with DOIs and citations.
  - Appendix 4: Correspondence matrices (confusion/accuracy) for class-level validation outcomes.
  - Appendix 5 and 6: Colour schemes and colour-blind friendly options for displaying classes, with accompanying QGIS symbol files.