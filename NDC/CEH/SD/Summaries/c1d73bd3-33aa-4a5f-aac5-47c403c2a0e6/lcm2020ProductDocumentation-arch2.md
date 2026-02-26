# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - This is the user guide for the UKCEH Land Cover Map for 2020 (LCM2020).
  - LCM2020 comprises six geospatial datasets for Great Britain (GB) and Northern Ireland (NI): three data layers per region (10 m Classified Pixels, Land Parcel attributes, and 25 m Rasterised Land Parcels).
  - The goal is to help users understand data production, validation, and accuracy to support informed decisions and monitoring of environmental health and policy performance over time.

- Land cover classification and classes
  - LCM2020 defines 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, with careful notes on differences between UKCEH classes and BAP Broad Habitats to maintain consistency and comparability with earlier products.
  - Classification is automated, based on Classification Scenes composed from Sentinel-2 Seasonal Composite Images plus Context Rasters, using Bootstrap Training and a Random Forest classifier.

- Data products and structure
  - 10 m Classified Pixel datasets (GB and NI)
    - Derived from Classification Scenes with a Random Forest probability for each class.
    - Band 1: most likely UKCEH Land Cover Class; Band 2: the associated class probability (confidence).
    - These pixels preserve high spatial detail and are not generalised by the Land Parcel Spatial Framework, suitable for specialist users.
  - Land Parcel datasets (GB and NI)
    - Result from intersecting 10 m Classified Pixels with the UKCEH Land Parcel Spatial Framework.
    - Provide parcel-level attributes and unique identifiers (gid) within region-specific coordinate systems (GB: EPSG 27700; NI: EPSG 29903).
    - Parcel counts: GB ~6.74 million parcels; NI ~0.90 million parcels.
  - 25 m Rasterised Land Parcel datasets (GB and NI)
    - Rasterised per parcel with 3 bands: dominant land cover (_mode), mean class probability (_conf), and parcel purity (_purity).
  - Seasonal Composite Images
    - Sentinel-2 multispectral data (bands 2,3,4,5,6,7,8,11,12) resampled to appropriate resolutions; seasonal medians computed for winter, spring, summer, and autumn.
    - Some seasonal gaps due to cloud cover, represented as nulls; classification can tolerate partial data.
  - Context Rasters
    - 10 m context layers to reduce spectral confusion; GB includes height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore and tidal water masks, and woodland mask.
    - NI includes height, aspect, slope, urban mask, and distances to coast, freshwater, and roads.
  - Classification Scenes and production approach
    - GB uses 100 x 100 km tiles to assemble 74 overlapping Classification Scenes; Scenes are trained and classified independently with some regional overlap for balance and accuracy.
    - NI uses a single 36-band Sentinel-2 Seasonal Composite Image plus NI Context Rasters to produce one Classification Scene per year (43 bands total).

- Methodology and training
  - Bootstrap Training
    - Automated, iterative training using historic LCMs (LCM2017–2019) to sample current satellite data; reduces need for costly ground-truth data.
    - Training datasets: GB 941,027 objects; NI 214,833 objects after filtering for >99% purity across three years.
  - Random Forest classification
    - Balanced sampling: 10,000 samples per class drawn with replacement to train the RF classifier.
    - Software stack includes a bespoke RF pipeline integrated with Weka, PostGIS, and GDAL (open-source).
  - Validation
    - Validation against countryside survey data (2019–2020), National Forest Inventory, IACS data, and bespoke LCM validation points (total 34,715 points).
    - Overall accuracy for LCM2020: 79.2% (just over 79% at full thematic detail; Appendix 4 presents full validation results).

- Data quality, interpretation, and cautions
  - Acknowledges that land cover products contain errors; no manual region-wide corrections are performed to enable annual production and comparability.
  - Annual maps help distinguish random errors (flicker over time) from real change (persisting signals).
  - Some spectral confusions persist (as detailed in Appendix 1 and 2), and certain upland and coastal habitats require contextual interpretation (e.g., peatlands, bracken, bracken vs acid grassland, brackish vs freshwater confusion near coasts).
  - MMU: minimum mapping unit ~0.5 hectares; small patches may be underrepresented in some classes, particularly those below the MMU or highly mosaicked (e.g., Fen/Marsh/Swamp patches, peatland vegetation).

- UKCEH Land Parcel Spatial Framework
  - The framework used for LCM2020 was developed from LCM2007 and updated since LCM2015; minor changes in storage and indices mean LCM2020 parcel identifiers do not exactly match LCM2015 identifiers.
  - Parcels are designed to represent discrete real-world units (e.g., fields, parks, urban areas) and are used to reduce classification noise and support change detection.

- Documentation, references, and appendix highlights
  - Appendix 1 and 2 provide detailed notes on UKCEH Land Cover Classes and their relationship to BAP Broad Habitats; they document potential sources of spectral confusion and mapping considerations.
  - Appendix 3 provides recommended color recipes for displaying UKCEH Land Cover Classes.
  - Appendix 4 contains the full correspondence matrices used in the validation process, including user’s and producer’s accuracies by class.
  - Appendix 5 lists the full set of LCM2020 datasets by region and product type.

- Practical implications for environmental monitoring
  - Enables standardized, annually updated maps to support monitoring of land cover change and environmental objectives across the UK.
  - Time-series consistency improves change detection and policy evaluation, while explicit caveats guide correct interpretation at fine spatial scales.
  - Encourages the use of both high-detail 10 m classified pixels for detailed analyses and parcel-based datasets for robust, comparable change metrics over time.