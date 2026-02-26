# Land Cover Map 2015 (LCM2015)

- Land Cover Map 2015 (LCM2015) is a parcel-based UK land cover map, classified from satellite data into 21 Broad Habitat classes (based on JNCC/Biodiversity Action Plan definitions). It updates previous LCMs (notably LCM2007) and is built from two-date Landsat-8 composites (30 m; supplemented with AWIFS 60 m as needed). It maps land cover (not necessarily land use) and provides multiple data products (vector, 25 m raster, and 1 km aggregates) to support diverse monitoring needs.

## Overview of Data Products and Structure

- Core data products
  - Vector dataset: ~6.7 million GB polygons (Great Britain) and ~0.9 million polygons (Northern Ireland) with rich attributes per parcel.
  - 25 m raster: two-band product; band 1 = dominant LCM2015 class, band 2 = mean per-polygon probability from Random Forest classifier.
  - 1 km raster products: dominant class and percentage cover for both 21 LCM2015 classes and 10 aggregate classes.
- Attributes and metadata
  - Vector: gid (unique parcel ID), dominant class (Modal_class), pixel breakdown per class (pix_dist), uncertainty (unc, unc_stdev), number of pixels (npix), proportion of dominant class (Modal_prop), and composite source indicator.
  - 25 m and 1 km products include per-polygon probability and aggregate/class mapping details.
  - Each product has DOIs for citation; GB and NI products have separate DOIs.
- Spatial specifics
  - Projections: Great Britain in British National Grid; Northern Ireland in TM75 Irish Grid.
  - Minimum mappable unit: polygons < 0.5 ha and linear features < 20 m dissolved into surrounding area.
  - Data access: 1 km rasters via CEH Environmental Information Platform; full vector and 25 m rasters available on request (licensing may apply).

## Classification Methodology and Data Production

- Classification approach
  - Random Forest classifier (RF) used for per-pixel classification, enabling handling of multi-modal training data and removal of spectral sub-classes.
  - Stable training areas from historical LCM datasets (LCM2000/LCM2007) used as a starting point and expanded to coastal zones and difficult classes (Fen, Marsh, Swamp; etc.).
  - Ancillary data (e.g., altitude, soil, slope, distance to rivers) are integrated as inputs rather than post-classification rules, making enhancements more objective.
- Training and data preparation
  - Training areas are built from legacy data and expanded with coastal and poorly mapped classes; no per-pixel spectral sub-classes are used.
  - Mixed woodland training uses pure stands for training; polygon labels are derived from modal_class after per-pixel classification and summarised to polygons.
  - No segmentation-based spatial framework is used in LCM2015; per-pixel classifications are mapped to polygons.
- Products and mapping approach
  - 21 target LCM2015 classes aligned with UK Broad Habitats; some classes are further subdivided for certain products (e.g., Built-up Areas subdivided into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - 1 km products provide aggregate and percentage-cover summaries to support national-scale analyses.
- Outputs and labeling
  - Each parcel receives a unique gid label; retaining gid is recommended for unambiguous communication.

## Key Differences from LCM2007 (Methodology and Output Changes)

- Output data changes
  - Montane class removed (reclassified as Inland Rock or upland habitats; use LCM2007 for Montane distribution).
  - Rough grassland class removed; grassland types re-aligned with Broad Habitats without soil data input.
  - 25 m raster now two-band (classification band + probability band).
  - Probability data presentation simplified (vector shows mean per-polygon probability; 25 m raster band 2 contains the same probability information; 1 km products do not include per-pixel probabilities).
  - No spectral sub-classes used; Random Forest obviates the need for sub-class grouping.
  - Spatial framework no longer uses segmentation; instead, per-pixel classifications are mapped directly to polygons, reducing segmentation-related errors.
  - Mixed woodland labeling adjusted: training uses pure stands with modal_class; some mixed stands may map to Coniferous or Broadleaved woodland depending on dominant signal; guidance is available in pix_dist for detailed exploration.
- Methodology changes
  - Shift from Maximum Likelihood Classifier (LCM2007) to Random Forest (LCM2015).
  - Stable training areas augmented with coastal and problematic classes; ancillary data are part of the input data for the RF classifier.
  - Ancillary data and knowledge-based enhancements become integral inputs rather than post-classification corrections.

## Uncertainty, Metadata, and Data Governance

- Uncertainty and quality
  - RF provides per-pixel probability estimates; these are captured at polygon level (mean probability) and in the 25 m raster as a second band.
  - Rich metadata accompany polygons, including counts of pixels per class and a breakdown of class proportions within each polygon.
- Metadata richness
  - LCM2015 vector product includes extensive metadata per polygon (dominant class, pixel distributions, probability metrics, and processing details).
- Data governance and reuse
  - DOIs assigned for citation to support repeatability and traceability.
  - The documentation emphasizes data provenance, processing history, and the need to cite DOIs when using data in publications.
  - Guidelines highlight the importance of sharing underlying data in a responsible manner and maintaining data provenance through gid and composite information.

## Accessibility, Usage, and Practical Considerations

- Access and licensing
  - 1 km raster data is openly accessible via CEH EIP.
  - Full vector and 25 m raster products are available on request under licence; licensing fees may apply.
- Important usage notes
  - The LCM2015 dataset is a stable, archived product with DOIs; it should be cited properly in publications.
  - The document warns that LCM2015 should not be used for change mapping in its current state; differences across LCM products arise from methodological changes, data sources, and spatial frameworks.
  - Users should consult appendices for mapping of LCM2015 classes to Broad Habitats and for color mappings, as well as for composite information and how to interpret probability data.
- Data structure and interpretation
  - The vector dataset provides detailed polygon-level attributes; the 25 m raster provides a parallel raster representation with probability data; 1 km products enable national-scale modeling by aggregating 25 m results.
  - A detailed crosswalk table links LCM2015 classes to Broad Habitat definitions and to aggregated/target class mappings for raster outputs.

## Appendices and Additional References

- Class definitions and Broad Habitat mappings (Appendix 1 and Appendix 2)
  - Provides in-depth explanations of how LCM2015 classes correspond to JNCC Broad Habitat definitions (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Grassland types, various coastal and rock/shore habitats, urban categories, etc.).
- Color mapping (Appendix 3)
  - Standard color values for each LCM2015 class to support visualization.
- Composite images and data provenance (Appendix 4)
  - Details about composite images used in the classification process, including dates and sensor information.
- Citations and DOIs
  - DOIs are provided for GB and NI vector, 25 m raster, and 1 km products to aid precise citation in publications.

- Contact and further information
  - Access information and Q&A: CEH Spatial Data team; contact details provided in the document.
  - The LCM2015 data paper is in preparation and will include additional information.