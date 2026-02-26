# Final Report for LCM2007 - the new UK land cover map

## Overview of data and products
- LCM2007 provides a UK-wide, parcel-based land cover map with 23 Broad Habitats, plus raster products at 25 m and 1 km resolutions.
- Outputs include a vector dataset (land parcels with rich metadata) and two raster products (25 m and 1 km), enabling both detailed mapping and broad-scale analyses.
- The dataset integrates a long time series of satellite imagery ( Landsat- TM/ETM+, SPOT-4/5, IRS LISS-3, AWIFS) across multiple target periods and composites to derive land cover.
- The project was developed to support policy and monitoring needs with stock estimates and spatial distributions of Broad Habitats across the UK, GB, England, Scotland, Wales, and Northern Ireland.

## Spatial framework and data sources
- Spatial framework built from detailed national cartography (Ordnance Survey MasterMap and LPS Large-scale Vector) to delineate real-world land units and enable stable, reusable boundaries for future monitoring.
- Parcel delineation combines image segments with cartography, and minimum mappable units (MMU) are applied to ensure coherent parcel geometry (roughly 0.5 ha threshold).
- Data sources include external spatial datasets for validation and context (e.g., Countryside Survey data), soil and urban boundary information, and coastal/shoreline datasets.
- Quality assurance included field validation using ground references across multiple years.

## Production approach and knowledge-based enhancements
- Image processing and segmentation:
  - Pre-processing with cloud masking, atmospheric and topographic corrections, and multi-date composites.
  - Image segmentation produces image segments which are linked to land parcels.
- Classification:
  - Parcel-based supervised maximum likelihood classification using 37 composite images and 21 single-date images.
  - Iterative training and refinement with ground reference data.
- Knowledge-based enhancements (KBEs):
  - Seven automated rules resolve spectral confusion and incorporate contextual data (terrain, soils, urban proximity, coastal proximity, etc.) to improve thematic resolution.
  - KBEs support one-to-many relationships between land cover and Broad Habitats and preserve original spectral classifications for user adjustments.
- Output and traceability:
  - Vector product includes 23 land cover classes with 10 processing attributes (e.g., Construct, ProbList, KBE history) for full traceability.
  - 25 m raster and 1 km raster products derived from the vector data, with the 1 km product offering both percentage cover and dominant class per pixel.

## Accuracy, validation, and comparability
- Bespoke validation approach relies on parcel-level metadata and external field data to assess accuracy; overall accuracy reported around 83% in ground-reference validation, with variation by class.
- Comparisons with Countryside Survey (CS) 2007 reveal:
  - Similar area estimates for Broadleaved woodland, Acid Grassland, and Inland Rock (within CS 95% confidence limits).
  - Dissimilar estimates for Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, and coastal habitats, due to factors such as:
    - Differences in how classes are defined and mapped (e.g., inclusion of boundary features in LCM2007's Arable and Horticulture).
    - Spectral confusion and high variability within arable classes.
    - Differences in spatial structure and MMU between CS and LCM2007, and the multi-year image requirement for UK-wide coverage.
    - How “Fen, Marsh and Swamp” is represented (mosaic nature leads to large discrepancies with CS).
- Grassland categories present persistent classification challenges due to one-to-many relationships with Broad Habitats; Broad Habitat Association (BHA) rules were developed to improve interpretability.
- The 1 km CS-based comparisons show good agreement for some classes (e.g., Arable and Horticulture), but CS area estimates can differ substantially from LCM2007 totals for the same Broad Habitats.

## National distribution and country variation
- UK-wide summary: just over half of land cover is intensive use (Arable and Horticulture plus Improved Grassland); about 12% is woodland; roughly 30% semi-natural; other categories include coastal, montane, freshwater, etc.
- England exhibits the highest levels of intensive land use; Scotland has the largest share of Coniferous Woodland and substantial upland semi-natural areas; Northern Ireland and Wales show different balances across grassland and built-up areas.
- Comparison with LCM2000 indicates changes in proportions of Arable, semi-natural grassland, and woodland types, with ongoing questions about the influence of spatial framework changes and temporal image ranges.

## Practical guidance for data users
- Use KBEs to refine classifications where habitat context is informative; apply user-driven validation for local studies given remaining uncertainties in some classes.
- For grassland-focused analyses, consider aggregating to a single grassland class to improve correspondence with CS data.
- When assessing habitat extents, consult both CS estimates and LCM2007 outputs, and use Broad Habitat Association mappings to interpret one-to-many relationships.
- For large-scale analyses, the 1 km raster product is suitable; use vector and 25 m raster products for finer-scale spatial analyses and change monitoring, with appropriate licensing.
- The parcel-level metadata (KBE history and ProbList) enables targeted quality assessment and potential reclassification by users.

## Access, licensing, and data management
- 1 km raster data are available via the CEH Information Gateway.
- Full vector and 25 m raster data are available on request from CEH; licensing may apply and fees may be charged for some uses.
- The data are designed to be a reusable, policy-relevant framework for ongoing UK-wide monitoring and future change detection.

## Discussion and future perspective
- LCM2007 represents a major advancement by delivering a continuous parcel-based UK land cover map with a robust, reusable spatial framework suitable for change detection and cross-sector policy support.
- The spatial framework based on MasterMap/LPS supports integration with other national data products and future monitoring activities, aiding consistency and comparability across time.
- Change detection across LCM generations requires careful methodological alignment due to differences in spatial structure and classification schemes; future work may emphasize re-aligning prior maps to a common spatial framework to enable more robust change analyses.
- LCM2007, in combination with Countryside Survey and other data sources, provides a comprehensive base for biodiversity assessment, habitat monitoring, ecosystem service analysis, and landscape planning.

## Data accessibility and supplementary resources
- Access to the LCM2007 datasets is documented, with multiple formats and product levels to support a range of applications.
- Appendices provide validation approaches, Broad Habitat Association rules, and dataset metadata to aid independent assessment and validation by data users.