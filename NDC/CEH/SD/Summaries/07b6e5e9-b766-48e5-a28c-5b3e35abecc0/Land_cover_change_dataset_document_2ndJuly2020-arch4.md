# Land Cover Change 1990 - 2015

- A 5-band, 25 m raster dataset mapping land cover change in the UK between 1990 and 2015 (LCC1990_2015), produced from simplified versions of Land Cover Map 1990 (LCM1990) and Land Cover Map 2015 (LCM2015).
- Intended for use as a data product to support change detection, modelling, and greenhouse gas inventory tracking (LULUCF), with bands designed for different analytical workflows.
- Two main modes of use:
  - Bands 1 and 2 provide complete spatial coverage for modelling change across the UK (1990 vs 2015).
  - Bands 3–5 provide partial coverage focused on areas where change occurred, useful for quantifying locations, types, and extents of change.

- Dataset lineage and aggregation:
  - LCM1990 and LCM2015 were originally 21-class maps; these have been aggregated to 6 simplified classes to improve change-mapping accuracy.
  - The 6 classes are suitable for LULUCF tracking and related reporting.
  - The product includes corresponding DOIs to enable reproducible citation.

- Band descriptions:
  - Band 1: Simplified 1990 classes (6-class mapping).
  - Band 2: Simplified 2015 classes (6-class mapping).
  - Band 3: Binary change layer (0 = no change, 1 = change).
  - Band 4: Change from class (0–6), showing what the area was in 1990 before the change.
  - Band 5: Change to class (0–6), showing what the area was in 2015 after the change.
- Bands 1–3 provide complete coverage (0 denotes no change for bands 1–3); Bands 4–5 map only areas undergoing change.

- Classes (simplified to 6):
  - 1: Woodland
  - 2: Arable
  - 3: Grassland
  - 4: Water (Freshwater)
  - 5: Built-up areas
  - 6: Other

- Corrections applied to improve reliability (bands 3–5; consistency with bands 1–2):
  - Inter-tidal and water classification issues excluded changes between water/inter-tidal classes.
  - Rock vs non-rock confusion above 600 m was mitigated using NextMAP DEM data.
  - River fragments and certain water bodies were identified and masked to remove false changes.
  - Corrections applied across bands 3–5 and also to band 1 for model-consistency.

- Derivation and purpose:
  - Aggregation to 6 classes increases mapping accuracy and supports LULUCF/GHG inventory reporting.
  - LCM1990/LCM2015 are parcel-based maps created from satellite data, aligned to UK Biodiversity Action Plan Broad Habitat definitions.

- Data access, structure, and metadata:
  - Available via the CEH Environmental Information Platform.
  - Great Britain: 25 m pixel size; 28,000 columns × 52,000 rows; British National Grid (EPSG 27700).
  - Northern Ireland: 25 m pixel size; 7,600 columns × 6,400 rows; TM75 Irish Grid (EPSG 29903).
  - Data distributed as uncompressed GeoTIFFs; potential compression recommended for storage.
  - GB and NI datasets provided separately to accommodate different projections.
  - Pixel origin: southwest corner of the lower-left pixel.

- Usage guidance and citation:
  - DOIs provided for Land Cover Change products to support citation and reproducibility.
  - When citing, include authors and date in text and full DOI in references.
  - Queries: spatialdata@ceh.ac.uk
  - A journal paper detailing the dataset is in preparation.

- Quality assurance:
  - Data produced using defined scripts and trained staff.
  - QA checks include projections, spatial completeness, band integrity, pixel size, and alignment with the specification (Tables 3 and 5 references).
  - Full validation conducted against other datasets (e.g., Countryside Survey, National Forest Inventory); results to be published separately.

- Documentation and acknowledgments:
  - Acknowledges NERC Environmental Environmental Information Centre support under UK-SCAPE programme.
  - References provided for foundational LCM1990/LCM2015 products and related methodology.

- Additional notes:
  - The documentation distinguishes between the original 21-class LCM data and the six-class aggregation used for the change product.
  - The correction steps specifically address known systemic issues to reduce spurious change detection and improve reliability for policy, planning, and scientific use.