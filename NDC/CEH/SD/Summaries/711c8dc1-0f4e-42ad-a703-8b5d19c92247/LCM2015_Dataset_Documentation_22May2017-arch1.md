# Dataset documentation

- LCM2015 is a UK parcel-based land cover map produced from satellite imagery (primarily Landsat-8, 30m; supplemented with AWIFS, 60m) classified into 21 Broad Habitat-based classes.
- Products include a core vector dataset, a 25m raster, and 1km aggregate products, with both Great Britain and Northern Ireland coverage.
- The dataset is designed for diverse user needs but the document warns that LCM2015 should not currently be used for change mapping in its present state due to real change plus classification error and cross-time differences.

## Key purpose and scale

- Maps land cover (not necessarily land use) and is intended to support a wide range of analyses, modelling, and reporting.
- Minimum mappable area is >0.5 ha; parcels smaller than 0.5 ha or very short linear features are dissolved into surrounding landscape.
- Spatial framework is per-pixel based; avoids segmentation to improve change mapping flexibility (notably in uplands).

## Data products and formats

- Vector data set (core product)
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Attributes include: land cover class (text and integer), source image, uncertainty, per-polygon pixel counts per class, dominant class proportion, and a unique geometry identifier (gid).
  - Rich metadata and uncertainty information (per-polygon probability from Random Forest, with standard deviation).
- 25m raster
  - Two-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from classifier.
- 1km raster (aggregate/percentage products)
  - Summary products by class (21-class and 10-aggregate-class schemes) and dominant class per 1km cell.
  - 1km products show percentage cover values (integer; sum may slightly exceed or fall short of 100 due to rounding and coastal edge effects).
- Data access and formats
  - 1km raster data available via CEH Environmental Information Platform (EIP).
  - Full vector and 25m products available under licence on request from CEH.
  - DOIs are provided for citing each product.

## Land Cover classes and labelling

- LCM2015 defines 21 target classes based on the UK Broad Habitats (JNCC Jackson definitions, 2000).
- Some classes are further subdivided for certain products (e.g., Built-up Areas and Gardens into Suburban and Urban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral categories subdivided into Littoral Sediment and Saltmarsh, etc.).
- Each parcel is assigned a unique gid for unambiguous communication and traceability.
- Appendix includes mappings and descriptions of Broad Habitat definitions used to label LCM2015 classes.

## Differences from previous maps (LCM2007)

- Output data differences
  - Montane class removed; areas previously Montane reclassified as Inland Rock or other upland habitats based on spectral data.
  - Rough grassland class removed; Grassland types aligned with JNCC Broad Habitats; no soil data used in LCM2015.
  - 25m raster now 2-band (classification band and per-polygon probability in band 2).
  - Probability information: vector stores mean polygon probability; 25m raster band 2 stores mean probability; 1km products do not include per-pixel probabilities.
  - No spectral sub-classes are used; Random Forest handles multi-modal data, eliminating need for spectral sub-classes.
  - Spatial framework: segmentation-based polygons removed; avoids segmentation inconsistencies across datasets; no segmentation applied to Northern Ireland area where segmentation was not previously used.
  - Mixed woodland labelling updated: pure pixel-level training used for Coniferous and Broadleaf woodlands; polygon labels reflect modal_class; some mixed-wood areas may be assigned to Coniferous Woodland; pix_dist attribute may be consulted for details.
- Methodology differences
  - Classification algorithm switched from Maximum Likelihood to Random Forest.
  - Stable training areas (areas consistently classified the same in 2000 and 2007) used as a base, with manual augmentation for coastal areas and poorly mapped classes.
  - Ancillary data (elevation, soil, etc.) are integrated as inputs rather than applied post-classification, making knowledge-based enhancements objective and integral.

## Methodology in brief

- Core classifier: Random Forest (robust to multi-model training data; better or equal performance to ML).
- Training data: initial stable areas plus additional targeted areas (coastal/intertidal, fen/marsh, semi-natural grasslands, etc.).
- Ancillary data: included in the input set to guide classification; reduces post-classification rule editing.
- Outputs include per-polygon probabilities and uncertainty metrics to support interpretation and quality assessment.

## Data provenance and citation

- Each LCM2015 product has a DOI for formal citation, supporting replicability and usage tracking.
- Vector and raster products provided with full metadata; polygon-level attributes include dominant class, pixel counts, and uncertainty.
- Guidance on citing DOIs and data papers is provided in the document.

## Projections and geographic coverage

- Great Britain: British National Grid (EPSG 27700).
- Northern Ireland: Irish Grid (TM75 Irish Grid, EPSG 29903).
- GB and NI data are provided separately to reflect their different projections.

## Access, licensing, and notes

- LCM2015 1km raster data: available via CEH EIP.
- Full vector and 25m raster products: available on licence on request from CEH.
- Licence fees may apply for some users and applications.
- The dataset is a stable, archived product with DOIs; use the DOIs in publications.
- The document notes that LCM2015 aims to be a repeatable method suitable for mapping change in future releases, but current use for direct change detection should be treated with caution.

## Appendices and additional details

- Appendix 1 and Appendix 2: clarifications on Broad Habitat class definitions and their per-class interpretations.
- Appendix 3: standard LCM2015 colour mapping rules for visualisation.
- Appendix 4: composite image references used in LCM2015 production.

## Summary takeaway for analysts

- LCM2015 provides a comprehensive, multi-resolution land cover dataset for the UK, underpinned by a Random Forest classifier and integrated ancillary data, with 21 Broad Habitat-based classes and detailed metadata and uncertainty information.
- It introduces methodological and data-structure changes that improve change mapping potential but require careful handling when comparing with earlier maps (LCM2007/LCM2000).
- Users should rely on the vector core for detailed per-polygon information, or on the 25m raster for a lighter-weight representation; 1km products are suitable for large-scale modelling and integration with other national datasets.
- Proper data citation via DOIs is encouraged, and licensing needs to be checked for each product.