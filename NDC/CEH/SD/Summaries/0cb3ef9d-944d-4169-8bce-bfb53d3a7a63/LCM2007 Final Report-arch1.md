# Final Report for LCM2007 - the new UK land cover map

- The document evaluates LCM2007, the first continuous parcel-based UK land cover map linked to Broad Habitats, and compares it with Countryside Survey (CS) field data from 2007.
- It highlights agreement patterns, sources of disagreement, and implications for monitoring, policy, and analysis.

## Key comparative findings with Countryside Survey (CS) 2007

- Very similar area estimates (within CS 95% bounds) for:
  - Coniferous Woodland
  - Freshwater
  - Built-up Areas and Gardens
  - Calcareous Grassland
- Similar area estimates (UK scale within CS 95% bounds) for:
  - Broadleaved Woodland
  - Acid Grassland
  - Inland Rock
- Dissimilar area estimates (beyond CS 95% bounds) for:
  - Arable and Horticulture
  - Improved Grassland
  - Neutral Grassland
  - Dwarf Shrub Heath
  - Bog
  - Montane Habitats
  - Coastal habitats
- Notes on particular patterns:
  - CS tends to differ in how “Arable and Horticulture” is defined; LCM2007 may include temporary grass and uncropped land within this class.
  - Calcareous Grassland alignment is strong in some contexts because LCM2007 mapped large areas (e.g., Salisbury Plain, South Downs) that CS also identifies.
  - Montane and coastal habitats show poorer correspondence due to CS’s limited upland/coastal sampling and the different spatial structures of the two products.
  - Spectral mixing and boundary features affect grassland and arable classifications; boundary/linear features are treated differently between products (CS maps field boundaries; LCM2007 often integrates boundaries into adjacent polygons).

## 4.3.3 Discussion (Implications of Agreement and Disagreement)

- CS area estimates are scaled-up national estimates based on ITE Land Classes; the method affects comparability.
- Key drivers of differences between CS and LCM2007:
  - Temporal range and multi-year imagery influence spectral signatures (e.g., temporary grass vs arable, spectral variability of arable crops).
  - Spectral confusion and classification of grassland classes (Improved, Neutral, Calcareous, Acid) complicates direct mapping.
  - Boundary and linear features: CS includes field boundaries that often fall below LCMMMU; LCM2007 tends to disperse such features differently across habitats.
  - Patch size: many Fen, Marsh and Swamp polygons are small or below LCM2007’s MMU, affecting detection.
  - Grassland mosaic and transitions (e.g., Dwarf Shrub Heath vs Acid Grassland) introduce ambiguities in attribution.
- Fen and swamp areas exhibit especially large discrepancies due to mosaic composition and small patch sizes; a notable portion of CS-recorded Fen areas may be mapped as Rough Grassland or Acid Grassland by LCM2007.

## 4.4 UK Land Cover (land cover distribution)

- More than 50% of the UK is in intensive land use (Arable and Horticulture plus Improved Grassland) or Built-up Areas and Gardens.
- Semi-natural areas dominate the remainder, with woodlands (~12% UK; split between Broadleaved and Coniferous) and 30% semi-natural other categories (coastal, semi-natural grassland, mountain/heath/bog).
- Spatial variation across the four UK countries:
  - England: highest intensive use (~76%).
  - Scotland: largest share of Coniferous Woodland; Scotland has the most semi-natural and montane habitats.
  - Northern Ireland and Wales: substantial intensive land use but differing distributions.
- Comparison with LCM2000 shows changes in percentages for Arable, Semi-natural Grassland, and Coniferous Woodland; questions remain about the influence of the spatial framework changes on these shifts.

## 4.5 Summary and discussion (overall interpretation)

- LCM2007 achieves substantial agreement with CS for several broad habitats, but grassland and upland/coastal classes show notable differences.
- Grassland categories are particularly challenging due to one-to-many relationships with Broad Habitats; Broad Habitat Association (BHA) rules were developed to better interpret correspondences.
- LCM2007 shows strong correspondence with CS 2007 for the Arable and Horticulture extent in CS data but tends to map a larger arable area overall, partly due to how boundaries and temporally dynamic land uses are captured.
- Fen, Marsh and Swamp estimates vary dramatically between CS and LCM2007, reflecting the mosaic nature of fen and the difficulty of spectral discrimination; a potential path forward is to develop additional KBEs to better allocate fen-related areas.
- Practical implication: use aggregated grassland classes or BHAs to improve comparability; recognize that LCM2007 provides a coastal-to-coast, policy-relevant UK-wide basemap with quantified uncertainties by habitat type.

## 5.1 Example areas

- The report presents example areas illustrating LCM2007 performance across habitats (upland, calcareous grassland, urban areas, arable/fen mosaics), demonstrating how the vector and raster representations capture landscape diversity.

## 5.2 Vector and raster products

- LCM2007 provides both vector (parcel-based polygons with extensive metadata) and raster products (25 m and 1 km resolutions).
- Vector products include attributes such as area, source images, Broad Habitat (BH), and processing history (Construct, ProbList, KBE history).
- 25 m raster offers 23 LCM2007 classes; 1 km rasters provide percent cover or dominant class per pixel.
- Access:
  - 1 km raster data via the CEH Information Gateway.
  - Full vector and 25 m products available on request from CEH (licences may apply).

## 6 Discussion (broader context and future directions)

- LCM2007 delivers the first continuous parcel-based UK land cover map with robust cross-UK spatial framework suitable for change detection and policy support.
- Change mapping across LCM1990, LCM2000, and LCM2007 is complex due to differences in spatial structure and class schemes; robust change detection requires approaches that integrate a common spatial framework and possibly aggregation of classes.
- LCM2007 complements the Countryside Survey by providing coast-to-coast coverage and enabling habitat network/connectivity analyses, while CS provides in-situ habitat quality and finer-scale changes.
- European links: LCM2007 supports national-to-European comparisons (e.g., Corine); data are designed for integration with other environmental data sources (soil, climate, hydrology, etc.).
- Access and governance: LCM2007 data support via CEH gateways; ongoing data sharing and licensing considerations.

## Appendix highlights (relevant for analysts)

- Broad Habitat Association (BHA): rules linking LCM2007 classes to CS correspondences, acknowledging complexities in bogs, dwarf shrub heath, montane habitats, fen, and grassland mosaics.
- Bespoke validation: LCM2007 provides parcel-level metadata (KBE history, probability lists) to enable users to validate classifications locally against high-resolution imagery; a Bayesian-like approach is proposed for “fit for purpose” assessment.
- Data structure and metadata: LCM2007 offers detailed metadata on processing steps, class history, and probabilities to support auditability and reproducibility.

- Overall takeaway for analysts: LCM2007 is a significant advancement in UK land cover mapping with extensive metadata and flexible classification enhancements, but users should account for differences with field surveys, especially for grassland, fen, and upland/coastal habitats, and consider aggregated habitat schemes when comparing with CS or other datasets.