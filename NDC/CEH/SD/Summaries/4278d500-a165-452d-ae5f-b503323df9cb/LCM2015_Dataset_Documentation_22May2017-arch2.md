# Dataset documentation

## Overview
- Land Cover Map 2015 (LCM2015) is a parcel-based UK land cover map produced from satellite data into 21 classes based on UK Broad Habitat definitions.
- Built from two-date Landsat-8 (30 m) composites, supplemented with AWIFS (60 m), updating LCM2007 and aligned with a revised spatial framework.
- Output aims to support monitoring of environmental health and policy performance, with multiple data products for varied user needs.

## Data products and formats
- Vector data set (core): 6.7 million GB polygons and 0.9 million NI polygons with attributes including dominant class, pixel counts per class, uncertainty, and communication-friendly identifiers (gid).
- 25 m raster: two-band product per polygon; band 1 = dominant class, band 2 = mean per-polygon probability.
- 1 km raster: percentage cover and dominant class summaries for both 21 target classes and 10 aggregate classes.
- 21 target classes map to Broad Habitats; 10 aggregate classes provide simplified summaries for 1 km.
- Spatial details: GB and NI are provided separately with different projections (GB: British National Grid; NI: TM75 Irish Grid).

## Methodology and differences from LCM2007
- Classification: Random Forest instead of Maximum Likelihood; handles multi-modal training data and simplifies training by removing spectral sub-classes.
- Training data: initial stable set from 2000 and 2007 supplemented with coastal areas and historically challenging classes; ancillary data (e.g., slope, proximity to rivers) are incorporated directly into the input data in 2015.
- Spatial framework: no segmentation-based polygons in LCM2015; per-pixel classification with polygons reflecting real-world boundaries, improving change mapping potential.
- Output data changes: Montane and Rough Grassland classes removed; 25 m raster becomes two-band; probability data recorded differently (vector and 25 m only); no spectral sub-classes; segmentation used in LCM2007 removed, affecting mainly upland GB data; nuanced handling of mixed woodland training.

## Classes and labeling
- LCM2015 includes 21 target classes aligned to Broad Habitats, with some classes further subdivided for specific products (e.g., Urban vs Suburban; Heather vs Heather grassland; Littoral subtypes).
- Each parcel receives a unique gid label in the vector product to support unambiguous communication.
- Metadata-rich polygons include detailed per-polygon class breakdown and mean classification probability.

## Uncertainty and data quality
- Random Forest provides per-pixel probability, stored as mean per-polygon probability (vector) and in band 2 of the 25 m raster.
- Caution: differences between LCM maps arise from real change and classification error; LCM2015 is not designed for change mapping in its current form.

## Data access and citation
- DOIs exist for all LCM2015 products (GB vector, GB 25 m, GB 1 km aggregate and percentage products, NI counterparts).
- 1 km raster data available via CEH Environmental Information Platform; full vector and 25 m products available on request (licence may apply).
- When citing, include the DOI and authors; example format provided in the document.

## Projections and data specifications
- GB vector/raster use British National Grid; NI vector/raster use TM75 Irish Grid.
- Data tables provide metadata such as spatial extents, pixel counts, and coordinate details for 25 m and 1 km products.

## Practical guidance for analysts
- LCM2015 maps land cover, not land use; interpret arable or grassland with care regarding use vs. spectral signature.
- Minimum mappable area is 0.5 ha; parcels smaller than this are dissolved into surrounding areas.
- For change analysis, use caution due to differences in methodology and class definitions across LCM generations.
- Uncertainty information is available to support risk-aware interpretation and downstream analyses.

## Appendices and definitions
- Appendix 1 covers class definitions mapped in LCM2015 with references to JNCC Broad Habitat definitions.
- Appendix 2 provides a mapped summary of Broad Habitat concepts to aid interpretation.
- Appendix 3 and 4 include color mappings and composite image details used in LCM2015 production.

## References and further information
- Key references: Jackson (2000) Broad Habitat classifications; Morton et al. (2011) LCM2007 technical report.
- Additional information and contact: spatialdata@ceh.ac.uk; project pages and data DOIs available via CEH and EIDC portals.