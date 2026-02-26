# The UKCEH Land Cover Map 2021

- Purpose and scope
  - User guide for LCM2021, UKCEH's annual land cover map.
  - Six datasets across Great Britain and Northern Ireland: three datasets per region.
  - Datasets include a 10 m classified pixel dataset, a dataset of classified land parcels, and a 25 m pixel (rasterised) land parcel dataset.
  - Annual production supports change detection, temporal consistency, and monitoring of the UK countryside.

- Product suite and data structure
  - 10 m Classified Pixel dataset
    - Derived from Classification Scenes; each pixel receives a most-likely UKCEH Land Cover Class.
    - Band 1: class identifier; Band 2: class probability/confidence.
    - Preserves fine landscape detail by not generalising with the Land Parcel Spatial Framework.
  - Land Parcel dataset
    - Created by intersecting 10 m pixels with the UKCEH Land Parcel Spatial Framework.
    - Provides parcel attributes and per-pixel breakdowns; parcels are designed to be approximately 0.5 ha (minimum mapping unit).
    - Used to reduce classification noise and facilitate change detection.
  - 25 m Rasterised Land Parcel dataset
    - Rasterised version of parcels with 3 bands: dominant land cover (mode), mean confidence (_conf), and mean purity (_purity).
  - 1 km raster products
    - Summaries of 25 m data: dominant cover (class and aggregate) and percentage cover (for both classes and aggregates) across 1 km pixels.
    - Percentage products are integer-valued; sums may not exactly equal 100 due to rounding.
  - Seasonal Composite Images
    - Four-season Sentinel-2 composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) derived from Google Earth Engine at 10 m resolution.
    - Include spectral bands and contextual information to improve discrimination of land cover types.
    - Occasional cloud gaps; the classifier tolerates partial spectral information.
  - Context Rasters
    - To reduce spectral confusion; GB uses 10 context rasters (e.g., height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore and tidal masks, woodland mask).
    - NI uses a mixed set including urban mask and distance layers to coast, freshwater, and roads.
  - Classification Scenes
    - GB: a grid of 32 tiles (~100 x 100 km each) for processing; NI: a single scene determined by NI land mass.
    - 49-band configuration for NI classification (Seasonal Composite + NI context rasters).
  - UK Land Parcel Spatial Framework
    - Framework used to structure parcel-level data; MMU ~0.5 ha; parcels aligned with national cartography.
    - Changes from LCM2015 mean parcel identifiers (gid) do not match exactly across years.
  - Bootstrap Training and Random Forest
    - Bootstrap Training uses historic land cover maps (LCM2018–LCM2020) to generate training data.
    - Balanced training with 10,000 samples per bag; RF classifier used to produce 10 m classified pixels.
    - Self-contained pipeline integrating Weka, PostGIS, and GDAL (open-source tools).
  - Validation and accuracy
    - Validation dataset: 35,182 points covering all 21 UKCEH Land Cover Classes.
    - Overall accuracy: 82.6% (95% CI: 82.19% – 82.99%).

- Data provenance, standards, and interpretation
  - UKCEH Land Cover Classes (21 classes) align with Biodiversity Action Plan (BAP) Broad Habitats but are not identical; some classes are combined or split to maintain spectral mapping feasibility.
  - Appendices detail relationships between UKCEH classes and BAP Broad Habitats, and guidance on interpretation and potential spectral confusion.
  - Data assets include explicit metadata on class definitions, validation, and the relationships to BAP habitats.

- Spatial references and extent
  - Great Britain: British National Grid (OSGB 27700).
  - Northern Ireland: Irish Grid (TM75, EPSG 29903).
  - Parcel counts: GB ~6,741,288 parcels; NI ~902,248 parcels.
  - Datasets delivered as 8-bit rasters for classification outputs; 10 m and 25 m resolutions; 1 km summary products.

- Data quality, limitations, and interpretation guidance
  - Validation is at 25 m raster level; 10 m pixel classifications are not re-validated against parcel framework, so some very fine features may differ in downstream parcel analyses.
  - Spectral confusion remains for certain habitats (e.g., bog, heather, acid vs neutral grassland); context rasters and seasonal signals improve discrimination but some ambiguity persists.
  - Saltwater vs Freshwater can be challenging in coastal and tidal areas; coastal classification emphasizes detection of water features rather than fine coastal land cover details.

- Temporal and update strategy
  - Aims for annual production to maximize temporal consistency and change detection capabilities.
  - Annual maps help distinguish real-world change from random classification error (errors are expected to flicker over time).

- Use considerations for data leaders
  - Clear data lineage: bootstrap training relying on LCM2018–LCM2020; evolving methods with potential cross-year re-application for consistency.
  - Emphasis on data quality and provenance: detailed validation, confidence metrics per pixel, and explicit notes on dataset limitations.
  - Interoperability and accessibility: standardized dataset naming, coordinate systems, and public-facing documentation; datasets are designed to support policy analysis, environmental monitoring, and cross-sector collaboration.
  - Community and collaboration: alignment with national habitat classifications while enabling cross-comparison across time and with older LCM products; opportunities for broader use through the 10 m detail and 25 m parcel-level products.

- Appendices and display guidance (highlights)
  - Appendix 1–2: notes on UKCEH Land Cover Classes and BAP Broad Habitats, including mapping nuances and interpretation guidance.
  - Appendix 3–4: official dataset names and validation matrices, including producer’s and user’s accuracy statistics by class.
  - Appendix 5–6: recommended color recipes for displaying UKCEH Land Cover Classes (including color-blind friendly options) to facilitate effective visual communication.