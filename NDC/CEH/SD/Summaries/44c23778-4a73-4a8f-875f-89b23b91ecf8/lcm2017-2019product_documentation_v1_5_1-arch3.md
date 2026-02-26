# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.5.1 30/06/2020

- The document is the user guide accompanying the release of three UKCEH land cover maps (LCMs) for 2017, 2018, and 2019, extending the national series that began with 1990, 2000, 2007, and 2015.
- All three maps share a consistent structure: 21 UKCEH Land Cover Classes aligned with Biodiversity Action Plan (BAP) Broad Habitats, with class definitions, metadata, and spatial frameworks described to aid informed use.
- Production is fully automatic, using Bootstrap Training with a Random Forest classifier to generate annual, country-wide maps rapidly, enabling near-real-time monitoring of land cover change.
- The team notes no manual corrections for these annual products due to the automated workflow, but conducts visual checks and formal validation to confirm map quality comparable to recent predecessors.

## Key Aims and Coverage

- Provide geospatial land cover products that enable scrutiny of environmental health and policy effectiveness.
- Support monitoring and decision-making with openly accessible datasets, accompanied by clear metadata, validation, and documentation.
- Deliver annual UK-wide maps (Great Britain and Northern Ireland) with 21 land cover classes, mapped from Sentinel-2 seasonal composites and enhanced by contextual information.

## Product Content and Data Structure

- Datasets included in the release:
  - 20m Classified Pixels: new RF classification results from Sentinel-2 Seasonal Composite Images (winter, spring, summer, autumn) with per-pixel class confidence.
  - Land Parcels: derived attributes summarising 20m pixels within the UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha).
  - 25m Rasterised Land Parcels: rasterised version of Land Parcels with three bands (mode, confidence, purity).
  - 1km Raster Products:
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
- Each year (2017, 2018, 2019) is produced for Great Britain (GB) and Northern Ireland (NI), yielding 42 datasets in total.

## Production Methodology and Data Flows

- Bootstrap Training:
  - Training data are bootstrapped from UKCEH LCM2015 (which itself originated from 1990–2007 observations) to create spectral training observations for 2017–2019.
  - The Bootstrap Training set uses land parcels with high purity (≥99%) to seed the classifier.
  - Future maps (2020, 2021) intend to bootstrap from majority signals across multiple years.
- Random Forest Classification:
  - Training samples: 10,000 per bag, with sampling with replacement to balance class representation.
  - Result: 20m Classified Pixels product, including per-pixel class probability (Band 2) to indicate confidence (0–100).
- Seasonal Composite Images and Context Rasters:
  - Seasonal Composite Images derived from Google Earth Engine using Sentinel-2 TOA reflectance (TOA chosen over SR after evaluation).
  - Four seasons produce the spectral information, supplemented by 20m Context Rasters (terrain, proximity to features, etc.) to mitigate spectral confusion.
- Classification Scenes and Tiling:
  - Great Britain uses overlapping 100x100 km tiles to create 74 GB Classification Scenes, each trained and classified independently; overlaps are resolved by visual inspection to select the best results.
  - Northern Ireland uses a single 43-band Classification Scene per year, determined by the minimum bounding rectangle of NI land mass.
- UKCEH Land Parcel Spatial Framework:
  - A fixed framework derived from generalised national cartography to create land parcels (minimum MMU ~0.5 ha) used to summarise 20m Classified Pixels.
  - gid identifiers are stable within each year but do not match LCM2015; parcel-based comparisons across years require using gid for within-year comparisons.
- Validation and Quality:
  - UK-wide validation against multiple sources (GB countryside survey 2019, National Forest Inventory, IACS, and bespoke validation points) with 22,325 points.
  - Reported overall accuracy: LCM2017 = 78.6%, LCM2018 = 79.6%, LCM2019 = 79.4%.
  - Validation points are subject to some misclassification and conversion nuances; results are indicators of performance rather than absolute truth.

