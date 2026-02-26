# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- Purpose and scope
  - User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Each map comprises a suite of geospatial datasets describing land cover across Great Britain and Northern Ireland.
  - 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats; emphasis on enabling informed decision-making and monitoring of environmental change.
  - Automatic production approach described; aims to help users apply data confidently and understand production choices, validation, and future plans.

- Content and structure
  - Datasets include 20m Classified Pixels, Land Parcels, 25m Rasterised Land Parcels, 1km Percent Cover (21 bands), 1km Percent Aggregate Cover (10 bands), 1km Dominant Cover (1 band), and 1km Dominant Aggregate Cover (1 band).
  - Separate GB and Northern Ireland (NI) versions; GB extents use 0–7000 km East and 0–1300 km North in British National Grid (EPSG:27700); NI uses Irish Grid (TM75, EPSG:29903).
  - Pixel classifications and parcel-level attributes are designed to support change detection and spatial analysis at multiple scales.
  - Appendix materials explain class derivations, relationships to UK BAP Broad Habitats, and color conventions for visualization.

- Production methodology and data sources
  - Bootstrap Training: automatic, self-starting training using historic LCM observations (primarily from LCM2015) to derive spectral training data for current imagery; future maps plan to bootstrap from majority signals across successive years.
  - Random Forest classification: supervised learning using balanced training samples (10,000 per bag) drawn with replacement; produces the 20m Classified Pixels product.
  - Seasonal Composite Images: Sentinel-2 TOA reflectance composites by season (winter, spring, summer, autumn) at 20m; used to create Classification Scenes.
  - Context Rasters: 20m contextual layers (terrain, proximity to buildings, roads, coast, freshwater, foreshore, tides, woodland) to reduce spectral confusion.
  - Classification Scenes: GB produced as 100x100 km tiles (36-band seasonal + 10 context = 46 bands; total 74 tiles overlapped to ensure training balance). NI uses a single 43-band year-specific Classification Scene.
  - UK Land Parcel Spatial Framework: fixed 0.5 ha minimum parcel size; 21 UKCEH Land Cover Classes mapped within parcels; parcel identifiers (gid) enable temporal comparisons (note gid changes between LCM2015 and later maps).
  - Output design philosophy: preserves detailed 20m information where useful (20m Classified Pixels) while providing aggregated parcel- and grid-based products for broader analysis.

- Data governance, metadata and usability notes
  - Detailed dataset descriptions, attribute definitions, and metadata are provided (Tables 2–5; Appendix 1–2; Appendix 5 lists datasets per year).
  - Pixel-level classification includes a confidence metric per pixel (Band 2 in 20m Classified Pixels; value 0–100).
  - Land Parcel attributes include hist (histogram of pixel class distribution within the parcel), mode, purity, conf (confidence), stdev, and n (number of pixels).
  - Some attribute name changes exist to align with production software conventions; users may need to adjust references when migrating from LCM2015.
  - Full validation is UK-wide using countryside survey data, National Forest Inventory, IACS, and bespoke validation points; results indicate approximately 78.6–79.6% overall accuracy for the three products, with class-by-class performance summarized in confusion matrices (Appendix 4).

- Product validation and accuracy
  - Validation scale: 22,325 validation points intersected with LCM Land Parcel datasets (GB and NI).
  - Reported overall accuracy: LCM2017 ≈ 78.6%, LCM2018 ≈ 79.6%, LCM2019 ≈ 79.4%.
  - Validation notes emphasize that accuracy is a best-available indicator, not absolute truth; cross-year consistency and updates will improve with methodology maturation.

- Key technical details and datasets
  - Dataset specifics
    - 20m Classified Pixels: RF-derived pixel classification with class probability; preserves fine-detail features (not generalized by parcels).
    - Land Parcels: parcel-level attributes including _hist (per-class pixel frequencies), _mode, _purity, _conf, _stdev, and _n.
    - 25m Rasterised Land Parcels: three bands per parcel raster (band 1: _mode, band 2: _conf, band 3: _purity).
    - 1km Raster datasets: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).
  - Spatial extents and grids
    - GB extents use British National Grid (EPSG:27700); NI extents use Irish Grid (EPSG:29903).
    - Pixel sizes: Classified Pixels at 20m; Land Parcels at 25m; Percent/Dominant rasters at 1km.
  - Dataset relationships and evolution
    - Datasets follow the LCM2015 lineage with minor attribute changes to support production efficiency.
    - The Land Parcel Spatial Framework is retained for comparability, but gid uniqueness means cross-year parcel IDs may differ; gid-based comparison is recommended for LCM2017–2019.

- Visualization and accessibility
  - Appendix 3 provides recommended RGB color recipes linking colors to each UKCEH Land Cover Class for map display.
  - The document includes visual figures demonstrating examples of 20m Classified Pixels, Land Parcels, and 25m Rasterised Land Parcels, as well asSeasonal Composite and Classification Scene workflows.

- Future plans and usage guidance
  - The release cadence targets annual updates (LCM2017–2019 demonstrate rapid production enabled by automation; plans to maintain annual publication).
  - Potential enhancements include expanding satellite input options (e.g., considering Sentinel-1 radar data and alternative optical sources to fill seasonal gaps) and exploring higher-resolution, finer parcel frameworks as data capabilities evolve.
  - Users are encouraged to consult Appendix 4 for validation details and Appendix 5 for a full list of year-specific datasets.

- Key references and appendices
  - Appendices provide detailed notes on UKCEH Land Cover Classes (Appendix 1), Biodiversity Action Plan Broad Habitats (Appendix 2), color recipes (Appendix 3), validation matrices (Appendix 4), and complete dataset listings (Appendix 5).