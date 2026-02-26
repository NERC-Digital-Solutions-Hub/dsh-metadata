# Vegetation map of Roudsea Wood National Nature Reserve, 1962

## Overview
- ESRI Shapefile containing polygons that represent vegetation areas within Roudsea Wood National Nature Reserve (Cumbria), digitized from the original 1962 field map.  
- Original map created by R. Donelly and N. English (1962) at the Nature Conservancy’s Merlewood Research Station; vegetation mapped in the field after designation as a National Nature Reserve in 1955.  
- Digitisation performed in 2019 by the Centre for Ecology & Hydrology (CEH) using ESRI GIS software. Species nomenclature follows Flora of the British Isles (1962).

## Data lineage and methods
- Field mapping conducted by regional Nature Conservancy officers; parcels categorized by tree cover type, stocking rates, and ground flora communities.  
- The Western side of the reserve is covered by this dataset.  
- Quality control: values were range checked and cross-checked against the original map; no formal quality metadata recorded.

## Technical details
- Format: ESRI Shapefile (polygon geometry)  
- Coordinate system: British National Grid (OSGB1936), Transverse Mercator projection  
- Extent: Great Britain  
- Data fields (primary and secondary components):  
  - TREE_COV / DESC_TC: tree cover code and description  
  - TREE_COV2 / DESC_TC2: secondary tree cover code and description  
  - STOCKING / DESC_ST: stocking code and description  
  - STOCKING2 / DESC_ST2: secondary stocking code and description  
  - GVEG_MAJ / DESC_MAJ: ground vegetation major communities - code and description  
  - GVEG_MAJ2 / DESC_MAJ2: secondary major communities - code and description  
  - GVEG_MIN / DESC_MIN: ground vegetation minor communities - code and description  
  - GVEG_MIN2 / DESC_MIN2: secondary minor communities - code and description  
  - OTHER: any other information not covered by above  
  - GLOBALID: unique identifier  
  - POLY_AREA: polygon area in square meters

## Attribute schemas and code lists
- Tree cover codes (primary and secondary): codes include a, b, c, d, e, g, h, i, j, k, O (no tree cover), X (Other/ride/not known), and 99 = Other (with descriptive text provided).  
- Stocking codes: 1, 2, 4, 5 with corresponding descriptions; secondary stocking codes and descriptions accompany the primary ones.  
- Ground vegetation – major communities: I, Ia, Ib, Ic, II, III, IV, IVa, IVb, V, Vb, VI, VIa, VII, VIII with detailed descriptions.  
- Ground vegetation – minor communities: m1, m2, m3, m5, m6, m7 with corresponding descriptions.  
- Note: there are primary (no suffix) and secondary (suffix 2) field pairs to capture two-way classification per parcel.  

## Scope and usage
- Purpose: to support map-based data visualisations and spatial analyses of historical vegetation within Roudsea Wood NNR.  
- Suitable for GIS workflows, integration with other spatial datasets, and historical vegetation studies.  

## Access and provenance
- Document Version: 1 (5/6/2019)  
- Provenance: CEH digitisation of the 1962 field map; original field map by Donelly & English (1962).  
- Coverage: western side of Roudsea Wood NNR; projection uses OSGB36 British National Grid.