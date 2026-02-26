# The UKCEH Land Cover Map for 2023

- Purpose and scope
  - User guide for UKCEH Land Cover Map 2023 (LCM2023), detailing data production, validation, accuracy, and guidance for informed use in policy monitoring and decision-making.
  - Product suite includes seven geospatial datasets (three for Great Britain and Northern Ireland each): three data types at different resolutions plus a 1 km summary raster product.
  - Aims to support monitoring of UK countryside state and change and to assist environmental objectives, with annual updates to maximise temporal consistency and change detection.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI)
  - 25 m Rasterised Land Parcel datasets (GB and NI)
  - Land Parcel Vector datasets
  - 1 km Summary Raster products (GB and NI; includes dominant class and percentage cover)
  - UKCEH Land Cover Classes: 21 classes derived from Biodiversity Action Plan (BAP) Broad Habitats; relationships to BAP are documented and sometimes split (e.g., Urban vs Suburban; Heather vs Heather grassland).

- Production workflow and components
  - Seasonal Composite Images: Sentinel-2 data resampled to 10 m; four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) used to capture phenology; 10-band spectral information plus contextual data.
  - Context Rasters (10 m): GB and NI-specific layers to reduce spectral confusion (e.g., terrain, distance to buildings/roads/water, foreshore, woodland, saltmarsh; urban mask for NI).
  - Classification Scenes: GB uses a grid of 32 classification scenes (~100 x 100 km tiles); NI uses a single 49-band scene for the island.
  - Bootstrap Training: automatic, data-driven training avoiding new field collection; uses historic LCM data (LCM2020–LCM2022) with >80% probability and consistent class across three years to train a Random Forest classifier.
  - Random Forest classifier: balanced sampling (10,000 samples per bootstrapped bag) to prevent dominance by common classes; output includes the most likely class and a confidence/probability band.
  - UK Land Parcel Spatial Framework: MMU ~0.5 ha; parcels aggregate pixels to reduce noise and enable change detection; parcel IDs (gid) are re-ordered in LCM2023, so cross-version parcel comparisons by ID may be nontrivial.

- Validation, accuracy, and caveats
  - Validation: 33,107 reference points across all 21 classes, combining countryside surveys, open data inventories, bespoke validation points.
  - Overall accuracy: 83% for LCM2023 (full thematic detail).
  - Validation against the 25 m rasterised land parcel dataset (not the 10 m classified pixels).
  - Known issues: a small number of polygons missing from vector land parcel products (negligible impact on 1 km products); 10 m classified pixels unaffected.

- Dataset details and standards
  - Coordinate systems: GB – British National Grid (EPSG 27700); NI – Irish grid TM75 (EPSG 29903).
  - 10 m Classified Pixels: two-band product per region (class ID and confidence). No generalisation to Land Parcel Spatial Framework in this dataset to preserve detailed landscape features.
  - 25 m Rasterised Land Parcels: three-band raster (dominant land cover class _mode, confidence _conf, and purity _purity) per parcel.
  - 1 km summary rasters: dominant class (1 band) and percentage cover (21 bands for classes; 10 bands for aggregate classes); percentages are integer values with rounding leading to possible sums not exactly 100.
  - Data product DOIs and citations are provided for each dataset; see Table 5 in the document for details.

- Seasonal, contextual, and spatial considerations
  - Seasonal composites enable temporal differentiation of classes; gaps due to cloud are handled by the classifier’s tolerance to partial spectral information.
  - Context rasters address spectral confusion among spectrally similar classes (e.g., rocks vs vegetation, urban vs bare ground).
  - The Classification Scene approach ensures manageable processing and accommodates regional phenological variation; some tile extents are adjusted to account for sea/land balance.

- Method transparency, governance, and use in monitoring
  - Methods are documented to aid monitoring framework decision-making, including how data are produced, validated, and how to interpret accuracy and confidence.
  - The project emphasizes transparency in data provenance, metadata, and data sharing; metadata and underlying data sharing can be barriers in some contexts.
  - Data governance considerations include the need to keep datasets up to date, openness of datasets, and the management of data provenance and quality control.

- Usage guidance and caveats for policymakers
  - Annual maps help distinguish real land cover change from random classification errors; persistent changes across years indicate genuine change.
  - The distinction between BAP Broad Habitats and UKCEH Land Cover Classes is maintained for continuity with earlier products, with careful notes on potential ambiguities.
  - Users should reference the DOIs and cited literature when using LCM2023 data in analyses or policy reporting.

- Citations, references, and collaborative notes
  - LCM2023 data products are associated with DOIs; recommended citations include Marston et al. (2024a–g) and related methodological papers (e.g., Marston et al. 2023; Breiman 2001).
  - Disclaimer: slight methodological changes across recent maps mean some differences may reflect production changes rather than real land cover change.

- Appendices and additional context
  - Appendix 1 and 2 provide notes on UKCEH Land Cover Classes and BAP Broad Habitat definitions, including considerations for class interpretation and common spectral confusions.
  - Appendix 3 lists full datasets and their citations.
  - Appendix 4 includes correspondence matrices illustrating classifier performance and user/producer accuracies by class.
  - Appendices 5 and 6 provide recommended color recipes for visualizing land cover classes (including color-blind friendly options) and accompanying QGIS files.