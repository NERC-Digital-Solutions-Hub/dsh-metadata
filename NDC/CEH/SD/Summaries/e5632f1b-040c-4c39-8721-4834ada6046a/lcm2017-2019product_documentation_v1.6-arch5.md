# The UKCEH Land Cover Maps for 2017, 2018 and 2019 v1.6 18/06/2020

## Purpose and scope
- User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
- Each map represents a range of geospatial datasets describing land cover across Great Britain (GB) and Northern Ireland (NI).
- Aims to help users understand data content, production decisions, validation, and future plans for informed application and governance.

## Data products overview
- Land Cover Classes: 21 UKCEH Land Cover Classes based on UKBAP Broad Habitats; generally aligned with LCM2015. Aimed at consistent change detection over time.
- Aggregate classes: 10 UKCEH Aggregate Classes, providing generalized summaries.
- Product suite and extents: dataset package described similarly to LCM2015 but expanded with an additional dataset; GB and NI versions produced for each year (2017–2019), yielding 42 datasets in total.
- Spatial resolution and data types:
  - 20 m Classified Pixels: new RF-based pixel classifications with per-pixel class and confidence (0–100).
  - 25 m Rasterised Land Parcels: rasterised summaries of land parcel attributes.
  - 1 km Raster Products: including Percent Cover (21 bands), Percent Aggregate Cover (10 bands), Dominant Cover (1 band), and Dominant Aggregate Cover (1 band).
- Coordinate systems and extents:
  - GB: British National Grid (EPSG: 27700).
  - NI: Irish Grid (TM75 / EPSG: 29903).
- Dataset structure: GB and NI versions for each year; Level breakdown shown in figures/tables; Appendix 6 lists full dataset names.

## Production workflow and methodology
- Bootstrap Training:
  - Automatic training process using historic UKCEH LCM observations to bootstrap training data.
  - Bootstrap training data originate from UKCEH LCM2015 (majority signal approach), enabling rapid production without new field surveys.
  - Future plans continue bootstrap from majority signals (e.g., 2017–2019 for 2020; 2018–2020 for 2021).
- Random Forest classification:
  - RF classifier trained with balanced sampling (10,000 samples per class per training bag) using bootstrap-derived training data.
  - Produces 20 m Classified Pixels, the basis for subsequent derivatives (Land Parcels, 25 m raster parcels, and 1 km products).
  - Production uses a bespoke pipeline combining Weka, PostGIS, and GDAL (open source).
- Seasonal data and classification scenes:
  - Sentinel-2 Seasonal Composite Images (TOA reflectance) by season, produced in Google Earth Engine.
  - Context rasters (10–20 m) provide terrain, proximity to features, and other contextual cues to aid classification.
  - GB Classification Scenes: 100 km x 100 km tiles (36-band spectral + 10 context bands; 46 bands total) used for independent training/classification; NI uses a single 43-band scene per year (36 spectral + 7 context).
- Context rasters and ancillary data:
  - 20 m GB context rasters include height, aspect, slope, distances to buildings/roads/sea/freshwater, foreshore and tidal masks, and a woodland mask.
  - NI context rasters include similar terrain metrics plus urban mask, coast and freshwater proximity measures.
- Land Parcel Spatial Framework:
  - 0.5 ha minimum mappable unit (MMU); parcels generalised from national cartography to represent discrete land units (fields, parks, urban areas, etc.).
  - Framework enables time-series comparison via overlap with 20 m Classified Pixels summaries.
  - The gid identifiers for parcels differ from LCM2015 but gid-based comparisons are possible across LCM2017–2019.
- Changes since LCM2015:
  - Attribute naming updated to align with production software; some field descriptions removed (e.g., Composite).
  - 20 m Classified Pixels retain finer details than 25 m parcels; land parcel attributes updated (see Table 3).

## Data structure, datasets, and metadata
- Datasets included in each year’s package (GB and NI variants):
  - 20 m Classified Pixels (GB/NI)
  - Land Parcels (GB)
  - 25 m Rasterised Land Parcels (GB)
  - 1 km Dominant Cover (GB/NI)
  - 1 km Dominant Aggregate Cover (GB/NI)
  - 1 km Percent Cover (GB/NI)
  - 1 km Percent Aggregate Cover (GB/NI)
