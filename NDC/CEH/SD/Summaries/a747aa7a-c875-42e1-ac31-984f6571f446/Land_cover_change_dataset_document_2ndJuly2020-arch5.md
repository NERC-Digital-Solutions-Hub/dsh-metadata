# Dataset documentation

- The Land Cover Change 1990-2015 dataset is a 5-band, 25 m raster covering the UK, designed to map changes between 1990 and 2015. The document focuses on the Land Cover Change product; details for the Land Cover Maps are in separate dataset documents.
- It is derived from simplified versions of the Land Cover Maps (LCM1990 and LCM2015) and uses a consistent method to enable reliable change detection. A revised LCM1990 version enables the 25-year change product.

## Land Cover Change product
- Produced by casting 21-class LCMs into 6 simplified classes to improve change mapping accuracy.
- The 5 bands are:
  - Band 1: simplified 1990 classes (6 classes)
  - Band 2: simplified 2015 classes (6 classes)
  - Band 3: binary change layer (0 = no change, 1 = change)
  - Band 4: 'change from' class (0–6; only where change occurred)
  - Band 5: 'change to' class (0–6; only where change occurred)
- Two principal use modes:
  - Bands 1–2 provide full UK coverage for modeling; the 1990 vs 2015 difference reflects overall change.
  - Bands 3–5 provide partial coverage of change areas for analyses focused on where and what changes occurred.

## Data Structure
- Band 1 and Band 2 are the complete spatial coverage (GB and NI) for model inputs.
- Bands 3–5 map only areas undergoing change; values indicate change type and direction.
- The 6 simplified classes are mapped from the original 21 LCM classes (see detailed mappings in the documentation).

## Corrections applied to the change data set
- Inter-tidal areas: changes between water and inter-tidal zones excluded to avoid false change signals; freshwater-saltwater confusion addressed.
- Rock/non-rock confusion above 600 m: excluded changes using the NextMAP DEM due to challenging conditions (cloud, topography, snow).
- River fragments and water bodies: false positives in change-to water removed using known river networks and manual masking.
- Corrections applied to bands 3–5 (and also to band 1 for consistency when used as model inputs).

## Derivation of the Land Cover Change data set
- 1990 and 2015 LCMs (21 classes) were reclassified into 6 simplified classes to improve accuracy of detected changes.
- LCM1990 and LCM2015 are parcel-based maps created from consistent methods to enable robust change mapping, aligned with Biodiversity Broad Habitat definitions.
- The 6-class schema supports LULUCF tracking for greenhouse gas inventories.

## Citing Land Cover Change (DOI's)
- Each dataset (GB and NI) has a DOI to enable repeatable methods and usage tracking.
- Guidance provided for including authors/date and DOI in citations; DOIs enable traceable use and publication standards.

## Quality Assurance
- Data are produced with defined scripts and trained staff.
- QA checks verify projections, completeness, band integrity, pixel size, and alignment with the specified product.
- The parcel framework is based on 2007 Ordnance Survey Mastermap data; full validation against other datasets is planned and will be published separately.

## Data Access and Further Information
- Available via the CEH Environmental Information Platform.
- Separate datasets for Great Britain and Northern Ireland to reflect different projections.
- Metadata details:
  - Pixel size: GB and NI both 25 m
  - Dimensions: GB 28,000 columns x 52,000 rows; NI 7,600 x 6,400
  - Origin: GB lower-left easting/northing start at 1; NI starts at easting 180,000 and northing 300,000
  - Data type: unsigned 8-bit, uncompressed GeoTIFF (GB 27700; NI 29903)
  - Coordinate systems: GB = British National Grid (EPSG 27700); NI = TM75 Irish Grid (EPSG 29903)
- Data access contact: spatialdata@ceh.ac.uk
- A journal paper with additional information is in preparation.

## Acknowledgement
- Funded by the Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE programme delivering National Capability.

## References
- Jackson, 2000; Broad Habitat guidance
- Rowland et al., 2017a,b; LCM2015
- Rowland et al., 2017a,b; LCM2015 (NI)
- Rowland et al., 2020a,b; LCM1990
- Data citations for GB and NI Land Cover Change products (DOIs provided in the document)