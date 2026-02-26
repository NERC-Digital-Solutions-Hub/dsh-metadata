# Land Cover Map 2015 (LCM2015) dataset documentation

- UK parcel-based land cover map created by classifying satellite data into 21 Broad Habitat classes, based on UK Biodiversity Action Plan definitions.
- Primary data sources: Landsat-8 (30 m) two-date composites, supplemented by AWIFS (60 m) as needed.
- Builds on LCM2007 with a focus on change mapping and reproducible production; no segmentation in the final spatial framework; minimum mapping unit of 0.5 ha.
- Outputs include a core vector dataset, a 25 m raster, and 1 km aggregated products; per-polygon uncertainty and class composition information are provided.

## Data products

- Vector data set (core product)
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Attributes include: dominant land cover (BHAB), per-polygon pixel breakdown (Pix_dist), uncertainty metrics (unc, unc_stdev), polygon pixel count (npix), modal_class (final recommended class), modal_prop, and composite image source (Composite).
- 25 m raster
  - Two-band raster: band 1 = dominant LCM2015 class per polygon; band 2 = mean per-polygon probability from Random Forest.
- 1 km raster products
  - Dominant class per 1 km cell (21-class and 10-aggregate-class options).
  - Percentage cover per 1 km cell for each class (21 bands for GB, 10 bands for aggregates).
  - GB and NI datasets provided separately with their respective projections.
- Metadata and labeling
  - Each parcel has a unique geometryId (gid).
  - Rich metadata for each polygon; uncertainty represented as mean per-polygon probability (0–255 scale in vector; band 2 of 25 m raster).

## Classification approach and training

- Classifier: Random Forest (replacing the previous Maximum Likelihood approach).
- Input data: satellite imagery plus ancillary data integrated into the classification process (no post-classification KBEs for LCM2015; ancillary data used as required by the classifier).
- Training data: stable training areas defined from areas classified the same in 2000 and 2007, supplemented with coastal areas and classes historically challenging to map.
- No spectral sub-classes are used; training data is prepared to support multi-modal outputs without sub-class grouping.
- Spatial framework: per-pixel classification without segmentation of polygons; aims to improve change mapping reliability and production speed.

## Differences from LCM2007 (output and methodology)

- Output data changes
  - Montane class removed; upland areas reclassified using spectral data (now under Inland Rock or other upland habitats).
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitats; no soil data used in LCM2015.
  - 25 m raster is two-band; 1 km products exclude per-pixel probability data.
  - No spectral sub-classes; sub-classes deemed redundant for most users.
  - Spatial segmentation removed in LCM2015; no segmentation-based polygons; segmentation issues in uplands addressed by removal.
  - Mixed woodland training uses pure stands at pixel level; polygon labels derived from modal_class.
- Methodology changes
  - Random Forest classifier adopted.
  - Stable training areas built from legacy data plus coastal and poorly mapped classes.
  - Ancillary datasets are integrated as inputs rather than applied post-classification.
- Additional notes
  - LCM2015 focuses on land cover rather than land use.
  - A minimum mappable area of >0.5 ha; smaller parcels dissolved into surrounding landscape.

## Class structure and mapping notes

- LCM2015 maps 21 target classes, based on UK Broad Habitats; some classes subdivided for spectral reasons (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather Grassland; Littoral Sediment into Littoral Sediment and Saltmarsh).
- Aggregates: 10 aggregated classes used for certain 1 km products; correspondence to Broad Habitats documented in tables/appendices.
- Special labeling and mappings
  - gid provides a stable identifier for communication and data integration.
  - Vector attributes include breakdown of pixel counts by class within each polygon, enabling detailed uncertainty assessment.
- Size and scope
  - GB vs NI datasets provided separately; GB uses British National Grid (EPSG 27700); NI uses TM75 Irish Grid (EPSG 29903).

## Data access, usage, and citation

- Access
  - 1 km raster data: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m raster products: available under licence on request from CEH.
- Licensing and fees
  - Some users/applications may incur licence fees.
- Citation and DOIs
  - Each LCM2015 product has a Digital Object Identifier (DOI); recommended format for publications includes authors, date, and DOI.
  - DOIs cover vector (GB and NI), 25 m raster, and 1 km percentage/dominant/aggregate products (separate DOIs for GB and NI).
- Projections and metadata
  - GB vector/raster in British National Grid; NI in Irish Grid.
  - Rich metadata and uncertainty information are provided with the data.

## Practical guidance for analysts

- Use the vector product when you need per-polygon metadata, pixel composition within polygons, and explicit uncertainty; prefer the 25 m raster when polygon-level metadata is not needed or when simpler data structures are required.
- For change mapping or time-series analyses, be aware that LCM2015 removed segmentation complexity and montane/rough grassland classes; ensure compatibility if comparing with LCM2007 or earlier.
- When aggregating to 1 km, use the 1 km dominant and percentage cover products, noting that total percentages may not sum exactly to 100% due to rounding and coastal/ocean boundary considerations.
- Consult Appendix-based class definitions and color mappings to interpret Broad Habitat categories consistently.
- Ensure proper data citation by using the dataset DOIs in any publications or analyses.

Appendix references (for further detail)
- Appendix 1 & 2: Broad Habitat definitions and mapping caveats.
- Appendix 3: Standard colour mapping recipe for LCM2015 classes.
- Appendix 4: Composite images used in LCM2015 production.