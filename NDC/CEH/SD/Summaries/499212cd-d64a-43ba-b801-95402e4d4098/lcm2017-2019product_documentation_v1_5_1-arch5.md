# The UKCEH Land Cover Maps for 2017, 2018 and 2019

## Purpose
- User guide for three UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Describes content, structure, data production, validation, and future plans.
- Affirms 21 UKCEH Land Cover Classes (aligned with UKCEH LCM2015) and a rapid, automated production approach.

## Datasets and Content
- Dataset suite (per year) includes:
  - 20m Classified Pixels (new addition; GB and NI versions)
  - Land Parcels (GB and NI)
  - 25m Rasterised Land Parcels (GB and NI)
  - 1km Dominant Cover (GB and NI)
  - 1km Dominant Aggregate Cover (GB and NI)
  - 1km Percent Cover (GB and NI) – 21 bands
  - 1km Percent Aggregate Cover (GB and NI) – 10 bands
- GB uses 36-band Seasonal Composite Images overlain with 20m Context Rasters to form Classification Scenes; NI uses a single 43-band/36+7 scene.
- Pixel resolution and class count:
  - 21 UKCEH Land Cover Classes (GB and NI), mapped to UK BAP Broad Habitats where relevant.
  - 21-class and 10-class aggregates are provided; MMU (minimum mapping unit) ~0.5 ha for land parcels.
- Coordinate systems:
  - GB: British National Grid (EPSG: 27700)
  - NI: Irish Grid (TM75, EPSG: 29903)

## Production Methodology
- Fully automatic production using Bootstrap Training and Random Forest (RF) classification:
  - Bootstrap Training selects historical training observations from UKCEH LCM2015, now sampled to ensure class balance.
  - RF classifier trained on 10,000 samples per training bag; outputs 20m Classified Pixels with per-pixel class probability (Band 2).
- Data inputs:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance; 20m resolution) for winter, spring, summer, autumn.
  - 9 Sentinel-2 bands plus 20m Context Rasters (terrain, proximity to buildings/roads/seas/freshwater, foreshore, tidal water, woodland).
  - Google Earth Engine used to generate seasonal composites; SR (surface reflectance) considered but TOA used for consistency in this release.
- Classification Scenes:
  - GB: 100x100 km tiles producing 46-band GB Classification Scenes; 74 overlapping scenes classified independently; visual inspection selects best results.
  - NI: 43-band scene per year based on minimum bounding rectangle of NI landmass.
- UKCEH Land Parcel Spatial Framework:
  - Maintains 0.5 ha MMU; parcels structurally unchanged from LCM2015, but with reordered storage and new indices.
  - gid identifiers are not consistent with LCM2015; comparison across years requires gid, though cross-year comparisons are possible via parcel overlap.
- Summary of changes since LCM2015:
  - Introduction of 20m Classified Pixels; all other products derived from these pixels via the Land Parcel Framework.
  - Attribute changes in Land Parcels (renamed fields; some historical attributes removed); 25m Rasterised Parcels include three bands: _mode, _conf, _purity.
  - 1km rasters aggregate 25m pixels to annual 1km grids.

## Data Model and Metadata
- Datasets described with detailed attributes, spatial extents, pixel sizes, and band counts.
- Table relationships and notes explain how 21 UKCEH Land Cover Classes map to UK BAP Broad Habitats and to aggregated classes.
- Attribute changes noted for user guidance (e.g., renamed fields, removal of obsolete attributes like Composite).
- Dataset descriptions include visual examples and cross-year guidance for understanding changes and generalization effects from 20m to 1km products.

## Validation and Quality
- Validation conducted against multiple sources: GB countryside survey (2019), National Forest Inventory, IACS, and manually interpreted validation points.
- Validation sample: 22,325 points across LCM2017, LCM2018, LCM2019.
- Overall accuracy:
  - LCM2017: ~78.6%
  - LCM2018: ~79.6%
  - LCM2019: ~79.4%
- Notes:
  - Validation points come from datasets with different purposes and class definitions; conversions introduce subjectivity.
  - About 80% correspondence is considered strong for an automatically produced 21-class map; accuracy is expected to improve as methods mature.
  - Full validation detail and confusion matrices are provided in Appendix 4.

## Practical Guidance for Data Stewards
- Data lineage and reproducibility:
  - Bootstrap Training uses historic maps (starting from 2015 for 2017–2019) to generate training data; approach will evolve (future bootstraps aim to use multi-year majority signals).
  - Fully automated production reduces manual correction, aligning with rapid annual updates.
- Data governance and interoperability:
  - gid changes mean cross-year parcel-level comparisons require careful handling; use gid for LCM2017–2019 parcel comparisons rather than LCM2015 identifiers.
  - Two primary spatial frameworks exist: 20m Classified Pixels and Land Parcels (with MMU ~0.5 ha); users can apply alternate parcel schemes if desired.
- Data quality and usage:
  - Several classifications are spectrally confounded; context rasters (terrain, proximity) help reduce confusion.
  - Coastal and rivers/freshwater classifications can be affected near shorelines; Saltwater vs Freshwater differentiation relies on context layers and partial spectral information.
- Update cadence:
  - UKCEH plans to release a new LCM annually (LCM2017–2019 released together with a plan for 2020+).
  - Future iterations may expand input data types (e.g., additional optical sources or SAR) and refine training data with new observations.

## Appendices and References (highlights)
- Appendix 1 and 2: UKCEH Land Cover Classes and Biodiversity Action Plan (BAP) Broad Habitats definitions and mappings; detailed notes on class derivation and detection considerations.
- Appendix 3: RGB color recipes for display of UKCEH Land Cover Classes.
- Appendix 4: Validation and confusion matrices for LCM2017, LCM2018, LCM2019.
- Appendix 5: Full list of datasets per year and their respective GB/NI holdings and dataset naming.
- References: Foundational works on Random Forests, bootstrap training, and previous UKCEH LCM methodologies.