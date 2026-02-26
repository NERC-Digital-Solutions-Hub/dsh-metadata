# Dataset documentation

- The Land Cover Map 2015 (LCM2015) dataset is documented here. It provides UK-wide land cover maps to support monitoring, policy scrutiny, and decision-making in environmental health and land cover/change analysis.
- LCM2015 uses satellite imagery (Landsat-8 30 m, with AWIFS 60 m as needed) to classify into 21 Broad Habitat-based land cover classes, aligned with UK Biodiversity Action Plan definitions.
- Outputs are designed for a range of users and applications, with a focus on per-polygon (vector) data, complemented by raster products at 25 m and 1 km resolutions.

- Data products and formats
  - Core vector data set: polygons with rich attribute information per parcel.
  - 25 m raster: two-band product (band 1 = dominant class per polygon; band 2 = mean per-polygon probability).
  - 1 km raster: aggregate products including dominant class, percentage cover per class, and dominant/percentage for aggregate classes.
  - Separate data sets for Great Britain and Northern Ireland; projections in British National Grid (GB) and TM75 Irish Grid (NI).
  - Minimum mappable unit: parcels >0.5 ha; small features dissolved into surrounding landscape.
  - 21 target classes plus 10 aggregate classes for 1 km products.

- Data access and citation
  - 1 km raster products available via CEH Environmental Information Platform.
  - Full vector and 25 m raster products licensed on request from CEH.
  - Each LCM2015 product has a DOI for proper citation; DOIs provided for GB and NI vector, 25 m raster, 1 km products (both GB and NI).
  - Data should be cited with author names, date, and DOI in publications.

- Key methodological features
  - New classification algorithm: Random Forest (replaces previous Maximum Likelihood).
  - Ancillary data incorporated into the input data (not post-classification) to inform the classifier.
  - Stable training areas used to bootstrap the initial training set, expanded with coastal areas and under-mapped classes.
  - No spectral sub-classes used; multi-modal training handled by Random Forest.
  - Spatial framework: no segmentation in LCM2015; polygons are per-pixel classifications without prior segmentation, improving consistency for change mapping.
  - Classification outputs are per-pixel with polygon-level aggregation and uncertainty information.

- Differences from earlier LCM versions
  - Montane class removed; Inland Rock and other upland habitats adjust mappings.
  - Rough grassland class removed; grassland types align with JNCC Broad Habitats without soil data inputs.
  - 25 m raster now two-band (classification and mean probability).
  - Probability data simplified: polygon-mean probability stored in vector; band 2 of 25 m raster; no probability data for 1 km products.
  - No spectral sub-classes; all classification handled by Random Forest.
  - Spatial segmentation removed from the framework; upland segmentation adjustments fixed errors in the previous framework.
  - Mixed woodland training now uses pure stands for training and pixel-level classification with modal class assigned to polygons.

- Product details and metadata
  - Vector product contains per-polygon attributes, including gid (unique parcel ID), dominant class, pixel counts per class, uncertainty measures, and modal_class (target class).
  - 9 attributes in vector product; 23 numbers in Pix_dist listing per-class pixel counts, npix, and modal_class; uncertainty expressed as a per-polygon probability.
  - Rich metadata accompanying polygons; per-polygon mean probabilities available; composite image information tracked to indicate data sources.
  - Colour mapping and class definitions provided in appendices; 21 target classes and their Broad Habitat mappings are detailed.

- Class structure and mappings
  - 21 LCM2015 target classes mapped to UK Broad Habitats; several Broad Habitats are further subdivided for certain products (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - Aggregated classes (10) used for 1 km products to support broad-scale analyses and modelling.

- Data quality, limitations, and cautions
  - LCM2015 is a stable, archived dataset; differences between LCM2007 and LCM2015 require careful handling when comparing across versions.
  - Changes in methodology and class definitions mean that direct change mapping should be done with caution; differences reflect methodological evolution as well as real-world changes.
  - Differences between the UK and Northern Ireland data (projection, coordinate systems) require attention during cross-border analyses.
  - Some habitat classes (e.g., Fen, Marsh and Swamp) may be underestimated due to spectral and scale limitations; users should consult guidance in Appendix 1/2 for interpretation nuances.

- Data governance and usage notes
  - Data provenance, processing details, and metadata are preserved to facilitate transparency, repeatability, and governance.
  - Gid attribute enables unambiguous communication of parcel-level data across analyses and applications.
  - Users are advised to cite the DOIs when using LCM2015 data in outputs, reports, or publications.

- Practical implications for monitoring frameworks
  - Provides a robust, well-documented dataset suitable for policy scrutiny, impact assessment, and scenario analysis across environmental health and land-use planning.
  - Rich uncertainty metrics allow integration into monitoring frameworks that require confidence estimates.
  - The combination of vector and raster products enables flexible analyses, from per-polygon expert reviews to wide-area modelling with 1 km aggregates.
  - The dataset’s governance framework (metadata, DOIs, licensing) supports transparent data management and data-sharing initiatives.