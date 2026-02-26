# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - UKCEH’s eighth land cover map (LCM2020) delivering 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats.
  - Aims to support monitoring of state and change, inform policy, and guide future decisions; designed for annual production to enhance change detection and temporal consistency.
  - Includes guidance on data production, validation, accuracy, and appropriate use.

- Data products and structure
  - Three geospatial datasets per region (GB and Northern Ireland):
    - 10m Classified Pixel datasets: pixel-level land cover classifications with a probability/confidence band; first band = most likely class, second band = class membership confidence.
    - Land Parcel Spatial Framework: parcels that group pixels to reduce classification noise and enable change detection.
    - 25m Rasterised Land Parcel datasets: per-parcel raster products carrying three attributes (mode, conf, purity) over 25m pixels.
  - Plus 1km summary raster products for GB and NI (dominant class, percentage cover for classes and aggregates).
  - Appendix 6 lists the official dataset names; seven products in total (GB and NI combined).
  - Coordinate systems:
    - GB: British National Grid (EPSG 27700)
    - NI: TM75 Irish Grid (EPSG 29903)

- Classification methodology
  - Seasonal Composite Images and context rasters
    - Seasonal composites from Sentinel-2 (winter, spring, summer, autumn) using nine spectral bands; context rasters (10 layers) capture terrain and proximity to features (buildings, roads, coast, freshwater, etc.).
  - Classification Scenes and tiling
    - GB uses 100x100 km tiles producing 74 overlapping Classification Scenes (46-band per scene); NI uses a single Classification Scene per year (43-band).
    - Scenes are trained and classified independently; overlaps provide robustness; minor differences due to separate training observations.
  - Bootstrap Training
    - Fully automatic training using historic LCMs (2017–2019) filtered for high-purity parcels (>99% across three years), yielding large training sets (GB ~941,027; NI ~214,833).
    - Enables training without new field data, leveraging wall-to-wall historic coverage.
  - Random Forest classification
    - Training samples are drawn with replacement to ensure class balance; 10,000 samples per bag; RF classifier yields 10m Classified Pixels with two-band output (class ID, mean probability/confidence).
  - Validation and accuracy
    - Validation against GB countryside survey data (2019–2020), National Forest Inventory, IACS, and bespoke validation points (total 34,715 points).
    - Overall accuracy: 79.2% (full thematic detail) per Appendix 5.

- Land Parcel framework and data governance
  - UK Land Parcel Spatial Framework designed to represent discrete real-world units (minimum mapping unit ~0.5 ha) and reduce classification noise for stable time-series comparisons.
  - Parcels facilitate change detection and cross-time analyses, though unique parcel identifiers (gid) differ from LCM2015, affecting cross-year parcel-based comparisons.
  - Data sharing and metadata considerations are addressed through openly produced outputs (maps, reports, and data products) to support transparency and reuse.

- UKCEH Land Cover Classes and BAP Broad Habitats
  - 21 UKCEH Land Cover Classes mapped to UK BAP Broad Habitats; historical BAP nomenclature is retained for consistency and comparability with earlier products.
  - Appendices provide detailed mappings, notes, and considerations for interpreting classes (e.g., spectral ambiguity, context layers aiding discrimination).

- Seasonal components and contextual data
  - Seasonal Composite Images (Sentinel-2) provide temporal signals to differentiate vegetation types.
  - Context Rasters (GB and NI) include terrain (height, aspect, slope) and proximity masks (buildings, roads, sea, freshwater) to resolve spectral confusion.

- Practical outputs and usage guidance
  - 10m Classified Pixels: two-band rasters (class ID, confidence) suitable for specialist users who understand the limitations of not being generalized by the Land Parcel framework.
  - 25m Rasterised Land Parcels: consolidated parcel-level outputs with per-parcel mode, confidence, and purity metrics.
  - 1km rasters: summarised products describing dominant class and percentage cover (with rounding implications near 100% sums and coastlines).
  - Validation context and accuracy metrics provided to support decision-making and uncertainty assessment.

- Appendices and additional notes
  - Appendix 1–3: Class definitions, BAP Broad Habitat mappings, and recommended color schemes for display (including color-blind friendly versions).
  - Appendix 5: Detailed correspondence matrices and accuracy statistics by class.
  - Appendix 6: Full list of LCM2020 datasets and their official names.

- Relevance to monitoring framework authors
  - Demonstrates an automated, repeatable monitoring workflow that minimizes field data needs through Bootstrap Training and historic map priors.
  - Combines high-resolution imagery, contextual data, and machine learning (Random Forest) to produce timely, policy-relevant environmental state information.
  - Provides transparent validation, clear data products, and well-documented relationships to legacy habitat classifications, aiding comparability over time.
  - Addresses data challenges such as metadata clarity, data governance, and data sharing by detailing dataset structure, provenance, and validation processes.