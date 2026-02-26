# The UKCEH Land Cover Map for 2022

- The LCM2022 is the UKCEH land cover mapping product for 2022, produced annually using automated methods and spanning Great Britain (GB) and Northern Ireland (NI).
- It comprises seven datasets: three for GB and NI (10 m classified pixels, land parcels, and 25 m rasterised land parcels) plus a 1 km summary raster product covering GB and NI. Appendix 3 lists official dataset names.

## Key concepts and structure

- 21 UKCEH Land Cover Classes: mapped classes are tied to Biodiversity Action Plan (BAP) Broad Habitats; relationships between UKCEH classes and BAP categories are described in appendices. Classes are capitalized when referring to a defined class.
- Classification framework: Classification Scenes combine Sentinel-2 Seasonal Composite Images with Context Rasters to produce training data and classify land cover automatically via Bootstrap Training and Random Forest (RF).
- Seasonal information: Seasonal Composite Images are derived from Sentinel-2 across four seasons to provide phenological signals for better discrimination of vegetation types.
- Context rasters: 10 m contextual layers reduce spectral confusions (e.g., terrain, proximity to buildings/roads, coastal features, water, vegetation masks). NI and GB have slightly different context rasters.

## Data products and how they are structured

- 10 m Classified Pixel datasets (GB and NI)
  - Two-band rasters per location: Band 1 = most probable UKCEH Land Cover Class (integer ID); Band 2 = probability/confidence (0–100 scale).
  - Not generalised by Land Parcel Spatial Framework to preserve fine features (e.g., narrow patches).
  - Validation was performed against the 25 m rasterised land parcel dataset; 10 m data remain unvalidated at pixel level in this version.
- Land Parcel datasets (GB and NI)
  - Vector land parcels derived from the 10 m classified pixels using the UKCEH Land Parcel Spatial Framework (minimum parcel size ~0.5 ha).
  - Parcel-level attributes summarize how pixels within each parcel map to land cover classes.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterise the Land Parcel dataset to 25 m resolution; three 8-bit bands carried forward from parcels:
    - Band 1: dominant land cover class (mode)
    - Band 2: mean class membership confidence (conf)
    - Band 3: parcel-level purity (purity)
- 1 km Summary rasters (GB and NI)
  - Dominant class at 1 km resolution (one band for class; one for aggregate class).
  - Percentage cover at 1 km for each class (21 bands for classes; 10 bands for aggregates). Values are integer percentages; sums may differ from 100 due to rounding and coastal effects.
- Seasonal Composite Images
  - Four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) from Sentinel-2, 10 m resampled; occasional cloud-related gaps but the classifier tolerates partial data.
- Classification Scenes
  - GB: 32 Classification Scenes tiled across the GB land surface (roughly 100 x 100 km tiles; some larger in remote/sea-heavy areas).
  - NI: Single Classification Scene aligned to NI extents (minimum bounding rectangle).
- UKCEH Land Parcel Spatial Framework
  - Framework used to define land parcels (~0.5 ha minimum) and to provide stable units for change detection; parcel identifiers may not align with LCM2015 due to framework reordering.
- Coordinate systems and extent
  - GB: British National Grid (EPSG 27700)
  - NI: Irish Grid (TM75, EPSG 29903)

## How the data are produced

- Bootstrap Training
  - Automated training data generation without fresh field data.
  - Uses historic LCM outputs (LCM2019–LCM2021) filtered for high certainty (>80% probability) and consistent class across three years to train the RF classifier.
  - This approach leverages large, wall-to-wall historical coverage to balance learning across classes.
- Random Forest classification
  - RF classifier trained on Bootstrap Training pixels; 10,000 samples per bootstrap bag with replacement to balance class representation.
  - Produces the 10 m Classified Pixel dataset; outputs include per-pixel class and associated confidence.
- Data fusion and context
  - Classification Scenes integrate spectral information (Seasonal Composite Images) with Context Rasters to reduce misclassifications due to spectral similarity.
