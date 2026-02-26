# The UKCEH Land Cover Map for 2021

- Ninth UK land cover map produced by UKCEH (LCM2021); aimed at providing annual, comparable land cover data for the UK.
- Product consists of six geospatial datasets (three for Great Britain and three for Northern Ireland):
  - 10 m Classified Pixel datasets (GB and NI)
  - Land Parcel datasets (GB and NI)
  - 25 m Rasterised Land Parcel datasets (GB and NI)
- Also supported by derived products at 1 km resolution (dominant class and percentage cover for both GB and NI) to aid broader-scale analyses.
- 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats (with careful cross-referencing to maintain historical continuity).
- Formal validation reports an overall accuracy of 82.6% (95% CI: 82.19%–82.99%).

- Dataset scope and class structure
  - UKCEH Land Cover Classes are defined from BAP broad habitats and mapped using satellite imagery and context layers; general narrative and appendices explain relationships and ambiguities with BAP terminology.
  - 21 classes include: Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral Grassland, Calcareous Grassland, Acid Grassland, Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, Standing Open Water and Canals, Rivers and Streams, Montane, Inland Rock, Built-Up Areas and Gardens (Urban and Suburban), Supralittoral Rock, Supralittoral Sediment, Littoral Rock, Littoral Sediment, Saltmarsh, and Urban/Suburban distinctions.
  - The LCM2021 dataset is designed to capture both detailed 10 m pixel-level information and coarser parcel-based summaries for change detection and governance needs.

- Production chain and data structures
  - Seasonal Composite Images: derived from Google Earth Engine using Sentinel-2 data; four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) at 10 m with 10 spectral bands; gaps represented as nulls but handled by the classifier.
  - Context Rasters: 10 m context layers used to reduce spectral confusion (GB: height, aspect, slope, distances to buildings, roads, sea, freshwater, foreshore, tidal waters, woodland; NI: height, aspect, slope, urban mask, distances to coast, freshwater, roads, foreshore, tidal waters).
  - Classification Scenes: GB classified on a grid of tiles (~100 x 100 km) producing 50-band scenes; NI uses a single 49-band scene. Each Classification Scene is trained and classified independently.
  - Bootstrap Training: an automatic, data-driven training approach that uses historic LCM maps (LCM2018–LCM2020) with >80% purity and consistent class across three years to sample training observations, enabling stable RF training without new field data.
  - Random Forest classification: 10,000 samples per class per scene, balanced via sampling with replacement to avoid dominance by common classes; the classifier outputs the 10 m Classified Pixel product, with a second band indicating the associated class probability.
  - UKCEH Land Parcel Spatial Framework: a fixed 0.5 ha minimum mapping unit (MMU) used to aggregate 10 m pixels into land parcels for consistent change detection and analysis; parcels have structured attributes and a defined GID, though the parcel identifiers do not align exactly with LCM2015.
  - 25 m Pixel Rasterised Land Parcel datasets: 25 m rasters derived by rasterising the land parcels, carrying three attributes (dominant land cover class, mean probability/confidence, and parcel purity) per parcel.
  - 1 km raster products: summaries of the 25 m rasters to provide dominant class per 1 km pixel and percentage cover per class/aggregate class, noting rounding effects and coastal area variability.
  - Data extents and coordinates: Great Britain uses British National Grid (EPSG 27700); Northern Ireland uses Irish Grid (TM75, EPSG 29903).

- Data accessibility and metadata
  - Official dataset naming and structure are documented (Appendix 3 lists dataset names for GB and NI).
  - The 10 m Classified Pixel datasets preserve detailed features not generalized by the Land Parcel framework, suitable for specialist users who understand the trade-offs between pixel-level detail and parcel-level generalisation.
  - The 25 m Rasterised Land Parcel datasets provide a stable, production-friendly summary aligned to the Land Parcel Spatial Framework.
  - The 1 km products provide a scalable, coarse-resolution overview for broad analyses, with caveats on exact total percentages due to rounding near coastlines.

- Validation, accuracy, and caveats
  - Validation used 35,182 reference points across all 21 classes, combining GB countryside survey data, National Forest Inventory data, Rural Payments data, and bespoke validation points.
  - Overall accuracy: 82.6% (95% CI 82.19%–82.99%).
  - Appendix 4 provides confusion matrices and class-level producer and user accuracies; notable variability exists across classes (e.g., Arable, Improved Grassland, Heather-related classes, Saltwater, Freshwater, and Urban/Suburban distinctions).
  - Important caveats for data stewards:
    - The 10 m Classified Pixel dataset is not generalised by the UKCEH Land Parcel Spatial Framework, so intricate features (e.g., narrow linear elements) are preserved, but validation was performed against the 25 m Land Parcel dataset, not the 10 m pixel data.
    - Relationship and mapping between UKCEH Land Cover Classes and UK BAP Broad Habitats can be ambiguous; Appendix 1 and Appendix 2 provide guidance and notes for distinguishing terms.
    - Parcel identifiers (gid) do not align with LCM2015 when comparing across versions; spatial overlap is the recommended comparison approach.

- Methodological notes relevant to data governance
  - The methodology emphasizes continuous improvement and annual production, enabling better change detection and temporal consistency; new methods may be reapplied across the entire catalog if accuracy improves.
  - Bootstrap Training relies on historical map quality; gains in temporal consistency support governance and monitoring objectives, while random classification errors are expected to flicker over time as real changes persist.
  - The product suite supports both detailed (10 m) and summary (1 km, 25 m parcel) analyses, enabling governance, planning, and environmental monitoring across scales.

- Practical guidance for use and stewardship
  - Use 10 m Classified Pixels with caution for change detection and landscape-detail analyses; validate against parcel-based products when possible.
  - Leverage Land Parcel datasets for stable, repeatable time-series analyses and change detection at the parcel level; be mindful of MMU and GID changes between versions.
  - For broad-scale assessments or cross-border coordination, utilize 1 km products with awareness of rounding effects and coastal partial-area behaviors.
  - When comparing with historical maps or other classifications, consult Appendix 1 and Appendix 2 for guidance on differences between UKCEH Land Cover Classes and BAP Broad Habitats, and use the provided crosswalks and notes.

- Appendices and supporting context
  - Appendix 1 and Appendix 2 provide detailed notes on UKCEH Land Cover Classes and BAP Broad Habitats definitions and their relationship.
  - Appendix 3 lists the full dataset names and extents for GB and NI.
  - Appendix 4 presents the detailed correspondence matrices (confusion matrices) and accuracy metrics by class.
  - Appendix 5 and Appendix 6 give recommended color recipes for visualization (color and color-blind friendly) of the Land Cover Classes.