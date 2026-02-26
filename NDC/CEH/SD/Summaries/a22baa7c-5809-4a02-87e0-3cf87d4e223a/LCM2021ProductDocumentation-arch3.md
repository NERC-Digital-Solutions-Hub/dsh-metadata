# The UKCEH Land Cover Map for 2021

- Purpose of the document
  - User guide for LCM2021, detailing data production, validation, accuracy, and guidance for informed use in current and future work.

- What LCM2021 is
  - Ninth UK land cover map produced by UKCEH, aligned with 21 UKCEH Land Cover Classes based on Biodiversity Broad Habitats (BAP).
  - Classifications produced automatically using Bootstrap Training with a Random Forest classifier.
  - Aims to maximise temporal consistency, comparability, and change detection to support environmental objectives.

- Data products (datasets)
  - Six datasets across Great Britain and Northern Ireland, comprising three core products for each area:
    - 10 m Classified Pixel datasets (GB and NI)
      - Pixel-level land cover class (UKCEH Land Cover Class) plus a confidence/probability band.
      - No generalisation with the UKCEH Land Parcel Spatial Framework to preserve fine-scale features.
    - Land Parcel datasets (GB and NI)
      - Connects 10 m pixels to land parcels via the UKCEH Land Parcel Spatial Framework.
      - Parcel-level attributes such as hist (frequency per class), mode (dominant class), purity, confidence, standard deviation, aggregated class, and count.
    - 25 m Rasterised Land Parcel datasets (GB and NI)
      - Rasterised per-parcel outputs with three bands: per-parcel Land Cover (mode), mean confidence (conf), per-parcel purity (purity).
  - Additional 1 km raster products (summary level)
    - Dominant cover (1 km) for both classes and aggregates (1-band).
    - Percentage cover (1 km) for both classes and aggregates (multi-band; 21 for classes, 10 for aggregates).
    - Note: rounding means some totals may not sum exactly to 100; coastal areas may be underrepresented due to mapping resolution and MMU.

- Seasonal and contextual data used in classification
  - Seasonal Composite Images
    - Derived from Sentinel-2, 10 m resolution, four seasons (January–March, April–June, July–September, October–December).
    - Bands 2, 3, 4, 5, 6, 7, 8, 8A, 11, 12 used; occasional gaps due to cloud are accommodated.
  - Context Rasters (10 m)
    - Britain: height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal water mask, woodland mask.
    - Northern Ireland: height, aspect, slope, urban mask, distance to coast, freshwater, roads, foreshore mask, tidal water mask.
  - Classification Scenes
    - GB: 32 scenes formed on a modified 100 x 100 km OS tile grid; each scene classified independently with 50-band seasonal data plus 10 context rasters (total about 60 bands per scene).
    - NI: single 49-band classification scene combining a 40-band Sentinel-2 Seasonal Composite with NI context rasters.
  - Bootstrapping and training
    - Bootstrap Training uses historic LCMs (LCM2018–LCM2020) to derive training samples, selecting parcels with >80% purity and consistent class across three years.
    - RF classifier trained with balanced sampling (10,000 samples per bag) to ensure adequate representation of all classes.

- UKCEH Land Parcel Spatial Framework
  - Framework developed for LCM2007 and refined for LCM2015; MMU of ~0.5 ha.
  - Parcels represent discrete real-world units (fields, parks, urban areas, etc.) and help smooth noise for change detection.
  - Updated storage and indices for faster processing; gid identifiers may not align with LCM2015 when comparing parcels.

- Validation and accuracy
  - Validation dataset: 35,182 reference points spanning all 21 classes.
  - Overall accuracy: 82.6% (95% CI: 82.19%–82.99%).
  - Validation data derived from GB countryside survey, National Forest Inventory, Rural Payments Agency data, and bespoke points.

- Data access, structure, and implementation notes
  - Coordinate systems
    - Great Britain: British National Grid (EPSG 27700)
    - Northern Ireland: Irish Grid (EPSG 29903)
  - Datasets include metadata-rich attributes (e.g., _hist, _mode, _conf, _purity, _n, _agg) for detailed parcel-level analysis.
  - The 10 m Classified Pixel product preserves fine landscape features; the 25 m rasterised parcel product provides a simplified, parcel-based view suitable for broader analyses.
  - Some class-level spectral confusion is acknowledged (e.g., between certain grassland types, bog, fen, scrub, and urban features), and context layers help mitigate misclassification.
  - Saltwater vs Freshwater distinctions near coastlines can be challenging; Saltwater is driven largely by coastal context rasters and may have slightly lower accuracy than Freshwater in some areas.

- Practical use for monitoring frameworks and policy scrutiny
  - Enables annual monitoring of land cover state and change, distinguishing real land surface change from random mapping noise due to the temporal series.
  - Provides multi-scale outputs:
    - 10 m pixel data for fine-grained monitoring and detailed habitat analysis (with high spatial detail).
    - 25 m parcel data and 1 km summaries for integration with policy reporting, planning, and regional analyses.
  - Facilitates change detection over time, supporting environmental objectives and trend analyses while allowing cross-walks to BAP Broad Habitats.
  - Bootstrap Training and automated RF classification reduce the need for fresh field data, enabling scalable, repeated mapping with consistent methodology.

- Metadata, governance, and barriers
  - Public sharing of underlying data is supported but may face governance and accessibility constraints; outputs are designed to promote openness and comparability.
  - Data governance processes are in place to ensure standardisation, storage, and update of datasets; notes on alignment with historical products are provided (gid changes between LCM2015 and LCM2021).

- Appendices and additional resources
  - Appendix 1–2: notes on UKCEH Land Cover Classes and BAP Broad Habitats, including mappings and nuances in interpretation.
  - Appendix 3–4: full list of datasets and correspondence matrices for validation (including user/producer accuracy across classes).
  - Appendix 5–6: recommended colour recipes for displaying UKCEH Land Cover Classes, including colour-blind friendly palettes.
  - Data descriptions and official dataset names are provided to assist data management, sharing, and integration into monitoring frameworks.

- Key considerations for monitoring and policy decision-making
  - Use annual LCM2021 outputs to separate real change from random errors; leverage the 1 km and 10 m products for different policy and reporting needs.
  - Recognise and account for potential classification confusions (notably among grassland types, bog/fen, heather-related classes, and coastal classifications) and employ context rasters and parcel-level data to improve interpretation.
  - Exploit Bootstrap Training to maintain a scalable, up-to-date training framework and reduce field data collection burdens.
  - Consider MMU limitations and the 0.5 ha parcel minimum when aggregating results for policy reporting or ecological assessments.
  - Align analyses with BAP Broad Habitats where relevant, using the mappings and notes to interpret land cover classes in ecological terms.