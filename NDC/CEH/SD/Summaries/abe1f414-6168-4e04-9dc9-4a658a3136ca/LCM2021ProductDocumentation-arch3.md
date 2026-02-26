# The UKCEH Land Cover Map for 2021

- UKCEH’s ninth national land cover map (LCM2021) covering Great Britain and Northern Ireland.
- Provides 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats, with careful mapping to maintain consistency with past products.
- Aims to enable monitoring of land cover state and change to inform policy and decision-making.

## Purpose and scope

- Describes data production, validation, and data accuracy to support informed application of LCM2021 in current and future work.
- Supports monitoring, change detection, and environmental objectives through an annually updated land cover dataset.
- Emphasises the need for understanding data structure and limitations for appropriate use.

## UKCEH Land Cover Classes and BAP relationships

- 21 UKCEH Land Cover Classes are closely related to BAP Broad Habitats but are not identical; the guide explains the mapping and where deviations occur.
- Appendices provide detailed definitions and relationships, including notes on when UKCEH classes align with or differ from BAP Broad Habitats.
- A general- or aggregate-class option (UKCEH Aggregate Classes) is provided to accommodate users needing simplified classifications.

## Datasets and product suite (GB and NI)

- Three primary geospatial datasets per mass: 10 m Classified Pixel datasets, Land Parcel datasets, and 25 m Rasterised Land Parcel datasets.
- A total of six datasets across GB and NI (GB and NI each have 10 m Classified Pixels, Land Parcel Product, and 25 m Rasterised Land Parcel Product).
- Additional 1 km raster products summarize 25 m data to 1 km squares (dominant class and percentage cover for both classes and aggregates).
- Appendix 3 lists official dataset names; Appendix 4 provides confusion matrices and accuracy metrics; Appendix 5 and 6 give color recipes for displaying classes.

## Data inputs and structural elements

- Seasonal Composite Images: Sentinel-2 data resampled to 10 m, four seasons (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with 10 spectral bands; occasional gaps handled by classifier tolerance.
- Context Rasters: 10 contextual layers to reduce spectral confusion (GB: height, aspect, slope, distance to buildings/roads/sea/freshwater, foreshore and tidal masks, woodland mask; NI: height, aspect, slope, urban mask, distances to coast, freshwater, roads, foreshore and tidal masks).
- Classification Scenes: GB uses a grid of tiles (~100 x 100 km) resulting in 32 Classification Scenes for GB; NI uses a single 49-band Scene for Northern Ireland.
- Land Parcel Spatial Framework: defines parcel-level units (~0.5 ha MMU) used to generalise 10 m pixels into discrete parcels for stable change detection.

## Data production workflow

- Bootstrap Training: automatic training data derived from historic LCMs (LCM2018–LCM2020) filtered for >80% purity and consistent class across years; used to bootstrap current classification.
- Random Forest classification: supervised learning using Bootstrap Training; 10,000 samples per class with replacement to balance classes; produces the 10 m Classified Pixel dataset and the associated probability/confidence per pixel.
- Parcel-level synthesis: 10 m Classified Pixels intersected with the Land Parcel Spatial Framework to generate parcel attributes and produce the Land Parcel dataset (including statistics like purity, confidence, and aggregation).
- Rasterised parcels and 1 km products: Land Parcel dataset rasterised to 25 m pixels; 1 km products summarise 25 m data to derive dominant class and percentage cover per 1 km pixel.

## Validation, accuracy, and caveats

- Validation: 35,182 reference points across all 21 classes; composite validation dataset drawn from GB countryside surveys, open data inventories, and bespoke validation points.
- Overall accuracy: 82.6% (95% CI: 82.19%–82.99%) for the 25 m rasterised parcel validation; the 10 m pixel data were not independently validated against the 10 m dataset but against the 25 m parcel framework.
- Notes on limitations: spectral confusion between similar classes (especially in coastal, urban, wetland, and certain habitat types); coarser MMU can affect detection of small features; Saltwater vs Freshwater distinctions are partly driven by coastal context rasters; some BAP Broad Habitat distinctions (e.g., bog, fen, acid grassland) exhibit inter-class confusion; linear features and shape-based distinctions are not captured by current spectral methods.
- Validation caveat: formal validation was performed against the 25 m Land Parcel dataset, not the 10 m Classified Pixels.

## Practical data characteristics and accessibility

- Coordinate systems: GB uses British National Grid (OSGB36, EPSG 27700); NI uses Irish Grid (TM75, EPSG 29903).
- Parcel counts: GB ~6,741,288 parcels; NI ~902,248 parcels.
- Pixel resolutions: 10 m and 25 m for classified pixels and rasterised parcels; 1 km summary products created from 25 m data.
- Data governance and openness: outputs are shared with underlying data, and governance processes are in place; however, publicly sharing datasets can be a barrier for some users, highlighting the importance of data management and governance for reuse and transparency.
- Update cadence: annual production to maximize temporal consistency, comparability, and change detection; potential re-application of methods to all products if significant accuracy improvements arise.

## Technical and usage notes for monitoring framework practitioners

- The 10 m Classified Pixel dataset provides detailed spatial features but is not generalised by the Land Parcel Framework; best suited to specialist users who understand how this affects validation and interpretation.
- The Land Parcel and 1 km products enable robust time-series comparisons and change detection with a fixed spatial framework.
- The methodological approach (Bootstrap Training + Random Forest + Contextual layers) supports scalable, repeatable national mapping while allowing updates as new data and methods become available.
- Appendix resources offer detailed mappings between UKCEH classes and BAP Broad Habitats, including guidance for interpretation and potential field-based or habitat-based crosswalks.
- Colour recipes (Appendix 5 and 6) provide guidance for consistent visualisation of classes, including color-blind friendly options.

## Endnotes and references

- The guide includes references to foundational works on Random Forests, Sentinel-2 and Google Earth Engine-based classifications, and historical UK land cover mapping programs.
- Appendices provide comprehensive notes on UKCEH Land Cover Classes, BAP Broad Habitats, full dataset lists, correspondence matrices, and display recommendations.