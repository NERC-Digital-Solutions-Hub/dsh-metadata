# Dataset documentation

- LCM2015 provides UK-wide land cover maps in multiple formats to support diverse user needs, including a vector per-polygon dataset, a 25m raster, and 1km aggregate products. It maps 21 Broad Habitat classes and is designed as a stable, archived resource with DOIs for citation. Note: not recommended for current change-mapping without caution.

## Key purpose and scope
- Parcel-based land cover map for the UK, classifying satellite data into 21 land cover classes based on UK Biodiversity Action Plan Broad Habitats.
- Uses two-date Landsat-8 composites (30m) with AWIFS data as needed.
- Distinguished from previous LCM versions by aiming to support change mapping better and enabling repeatable production methods.
- Maps land cover (not always directly equating to land use); provides rich metadata and uncertainty information.

## Data products and structure
- Vector data set
  - About 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon has attributes including dominant land cover (Modal_class), distribution of class pixels (Pix_dist), uncertainty (unc, unc_stdev), number of pixels (npix), and a unique geometry identifier (gid).
  - Contains 21 target LCM2015 classes with detailed metadata per polygon.
- Raster data sets
  - 25m raster: 2-band product (band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from Random Forest).
  - 1km raster: aggregate products including dominant class and percentage cover for both 21 classes and 10 aggregate classes.
  - Data zones split GB and NI with appropriate projections.
- Spatial resolution and coverage
  - Minimum mapping unit of 0.5 ha; polygons smaller than 0.5 ha or very short lines are dissolved into surroundings.
  - GB uses British National Grid; NI uses TM75 Irish Grid.
- Labelling and color mapping
  - Unique labeling via gid; color assignments follow a standard mapping (Appendix 3).

## Classification methodology and inputs
- Core classifier: Random Forest (robust to multi-modal training data).
- Training data: built from a stable core (areas classified the same in 2000 and 2007) plus manual augmentation for coastal areas and challenging classes.
- Ancillary data: treated as input data alongside satellite imagery; enables objective knowledge-based enhancements within the classifier.
- No segmentation is used in the LCM2015 spatial framework to avoid segmentation-induced mismatches.
- Outputs include per-polygon dominant class with accompanying probability metrics; sub-class spectral subdivisions used in earlier versions are not retained.

## Differences from LCM2007 and methodological notes
- Output data changes
  - Montane class removed; inland rock/ upland habitats reformulated to align with spectral data.
  - Rough grassland class removed; grassland types align with JNCC Broad Habitat types.
  - 25m raster becomes a two-band image; 1km products exclude probability data.
  - No spectral sub-classes in 21-class vector; 1km products reflect aggregated classes.
  - Spatial framework stripped of per-image segmentation, reducing segmentation-related errors.
  - Mixed woodland training uses pure stands for labeling, with modal_class applied to polygons.
- Methodology shifts
  - Transition from Maximum Likelihood to Random Forest classifier.
  - Stable training areas augmented with coastal and poorly mapped classes.
  - Ancillary data integrated as inputs rather than post-classification adjustments.
- Data scope and map meaning
  - LCM2015 maps land cover (spectral/signature-based), not strictly land use.
  - Includes a fixed, documented minimum mapping unit and explicit cautions about change mapping suitability.

## Classes and labeling
- 21 target LCM2015 classes anchored to UK Broad Habitats (with some subdivisions for higher detail):
  - Examples include Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral/Calcareous/Acid Grasslands, Bracken, Dwarf Shrub Heath, Fen/Marsh/Swamp, Bog, Standing Open Water/Canals, Rivers and Streams, Montane, Inland Rock, Built-Up Areas and Gardens (split into Urban and Suburban), Supra-littoral and Littoral coastal classes, Saltmarsh, and various Littoral/Supralittoral and Sediment categories.
- Some broad habitats are subdivided for finer distinctions (e.g., Urban vs Suburban; Heather vs Heather grassland).
- Appendix 1–3 provide detailed definitions, mapping rules, and standard color mappings for these classes.

## Data quality, uncertainty, and limitations
- Uncertainty information provided for vector polygons as mean per-polygon probability from Random Forest; included in the unc attribute (0–255 scale) and unc_stdev.
- Probability data is available for vector and 25m raster products; not available for 1km aggregate products.
- Spatial framework and methodological changes improve consistency for change mapping but may affect backward comparability with LCM2007 data, particularly in upland areas.
- Differences between LCM products (e.g., montane removal, grassland reclassification) may affect interpretation and require re-validation when comparing with older datasets.
- The documentation cautions that differences between LCM products are due to both real changes and classification errors, amplified by changes in thematic and spatial frameworks.

## Data access, licensing, and citation
- Access
  - 1km raster data sets available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25m products available on request under license from CEH.
  - Online application process and contact: spatialdata@ceh.ac.uk.
- Projections and coordinates
  - GB data: British National Grid (OSGB 27700); NI data: Irish National Grid (TM75 Irish Grid).
- Citations and DOIs
  - Each LCM2015 product has a DOI for formal citation (GB vector, GB 25m, GB 1km percent, GB 1km dominant, GB 1km aggregate, NI vector, NI 25m, NI 1km percent, NI 1km dominant, NI 1km aggregate).
  - DOIs are provided to ensure reproducibility and traceability in publications.
- Metadata and data provenance
  - Rich metadata accompany the vector product, including dominant class, pixel counts per class, and mean polygon probability.
  - Gid attribute retained for unambiguous cross-user communication and data integration.

## Practical notes for Data Stewards
- Use gid to maintain consistent communication about specific parcels across systems.
- When publishing, cite the appropriate LCM2015 DOI and include authors and date in references.
- Consider the 0.5 ha minimum mapping unit when planning analyses or integrations that rely on small features.
- For change mapping purposes, verify current suitability and be mindful of known differences from LCM2007 and the potential for classification-based artifacts.
- Leverage the multiple products (vector, 25m, 1km aggregates) to balance detail, metadata richness, and processing efficiency depending on user needs.