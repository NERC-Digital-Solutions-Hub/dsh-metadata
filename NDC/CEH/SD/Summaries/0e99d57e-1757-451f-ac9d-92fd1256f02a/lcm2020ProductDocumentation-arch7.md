# The UKCEH Land Cover Map for 2020

- LCM2020 is the eighth UK land cover map produced by UK CEH, classifying land into 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP). It uses automated Bootstrap Training with a Random Forest classifier on Sentinel-2 Seasonal Composite Images plus 10 Context Raster Layers to create annual national land cover maps.

- The product suite comprises six datasets for Great Britain and Northern Ireland (GB and NI): three dataset types per region
  - 10m Classified Pixel datasets (GB and NI)
  - Land Parcel datasets (GB and NI)
  - 25m Rasterised Land Parcel datasets (GB and NI)
  - Additionally, a 20m Classified Raster Product for NI is listed in the dataset catalog.

- Classification and data structure
  - 10m Classified Pixels: output from Classification Scenes; two bands per pixel — band 1 = most likely UKCEH Land Cover Class, band 2 = class probability/confidence. These pixels preserve fine landscape detail and are not generalized to the Land Parcel Spatial Framework.
  - 25m Rasterised Land Parcels: three-band rasters per parcel — band 1 = modal land cover (_mode_), band 2 = mean class membership probability (_conf_), band 3 = parcel-level purity (_purity_). Per-parcel attributes are provided.
  - Land Parcel Spatial Framework: parcels are generalized, minimum area ~0.5 ha MMU; used to reduce noise and enable change detection over time. Unique identifiers (gid) changed from LCM2015, which may affect direct parcel-ID comparisons across years.

- Spatial framework and coordinates
  - GB datasets: EPSG: 27700 (OSGB36 / British National Grid); GB extents approx East 0–700,000 m; North 0–1,300,000 m.
  - NI datasets: EPSG: 29903 (Truncated Irish Grid); NI extents specified as East 180,000–400,000 m and North 300,000–500,000 m for the truncated NI grid.

- Seasonal inputs and classification scenes
  - Seasonal Composite Images: derived from Sentinel-2, four seasons (winter, spring, summer, autumn) with nine spectral bands (bands 2,3,4,5,6,7,8,11,12) resampled to 10–20 m; gaps due to clouds are tolerated by the classifier.
  - GB Classification Scenes: 74 overlapping 100x100 km tiles, producing 46-band Classification Scenes (36-band Sentinel-2 plus 10 Context Rasters). Each tile is trained and classified independently; overlaps may yield small regional differences, resolved by a manual precedence step.
  - NI Classification Scene: a single 36-band Sentinel-2 scene combined with 43-band NI Context Rasters.

- Context rasters
  - GB (10 rasters): height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore mask; tidal water mask; woodland mask.
  - NI (7 rasters): height, aspect, slope; urban mask; distance to coast, freshwater, roads.

- Bootstrap Training and classification
  - Bootstrap Training uses historic LCM maps (2017–2019) to automatically sample training observations from parcels with >99% purity across three years, generating large training sets.
  - GB training set: 941,027 objects; NI training set: 214,833 objects.
  - Random Forest classifier trained with balanced sampling (10,000 samples per class per bag) to ensure rare classes are adequately learned.
  - Software stack: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL open-source tools.

- Validation and accuracy
  - Validation against GB countryside survey (2019–2020), National Forest Inventory, IACS data, and bespoke validation points (34,715 points total) intersected with Land Parcel datasets.
  - Overall accuracy: 79.2% (Appendix 4).

- Relationship to BAP Broad Habitats
  - The 21 UKCEH Land Cover Classes are aligned with BAP Broad Habitats but are not identical; several mappings and notes explain translation, including italicised BAP terms when referencing Broad Habitats.
  - Appendices 1–2 provide detailed crosswalks and notes on how classes relate to BAP Broad Habitats, including specific nuances and potential spectral confusions.

- Data usage notes for GIS work
  - The 10m Classified Pixels retain detailed landscape features but were not generalized to the Land Parcel Framework; suitable for specialists who need fine-scale detail and are aware of potential differences with parcel-based products.
  - The Land Parcel Data allow easier time-series comparison and change detection, subject to changes in parcel identifiers between LCM2015 and LCM2020.
  - Expect some classification noise to be random year-to-year; annual maps help differentiate real change from random errors.

- Appendices and datasets catalog
  - Appendix 4 provides full validation matrices and class-level accuracies.
  - Appendix 5 lists the six official datasets with extents and naming conventions for GB and NI datasets, including 10m, 20m, and 25m products and their respective coordinate reference systems and extents.
  - Appendix 1–3 contain class notes, BAP Broad Habitat definitions, and recommended color recipes for displaying UKCEH Land Cover Classes.