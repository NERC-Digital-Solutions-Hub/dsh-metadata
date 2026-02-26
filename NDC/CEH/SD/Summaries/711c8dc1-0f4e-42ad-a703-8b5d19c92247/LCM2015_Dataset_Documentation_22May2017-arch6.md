# Dataset documentation

- CEH/NERC comprehensive documentation for Land Cover Map 2015 (LCM2015), a complex UK land cover dataset intended to support diverse data-usage across organizations.

## Overview
- LCM2015 provides parcel-based land cover mapped from two-date satellite composites (primarily Landsat-8 at 30 m, supplemented by AWIFS at 60 m).
- Based on 21 UK Broad Habitat classes (JNCC definitions), reflecting real-world boundaries for easy interpretation and compatibility with other datasets.
- Outputs multiple data products to support different application needs: vector (core), 25 m raster, and 1 km raster (dominant and percentage covers for both 21 target and 10 aggregate classes).

## What’s in LCM2015
- Unique object-based parcel labeling (gid) with rich metadata and per-polygon classification details.
- Uses Random Forest classifier, incorporating satellite data and ancillary data (e.g., slope, proximity to water) as inputs.
- Provides uncertainty information: mean per-polygon probability from the classifier (also available in 25 m raster band 2).
- Distinct data products:
  - Core vector dataset (parcels with attributes)
  - 25 m raster dataset (two bands: band 1 = dominant class, band 2 = mean per-polygon probability)
  - 1 km raster datasets (dominant and percentage covers for both 21 target and 10 aggregate classes)
- Spatial coverage: separate datasets for Great Britain and Northern Ireland; projections correspond to GB National Grid (27700) and NI grid (TM75 Irish Grid, 29903).

## Data products and formats
- Vector data set
  - 6.7 million polygons (Great Britain) and 0.9 million (Northern Ireland)
  - Attributes include gid, dominant Broad Habitat (BHAB), per-class pixel counts (Pix_dist), uncertainty (unc), number of pixels (npix), modal class (Modal_class), proportion of polygon classified as dominant class (Modal_prop), and composite source indicator.
- 25 m raster
  - 2-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability from Random Forest
- 1 km raster
  - Products include: dominant cover (21-target and 10-aggregate), and percentage cover (21 bands and 10-aggregate bands)
  - Values are integers; sums may deviate from 100% due to rounding; coastal areas may sum to less than 100%

## Classification methodology
- Algorithm: Random Forest classifier (handles multi-modal training data; avoids spectral sub-class grouping)
- Training data: initial stable training areas (from 2000 and 2007) with manual supplementation for coastal and poorly mapped classes
- Ancillary data: integrated as input features (not post-classification) to improve accuracy and objectivity
- Output labeling: polygons labeled with dominant class; users can inspect per-pixel distributions (Pix_dist) for more detail

## Differences from previous LCM2007
- Output classes and methodology differences designed to support change mapping:
  - Montane class removed; Inland Rock and other upland habitats used instead of Montane
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitats (no soil data used)
  - 25 m raster updated to two-band structure
  - Probability data simplified (vector carries mean polygon probability; 25 m raster band 2 carries this)
  - No spectral sub-classes in outputs (simplifies training and reduces redundancy)
  - Spatial segmentation removed from the GB framework to improve consistency across LCMs and change mapping
  - Mixed woodland labeling adjusted based on pixel-level modal_class rather than training-area blocks
- Methodology changes: adoption of Random Forest, inclusion of ancillary data during classification, and refined stable training data.

## Uncertainty and metadata
- Uncertainty provided as mean per-polygon probability for vector; 25 m raster band 2 contains this information.
- Rich metadata: per-polygon attributes include dominant class, pixel counts per class, and composite image source.
- DOIs: each LCM2015 product has a DOI for citation and reproducibility.

## Data access and citation
- 1 km raster data: available via CEH Environmental Information Platform (EIP)
- Full vector and 25 m raster products: available on request under licence (spatialdata@ceh.ac.uk)
- DOIs provided for Great Britain and Northern Ireland products (vector, 25 m raster, 1 km percentage and dominant classes, with aggregates)
- Projections: GB Vector/Raster in British National Grid; NI in Irish National Grid
- Guidance to cite: include DOIs and dataset authors in references

## Class taxonomy and mapping
- LC2015 uses 21 target classes based on UK Broad Habitats (JNCC definitions)
- Some classes are subdivided or aggregated for raster products (e.g., Urban vs Suburban within Built-up Areas and Gardens; multiple grassland variants consolidated for some products)
- Appendix resources provide color mappings and detailed class descriptions for user interpretation

## Practical use notes for data support
- LCM2015 is a stable, archived dataset; consider version-specific differences when integrating with newer datasets or scripts
- For change mapping, be cautious: differences in classification schemes, removed classes, and methodology can affect cross-version comparisons
- The vector dataset is rich but larger in file size; 25 m raster offers a compact alternative with consistent classification but less metadata
- The dataset aligns with UK biodiversity and habitat classifications, enabling direct cross-walks to Broad Habitat definitions and related ecological analyses

## Additional information
- Links for further information and access:
  - CEH LCM2015 pages and data access
  - Citing data: CEH eidc data citation guidelines
- Appendices cover standard color mappings, composite image details, and in-depth habitat definitions for user reference