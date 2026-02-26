# Final Report for LCM2007 - the new UK land cover map

## Overview
- Presents a UK-wide land cover map (LCM2007) and its comparison with Countryside Survey (CS) 2007 data, including cross-walks to Broad Habitats (BH) and Broad Habitat Associations (BHA).
- Documents area estimates, validation results, methodological reasons for similarities/differences, and implications for policy and monitoring.
- Describes data products (25 m raster, 1 km raster, and vector parcels) and access arrangements.

## 4.3 Comparison with Countryside Survey (GB focus)

### 4.3.1 Very similar area estimates
- Very similar areas between CS 2007 and LCM2007 for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland
- The strong agreement for Coniferous Woodland aligns with the correspondence analysis between CS and LCM2007.

### 4.3.2 Similar area estimates
- Similar area estimates (within CS 95% confidence limits UK-wide) also observed for:
  - Broadleaved woodland
  - Acid Grassland
  - Inland Rock

### 4.3.3 Dissimilar area estimates
- Dissimilar areas (outside CS 95% limits) occur for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Key drivers of differences:
  - Differences in what CS and LCM2007 classify as, especially for Arable and Horticulture (spectral confusion, temporal range across several years, and inclusion of boundary/linear features in LCM2007).
  - MMU and how boundaries are represented; CS uses field parcel delineations that often differ from LCM’s parcel-based approach.
  - Grassland classifications (Neutral vs Improved vs Calcareous/Acid) and how spectral variability is handled; Broad Habitat Association (BHA) rules are used to reconcile some of this but residual differences remain.
  - Fen, Marsh and Swamp (FMS) is particularly challenging due to mosaic nature and spatial scale differences; CS patches below the LCM MMU affect comparability.
- Specific notes on Arable and Horticulture:
  - LCM2007 tends to include more area in this class due to spectral variability, boundary features, and the need to harmonise multi-year imagery, which can inflate arable estimates relative to CS.
  - DEFRA agricultural data show a broader context for arable/grassland components, contributing to observed differences.

## 4.4 UK Land Cover
- LCM2007 shows UK-wide patterns: more than 50% of land under intensive use (Arable and Horticulture plus Improved Grassland) or Built-up Areas and Gardens.
- Variations across the four UK countries:
  - England and Northern Ireland: highest shares of intensive land use.
  - Scotland: largest share of Coniferous Woodland and the greatest extent of upland semi-natural habitats.
  - Wales: intermediate patterns with notable arable/grassland components.
- Baseline comparison with LCM2000 indicates changes in the proportions of Arable, Semi-natural Grassland, and Coniferous Woodland; the impact of the updated spatial framework on these figures is not fully isolated.

## 4.5 Summary and discussion
- Agreement between LCM2007 and CS 2007 varies by BH; grassland classes are particularly problematic due to one-to-many relationships and spectral variability.
- Broad Habitat Association (BHA) rules provide a third level of thematic accuracy to improve cross-dataset correspondences.
- LCM2007 shows high correspondence with CS 2007 data for Arable and Horticulture at the 1 km square level, but national-scale Broad Habitat estimates generally differ, due in part to classification differences, MMU effects, and temporal differences in imagery.
- Fen, Marsh and Swamp estimates show large UK-level discrepancies due to the mosaic nature and patch sizes, with many Fen areas in CS being mapped as Rough Grassland or Acid Grassland in LCM2007.
- For change detection and policy analysis, users should consider data structure differences, spectral confusion, and KBE (Knowledge-Based Enhancements) history; using the BH Association framework can aid cross-dataset alignment.
- LCM2007 provides a rich, parcel-level validation framework with metadata on processing history and spectral probabilities, enabling user-driven quality checks.

## 5.1 Example areas
- The report presents example areas illustrating LCM2007 performance across upland, calcareous, urban, and arable/fenland landscapes, demonstrating how different habitat types are captured in practice.

## 5.2 Vector and raster products
- Products include:
  - Vector: land parcels with attributes such as area, source images, Broad Habitat (BH), processing history, and KBE history.
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: two summaries per pixel:
    - Percentage cover for each class
    - Dominant class per pixel
- Access:
  - 1 km data via CEH Information Gateway.
  - Full vector and 25 m data available on request (licences may apply).

## 6. Change detection and data integration
- Comparing LCM2017 with earlier CEH maps is complex due to differing spatial structures (pixel-based vs parcel-based vs segment-based), thematic granularity, and generalisation approaches.
- A robust strategy may involve re-organising earlier maps into a common spatial framework and focusing on aggregated or consistently mapped classes, or using trajectory-based statistical methods to identify plausible changes.

## Access and licensing
- 1 km data: CEH Information Gateway.
- 25 m raster and vector data: available under licence from CEH (online application or contact details provided); licences may apply for some users/applications.

## Appendices (validation and Cross-dataset relations)

- Bespoke validation (Appendix 4)
  - Emphasises “fit for purpose” validation using parcel-level metadata and a proposed informal Bayesian-style approach to assess consistency with high-resolution imagery.
  - Recommends using multiple fuzzy categories (plausible, probably, possibly) to bound accuracy per target class.

- Broad Habitat Association (Appendix 5)
  - Provides the rationale and rules (BH Association) linking LCM2007 classes to CS Broad Habitats for cross-dataset interpretation.
  - Examples include Bog, Dwarf Shrub Heath, Montane Habitats, Built-up Areas and Gardens, Fen Marsh and Swamp, Rough Grassland, and Water classes.
  - Rules describe acceptable correspondences and reciprocal expectations between LCM2007 and CS classifications, acknowledging mosaic and edge-case transitions.

- Access to data sources
  - UK data and European context (Corine/LUCAS) discussed, highlighting the role of LCM2007 as a consistent national frame for habitat monitoring and its integration with other data sources.

- Data provenance and references
  - Describes data sources, spatial frameworks, and detailed metadata for LCM2007 products, with license and access notes and acknowledgments.