# The UKCEH Land Cover Map for 2021

- UKCEH’s ninth land cover map produced for Great Britain and Northern Ireland, with annual production to monitor state and change. Classifies land cover into 21 UKCEH Land Cover Classes (based on Biodiversity Broad Habitats) using automatic classification of Classification Scenes derived from Sentinel-2 Seasonal Composite Images plus 10 Context Rasters. Overall validation accuracy: 82.6% (95% CI: 82.19–82.99%).
- Production approach combines Bootstrap Training with a Random Forest classifier to enable annual updates and improve temporal comparability, while preserving the ability to detect real change vs. random classification errors.

## Data products and structure

- Six geospatial datasets (three per region: Great Britain and Northern Ireland):
  - 10 m Classified Pixel datasets
  - Land Parcel datasets
  - 25 m Rasterised Land Parcel datasets
  - Additionally, 1 km raster products summarize the 25 m data for broader use
- Datasets are described in Appendix 3; coordinate systems:
  - Great Britain: EPSG 27700 (British National Grid)
  - Northern Ireland: EPSG 29903 (TM75 Irish Grid)
- Key dataset characteristics:
  - 10 m Classified Pixels: two bands per pixel — class identifier (UKCEH Land Cover Class) and associated classification probability. Not generalized by the UKCEH Land Parcel Spatial Framework to preserve fine landscape detail.
  - Land Parcel dataset: attributes derived from intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework; minimum parcel size ~0.5 ha (MMU); gid unique identifier; _hist, _mode, _conf, _stdev, _agg, _n, and other parcel-level metadata.
  - 25 m Rasterised Land Parcel dataset: three-band raster per parcel (band1: modal class _mode; band2: mean class confidence _conf; band3: class purity _purity).
  - 1 km raster products: four products - dominant class (1-band) for both classes and aggregates, plus percentage cover (21 bands for classes, 10 bands for aggregates).
- Seasonal and Context data:
  - Seasonal Composite Images: four seasons from Sentinel-2 (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec); 50-band GB scenes (49-band NI scene) used for classification.
  - Context Rasters: 10 GB GB rasters (height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore, tidal water, woodland); NI includes urban mask and distance layers.
  - Classification Scenes: GB classified into 32 tiles (~100x100 km) with a 50-band Seasonal Composite plus context rasters; NI uses a single 49-band scene.
- Data products span the GB and NI regions with detailed metadata, including grid extents, parcel counts (GB ~6.74 million parcels; NI ~0.90 million parcels), and pixel resolutions (10 m and 25 m).

## Methods and data lineage

- Bootstrap Training: an automated training approach that samples training observations from historic UKCEH land cover maps (LCM2018–LCM2020) to train the classifier, reducing need for new field data. Training data are filtered to include parcels with >80% purity and consistent class across three years.
- Random Forest classification: balanced sampling (10,000 samples per bag) across classification Scenes to produce the 10 m Classified Pixel product. The process balances rare classes to avoid bias toward common classes.
- Classification workflow: uses a bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL; context rasters are used to reduce spectral confusion.
- Data framework: UK Land Parcel Spatial Framework (0.5 ha MMU) provides structured parcel-based output and supports change detection across years.
- Catalogue and update scope: annual production aims for temporal consistency and comparability; if new methods yield significant improvements, UKCEH may re-apply across the catalogue to maximize consistency.

## Validation and accuracy

- Validation involved 35,182 reference points across all 21 classes; the overall accuracy is 82.6% with a 95% confidence interval of 82.19%–82.99%.
- Appendix 4 contains detailed confusion matrices and producer’s/user’s accuracy by class, illustrating inter-class confusion (e.g., Saltmarsh, Urban, Suburban, Bracken, Bog, Neutral/Calcareous/Acid Grassland, etc.) and the varying levels of classification confidence per class.
- Validation references derived from a composite dataset (GB countryside survey, National Forest Inventory, Rural Payments data, and manual/field validation).

## Spatial details and metadata

- Datasets and naming: Appendix 3 lists official dataset names for GB and NI holdings (10 m Classified Pixels, Land Parcel Product, 25 m Rasterised Land Parcel Product).
- Spatial extents and grids: GB extent in British National Grid; NI extent in Irish Grid; classification tiles for GB and single NI scene ensure manageable processing and local adaptability.
- MMU and parcel framework: Land Parcel Spatial Framework uses minimum mapping unit ~0.5 ha; parcels typically dominated by a single land cover type but not guaranteed.
- Crosswalk to BAP Broad Habitats: Appendix 1/2 describe the relationship between UKCEH Land Cover Classes and Biodiversity Action Plan Broad Habitats, including where mappings differ and where ambiguities arise.

## Data governance and stewardship considerations

- Provenance and lineage: outputs are derived from Bootstrap Training using historical maps and Sentinel-2 data; maintain clear documentation of training data sources and year-to-year changes for auditability.
- Interoperability and comparability: 10 m Classified Pixels retain high detail but are not aligned to the Land Parcel Spatial Framework, which may affect cross-year parcel-based analyses; gid values in NI/GB parcels differ from LCM2015, complicating long-term cross-year comparisons by parcel identifiers.
- Metadata and documentation: comprehensive metadata available (dataset descriptions, classification parameters, context rasters, validation results, and appendix details); Appendix 3–6 provide dataset naming, validation, and display guidance.
- Limitations and transparency: known spectral confusion among land cover types (e.g., Arable vs. Improved Grassland, various Grassland types, Saltwater vs Freshwater near coasts); some very small patches remain below MMU; Saltwater classification is partly boundary-determined by coastal context rasters.
- Update and governance: annual production supports change detection but requires ongoing maintenance of training data, classification schemas, and cross-year comparability; potential re-application of methods across datasets if accuracy improvements are realized.

## Guidance for use and caveats

- Use cases:
  - 10 m Classified Pixels for detailed, high-resolution mapping tasks where fine-grained patterns matter (specialist users only due to lack of generalized parcel framework).
  - 25 m Rasterised Land Parcels for stable, parcel-based analyses and change detection over time.
  - 1 km products for broad-scale landscape assessments and regional planning.
- Cautions:
  - Interpret results with awareness of class-specific accuracy and potential spectral confusion; review Appendix 4 confusion matrices for class-level performance.
  - When comparing to previous LCM releases, be mindful of changes in parcel identifiers and the Land Parcel Spatial Framework; cross-year comparisons by spatial unit may require spatial overlap methods rather than parcel-id matching.
  - Coastal and water classes (Saltwater vs Freshwater; Supralittoral/Littoral categories) rely heavily on Context Rasters; coastal dynamics may affect accuracy in tidal zones.
- Display and dissemination:
  - Appendices 5 and 6 provide recommended color recipes for displaying UKCEH Land Cover Classes and color-blind friendly schemes to support consistent map rendering.

## Appendices and supplementary information at a glance

- Appendix 1: Notes on UKCEH Land Cover Classes with interpretation guidance and cautions regarding spectral confusion.
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions and the relationship to UKCEH classes.
- Appendix 3: Full list of UKCEH LCM2021 datasets (GB and NI).
- Appendix 4: Correspondence matrices (confusion matrices) showing class-by-class accuracy and producer’s/user’s accuracy.
- Appendix 5–6: Colour schemes for displaying classes (standard and color-blind friendly).
- Additional references and methodological details referenced throughout the document.