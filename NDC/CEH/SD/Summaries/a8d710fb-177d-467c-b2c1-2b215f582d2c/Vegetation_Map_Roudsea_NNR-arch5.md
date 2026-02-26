# Vegetation map of the Roudsea Wood National Nature Reserve, 1962

## Overview
- A digital shapefile (Roudsea_Veg_1962.shp) representing vegetation parcels within Roudsea Wood NNR (Cumbria) on the western side of the reserve.
- Original field map created in 1962 by R. Donelly and N. English; digitized in 2019 by the Centre for Ecology & Hydrology from the original map.
- Nomenclature follows Flora of the British Isles (1962).

## Data content and format
- Format: ESRI Shapefile containing polygons (SHAPE) for vegetation parcels.
- Core attributes include:
  - TREE_COV and DESC_TC (tree cover code and description)
  - TREE_COV2 and DESC_TC2 (secondary tree cover code/description)
  - STOCKING and DESC_ST (stocking code/description)
  - STOCKING2 and DESC_ST2 (secondary stocking code/description)
  - GVEG_MAJ and DESC_MAJ (major ground vegetation communities)
  - GVEG_MAJ2 and DESC_MAJ2 (secondary major communities)
  - GVEG_MIN and DESC_MIN (minor ground vegetation communities)
  - GVEG_MIN2 and DESC_MIN2 (secondary minor communities)
  - OTHER (any additional information)
  - GLOBALID (unique identifier)
  - POLY_AREA (polygon area in square meters)
- Field types include geometry, text, and long integer values.

## Provenance, methods, and field mapping
- Original mapping conducted in the field shortly after the 1955 designation of the reserve, using a basemap with parcels by tree cover type, stocking, and ground flora communities.
- Digitization performed in 2019 by CEH using ESRI GIS software.
- Coordinate system and projection: British National Grid (OSGB1936), suitable for Great Britain-wide context.

## Data schema and key attributes
- Tree cover: TREE_COV with descriptions (e.g., a, b, c, d, e, g, h, i, j, k, O, X) describing various tree compositions.
- Stocking: STOCKING with values and descriptions (including secondary codes STOCKING2/DESC_ST2).
- Ground vegetation major (GVEG_MAJ) and minor (GVEG_MIN) communities with corresponding descriptions (e.g., I, II, III, IV, IVa, V, VI, VII, VIII and subtypes Ia, Ib, Ic; m1–m7 for minor communities).
- Secondary codes provide additional detail for more than one parcel.
- OTHER field captures uncategorized or supplementary information.
- Spatial attributes: POLY_AREA for area calculations; GLOBALID for unique feature identification.

## Spatial reference and extent
- Coordinate system: British National Grid (OSGB1936).
- Extent: Great Britain; dataset specifically covers the western side of Roudsea Wood NNR.
- SHAPE type: Geometry.

## Data quality, lineage, and governance notes for Data Stewards
- Data quality information is not recorded in this dataset; quality checks performed during entry included range checks against the original map.
- Provenance clearly documented: 1962 field map as source, digitized in 2019; nomenclature aligned to Flora of the British Isles (1962).
- Legacy coding schemes (TREE_COV, STOCKING, GVEG_MAJ/MIN and their subtypes) are extensive and may require crosswalks for interoperability with newer vocabularies.
- Metadata would benefit from explicit documentation of data entry decisions, any discrepancies with the original map, and planned maintenance or updates.

## Usage considerations and maintenance
- Users should be aware of potential limitations due to the absence of recorded quality information beyond initial checks.
- For sharing or cross-dataset integration, provide clear mappings for legacy codes (tree cover, stocking, major/minor vegetation) to current vocabularies.
- If updates or re-digitization are planned, establish a revision log, update the metadata, and maintain GLOBALID consistency for traceability.

## Access, licensing, and maintenance recommendations for data custodians
- Format availability: Shapefile suitable for common GIS workflows; ensure accompanying metadata is complete.
- Recommend maintaining a detailed metadata record including lineage, digitization process, code lists, and any caveats.
- Consider creating a code crosswalk to modern vegetation nomenclatures to improve interoperability with newer datasets.