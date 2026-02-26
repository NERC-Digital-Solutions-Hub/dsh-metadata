# The UKCEH Land Cover Map for 2022

- Purpose and scope
  - User guide for UKCEH Land Cover Map 2022 (LCM2022), the tenth UK land cover map.
  - Product consists of seven datasets: three for Great Britain (GB) and Northern Ireland (NI) each (a 10 m classified pixel dataset, a dataset of land parcels, and a 25 m pixel rasterised land parcel dataset) plus a 1 km summary raster product covering GB and NI.
  - Aims to help users understand data production, validation, and data accuracy to make informed decisions on applications.

- Data products and structure
  - 10 m Classified Pixels (GB and NI): mosaic of Classification Scenes; each pixel holds the most likely UKCEH Land Cover Class plus a class membership probability/confidence.
  - Land Parcel datasets (GB and NI): derive parcel attributes by intersecting 10 m classified pixels with the UKCEH Land Parcel Spatial Framework (minimum parcel size ~0.5 ha/MMU).
  - 25 m Rasterised Land Parcels (GB and NI): raster version of parcel data with three bands per parcel (dominant land cover, mean confidence, and parcel purity).
  - 1 km Summary Rasters (GB and NI): summarised from 25 m data to provide dominant class, percentage cover per class, and aggregate classes (with rounding considerations near coastlines).
  - Seasonal Composite Images: four-season Sentinel-2 based oblique spectral data; used with Context Rasters to form Classification Scenes.
  - Context Rasters (GB and NI): 10 m ancillary layers (terrain, proximity to features such as roads, water, buildings, foreshore, etc.) to improve discrimination among spectrally similar classes.
  - Classification Scenes: GB divided into ~32 tiles; NI uses a single 49-band scene; scenes are trained/classified independently to manage regional variation.

- Methodology and production
  - Bootstrap Training: automatic, field-data-free training using historic LCM observations (LCM2019–LCM2021) filtered for high probability and cross-year consistency; enables self-starting improvements without fresh field data.
  - Random Forest classification: balanced sampling of 10,000 samples per bag; produces per-pixel class and associated confidence.
  - Software stack: bespoke UKCEH pipeline integrating Weka, PostGIS, and GDAL (open source).
  - UK Land Parcel Spatial Framework: fixed structure to reduce noise and support change detection; MMU ~0.5 ha; parcel identifiers may differ from LCM2015 for cross-map comparison.
  - Dataset updates: annual production with ongoing methodological improvements; significant accuracy improvements can trigger re-application across the catalogue to maximise temporal consistency and change detection.

- Data quality, validation and accuracy
  - Validation: 33,107 validation points across all 21 UKCEH Land Cover Classes.
  - Overall accuracy: 86.1% for LCM2022 (full thematic detail).
  - Known issues: a small number of polygons missing from vector land parcel products (affects 25 m rasterised parcels minimally; 10 m classified pixels unaffected).
  - Validation caveats: validation against 25 m rasterised land parcels; some inter-class confusion remains (notably among upland vegetation, bog, fen, acid/neutral/calcareous grassland, and coastal types).

- Access, citation, and provenance
  - Each LCM2022 dataset has a DOI and should be cited accordingly; DOIs and references are provided in the dataset tables.
  - References include Marston et al. (2023, 2024) detailing production methods and dataset-specific publications.
  - Disclaimer: methods evolve; annual changes may reflect real land-cover change or methodological updates.

- Governance, usability, and future directions (Data Stewards perspective)
  - Annual production supports monitoring state and change of UK countryside; helpful for change detection and attributing observed changes.
  - Clear metadata needs: ensure accessibility of 10 m vs 25 m products, parcel identifiers, MMU and spatial framework details, CRS, extents, and band definitions.
  - Data management considerations: maintain provenance by linking DOIs to each product; track updates to bootstrap training data sources (LCM2019–LCM2021) and any re-application decisions.
  - Interoperability: be aware of potential differences with prior LCM versions (e.g., parcel IDs not matching LCM2015); plan for cross-map temporal analyses accordingly.
  - Documentation and tools: Appendix materials include class descriptions, BAP Broad Habitats mappings, recommended colour schemes (including colour-blind friendly options) and QGIS symbology files to support usable workflows.

- Key data schemas and formats (high level)
  - 10 m Classified Pixels: GB and NI, 2 bands (class, confidence) per pixel.
  - 25 m Rasterised Land Parcels: 3-band rasters per parcel (dominant class, conf, purity).
  - 1 km Summary Rasters: multiple bands (dominant and percentage covers for both classes and aggregates).
  - Coordinate systems: GB (British National Grid, EPSG:27700) and NI (TM75 Irish Grid, EPSG:29903).
  - Extents and extent details: GB full extent; NI truncated to Irish grid as specified.
  - MMU and parcel framework: ~0.5 ha minimum parcel; designed to represent real-world units such as fields, parks, woodlands, etc.

- Appendices and supporting resources (highlights)
  - UKCEH Land Cover Classes descriptions and crosswalks to UK BAP Broad Habitats; detailed descriptions and notes on potential spectral confusion.
  - Full dataset catalog and DOIs; recommended delivery and usage references.
  - Appendix 5 and 6: colour recipes for displaying land cover classes (including colour-blind friendly variants) and accompanying QGIS symbology files.
  - Bootstrap Training and classification notes, context for understanding classifier behavior and interpretation of confidence values.

- Practical considerations for data stewardship
  - Ensure datasets are discoverable with proper DOIs and citation guidance; provide users with guidance on interpreting 10 m confidence bands and 25 m parcel attributes.
  - Communicate validation status and known issues to data users; maintain versioning aligned with annual updates.
  - Manage expectations around accuracy limits and potential classification confusions, especially for habitat types with spectrally similar signals.
  - Facilitate reuse by documenting methodology, data lineage, and access pathways to all product components (10 m pixels, land parcels, 25 m rasters, 1 km rasters).