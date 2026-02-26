# The UKCEH Land Cover Map for 2022

- A user guide for the UKCEH Land Cover Map 2022 (LCM2022), describing production, validation, data accuracy, and guidance for informed use.
- LCM2022 comprises seven datasets split across Great Britain (GB) and Northern Ireland (NI), plus a 1 km summary raster covering GB and NI.
- Goal: enable informed use, with emphasis on data production, validation, and accuracy, to support monitoring and decision-making.

## Data products and datasets

- 10 m Classified Pixel datasets
  - Generated from multiple Classification Scenes; each pixel gets a most-likely UKCEH Land Cover Class (first band) and a confidence/probability (second band).
  - Preserves 10 m detail (no aggregation to Land Parcel Framework) to retain small features; validation focused on the 25 m rasterised Land Parcel dataset.
- Land Parcel datasets
  - Result from intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework to produce parcel attributes (Table 3 attributes).
- 25 m Pixel Rasterised Land Parcel datasets
  - Rasterised version of Land Parcels with three bands: dominant land cover (mode), mean confidence (conf), and mean parcel purity (purity).
- Land Parcel products (vector)
  - Parcel-level attributes and identifiers (gid) for use in vector analysis and change detection.
- 1 km raster products
  - Summary rasters summarising 25 m data to 1 km cells:
    - Dominant class (1 band) and Dominant Aggregate class (1 band)
    - Percentage cover for 21 (classes) and 10 (aggregate) bands
  - Note: percentage values are rounded; coastal cells may sum to slightly less than 100 due to mapping resolution.
- Seasonal Composite Images and Context Rasters
  - Seasonal Composite Images derived from Sentinel-2 (four seasons), resampled to 10 m; context rasters provide terrain and proximity data to resolve spectral confusion.
  - Context rasters differ GB vs NI (e.g., Urban binary mask for NI; coastal/water masks for GB).
- Classification Scenes
  - GB: 32 tiles (classification scenes) for full GB coverage; NI: single 49-band scene, determined by NI extent.
- Coordinate systems and extents
  - GB: British National Grid (EPSG:27700)
  - NI: Irish Grid TM75 (EPSG:29903)
  - GB and NI parcel extents and pixel resolutions as specified (10 m and 25 m).

## Production workflow and methods

- Land cover mapping approach
  - Classifies Classification Scenes by combining Sentinel-2 Seasonal Composite Images with Context Rasters to form Classification Scenes.
  - Automatic classification using Bootstrap Training with a Random Forest (RF) classifier.
- Bootstrap Training
  - Uses historic LCM training data (LCM2019, LCM2020, LCM2021) filtered to pixels with >80% probability and consistent class across years.
  - Provides large, wall-to-wall training data to enable robust RF learning.
- Random Forest classification
  - Each Bootstrap Training pixel is assigned to a class; 10,000 samples per bag with replacement are drawn for balanced training across classes.
  - Software stack: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open-source).
- Data processing details
  - The 10 m Classified Pixels retain fine landscape features; 25 m rasterised parcels provide a stable, comparable product for time-series and change detection.
  - The UKCEH Land Parcel Spatial Framework generalises national cartography to ~0.5 ha MMU (minimum mapping unit).
- Seasonal and contextual data
  - Seasonal Composites: four seasons, Sentinel-2 bands 2,3,4,5,6,7,8,8A,11,12; gaps may occur but classification tolerates partial data.
  - Context rasters include height, slope, aspect, distance to buildings/roads/water, foreshore and land cover masks, etc. (GB and NI differences noted).

## Validation, accuracy, and known issues

- Validation and accuracy
  - Validation dataset: 33,107 points across all 21 UKCEH Land Cover Classes.
  - Overall accuracy: 86.1% for LCM2022 (full thematic detail).
  - Validation data drawn from GB countryside survey, National Forest Inventory, Rural Payments data, and bespoke validation points.
- Known issues
  - A small number of polygons missing from vector Land Parcel products; corresponding nodata areas in 25 m rasterised land parcels; negligible effect on 1 km products; 10 m pixels unaffected.
  - Unique parcel identifiers (gid) in LCM2022 do not match LCM2015 identifiers, affecting cross-year parcel ID comparisons (spatial overlap remains possible).
  - Differences in methods across annual updates mean some changes reflect methodological change as well as real land-cover change.
  - Bootstrap Training limitations for some classes (e.g., crops like arable and certain grasslands) where training data scarcity or historical style of change reduces performance; alternative training data (e.g., LCM Plus Crops) used in some cases.

## Data access, attribution, and citation

- DOIs and citations
  - Each LCM2022 dataset has a DOI and recommended citation (Table 5 in the document).
  - Key references: Marston et al. 2023/2024, Morton et al. 2011 and 2007, plus methodological sources on Random Forest and related tools.
- Data availability and use
  - Datasets are hosted by NERC EDS Environmental Information Data Centre; cited and versioned with DOIs.
  - Users should include the dataset DOIs and references when citing or re-using LCM2022 products.

## Governance, maintenance, and practical considerations for Data Stewards

- Update cadence and evolution
  - LCM2022 follows an annual production cycle with continuous method improvements; future maps may re-apply methods if accuracy gains are significant.
  - Temporal consistency is a design goal to facilitate change detection and reduce spurious year-to-year noise.
- Metadata, lineage, and provenance
  - Detailed metadata for each dataset, including spatial extent, resolution, coordinate system, bands, and quality metrics.
  - Clear documentation of Bootstrap Training, RF classification, and the Land Parcel Spatial Framework as data lineage.
- Interoperability and comparability
  - Relationships between UKCEH Land Cover Classes and UK BAP Broad Habitats illustrated; some differences and caveats explained to reduce ambiguity.
  - 10 m vs 25 m products provide complementary perspectives: fine-scale detail versus stable parcel-based units for change detection.
- Data governance and user guidance
  - Users should consider potential classification differences due to methodological changes across years.
  - Be aware of MMU and parcel framework when aggregating or comparing across products or time periods.
- Display and visualization
  - Appendix 5 and 6 provide color recipes (including color-blind friendly options) for displaying UKCEH Land Cover Classes; accompanying QGIS symbology files are provided.

## Cited references and further reading

- Core production and validation references: Marston et al. (2023, 2024), Carrasco et al. (2019), Breiman (2001), Morton et al. (2011), Smith et al. (2007).
- Appendix materials offer detailed definitions of UKCEH Land Cover Classes and BAP Broad Habitats for interpretation and mapping considerations.

- Summary note for data stewards: LCM2022 delivers high-resolution, annually produced land cover data for GB and NI with robust validation (86.1% overall accuracy), structured around a parcel framework to support change detection. It emphasizes transparent data lineage, clear caveats, and DOI-based citation, suitable for governance, discovery, and reuse within data catalogues and inter-organisational data networks.