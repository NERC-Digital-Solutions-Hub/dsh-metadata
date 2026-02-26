# Dataset documentation

- Purpose: Land Cover Change 1990-2015 dataset (LCC1990_2015) provides a 5-band, 25m raster to map land cover change in the UK over 1990–2015, supporting environmental monitoring and greenhouse gas inventory tracking (LULUCF). Two main use modes: full-coverage bands 1 and 2 for model inputs and change visualization, or bands 3–5 for targeted analysis of areas where change occurred.

- Product scope: Based on simplified versions of Land Cover Maps for 1990 (LCM1990) and 2015 (LCM2015), created with consistent methods to enable change mapping. A revised 1990 version enables robust 25-year change mapping.

- Data structure (5 bands):
  - Band 1: Simplified 1990 classes (6 classes)
  - Band 2: Simplified 2015 classes (6 classes)
  - Band 3: Binary change layer (0 = no change, 1 = change)
  - Band 4: Change from class (0–6) for areas that changed
  - Band 5: Change to class (0–6) for areas that changed

- Class framework:
  - Bands 1–3 use a 6-class system: Woodland, Arable, Grassland, Freshwater, Built-up areas, Other
  - Bands 4–5 map the specific “change from” and “change to” classes for changed areas
  - Aggregated from 21 original LCM classes into the 6 simplified classes (Table 3 mapping)

- Spatial coverage and resolution:
  - Great Britain: 25m pixels, 28,000 columns × 52,000 rows
  - Northern Ireland: 25m pixels, 7,600 columns × 6,400 rows
  - Projections: GB uses British National Grid (EPSG 27700); NI uses TM75 Irish Grid (EPSG 29903)

- Corrections and quality adjustments:
  - Inter-tidal and water area classification corrections to avoid false change signals
  - Rock/non-rock changes above 600m altitude corrected using NextMAP DEM
  - River fragments and water body misclassifications identified and masked from bands 3–5 (and applied to bands 1–2 for consistency)

- Derivation and methodology:
  - LCM1990 and LCM2015 originally 21-class parcel-based maps; re-aggregated to 6-class system to improve change-mapping accuracy
  - Change product designed to support both complete coverage inputs and targeted change analyses
  - A full validation exercise comparing maps to other datasets (e.g., Countryside Survey, National Forest Inventory) completed; results to be published separately

- Data access and citation:
  - Available via the CEH Environmental Information Platform (eip.ceh.ac.uk)
  - DoIs per dataset for citation (GB and NI variants provided)
  - Usage guidance recommends citing with authors and date in text and full DOI in references

- Metadata and documentation:
  - Pixel size: 25m (GB and NI)
  - Data type: 8-bit unsigned GeoTIFF, uncompressed
  - Data lineage and related dataset DOIs listed for reference (Rowland et al. 2020; Rowland et al. 2017)
  - Queries: spatialdata@ceh.ac.uk

- Quality assurance and provenance:
  - Data created with defined scripts and trained staff; multiple QA checks for projections, completeness, band integrity, pixel size, and specification conformance
  - Ground-truthing and validation against alternative datasets planned for publication

- Acknowledgement and funding:
  - Supported by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme

- Related context:
  - The document focuses on Land Cover Change data; for full land cover maps, refer to corresponding LCM dataset documents.