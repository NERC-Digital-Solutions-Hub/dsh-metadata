# The UKCEH Land Cover Map for 2023

- Purpose and scope
  - UKCEH LCM2023 comprises seven datasets (three for Great Britain, three for Northern Ireland, plus a 1 km summary raster) including 10 m classified pixels, land parcels, and 25 m rasterised land parcels; a 1 km summary raster covers GB and NI.
  - Aims to support informed decisions with formal validation; overall accuracy reported at 83% for full thematic detail.
  - Annual production facilitates change detection and temporal consistency across the UK countryside.

- Key datasets and data products
  - 10 m Classified Pixel datasets (GB and NI): per-pixel land cover class (UKCEH Land Cover Class) plus a second band with the classification confidence; preserves fine landscape detail (no Generalised Parcel Framework applied).
  - 25 m Pixel Rasterised Land Parcel datasets (GB and NI): rasterised view of Land Parcel outputs, carrying per-parcel attributes (mode, conf, purity).
  - Land Parcel Vector products: parcel-based attributes with fields such as gid, hist, mode, conf, purity, and agg class.
  - 1 km Summary rasters (GB and NI): dominant class and percentage cover per 1 km pixel derived from 25 m data.
  - Context rasters and Seasonal Composite Images: 10 m context layers (terrain, proximity to buildings/roads/water, foreshore, etc.) used with Sentinel-2 seasonal composites (four seasons) to improve classification.
  - Sentinel-2 bands and spatial resolutions: 10 m (bands 2,3,4,8,8A,11,12) and higher-resolution context bands; occasional gaps due to cloud acknowledged and tolerated by the classifier.
  - 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats; mappings described and cross-referenced with Appendices for clarity.

- Methodology and production approach
  - Bootstrap Training: automatic training data generated from historic LCM maps (LCM2020–2022) to train a Random Forest classifier; only pixels with high probability and consistent class across three years are used.
  - Random Forest classification: balanced training sets (10,000 samples per bag) to avoid dominance by common classes; classification yields per-pixel class and confidence.
  - Classification Scenes: GB split into 32 tiles; NI uses a single Classification Scene; scenes combine Sentinel-2 Seasonal Composite Images with Context Rasters to reduce spectral confusion.
  - UK Land Parcel Spatial Framework: framework used to produce Land Parcel datasets with a minimum mapped unit of ~0.5 ha; designed to support change detection over time.
  - Validation: 33,107 reference validation points across all 21 classes; overall accuracy 83% (Appendix 4).

- Data specifics and formats
  - Coordinate systems: GB uses British National Grid (EPSG: 27700); NI uses Irish TM75 grid (EPSG: 29903).
  - GB and NI parcel counts: GB ~6,741,294 parcels; NI ~902,252 parcels (for parcel-based products).
  - Pixel resolutions and bands:
    - 10 m Classified Pixels: 2-band product (class, conf).
    - 25 m Rasterised Land Parcels: 3-band raster (mode, conf, purity).
  - 1 km rasters: dominant class and percentage cover (21 class bands for GB+NI; sums may deviate from 100 due to rounding and coastal edge effects).
  - Validation detail: both producer’s and user’s accuracies reported by class; overall user’s accuracy and producer’s accuracy summarized in the provided matrices.

- Class definitions and relationships
  - 21 UKCEH Land Cover Classes derived from BAP Broad Habitats (with careful notes on alignment and some deviations due to remote-sensing constraints).
  - Appendices describe nuances for several classes (e.g., Broadleaved vs Coniferous woodland; Arable vs grasslands; Fen/Marsh/Swamp vs Bog; Saltwater vs Freshwater near coast).
  - Colour recipes (Appendix 5 and 6) offer both standard and color-blind-friendly schemes for visualising land cover classes in GIS.

- Validation, known issues, and caveats
  - Known issues: a small number of polygons missing from vector land parcel products; minimal impact on 1 km products; 10 m pixels remain unaffected.
  - Method changes between years may yield minor differences beyond real land-cover change; users should consider methodological shifts when comparing across years.
  - Saltwater vs Freshwater distinctions near tidal zones can incur confusion; coastal water features are lower priority and sometimes less accurate.

- Accessibility and citations
  - Each LCM2023 dataset has a DOI and formal citation:
    - 10 m Classified Pixels (GB and NI)
    - 25 m Rasterised Land Parcels (GB and NI)
    - Land Parcels (GB and NI)
    - 1 km Summary Rasters (GB and NI)
  - References and methodological overviews available in Marston et al. (2023/2024) and related Morton et al. documentation.
  - Data products are accompanied by metadata, including Appendix notes on data structure and validation.

- Practical considerations for analysts
  - Best use cases: annual maps for change detection, high-resolution land-cover mapping, integration with other environmental datasets, and informing policy or land-management decisions.
  - Data quality indicators: 83% overall accuracy; class-level producer’s/user’s accuracy matrices provide per-class reliability.
  - Analytic readiness: data produced with open-source tools (Weka, PostGIS, GDAL); rich metadata and DOIs enable reproducibility and traceability.
  - When using: consider the MMU (0.5 ha) of Land Parcels, 10 m vs 25 m resolution differences, and potential class confusion in upland and coastal zones. Utilize the 1 km summaries for large-scale syntheses and the 10 m data for detailed analyses.

- Notable appendices and resources
  - Appendix 1–4: class notes, Biodiversity Action Plan mappings, and validation matrices.
  - Appendix 5–6: colour schemes for display, including color-blind friendly options.
  - Appendix 3: full list of datasets and DOIs; Appendix 4: correspondence matrices for LCM2023.
  - Disclaimer: method variations across years may produce minor changes independent of actual land-cover change.