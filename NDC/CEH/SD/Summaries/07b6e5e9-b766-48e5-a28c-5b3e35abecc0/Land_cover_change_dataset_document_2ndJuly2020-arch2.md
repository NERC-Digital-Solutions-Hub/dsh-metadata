# Dataset documentation

- Land Cover Change 1990-2015 (LCC1990_2015) is a 25m, 5-band raster dataset produced to map land cover change over 1990–2015 and support environmental monitoring and greenhouse gas inventory reporting.
- The dataset is derived from simplified versions of LCM1990 and LCM2015 to enable consistent change mapping.

## Data product and structure
- Band 1: Simplified 1990 classes cast into 6 classes.
- Band 2: Simplified 2015 classes cast into 6 classes.
- Band 3: Binary change layer (0 = no change, 1 = change).
- Bands 4 and 5: 'Change from' and 'change to' classes for areas that changed (values 0–6).
- Two principal usage modes:
  - Bands 1–2 provide full UK coverage and can be used as model inputs to reflect 1990→2015 differences.
  - Bands 3–5 provide partial coverage focusing on areas where change occurred, useful for quantifying locations, extent, and types of change.

## Class scheme
- 6 simplified land cover classes (Table 2):
  - 1 Woodland
  - 2 Arable
  - 3 Grassland
  - 4 Water (Freshwater)
  - 5 Built-up areas
  - 6 Other

## Derivation and aggregation
- LCM1990 and LCM2015 (originally 21 classes) were reclassified to 6 aggregate classes to improve change-detection accuracy and support LULUCF tracking.
- Aggregation aligns with 21-class LCM definitions and broader habitat classifications.

## Corrections and data quality adjustments
- Inter-tidal areas: water and inter-tidal zones classified differently; changes between these classes excluded from bands 3–5 to avoid false changes.
- Rock/non-rock confusion above 600 m: areas above 600 m (based on NextMAP DEM) excluded from change bands due to spectral/topographic challenges.
- River fragments and water bodies: false positive water change adjustments; river networks used to identify/remove erroneous changes; other water bodies also masked as needed.
- Corrections applied to bands 3–5 and applied to band 1 to maintain consistency with model inputs.

## Digital Object Identifiers (DOIs) and citation
- Each Land Cover Change product has a DOI for citation to ensure reproducibility (GB and NI variants listed in Table 4).
- Guidance: cite authors and date in text and include full DOI in references.

## Quality Assurance
- QA checks cover projection correctness, spatial completeness, band integrity, pixel size, and overall conformance to the specification.
- Validation against independent datasets (e.g., UK Countryside Survey, National Forest Inventory) has been conducted; results to be published separately.

## Access and metadata
- Available via the CEH Environmental Information Platform (EIP): https://eip.ceh.ac.uk/
- Separate data sets for Great Britain and Northern Ireland due to different projections:
  - Great Britain: 25 m pixel size; 28,000 columns × 52,000 rows; lower-left easting/northing 0/0; British National Grid (EPSG 27700).
  - Northern Ireland: 25 m pixel size; 7,600 columns × 6,400 rows; lower-left easting 180,000; lower-left northing 300,000; TM75 Irish Grid (EPSG 29903).
- Data type: unsigned, uncompressed 8-bit GeoTIFF for both GB and NI.
- Notes: SW corner pixel references; uncompressed files may be reduced in size via compression.

## Usage notes for analysts
- Purpose-built for monitoring environmental change and policy performance over time.
- Suitable for:
  - Using bands 1–2 as inputs to models to assess 1990–2015 transitions.
  - Analyzing bands 3–5 to quantify change locations, extents, and transition types (change from/to).
- Data corrections improve reliability in intertidal, high-altitude rocky areas, and river/water-change detection, enhancing accuracy for environmental monitoring and reporting.

## Documentation and references
- Primary documentation and data citations maintained; see accompanying references for methodology and data lineage (Rowland et al. 2017a,b; 2020a,b; Jackson 2000).
- Acknowledgement: funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability.