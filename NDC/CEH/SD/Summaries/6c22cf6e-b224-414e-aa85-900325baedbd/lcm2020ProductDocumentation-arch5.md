# The UKCEH Land Cover Map for 2020

## Overview and Purpose
- User guide for UKCEH Land Cover Map 2020 (LCM2020), the eighth UK land cover map.
- Product comprises six geospatial datasets (three for GB and three for Northern Ireland), described in detail in Appendix 5.
- LCM2020 provides 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; designed for annual production to enable change detection and temporal consistency.
- Classifications are produced automatically using Bootstrap Training with a Random Forest (RF) classifier, based on Sentinel-2 Seasonal Composite Images plus 10 Context Layers.

## Data Holdings and Structure (Data Steward Perspective)
- Six datasets in total:
  - Great Britain (GB): 
    - 10m Classified Pixel dataset (two-band: most-likely class and associated probability)
    - Land Parcel dataset (attributes derived from UKCEH Land Parcel Spatial Framework)
    - 25m Rasterised Land Parcel dataset (per-parcel, three-band rasters: mode, conf, purity)
  - Northern Ireland (NI):
    - 20m Classified Pixel dataset
    - Land Parcel dataset
    - 25m Rasterised Land Parcel dataset
- Coordinate systems:
  - GB datasets use EPSG 27700 (British National Grid)
  - NI datasets use EPSG 29903 (Irish Grid)
- Data schema highlights:
  - 10m classified pixels: two bands (class identifier, classification confidence)
  - 25m raster: three bands (per-parcel mean probability/confidence, parcel purity)
  - Land Parcel attributes include per-parcel hist, mode, conf, stdev, agg, n, and gid identifiers
- Dataset scope and extent details are formalised in Appendix 5 (official dataset names and coverage)

## Methodology: Data Production and Classification
- Sentinel-2 Seasonal Composite Images (winter, spring, summer, autumn) combined with 10 Context Rasters to form Classification Scenes.
- Bootstrap Training:
  - Training data derived from historic LCM products (LCM2017–2019), filtered to parcels with >99% purity.
  - Final Bootstrap Training set: 941,027 objects (GB) and 214,833 (NI).
  - Bootstrap Training enables automatic generation of training samples for classifier updates.
- Random Forest classification:
  - 10,000 samples per class per training iteration, drawn with replacement to balance class representation.
  - Produces the 10m Classified Pixel product; confidence/probability captured as second band.
- Classification Scenes:
  - GB: 36-band scenes over 74 overlapping 100x100 km tiles; final cut resolved by manual precedence in overlaps.
  - NI: single 36-band scene per year (43 bands total with context rasters).
- Data processing tools:
  - Bespoke UKCEH software integrating Weka, PostGIS, and GDAL (open-source stack).

## Data Quality, Validation, and Limitations
- Validation approach:
  - Compared LCM2020 to countryside survey (2019–2020), National Forest Inventory data, IACS data, and bespoke validation points (total 34,715 locations).
  - Overall thematic accuracy: 79.2% (Appendix 4).
- Validation details and confusion:
  - Appendix 4 includes detailed producer’s and user’s accuracy per class and a comprehensive correspondence matrix.
  - Acknowledges inherent classification errors (random and persistent) and that manual post-editing was not performed to preserve annual production efficiency.
  - Random errors expected to flicker over time; real changes persist, enabling robust change detection in time series.
- Data limitations and notes for users:
  - 10m Classified Pixels are not generalized by the UKCEH Land Parcel Spatial Framework, preserving fine-scale features but complicating direct comparability with parcel-derived products.
  - The UKCEH Land Parcel Spatial Framework has a minimum mapping unit of ~0.5 ha; parcels are designed to represent discrete land units.
  - Gid identifiers in LCM2020 do not match LCM2015 for parcel comparison; time-series comparisons by parcel ID may require spatial overlap rather than ID overlap.
  - Saltwater vs Freshwater distinctions rely on coastal context rasters and can exhibit some confusion, particularly in tidal zones.
  - Some upland vegetation categories (e.g., peatland) are challenging to map with satellite data; ongoing methodological improvements anticipated.

## Data Model: Land Cover Classes and Crosswalks
- 21 UKCEH Land Cover Classes aligned with UK Biodiversity Action Plan (BAP) Broad Habitats, with explicit notes on where UKCEH classes diverge from BAP definitions.
- Appendix 1 rationale and Notes:
  - Provides guidance on how BAP Broad Habitats map to UKCEH classes (e.g., Broadleaved woodland vs. Deciduous woodland, Urban vs. Suburban).
  - Highlights potential spectral confusion (e.g., arable vs. improved grassland; acid vs. neutral grassland) and how context rasters improve discrimination.
- Appendix 2 offers a detailed BAP Broad Habitat taxonomy to support users needing regulatory or field-interpretation alignment.
- Appendix 3 provides color-coding guidance for displaying UKCEH Land Cover Classes.

## Practical Implications for Data Discovery and Reuse
- Frequent, annual updates enable monitoring of real-world changes and differentiation from random classification noise.
- The time series can support change detection and trend analysis across the UK countryside, supporting environmental objectives.
- For users requiring high-detail land cover, the 10m Classified Pixel dataset provides fine-scale features not generalized by parcel frameworks; for applications requiring stable time-series comparisons, parcel-based products offer a consistent framework.
- Metadata and lineage:
  - Data production workflow and validation details are documented (Bootstrap Training, RF classifier, classification Scenes, Validation).
  - Methodological notes help data stewards communicate provenance and limitations to users.

## Governance and Stewardship Considerations
- Data Accessibility and Updates:
  - Annual production cycle with evolving methods; consider documenting reproducibility and versioning in metadata.
- Standards and Metadata:
  - Ensure metadata captures: dataset name, resolution, CRS, band definitions, class identifiers, confidence metrics, MMU, parcel framework details, and validation results.
- Interoperability:
  - Be aware of gid changes between LCM2015 and LCM2020; when linking time-series, prefer spatial overlap or alternative stable identifiers.
- User Guidance:
  - Provide clear notes on the 10m pixel detail vs. 25m rasterised parcels, and guidance on when to rely on parcel-level attributes for change detection.
- Crosswalks and Reporting:
  - Maintain mapping between UKCEH Land Cover Classes and BAP Broad Habitats (and the necessary italicization conventions) to support regulatory reporting and field interpretation.

## Quick Reference: Key Datasets in LCM2020
- GB: 10m Classified Pixels; GB Land Parcel Product; GB 25m Rasterized Land Parcel Product
- NI: 20m Classified Pixels; NI Land Parcel Product; NI 25m Rasterized Land Parcel Product
- Supporting constructs:
  - Seasonal Composite Images (Sentinel-2) and 10 Context Rasters
  - UKCEH Land Parcel Spatial Framework (MMU ~0.5 ha)
  - Bootstrap Training data derived from LCM2017–2019
  - RF classification outputs with class and confidence bands
  - Appendix-driven documentation on class definitions, color schemes, and validation matrices

## Appendices and Supporting Information (For Reference and Compliance)
- Appendix 1: Notes on UKCEH Land Cover Classes (and UK BAP Broad Habitats crosswalk)
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats definitions
- Appendix 3: Recommended color recipe for displaying UKCEH Land Cover Classes
- Appendix 4: Correspondence matrices and validation statistics (class-by-class, producer’s and user’s accuracies)
- Appendix 5: Full list of datasets and official dataset names for LCM2020