- Validation
  - 33,107 validation points across all 21 classes, using a composite reference dataset from field surveys and validation points.
  - Overall accuracy reported: 86.1%.

## Data accessibility, metadata, and citations

- DOIs and citations are provided for each dataset. The document lists DOIs and references for 10 m classified pixels (GB and NI), 25 m rasterised land parcels (GB and NI), land parcels (GB and NI), and 1 km summary rasters (GB and NI).
- Primary literature for production methods: Marston et al. (2023–2024) series; overview in Marston et al. 2024g for 1 km products; related historical methodological papers cited in the document.
- Notes on usage
  - Outputs may differ year-to-year due to method updates; changes reflect real change, methodological updates, and data availability.
  - Output products are designed to enable downstream analysis, change detection, and cross-year comparisons, with clear metadata on class relationships and validation.

## Known issues and caveats

- Known issues
  - A small number of polygons are missing from the vector Land Parcel products, causing nodata areas in the 25 m rasterised land parcels. Impact on 1 km products is negligible; 10 m classified pixels are unaffected.
- Accuracy and interpretation
  - Overall thematic accuracy is 86.1% at 21-class detail; inter-class confusion remains for some broad habitats (e.g., various grassland types, bog/fen, and bracken interactions).
  - Saltwater and coastal water signals can exhibit occasional confusion with freshwater and non-vegetated surfaces, particularly near tidal zones.
- Comparison across datasets
  - The 10 m classified pixels are not directly overlapped with the Land Parcel framework for validation purposes; validation is against the 25 m rasterised land parcel dataset.
- Parcel identifiers
  - Land Parcel identifiers (gid) in the new framework do not match those from LCM2015 parcel datasets for direct comparison, due to reordering and index changes in the spatial framework.

## Practical notes for data users

- Data formats and viewing
  - 10 m classified pixels: two-band raster with class ID and confidence per pixel; suitable for direct mapping, but not generalised to parcel units.
  - 25 m parcel rasters: three-band rasters suitable for per-parcel analysis and aggregation within the Land Parcel Spatial Framework.
  - Land Parcel vector product: comprehensive parcel attributes for change detection and analysis at the parcel level.
  - 1 km rasters: suitable for regional-scale summaries and integration with other 1 km datasets.
- Class definitions and display
  - Appendix materials provide detailed definitions and relationships between UKCEH Land Cover Classes and BAP Broad Habitats. Appendix 5 and 6 offer recommended color schemes and color-blind friendly palettes (plus QGIS symbology files) for mapping these classes.
- How to cite
  - Each dataset has a DOI; use the DOIs and the accompanying references when citing LCM2022 data products. See the listed Table 5 in the document for the exact DOIs and citations.
- Applicability
  - The annual production facilitates monitoring of state and change in the UK countryside and supports environmental objectives, with the understanding that methodological refinements may yield small year-to-year differences independent of actual land-cover change.

## Appendix highlights (high level)

- UKCEH Land Cover Classes
  - 21 classes linked to UK BAP Broad Habitats (with notes on where BAP and UKCEH classifications diverge and how they map to each other).
- BAP Broad Habitats overview
  - Descriptions of Broad Habitats such as Broadleaved woodlands, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Fen/Marsh/Swamp, Bog, Standing Open Water, Rivers and Streams, Montane, Inland Rock, Urban and Suburban, Supralittoral/Littoral habitats, etc.
- Datasets list
  - Full list of LCM2022 datasets with region, citations, and DOIs (10 m classified pixels GB/NI, land parcels GB/NI, 25 m rasterised land parcels GB/NI, and 1 km summary rasters GB/NI).
- Display palettes
  - Appendix 5 and 6 provide color recipes for standard and color-blind-friendly display, plus accompanying QGIS style files (lcm_raster.qml and lcm_raster_cb_friendly.qml).