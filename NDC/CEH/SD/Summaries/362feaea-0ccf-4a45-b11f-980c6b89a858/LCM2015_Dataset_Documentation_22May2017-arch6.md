# Dataset documentation

- A comprehensive dataset release for Land Cover Map 2015 (LCM2015) by CEH/NERC.
- UK-wide parcel-based land cover classification into 21 Broad Habitat classes, derived primarily from Landsat-8 (30 m) with AWIFS supplements.
- Outputs include a core vector product, a 25 m raster, and 1 km percentage/dominant products; designed to support a wide range of users from policy to modelling.

## What LCM2015 is and aims

- Parcel-based land cover map for the UK, using 21 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Produced from two-date composite satellite imagery; supports change mapping and cross-dataset compatibility via real-world polygon boundaries.
- Clear distinction between land cover (what is on the ground) and land use (not always directly inferred).

## Data products and formats

- Core products:
  - Vector data set (polygons with rich attributes).
  - 25 m raster (classification band plus probability band).
  - 1 km raster products (percentage cover and dominant class for both 21-target and 10-aggregate classes).
- Attributes and uncertainty:
  - Vector includes gid (unique parcel ID), dominant class, Pix_dist (pixel-level breakdown for all classes), uncertainty (mean RF probability), npix, modal_class, modal_prop, and Composite (source composite image).
  - 25 m raster band 2 contains mean per-polygon probability; band 1 is the dominant class.
  - 1 km products provide percentage cover (integer values) and the dominant/aggregate classes.
- Spatial details:
  - GB and NI have separate datasets and coordinate systems (British National Grid for GB; Irish Grid for NI).
  - Minimum mappable area: >0.5 ha; parcels smaller than 0.5 ha and linear features < 20 m dissolved into surroundings.
- Class structure:
  - 21 target classes, with some higher-level aggregations used for 1 km rasters (aggregate classes).
  - Some classes subdivided in the mapping (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).

## Data access and licensing

- Access:
  - 1 km raster data available via the CEH Environmental Information Platform.
  - Full vector product and 25 m raster available on request under licence from CEH.
- Licensing considerations:
  - Licence fees may apply for some users/applications.
  - Full DOIs are provided for citing each product (vector, 25 m, 1 km for GB and NI).

## Metadata, labeling, and uncertainty

- Rich metadata:
  - Each polygon carries dominant class, pixel counts per class, and mean probabilities.
  - gid enables unambiguous communication and traceability of parcels.
- Uncertainty:
  - Random Forest classifier provides per-pixel probability estimates; reported as mean polygon probability (uncertainty) in vector and as band 2 in the 25 m raster.
- Documentation and reproducibility:
  - DOIs accompany all products to support transparent citation and repeatability.
  - Appendix sections provide class definitions and colour mappings to assist interpretation.

## Key methodological differences from earlier maps (LCM2007)

- Classification algorithm:
  - LCM2015 uses Random Forest instead of Maximum Likelihood, improving handling of multi-modal and complex classes.
- Training data approach:
  - Transition from manually defined stable training areas to data-driven training with additional coastal and hard-to-map classes; training areas built on historical consistency plus targeted additions.
- Ancillary data integration:
  - For LCM2015, ancillary datasets (e.g., slope, proximity) are part of the input data and used by the classifier, rather than applied post-classification.
- Output data structure:
  - Montane class removed (mapped via spectral data to Inland Rock or other upland habitats) to enable robust change mapping.
  - Rough grassland removed; grassland types align with JNCC Broad Habitats with no separate soil-based classification.
  - 25 m raster becomes a two-band product; probability data moved to band 2; spectral sub-classes removed.
  - No per-class spectral sub-classes in vector data; sub-classes deprecated due to limited validation.
- Spatial framework:
  - Segmentation-based segmentation removed; per-pixel approach used, improving consistency for change mapping, especially in upland areas.
- Mixed woodland handling:
  - Training uses pure stands for either Coniferous or Broadleaf woodland; polygon labels derived from modal_class, with pix_dist available to explore mixed woodland classifications.

## Class definitions and mapping context

- LCM2015 maps 21 Broad Habitat classes, with some subdivisions or aggregations for raster outputs.
- Appendix-level details explain the JNCC Broad Habitat definitions used to interpret classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, various grasslands, wetlands, urban/built-up areas, and coastal/intertidal classes).
- The classification emphasizes spectral signatures, with limited reliance on ancillary data for individual class boundaries.

## Practical considerations for users

- Change mapping cautions:
  - Differences in methodology and class definitions mean LCM2015 should not be used directly for change mapping without considering the methodological context.
- Data suitability:
  - Outputs are designed for self-serve analytics via the vector, 25 m, and 1 km products, with varying detail and metadata richness to suit different applications.
- Citation and reuse:
  - Each product has a DOI; users should cite these when publishing or presenting results.
- The dataset is positioned as a stable, archived resource suitable for long-term analyses, with ongoing support and documentation.

## Projections, data access, and contact

- Projections:
  - GB data in British National Grid; Northern Ireland data in Irish/TM75 grids.
- Access points:
  - CEH EIP for 1 km rasters; full vector and 25 m rasters available on request with licensing.
- Contact and information:
  - dataset information and queries via spatialdata@ceh.ac.uk; more information at CEH LCM2015 pages.
- Reference and DOI guidance:
  - The LCM2015 data paper is in preparation; DOIs provided for all data products to aid citation and reproducibility.