## Data Details and Interpretations

- 20m Classified Pixels:
  - Two-band raster per year per region; band 1 is the most likely land cover class, band 2 is the rescaled membership probability (0–100) indicating classifier confidence.
  - Maintains high spatial detail (preserving narrow features that are lost in parcel-based summaries).
- Land Parcels:
  - Attributes per parcel include gid, _hist (per-class counts), _mode (dominant class), _purity (dominant class share), _conf (mean class membership probability), _stdev (uncertainty), and _n (number of pixels within parcel).
  - New attribute naming alignments reflect production software conventions (descriptions may differ slightly from LCM2015).
- 25m Rasterised Land Parcels:
  - Three-band rasters: band 1 = _mode, band 2 = _conf, band 3 = _purity.
- 1km Gridded Products:
  - 1km Percent Cover: 21-band 8-bit raster indicating per-class cover percentage.
  - 1km Percent Aggregate Cover: 10-band 8-bit raster for aggregate class percentages.
  - 1km Dominant Cover: single-band raster for the dominant class in each 1km cell.
  - 1km Dominant Aggregate Cover: 1-band raster for dominant aggregate class.
- Classification Scenes and Satellite Input:
  - Sentinel-2 bands used span visible to shortwave infrared ranges; 9 bands (2, 3, 4, 5, 6, 7, 8, 11, 12) across four seasons.
  - Some data gaps due to cloud are handled by the classifier’s tolerance, with exploration of using Sentinel-1 SAR or alternative sources for future gap-filling.

## Contextual and Geographic Information

- Context Rasters (GB and NI) provide auxiliary information to help separate spectrally similar classes (e.g., urban vs. bare rock near coast, proximity to water bodies).
- GB context layers include terrain (Height, Aspect, Slope) and proximity to buildings, roads, sea, freshwater, foreshore, tidal water, and woodland masking.
- NI context layers include terrain plus urban mask, distance to coast, freshwater, and roads.

## Spatial Framework and Data Governance

- UKCEH Land Parcel Spatial Framework is fixed to match LCM2015 parcel structure, enabling stable spatial units for change detection within a year, but cross-year comparisons require gid-based linkage and acknowledge parcel id changes.
- The data are designed for openness and reuse, with a strong emphasis on metadata clarity, validation, and documentation to support governance and policy monitoring decisions.

## Appendix Highlights and Supporting Material

- Appendix 1: Notes on UKCEH Land Cover Classes (detailed class definitions and caveats for spectral detection, including limitations for upland and peatland vegetation).
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats – definitions and relationships to UKCEH land cover classes.
- Appendix 3: RGB color recipes for displaying UKCEH Land Cover Classes (display guidelines for map rendering).
- Appendix 4: Validation and confusion matrices (LCM2017, LCM2018, LCM2019) including user’s and producer’s accuracy by class.
- Appendix 5: Full list of datasets per year and per region (GB and NI) with dataset names and hierarchical relationships.

## Practical Considerations for Monitoring and Policy Use

- The maps enable annual monitoring of land cover change, essential for policy evaluation, environmental health assessments, and planning.
- The combination of 20m detail and 1km generalized products supports both fine-scale analysis and broad regional assessments.
- Limitations are acknowledged (e.g., automated classification without manual corrections, potential cross-year parcel identifier mismatches, validate-point uncertainties, and TOA-based inputs in some cases).
- The producers anticipate ongoing enhancements, including expanding input data types, refining training data, and possibly improving upland vegetation classifications in future LCMs.

## Future Plans and Updates

- Continued annual releases (LCM2020 planned for 2021) with bootstrap strategies updated to reflect multi-year majority signals.
- Ongoing assessment of satellite inputs (e.g., exploring SR, alternative optical sources, and SAR data for filling seasonal gaps).
- Potential refinements to the Land Parcel Spatial Framework and to class delineation as training data and remote sensing capabilities evolve.