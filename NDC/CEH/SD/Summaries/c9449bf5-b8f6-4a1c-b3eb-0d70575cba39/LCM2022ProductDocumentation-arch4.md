# The UKCEH Land Cover Map for 2022

- A user guide describing LCM2022, the UKCEH land cover map produced annually.
- Product scope: seven datasets (three per region: Great Britain and Northern Ireland) plus a 1 km summary raster product.
- Purpose: enable informed use of land cover data by detailing data production, validation, accuracy, and usage considerations.

## Data products and structure

- 10 m Classified Pixel datasets (GB and NI)
  - Derived from multiple Classification Scenes; classification via Bootstrap Training and Random Forest.
  - Output: two bands per pixel — most likely UKCEH Land Cover Class and associated confidence/probability.
  - 10 m granularity preserves fine landscape features; not generalised by Land Parcel Spatial Framework.
- Land Parcel datasets (GB and NI)
  - Land Parcel Spatial Framework applied to 10 m classified pixels to create parcel attributes.
  - Includes vector parcel data with detailed per-parcel attributes.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterized version of Land Parcel data at 25 m resolution; three bands: dominant land cover, mean confidence, parcel purity.
- Land Parcel Product (Vector)
  - Vector representation of land parcels with attributes derived from the 10 m raster data.
- 1 km Summary rasters (GB and NI)
  - Summary of 25 m data to 1 km cells: dominant class, dominant aggregate class, and percent cover per class/aggregate.
  - Percent cover values are integers; totals may exceed or fall short of 100% due to rounding; coastal pixels may sum below 100%.
- Seasonal Composite Images
  - Four-season Sentinel-2 composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) resampled to 10 m; provide temporal spectral information for classification.
- Context Rasters
  - 10 m context layers to reduce spectral confusion (terrain, proximity to buildings/roads/water, coastal/fjord masks, etc.); GB and NI differ slightly in exact rasters.
- Classification Scenes
  - GB classified in 32 tiles (approx. 100 x 100 km); NI uses a single Scene; training and classification per Scene, with occasional overlap.

## Production methodology and data lineage

- Bootstrap Training
  - Automatic training data generated from historic LCMs (LCM2019–LCM2021) and Crops data (for some classes) to train classifiers without new field data.
  - Ensures balanced learning across classes to improve detection of rarer classes.
- Random Forest classification
  - RF classifier trained on Bootstrap Training samples; majority class probability used for final class membership.
  - Software stack includes bespoke UKCEH tooling with WEKA, PostGIS, and GDAL (open-source).
- Data production goals
  - Annual production to maximize temporal consistency, comparability, and change detection.
  - Time-series aim: differentiate real change (persistent) from random classification errors (flicker).
- Validation and accuracy
  - Formal validation against 33,107 reference points across 21 classes.
  - Overall accuracy: 86.1% (full thematic detail).

## Land cover classes and relationships

- UKCEH 21 Land Cover Classes
  - Based on Biodiversity Action Plan (BAP) Broad Habitats; some distinctions are slightly different in practice due to remote-sensing constraints.
  - Appendices provide mappings and notes on how UKCEH classes relate to BAP Broad Habitats and where similarities/differences exist.
- Practical usage notes
  - Some classes (e.g., Saltwater vs Freshwater, certain wetland types) show spectral confusions; context rasters and training data help mitigate this.
  - Explanations and caveats are provided to aid interpretation and cross-walk with historical products.

## UKCEH Land Parcel Spatial Framework and MMU

- Spatial framework used to generalise land parcels (minimum mapping unit ~0.5 ha).
- Parcels typically dominated by a single land cover type; parcels help reduce classification noise and support change detection over time.
- Differences with previous datasets: unique identifiers (gid) no longer align with LCM2015 for parcel comparison; spatial overlap comparison may require alternative linking.

## Validation, known issues, and data quality

- Validation
  - 33,107 validation points across all classes; results reported as overall accuracy (86.1%) and class-specific producer’s and user’s accuracies (Appendix 4).
- Known issues
  - A small number of polygons missing from vector land parcel products, causing nodata areas in 25 m rasters; negligible effect on 1 km products.
  - 10 m classified pixels datasets are unaffected by these missing polygons.
- Disclaimer on methods
  - Methodological changes across annual maps mean some differences reflect changes in production approach, not only real land cover changes.

## Access, citations, and metadata

- Each LCM2022 dataset has a DOI; recommended to cite respective data products (see Table 5 in the guide).
- Related literature and production overview available (e.g., Marston et al., 2023; Marston et al., 2024a–g).
- Data products include detailed metadata, including coordinate systems, extents, pixel resolutions, bands, and validation information.

## Practical considerations for Data Leaders

- System-wide view
  - LCM2022 exemplifies a data-led, end-to-end mapping workflow: seasonality, context, scalable classification, and parcel-based aggregation.
  - Emphasizes the importance of metadata, lineage, and reproducibility for governance and reuse.
- Data availability and reuse
  - Seven primary datasets plus 1 km rasters support multiple downstream analyses (change detection, landscape monitoring, policy support).
  - Clear pathways for attribution via DOIs and citations; longitudinal comparability supported by Bootstrap Training and annual updates.
- Use within organisational data strategy
  - Highlights the balance between high-resolution detail (10 m) and harmonised parcel-level outputs (25 m rasters, vector parcels) for different analytical needs.
  - Demonstrates integration of open-source tools and substantial validation to inform data quality decisions.

Appendices (high-level)
- Appendix 1–2: Notes on UKCEH Land Cover Classes and their relation to BAP Broad Habitats; definitions and nuances for key classes.
- Appendix 3: Full list of LCM2022 datasets with DOIs and citations.
- Appendix 4: Correspondence matrices (confusion/accuracy details) for class-level assessment.
- Appendix 5–6: Colour recipes (including color-blind friendly options) for displaying LCM2022 classes in GIS environments.