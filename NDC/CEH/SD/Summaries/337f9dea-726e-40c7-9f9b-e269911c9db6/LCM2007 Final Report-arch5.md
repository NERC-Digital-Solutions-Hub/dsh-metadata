# Final Report for LCM2007 - the new UK land cover map

## Overview for Data Stewards
- LCM2007 delivers the first continuous parcel-based UK land cover map, combining satellite imagery with national cartography to support policy, monitoring, and planning.
- Provides UK-wide stock estimates of Broad Habitats with accompanying vector (parcels) and raster products (25 m and 1 km resolutions), plus aggregate class summaries.

## Data Governance, Provenance, and Structure
- Data sources and lineage:
  - Ground truth and reference data from Countryside Survey (CS) and CEH training/validation points.
  - External layers: national cartography (OS MasterMap), agricultural boundaries, soils, DEMs, coast/topography, and urban boundaries.
  - Satellite imagery: multi-sensor, multi-temporal (Landsat TM/ETM+, Spot 4/5, LISS-III, AWIFS); 91% GB coverage via two-date composites; remainder via single-date images.
- Spatial framework and generalisation:
  - Uses generalized cartography as a primary spatial framework; image segments added to capture spectral heterogeneity.
  - Nine UK chunks defined to support seamless, high-quality vector output; clear image priority for assembly.
- Processing and QA:
  - Pre-processing, segmentation, parcel-based maximum likelihood classification, and seven knowledge-based enhancements (KBEs) to refine thematic resolution.
  - Post-processing includes manual edits and hole-filling; extensive metadata tracks processing history (KBEs, corrections, probabilities).
- Metadata and accessibility:
  - Vector product: 23 LCM2007 classes mapped to Broad Habitats with detailed per-polygon metadata (area, source images, KBEs, processing steps).
  - Raster products: 25 m (23 classes) and 1 km (percent cover and dominant class) rasters.
  - Minimum mapped unit: 0.5 ha; feature width: 20 m.
  - Licensing: 1 km rasters freely available via CEH Gateway; full vector and 25 m rasters on request with potential licensing fees.

## Data Products and Access
- Products and formats:
  - Vector: UK-wide polygons with Broad Habitat classifications and a 1–23 class scheme; includes KBEs and ProbList for top spectral variants.
  - 25 m raster: 23 LCM2007 classes coded per pixel.
  - 1 km raster: per-square percentage cover and dominant class for both 23-class and 10-aggregate schemes.
- Standards and applicability:
  - Minimum feature: 0.5 ha; minimum width: 20 m.
  - Rich metadata supports traceability of processing steps and KBEs; designed for policy support, habitat monitoring, landscape assessment, and ecosystem services analysis.
- Access terms:
  - 1 km rasters: free via CEH Gateway.
  - Full vector and 25 m rasters: available on licence (fees may apply); licensing details provided by CEH.

## Data Quality, Validation, and Comparisons
- Overall accuracy and class performance:
  - Ground validation: 9127 polygons; overall accuracy around 83% across LCM2007 classes.
  - Class-level accuracy varies; producer’s and user’s accuracies provided per class (KBEs improve some disambiguation but uncertainties remain for certain habitats).
- Comparison with Countryside Survey (CS) 2007:
  - Similar area estimates exist for some classes (e.g., Broadleaved woodland, Acid Grassland, Inland Rock) within CS 95% CIs.
  - Dissimilar estimates arise for several classes, notably Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane, and coastal habitats.
  - Reasons for differences:
    - Classification differences and spectral variability (e.g., Arable variability, temporary grass, uncropped land inclusion in LCM2007).
    - Boundary and linear features mapping: CS includes boundaries/linear features; LCM2007 often aggregates these into field polygons, inflating some class areas.
    - Grassland interpretation differences: Improved vs Neutral Grassland often misaligned spectrally; Neutral Grassland vs Improved Grassland ambiguity on neutral soils.
    - Fen, Marsh and Swamp: CS often maps as mosaic; LCM2007 frequently classifies as Rough Grassland or Acid Grassland due to spectral mix and small patch sizes.
    - Representation of montane and coastal habitats: CS data are sparse for these, leading to larger UK-level discrepancies.
- UK-wide land cover distribution (LCM2007 vs CS 2007 and LCM2000):
  - LCM2007 shows >50% of the UK in intensive land use (Arable + Improved Grassland) plus Built-up areas; Scotland contains more Conifer woodland and montane/semi-natural areas.
  - LCM2000 and LCM2007 show differences in arable and grassland extents; changes reflect methodological shifts, not only landscape change.
- Change detection and temporal aspects:
  - LCM2007 vs earlier maps involves complex change signals due to different spatial and thematic structures; robust change detection requires advanced methods or re-structuring older maps into a common spatial framework.

## Methodology and Implementation Details (Key Considerations)
- Classification framework and KBEs:
  - 23 LCM2007 classes aligned with Broad Habitats; several classes map to multiple Broad Habitats, necessitating KBEs for disambiguation.
  - Seven automated KBEs apply contextual cues (terrain, soils, coastal proximity, urban proximity, water classification) to improve thematic accuracy.
- Validation and bespoke validation:
  - The document emphasizes choosing target classes with regard to use-case; offers parcel-level metadata to support user-driven validation.
  - Bespoke validation approaches propose using high-resolution imagery to assess consistency with LCM2007 attribution, acknowledging uncertainty and using fuzzy categories (plausible, probably, possibly).
- Practical interpretation for data stewards:
  - When comparing with CS or other datasets, consider aggregating grasslands or using Broad Habitat associations to improve comparability.
  - Document automated reclassifications and uncertainties; KBEs should be transparently reported.
  - Be mindful of licensing terms and attribution when using LCM2007 products or derived data.

## Applications, Limitations, and Data Steward Guidance
- Uses and impact:
  - Supports habitat monitoring, biodiversity policy, landscape planning, and ecosystem services analysis; provides UK-wide, scalable basemap for monitoring and change detection.
- Limitations and caveats:
  - Grassland classifications are challenging due to a one-to-many mapping to Broad Habitats.
  - Change detection is difficult due to differing temporal bases and evolving spatial structures across LCM versions.
  - CS field data capture features (hedgerows, streams, small stands) not always resolved by satellite-derived maps.
- Practical guidance for data stewards:
  - Leverage KBEs for improved classification but document uncertainties and reclassifications.
  - For cross-dataset comparisons (e.g., CS), consider aggregating grassland classes or using Broad Habitat Associations.
  - Respect licensing and attribution requirements when using LCM2007 data or derivatives.

## Endnotes, Context, and Related Considerations
- LCM2007 represents a significant advancement in UK land cover mapping with enhanced spatial fidelity and cross-product compatibility, facilitating future monitoring and change detection.
- Chapter 6 discusses the challenges of comparing LCM-based products with CS and the value of integrating multiple data sources (earth observation, field surveys, LiDAR, soils, climate) for robust policy-relevant insight.
- Appendices cover Broad Habitat definitions, validation approaches, and Broad Habitat Association rules, plus extensive metadata and data descriptions for users requiring deeper technical understanding.