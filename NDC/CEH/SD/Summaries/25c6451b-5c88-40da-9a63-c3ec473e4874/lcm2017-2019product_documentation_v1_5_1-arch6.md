# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

- Overview
  - Release accompanies three UKCEH Land Cover Maps (LCM2017, LCM2018, LCM2019) with 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
  - Maps produced automatically using Bootstrap Training plus Random Forest; annual maps planned.
  - Data designed to be rapidly usable across Great Britain (GB) and Northern Ireland (NI) with multiple raster products and parcel-level attributes.
  - Validation indicates outputs are of similar quality to recent predecessors; manual corrections are not performed in this release.

- What’s included (dataset structure)
  - 42 datasets per year, duplicated for GB and NI:
    - 20m Classified Pixels (GB and NI)
    - Land Parcels (GB and NI)
    - 25m Rasterised Land Parcels (GB and NI)
    - 1km Dominant Cover (GB and NI)
    - 1km Percent Cover (GB and NI)
    - 1km Percent Aggregate Cover (GB and NI)
    - 1km Dominant Aggregate Cover (GB and NI)
  - Coordinate systems:
    - GB: British National Grid, EPSG: 27700
    - NI: Irish Grid, EPSG: 29903
  - Pixel sizes and classes:
    - 20m Classified Pixels: 2-band rasters (class, confidence 0–100); 21 UKCEH Land Cover Classes.
    - 25m Rasterised Land Parcels: 3-band rasters (dominant class, confidence, purity) plus parcel attributes.
    - 1km rasters: Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), Dominant Aggregate Cover (1 band).
  - Data structure notes:
    - The Land Parcel Spatial Framework is unchanged in geometry from LCM2015, but parcel identifiers (gid) are not the same as LCM2015; comparisons use gid only for LCM2017–2019.
    - The 20m Classified Pixels preserve detail not present in Land Parcels; 25m parcels generalise features.

- Data production and processing workflow
  - Bootstrap Training: Automatic training data drawn from historic LCMs (primarily LCM2015) to bootstrap classification without fresh field data.
  - Random Forest classification: Balanced sampling across classes; 10,000 samples per class per classification scene; produced the 20m Classified Pixels product.
  - Seasonal Composite Images: Sentinel-2 TOA reflectance per season (winter, spring, summer, autumn) derived in Google Earth Engine; bands 2,3,4,5,6,7,8,11,12 used; gaps due to clouds handled by classifier; future plans to leverage SAR and alternative inputs for gap filling.
  - Context Rasters: 20m context layers (GB: height, aspect, slope; distance to buildings, roads, sea, freshwater; foreshore and tidal water masks; woodland mask). NI includes similar or adapted contextual layers.
  - Classification Scenes: GB uses 100x100 km overlapping tiles to create 74 GB Classification Scenes; NI uses a single 43-band scene per year; scenes classified independently with overlap used to ensure coverage and balance; manual precedence used to select final results in overlaps.
  - UKCEH Land Parcel Spatial Framework: Framework of land parcels (~0.5 ha MMU) used to summarise 20m Classified Pixels into parcel-level attributes; framework geometry unchanged from LCM2015; new indices and storage reorganisations implemented.
  - Validation approach: Cross-year validation using GB countryside survey data, National Forest Inventory data, IACS, and bespoke validation points; ~22,325 points used for evaluation.

- Data accessibility and structure details
  - GB and NI data are provided in parallel across annual releases (LCM2017, LCM2018, LCM2019).
  - 20m Classified Pixels provide per-pixel class with a confidence score; useful for detailed, non-generalised analysis.
  - Land Parcels provide parcel-level statistics including histograms of class composition, modal class, purity, and confidence measures.
  - 25m Rasterised Land Parcels offer a reduced-detail summary with three bands (mode, conf, purity) suitable for coarser analyses.
  - 1km products aggregate 25m results within 1km grid cells to deliver:
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - Data quality and alignment:
    - The methodology is designed to maximize temporal comparability while acknowledging inevitable classification uncertainty.
    - Validation shows ~78.6%–79.6% overall agreement across 2017–2019 UK-scale products; not treated as absolute truth due to label differences and sampling limitations.
  - Dataset availability:
    - Appendix 5 lists the full dataset catalog for LCM2017, LCM2018, and LCM2019 (Gb NI breakdowns and dataset names).

- Classification details and key decisions
  - 4-season Sentinel-2 inputs with 9 spectral bands enabled by Google Earth Engine; TOA data used after assessment (no clear advantage from surface reflectance in this context).
  - Context rasters chosen to reduce spectral confusion between spectrally similar classes (e.g., coastal proximity, urban proximity, terrain effects).
  - Output classes and labeling:
    - Maps include 21 UKCEH Land Cover Classes aligned with UKCEH LCM2015/BAP-based scheme; notes on how BAP Broad Habitats relate to the 21 classes and occasional need for careful interpretation.
  - Manual corrections:
    - No manual region-specific corrections were performed in this release to enable rapid annual updates; visual checks and formal validation were performed to ensure quality.

- Validation and limitations
  - Validation against multiple independent datasets yields approximately 80% overall agreement across the three years (LCM2017–LCM2019), acknowledging limitations:
    - Validation points originate from sources with different purposes and class schemes; some conversions were required.
    - Class-wise accuracies vary; confusion persists for some upland, coastal, and mixed-vegetation classes.
  - Outputs are not absolute truth but robust indicators of land cover distribution and change over time; ongoing efforts aim to improve validation resources and methods.

- Appendix highlights and notes for data users
  - UKCEH Land Cover Classes and BAP Broad Habitats relationships documented; includes caveats about detection limitations from remote sensing.
  - Important changes from LCM2015:
    - Introduction of 20m Classified Pixels; 25m Land Parcels; revised parcel attributes; different gid alignment; removal of the Composite attribute.
  - Spatial and thematic guidance:
    - Built-up Areas and Gardens are split into Urban and Suburban classes; coastal classifications include Saltwater and Freshwater distinctions.
    - Some habitats (e.g., Bracken) are combined with related types due to spectral limitations; longer-term plans may enable finer separation with enhanced training data.
  - RGB color recipe and confusion matrices are provided in appendices to aid visualization and quality assessment.

- Practical takeaways for data support use
  - For detailed local analyses, use the 20m Classified Pixels to capture fine-grained variation; for scalable summaries, rely on 25m Land Parcels or 1km raster products.
  - To compare across years, prefer the gid-based parcel-based comparisons within the same Land Parcel Spatial Framework; be aware gid changes between LCM2015 and later products.
  - When communicating results, incorporate the noted uncertainties and rely on the provided validation figures as qualitative indicators of reliability.
  - Consider future data enhancements (gap filling with SAR inputs, expanded input data, and potential 4-season refinements) when planning longitudinal analyses.