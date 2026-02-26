# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1

## Purpose and scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018 and LCM2019.
- Land cover represented by 21 UKCEH Land Cover Classes based on Biodiversity Action Plan (BAP) Broad Habitats.
- Maps produced automatically using Bootstrap Training combined with Random Forest classifiers; annual maps planned going forward.
- Input sources include Sentinel-2 Seasonal Composite Images (TOA reflectance) and a set of 20m Context Rasters to reduce spectral confusion.

## Data content and structure
- Dataset package comprises 42 datasets (for GB and Northern Ireland, one GB and one NI version for each year).
- Datasets include:
  - 20m Classified Pixels: per-pixel land cover class with a confidence measure; preserves fine detail.
  - Land Parcels: attributes for each parcel (gid, hist, mode, purity, conf, stdev, n) and related metadata; enables parcel-based analyses and change detection.
  - 25m Rasterised Land Parcels: three bands for each parcel (mode, conf, purity) at 25m resolution.
  - 1km Raster products (per year): 
    - 1km Percent Cover (21-band)
    - 1km Percent Aggregate Cover (10-band)
    - 1km Dominant Cover (single band)
    - 1km Dominant Aggregate Cover (single band)
- GB and NI coordinate systems:
  - GB: British National Grid, EPSG: 27700
  - NI: Irish Grid, EPSG: 29903
- Pixel and parcel sizes:
  - Classified Pixels: 20m
  - Land Parcels: mapped to approximately 0.5 ha minimum mapping unit (MMU)
  - 25m Rasterised Parcels: 25m pixels
  - 1km rasters: aggregated from 25m parcels
- Output class relationships and color scheme are defined in accompanying appendices (e.g., Appendix 3 color recipe).

## How the maps were produced
- Bootstrap Training: automatic generation of training observations from historic maps (primarily LCM2015 bootstrap data) to enable rapid map updates without new field data.
- Random Forest classification: trained on balanced samples drawn from Classification Scenes; used to produce the 20m Classified Pixels product.
- Classification Scenes and tiling:
  - GB: 100x100 km tiles used to extract 36-band Seasonal Composite Images plus 20m Context Rasters, forming 46-band GB Classification Scenes; 74 overlapping scenes classified independently, with visual inspection resolving overlaps.
  - NI: single 43-band Classification Scene per year derived from the national extent.
- Digital inputs:
  - Sentinel-2 Seasonal Composite Images (TOA) for four seasons (winter, spring, summer, autumn).
  - 20m Context Rasters including terrain (Height, Aspect, Slope) and proximity masks (roads, buildings, coast, freshwater, foreshore, etc.).

## UKCEH Land Parcel Spatial Framework
- Existing framework maintained (same parcels as LCM2015, but storage and indices updated for speed).
- gid remains the parcel identifier, but new parcels will not match LCM2015 identifiers; gid is the preferred cross-year link.
- MMU approximately 0.5 ha; parcels represent discrete real-world units (fields, parks, urban areas, etc.).
- The framework is one option for summarising 20m Classified Pixels; UKCEH may encourage other parcel structures in the future as higher-resolution data become available.

## Validation and accuracy
- UK-scale validation using GB countryside survey (2019), National Forest Inventory data, IACS, and bespoke LCM validation points (22,325 total).
- Reported overall accuracy (approximate):
  - LCM2017: 78.6%
  - LCM2018: 79.6%
  - LCM2019: 79.4%
- Validation points are not perfect truth; they provide best-available indicators and involve some crosswalks between older class descriptions and the 21 UKCEH classes.
- Full validation tables are provided in Appendix 4.

## Notable production decisions and changes
- No manual corrections were performed this time to enable annual rollout; visual checks and formal validation still carried out to ensure quality comparable to recent predecessors (LCM2015).
- TOA was used for Sentinel-2 inputs; SR did not show improvements for the current class scheme, though future changes may revisit input types.
- The classification and outputs are designed to enable self-service use, trend analysis, and cross-year comparisons, with explicit notes about potential cross-year parcel identifier mismatches.

## Datasets, products, and usage notes
- Datasets and products per year:
  - 20m Classified Pixels (GB and NI)
  - Land Parcels (GB and NI)
  - 25m Rasterised Land Parcels (GB and NI)
  - 1km Dominant Cover, 1km Dominant Aggregate Cover, 1km Percent Cover, 1km Percent Aggregate Cover (GB and NI as applicable)
- Scale and application guidance:
  - 20m Classified Pixels preserve fine landscape features; useful when high spatial detail is needed.
  - 25m and 1km products provide aggregated views suitable for regional analyses and change detection.
- Appendix references:
  - Appendix 1–2: Notes on UKCEH Land Cover Classes and relationships to BAP Broad Habitats.
  - Appendix 3: RGB color recipes for displaying the 21 classes.
  - Appendix 4: Detailed confusion matrices and accuracy statistics by class (for validation across 2017–2019).
  - Appendix 5: Full list of datasets per year.

## Future plans and outlook
- UKCEH intends to release a new LCM annually.
- Ongoing evaluation of input data and potential expansion of land surface information products (e.g., incorporating additional optical sources or SAR data) and gap-filling strategies for incomplete seasons.
- Continued refinement of Bootstrap Training strategies and potential changes to parcel frameworks as higher-resolution data become more available.