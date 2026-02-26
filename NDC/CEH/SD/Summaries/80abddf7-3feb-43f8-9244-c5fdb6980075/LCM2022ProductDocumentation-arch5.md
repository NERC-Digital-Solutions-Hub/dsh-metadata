# The UKCEH Land Cover Map for 2022

- Purpose and scope: User guide for the UKCEH Land Cover Map 2022 (LCM2022). Describes data production, validation, and data accuracy to help users make informed decisions about applying LCM2022 data. Seven datasets cover Great Britain and Northern Ireland (GB and NI) plus a 1 km summary raster.

- Product suite (data held and structure):
  - 10 m Classified Pixel datasets (GB and NI): classified mosaic of Classification Scenes. First band = most likely UKCEH Land Cover Class; second band = class membership probability/confidence.
  - 25 m Rasterised Land Parcel datasets (GB and NI): rasterised version of land parcels with three bands per parcel (mode, conf, purity) to provide parcel-level attributes.
  - Land Parcel Products (GB and NI): vector/parcels aligned to the UKCEH Land Parcel Spatial Framework; includes descriptive attributes.
  - 1 km Summary Raster products (GB and NI): dominant class and percentage cover for each 1 km pixel derived from 25 m rasters; percentage values are integer and may not sum exactly to 100 due to rounding.
  - Additional context: Seasonal Composite Images (Sentinel-2 based), Context Rasters, and Classification Scenes underpin the 10 m pixel classification.

- Spatial and data governance details:
  - Coordinate systems: GB uses British National Grid (EPSG: 27700); NI uses Irish Grid (TM75, EPSG: 29903).
  - Extents: GB 0–700,000 m E, 0–1,300,000 m N; NI truncated to the extent of Northern Ireland.
  - Minimum mapping unit: approximately 0.5 ha (MMU) within the UKCEH Land Parcel Spatial Framework.
  - Land Parcel Spatial Framework: used to group 10 m pixels into parcels; changes in parcel identifiers relative to LCM2015 may affect cross-year parcel comparisons.
  - Access and citation: Each dataset has a DOI; citations provided (Marston et al. 2023/2024 family of papers) to support data provenance and methods.

- Data production workflow:
  - Seasonal Composite Images: created from Google Earth Engine using Sentinel-2 spectral bands (10 m resolution for most bands); four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec) with some gaps due to cloud cover.
  - Classification Scenes and Context Rasters: Classification Scenes combine seasonal spectra with 10 m Context Rasters (GB) or NI context (urban mask, coast/freshwater/road distances, etc.) to resolve spectral confusion.
  - Bootstrap Training and Random Forest: Bootstrap Training uses historical LCM data (LCM2019, 2020, 2021) with high-probability pixels (>80%) that remained consistent across years to train a Random Forest classifier; sampling balanced across classes to avoid domination by common classes.
  - Model and software: Custom UKCEH pipeline integrating Weka, PostGIS, and GDAL; RF classification yields the 10 m Classified Pixel product.
  - Validation approach: 33,107 validation points across all 21 classes; overall accuracy reported at 86.1%.

- Class definitions and relationships:
  - 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats; deliberate mappings and notes on differences between UKCEH classes and BAP Broad Habitats; Appendix 1 and 2 provide detailed mappings and caveats, including nuances for classes like Broadleaved woodland, Coniferous woodland, Arable, Various Grasslands, Bracken, Heather, Fen/Marsh/Swamp, Bog, Inland Rock, Saltwater, Freshwater, Urban/Suburban, and Coastal/Littoral classes.
  - Generalized aggregate classes are available in the Land Parcel product to support users who require less thematic detail.

- Validation and known issues:
  - Overall accuracy: 86.1% (full thematic detail) from formal validation.
  - Known issues: a small number of polygons missing from vector land parcel products causing nodata areas in 25 m rasterised parcels; effect is negligible for 1 km products and the 10 m classified pixels are unaffected.
  - Method changes and disclaimers: LCM2022 notes ongoing methodological evolution; changes between maps can reflect real land-cover change and/or shifts in classification methods.

- Data quality, provenance, and reuse:
  - DOIs and formal citations provided for all LCM2022 data products; references include Marston et al. (2024a–g) and prior LCM literature.
  - Disclaimer on method updates: annual production aims to improve temporal consistency and change detection; results can include both real change and methodological differences.
  - Appendices provide additional context for color schemes (Appendix 5 and 6) and correspondence matrices (Appendix 4) to support data use and validation.

- Practical guidance for data stewards:
  - Governance and interoperability: clear dataset naming, DOIs, versioning, and cross-dataset references support reproducibility and data integration across GB and NI.
  - Metadata and documentation: extensive methodological description, validation results, and appendices enable assessment of suitability for reuse, with explicit notes on BAP relationships and potential spectral confusion.
  - Update and maintenance considerations: annual map production with evolving methods; users should account for possible methodological shifts when performing temporal comparisons.
  - Accessibility: data hosted with DOIs at NERC EDS; accompanying resources include color palettes for mapping and QGIS symbology files to aid reuse.

- Appendices and resources at a glance:
  - Appendix 1–2: UKCEH Land Cover Class notes and BAP Broad Habitat mappings, including guidance on interpretation and potential spectral confusion.
  - Appendix 3: Full list of LCM2022 datasets and their DOIs.
  - Appendix 4: Correspondence matrices for validation accuracy by class (producer and user accuracy statistics).
  - Appendix 5–6: Recommended color schemes for displaying UKCEH Land Cover Classes (standard and color-blind friendly) plus corresponding QGIS symbology files.