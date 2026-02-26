# Vegetation map of Roudsea Wood National Nature Reserve, 1962

## Overview
- ESRI Shapefile containing polygons that represent vegetation areas within Roudsea Wood National Nature Reserve (Cumbria).
- Digitized by the Centre for Ecology & Hydrology from an original 1962 field map.
- Original map created by R. Donelly and N. English in 1962 at the Nature Conservancy’s Merlewood Research Station.
- Map covers the western side of the reserve (the woodland) and reflects post-designation field mapping (after 1955).
- Digitization completed in 2019 using ESRI GIS software.
- Species nomenclature follows Flora of the British Isles (1962).

## Data provenance and methods
- Field mapping conducted by regional Nature Conservancy officers in the years following the reserve’s designation.
- Parcels were delineated on a basemap according to tree cover type, stocking rates, and ground flora communities.
- The dataset provides a record of vegetation types as of 1962, converted to a digital format in 2019.
- Data entry was range-checked and cross-validated against the original map.
- Explicit quality metadata is not on record.

## Data structure and contents
- Shapefile fields (sampled): 
  - SHAPE (geometry)
  - TREE_COV, TREE_COV2 (tree cover codes and descriptions)
  - STOCKING, STOCKING2 (stocking codes and descriptions)
  - GVEG_MAJ, GVEG_MAJ2 (major ground vegetation communities and descriptions)
  - GVEG_MIN, GVEG_MIN2 (minor ground vegetation communities and descriptions)
  - DESC_TC, DESC_TC2; DESC_ST, DESC_ST2; DESC_MAJ, DESC_MAJ2; DESC_MIN, DESC_MIN2 (descriptions for codes)
  - OTHER (other notes)
  - GLOBALID (unique identifier)
  - POLY_AREA (polygon area in m2)
- Coordinate system and extent:
  - Projection: British National Grid (OSGB1936), Transverse Mercator
  - Extent: Great Britain
- Tree cover codes (examples):
  - 99 = Other; a = Birch; b = Birch/Scots Pine; c = Birch/Alder; d = Alder; e = Birch/Ash; g = Oak; h = Conifer plantations; i = Yew; j = Lime; k = Willow; O = No tree cover; X = Other/ride/not known
- Stocking codes (examples):
  - 1 = No tree cover (except for very young conifers); 2 = Scattered trees; 4 = High forest (Canopy 50–100%); 5 = Coppice; (additional notes provided in descriptions)
- Ground vegetation major communities (examples):
  - I, Ia, Ib, Ic (Deschampsia flexuosa with bracken and associates)
  - II (Molinia caerulea with bracken)
  - III (Brachypodium sylvaticum / Mercurialis perennis with bracken)
  - IV, IVa, IVb (grass-dominated with various taxa)
  - V (Phragmites or Phalaris in some variants)
  - VI, VIa (Vaccinium myrtillus associations)
  - VII, VIII (wet/shoreline or herb/brush associations)
- Ground vegetation minor communities:
  - m1–m7 (Caricetum, Juncus associations, Sphagnum bog, ponds, Iris, Dryopteris, etc.)

## Usage and interpretation
- Enables viewing and analysis of historic vegetation, particularly woodland composition and major/minor ground vegetation communities.
- Allows cross-referencing tree cover, stocking levels, and vegetation types to understand habitat structure in 1962.
- Requires decoding codes using the provided descriptions to interpret actual vegetation types.
- Suitable for integration with other spatial datasets to study historical landscape changes, biodiversity baselines, or conservation planning.

## Quality and limitations
- Quality metadata is not provided in the dataset.
- While values were range-checked and cross-verified against the original map, there is no explicit accuracy assessment published.
- Coverage is specified as the western side of Roudsea Wood; not a complete national dataset.
- Historical map reflects conditions from 1962 and may not represent current vegetation or broader landscape context.

## Spatial details and access
- Data format: ESRI Shapefile containing polygon geometries.
- Spatial reference: British National Grid (OSGB36).
- Extent: Great Britain (as mapped within the Roudsea Wood NNR context).
- Digitization date: 2019, enabling contemporary GIS use and integration with other layers.