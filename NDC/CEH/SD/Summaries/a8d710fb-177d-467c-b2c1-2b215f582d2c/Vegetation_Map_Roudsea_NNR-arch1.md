# Vegetation map of Roudsea Wood National Nature Reserve, 1962

## Overview
- Shapefile-based dataset representing vegetation parcels and tree cover types within the western side of Roudsea Wood National Nature Reserve (Cumbria).
- Digitized in 2019 from an original 1962 field map created by R. Donelly and N. English at the Nature Conservancy’s Merlewood Research Station.
- Field mapping conducted after the reserve’s designation in 1955, using parcels defined by tree cover type, stocking rates, and ground flora communities.

## Data content
- ESRI Shapefile with polygons for vegetation areas and tree cover types.
- Coordinate system: British National Grid (OSGB1936), Transverse Mercator projection.
- Extent: Great Britain.
- Attributes include codes and descriptions for tree cover, stocking, major and minor ground vegetation communities, plus an “OTHER” field for miscellaneous notes.
- Global unique identifier (GLOBALID) and polygon area (POLY_AREA in square meters).

## Methods and provenance
- Original mapping by regional Nature Conservancy officers after 1955 designation.
- Digitized in 2019 by the Centre for Ecology & Hydrology (CEH) using ESRI GIS software.
- Species nomenclature follows: Clapham, Tutin & Warburg (1962) Flora of the British Isles.
- Data set quality: No explicit quality record provided; values have been range-checked against the original map.

## Dataset details

- Field descriptions (highlights)
  - TREE_COV: Primary tree cover code (e.g., a = Birch; b = Birch/Scots Pine; c = Birch/Alder; d = Alder; e = Birch/Ash; g = Oak; h = Conifer plantations; i = Yew; j = Lime; k = Willow; O = No tree cover; X = Other/ride/not known).
  - STOCKING: Stocking code describing canopy and stocking status (e.g., 1 = No tree cover; 2 = Scattered trees; 4 = High forest; 5 = Coppice; with variations described in the descriptions).
  - GVEG_MAJ: Ground vegetation major communities codes (I, II, III, IV, V, VI, VII, VIII) with descriptive mappings (e.g., I = Deschampsia flexuosa ± bracken; II = Molinia caerulea ± bracken; V = Phragmites; VI = Vaccinium myrtillus, etc.).
  - GVEG_MIN: Ground vegetation minor communities codes (m1, m2, m3, m5, m6, m7) with descriptions (e.g., m1 = Carex spp., m3 = Sphagnum bog, m5 = Ponds and pools, etc.).
  - DESC_TC, DESC_TC2: Descriptions for primary and secondary tree cover codes.
  - DESC_MAJ, DESC_MAJ2: Descriptions for major ground vegetation communities (primary and secondary).
  - DESC_MIN, DESC_MIN2: Descriptions for minor ground vegetation communities (primary and secondary).
  - POLY_AREA: Area of each polygon (m²).
  - GLOBALID: Unique identifier for each polygon.
  - OTHER: Any additional information not covered by other fields.

## Attributes and classification schemes
- Tree cover and stocking are coded with single and sometimes dual (2) fields to capture primary and secondary conditions (TREE_COV/TREE_COV2, STOCKING/STOCKING2, etc.).
- Ground vegetation is categorized into major (GVEG_MAJ/DESC_MAJ and GVEG_MAJ2/DESC_MAJ2) and minor (GVEG_MIN/DESC_MIN and GVEG_MIN2/DESC_MIN2) communities, reflecting a hierarchical vegetation classification.
- Descriptions provide readable interpretations corresponding to the coded values, enabling interpretation of historical woodland structure and plant communities.

## Quality and limitations
- No quality metadata recorded for the 1962 vegetation map.
- Data quality reflects post-hoc digitization and range checks against the original source; potential limitations include age (1962), partial coverage (western side only), and the absence of formal quality indicators.
- Historical snapshot; may require additional contextual data for contemporary comparisons or scaled analyses.

## Access and usage notes
- Format: Esri Shapefile.
- Digitized version is derived from the 1962 field map, with genealization into GIS attributes for analysis and mapping.
- Users should consider the historical context and potential biases due to the mapping methods of the era when conducting comparative or trend analyses.

## Original authors and institutions
- Original field map created by R. Donelly and N. English (1962) at the Nature Conservancy’s Merlewood Research Station, Grange-over-Sands, Cumbria.
- Digitization and data organization completed by the Centre for Ecology & Hydrology (CEH) in 2019.