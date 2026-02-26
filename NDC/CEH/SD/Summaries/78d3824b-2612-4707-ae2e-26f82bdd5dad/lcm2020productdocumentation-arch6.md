# The UKCEH Land Cover Map for 2020

- Purpose and scope
  - User guide for UKCEH LCM2020, an annual land cover map product for Great Britain and Northern Ireland.
  - Product suite consists of six datasets (three per region): 10m Classified Pixel dataset, Land Parcel dataset, and 25m Rasterised Land Parcel dataset.
  - Aims to support informed decision-making with production methods, validation, and accuracy details to facilitate appropriate use.

- Datasets and formats
  - 10m Classified Pixel datasets (GB and NI): per-pixel land cover class (UKCEH LC Class) with a second band giving the classification probability/confidence; not generalized by the Land Parcel Spatial Framework to preserve fine features; intended for specialist users.
  - Land Parcel datasets (GB and NI): parcels derived by intersecting 10m pixels with the UKCEH Land Parcel Spatial Framework; parcel-level attributes provided; parcel counts: GB approx. 6.74 million; NI approx. 0.90 million.
  - 25m Rasterised Land Parcel datasets (GB and NI): per-parcel rasters with 3 bands: dominant land cover class (mode), mean probability/confidence (_conf), and mean purity (_purity).
  - 10m Context Rasters and Seasonal Composite Images (Sentinel-2) used for classification; 100x100 km classification Scenes for GB (74 overlapping tiles) and a single 100x100 km tile for NI.
  - Coordinate systems: GB datasets EPSG:27700; NI datasets EPSG:29903.

- How the classification is done
  - Bootstrap Training: uses historical LCM data (LCM2017–2019) filtered to >99% purity to automatically generate training data for subsequent maps; enables self-starting training without new field data.
  - Random Forest classifier: trained on labelled parcels; balanced classes by sampling 10,000 pixels per class with replacement; outputs per-pixel class membership and confidence.
  - Software stack: bespoke classifier integrating Weka, PostGIS, and GDAL (open-source tools).

- Data production and validation
  - Annual automated production to maximize temporal consistency and enable change detection; minimal manual correction to scale.
  - Validation: 34,715 validation points across GB countryside survey data, National Forest Inventory, IACS, and bespoke validation points; overall thematic accuracy 79.2% (Appendix 4).
  - Validation detail: confusion matrices show varying Producer’s and User’s accuracies by class (e.g., Urban ~82%, Heather grassland often lower ~34% in some cases; Saltmarsh ~96% User’s accuracy).

- Land Cover Classes and BAP Broad Habitats
  - 21 UKCEH Land Cover Classes linked to UK Biodiversity Action Plan (BAP) Broad Habitats, with notes on how they relate and where they diverge (Appendices 1–2).
  - Important nuance: BAP Broad Habitats describe field-interpretation classes; UKCEH classes are remote-sensing mapped and may differ slightly; italicization and capitalization conventions clarify mapping between systems.

- Seasonal imagery and context
  - Seasonal Composite Images derived from Sentinel-2 (bands 2–12) across four seasons; some cloud gaps exist but classifier tolerates partial spectral data.
  - Context Rasters (GB and NI) provide terrain, proximity, and coastal/open data masks to reduce spectral confusion (e.g., Height, Slope, Distance to buildings/roads/sea/freshwater; urban mask for NI).

- Land Parcel Spatial Framework
  - Framework used to aggregate 10m pixels into parcels; ensures discrete real-world units (approx. 0.5 ha MMU); supports change detection.
  - Note on identifiers: gid/parcel IDs do not exactly match LCM2015 if cross-year comparison is required.

- Outputs and interpretation guidance
  - 10m Classified Pixels: Band 1 = UKCEH Land Cover Class ID; Band 2 = class probability/confidence.
  - 25m Rasterised Land Parcels: Band 1 = modal class; Band 2 = conf; Band 3 = purity.
  - Outputs reflect detailed spatial patterns; 10m pixels preserve narrow features but were validated against parcel-based data rather than the 10m pixels alone.
  - Users should be aware of potential near-coastal Saltwater vs Freshwater confusion and upland peatland mapping challenges; small patches below the MMU may be underrepresented.

- Appendix highlights and metadata
  - Appendix 4: detailed correspondence matrices and accuracy metrics by class (Producer’s and User’s accuracies).
  - Appendix 5: full list of LCM2020 datasets and their official names by region.
  - Appendix 3: recommended color recipes for displaying each UKCEH Land Cover Class.

- Practical takeaway for data support and reuse
  - LCM2020 provides a reproducible, automated annual land cover product with substantial historical training data, enabling change detection and consistent time-series analyses.
  - The combination of 10m classified pixels and 25m land parcel rasters offers both detailed mapping and parcel-level summaries for diverse applications.
  - Users should reference Appendices for class definitions, validation details, and display conventions, and should be mindful of cross-year compatibility when comparing with LCM2015/earlier datasets.