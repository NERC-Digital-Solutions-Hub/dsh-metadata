# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for LCM2020, a UKCEH land cover mapping product.
  - Comprises six geospatial datasets (three for Great Britain and Northern Ireland), each available as a 10m classified pixel dataset, a land parcel dataset, and a 25m rasterised land parcel dataset.
  - Aims to support informed decision-making by providing annually produced, map-based land cover information.
  - Classification is automated and designed to support temporal consistency and change detection; ongoing method improvements are anticipated.

- Product suite and data structure
  - 10m Classified Pixel datasets
    - GB and NI: classification result per 10m pixel with two bands.
      - Band 1: UKCEH Land Cover Class identifier.
      - Band 2: associated class membership probability (confidence).
    - GB pixels are not generalised by the UKCEH Land Parcel Spatial Framework to preserve detailed features; primarily for specialist use.
  - Land Parcel datasets
    - Derived by intersecting 10m classified pixels with the UKCEH Land Parcel Spatial Framework.
    - Attributes include details such as hist (frequency of classes within parcels), mode (dominant class), conf (mean class probability), stdev, agg (aggregate class), n (pixel count).
    - GB and NI parcel datasets use different national grid references (EPSG: 27700 for GB; EPSG: 29903 for NI).
  - 25m Rasterised Land Parcel datasets
    - Rasterised per parcel into 25m pixels with 3 bands: mode (dominant class), conf (mean parcel probability), purity (dominance of the modal class within the parcel).
  - Additional context and supporting layers
    - Seasonal Composite Images (Sentinel-2, seasonal medians for winter, spring, summer, autumn).
    - Context Rasters (10m) to reduce spectral confusion (GB) or to supplement classification (NI).
    - Classification Scenes (GB uses 100x100 km tiles; NI uses a single scene covering NI).
  - Dataset naming and extents
    - Appendix 5 provides the official dataset names; GB uses British National Grid; NI uses Irish grid.

- How the data are produced
  - Seasonal Composition and context information
    - Seasonal Composite Images derived from Sentinel-2 reflectance; 9 bands used; some seasons may have gaps due to cloud but classification handles partial data.
    - 10 Context Rasters per region to help resolve spectral confusion (GB: height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore mask, tidal mask, woodland mask; NI: height, aspect, slope, urban mask, distances to coast/freshwater/road).
  - Classification Scenes and training
    - GB: 74 overlapping 100x100 km Classification Scenes; NI: single 36-band Sentinel-2 Seasonal Composite Scene plus NI context rasters.
    - Bootstrap Training: fully automatic training using historic UKCEH maps (LCM2017–2019) filtered for high-purity parcels; large training sets (GB ~941k objects; NI ~214k).
    - Random Forest classifier trained with balanced sampling (10,000 samples per class, with replacement) to produce 10m classified pixels.
  - Validation approach
    - Validation against GB countryside survey (2019–2020), open data National Forest Inventory, IACS, and bespoke validation points (34715 points total).
    - Reported overall accuracy: 79.2% (full thematic detail; Appendix 4).

- Land Cover classes and selection
  - 21 UKCEH Land Cover Classes
    - Based on Biodiversity Action Plan (BAP) Broad Habitats but not identical; crosswalks and notes provided to preserve historical comparability.
    - Class relationships and distinctions (e.g., Urban vs Suburban; coniferous vs deciduous woodland) are described, with some caveats due to spectral similarity and context layers.
  - Relationship to BAP Broad Habitats
    - 21 classes are aligned to BAP Broad Habitats in most cases, but some BAP categories are represented differently due to remote sensing constraints.
    - Appendix 1 and Appendix 2 provide detailed mappings and notes on potential confusions (e.g., Bracken, Heather vs Heather Grassland, Fen/Marsh/Swamp, Saltwater vs Freshwater).

- Data specifications and spatial framework
  - UK Land Parcel Spatial Framework
    - 0.5 ha minimum unit (MMU).
    - Parcels generalised from national cartography; provides a fixed structure for change detection.
    - gid identifiers in LCM2020 do not match LCM2015; affects direct parcel-id comparisons over time.
  - Spatial resolution and formats
    - 10m pixel data for detailed features; 25m rasterised parcel data for parcel-level summaries.
    - 8-bit raster products; parcels are mapped with a minimum mapping unit of ~0.5 ha.
  - Data quality and limitations
    - Validation shows overall accuracy ~79.2%; recognition that some classes exhibit higher/ lower accuracy depending on spectral separation and training data limitations.
    - Annual production emphasizes distinguishing real change from classification error; random errors are expected to flicker year-to-year.

- Usage guidance and display
  - Colour and display
    - Appendix 3 provides a recommended color recipe for displaying UKCEH Land Cover Classes, with specific RGB values per class to aid map design.
  - Practical use
    - The 10m classified pixels retain detailed landscape features (useful for high-resolution mapping and change detection in small patches).
    - The Land Parcel dataset provides a structured, comparable basis for time-series analysis.
    - The 25m rasterised parcel data offers a coarser but aligned representation suitable for broader-scale analyses.
  - Applications
    - Suitable for environmental monitoring, policy planning, land management, and change detection across the UK countryside.

- References and further details
  - Technical references for methods: Bootstrap Training, Random Forest, Sentinel-2 processing, and historical LCM products.
  - Appendices summarize UK BAP Broad Habitats and provide detailed mappings, notes on class definitions, and a full validation matrix.
  - Appendix 4 presents full validation matrices; Appendix 5 lists the complete set of LCM2020 datasets.

- Key takeaways for GIS workflows
  - Access both pixel-level (10m) and parcel-level (land parcel and 25m raster) representations to suit different analysis scales.
  - Use context rasters and seasonal composites to interpret spectral signals and improve classification accuracy.
  - Be aware of the MMU constraints and gid changes when conducting temporal comparisons with earlier LCM products.
  - Refer to the provided color recipe and class mappings to ensure consistent map design and interoperability with BAP-based terminology.