- Dataset attributes (highlights):
  - Gid: unique parcel identifier; _hist (histogram of class counts per parcel); _mode (dominant class); _purity (parcel-level purity); _conf (mean class membership probability); _stdev (uncertainty); _n (number of 20 m pixels in parcel).
  - 25 m Rasterised Land Parcels include three bands: dominant class (_mode), confidence (_conf), and purity (_purity).
- Class definitions and relationships:
  - UKCEH Land Cover Classes (21) and UK BAP Broad Habitats; Appendix 1 and 2 describe mapping rationales, code values, and mapping considerations.
  - Coastal and inland, urban, and various habitat classes defined with notes on spectral detectability and context-based distinctions.
- Validation and quality:
  - Validation against GB countryside survey data, National Forest Inventory, IACS, and bespoke validation points (n ≈ 22,325).
  - UK-scale overall accuracies: LCM2017 ≈ 78.6%, LCM2018 ≈ 79.6%, LCM2019 ≈ 79.4%.
  - Validation data are not absolute truth; status and class conversions introduce some subjectivity.
- Appendices and references:
  - Appendix 1–3 include detailed class descriptions, color schemes for display, and color-blind friendly schemes.
  - Appendix 5 provides confusion matrices and producer/user accuracy by class.
  - Appendix 6 lists full datasets per year and their digital holding names.

## Data governance, provenance, and stewardship
- Data lineage and reproducibility:
  - Fully automatic pipeline designed to minimize manual corrections; aims for annual updates.
  - Bootstrap Training ensures continuity with historical data to maintain consistency in time-series analyses.
- Metadata and standards:
  - Clear documentation of data content, methods, and decisions to enable reuse and governance.
  - Differences in parcel identifiers across years acknowledged; gid-based cross-year comparisons recommended.
- Validation and limitations:
  - Validation figures indicate strong performance but acknowledge potential misclassification due to spectral similarity, mosaic habitats, or training data limitations.
  - Spectral confusion managed via Context Rasters and Seasonal Composite information; some upland peatland nuances flagged for future improvement.
- Open-source and tooling:
  - Use of Weka, PostGIS, and GDAL; data processing and classification employ open-source technologies.

## Data access, formats, and management
- Coordinate systems and projections:
  - GB: British National Grid (EPSG: 27700).
  - NI: Irish Grid (EPSG: 29903).
- Data products and dissemination:
  - Yearly LCM2017, LCM2018, LCM2019 datasets and corresponding GB/NI variants.
  - Packaged with multiple dataset types, suitable for GIS analysis and change detection.
- Practical considerations for users and stewards:
  - The 20 m Classified Pixels provide the most detailed base and should be used when fine-scale features are important.
  - Land Parcels and 25 m rasters are useful for aggregated analyses and for reducing noise.
  - 1 km products enable rapid, wide-area summaries and compatibility with coarser-scale workflows.
- Future directions and updates:
  - Ongoing assessment of input data sources (e.g., SR vs TOA in Sentinel-2) and potential inclusion of radar data (Sentinel-1) to improve fill gaps.
  - Plan to increase the frequency of releases and to refine upland vegetation mappings with improved training data.

## Key caveats and practical notes
- Class definitions are tied to historical BAP Broad Habitats; some spectral/ground-truth distinctions may not be perfectly separable by satellite data.
- No manual corrections for this release; classification errors are expected to be randomly distributed over time, but localized biases can occur.
- The Land Parcel Spatial Framework is unchanged in geometry from LCM2015, but storage/indexing changes mean parcel IDs (gid) do not match exactly across years.
- Validation datasets come from varied sources with different objectives; results should be interpreted as indicative rather than absolute truth.

## Summary for data stewardship
- The UKCEH LCM2017–2019 v1.6 products provide a robust, automatically generated and validated set of land cover maps across GB and NI, with a transparent methodology and clear provenance.
- Governance considerations include maintaining versioned datasets, documenting methodological changes, handling gid cross-year comparability, and communicating uncertainties to users.
- The data are structured to support both detailed local analyses (20 m pixels) and broad-scale change monitoring (1 km products), with open-source tooling and extensive metadata to facilitate discoverability, reuse, and governance.